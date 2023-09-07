---
toc: true
comments: true
layout: post
title: Pokemon data
description:  testing
type: hacks
---

<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pokemon Data Table</title>
    <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
    <style> 
        /* Add your CSS styles for the table here */
    </style>
</head>
<body>
   <script>
        $(document).ready(function () {
            // URL to the Pokemon API (you may need to adjust the URL)
            var apiUrl = "https://pokeapi.co/api/v2/pokemon?limit=151";
            // Function to fetch and populate the table with Pokemon data
            function fetchPokemonData() {
                $.get(apiUrl, function (data) {
                    // Loop through the results and populate the table
                    $.each(data.results, function (index, pokemon) {
                        $.get(pokemon.url, function (pokemonData) {
                            var abilities = pokemonData.abilities.map(function (ability) {
                                return ability.ability.name;
                            }).join(", ");
                            var types = pokemonData.types.map(function (type) {
                                return type.type.name;
                            }).join(", ");
                            var newRow = "<tr>" +
                                "<td>" + pokemonData.id + "</td>" +
                                "<td>" + pokemonData.name + "</td>" +
                                "<td>" + types + "</td>" +
                                "<td>" + abilities + "</td>" +
                                "<td><img src='" + pokemonData.sprites.front_default + "' alt='" + pokemonData.name + "'></td>" +
                                "</tr>";
                            $("#pokemonTable tbody").append(newRow);
                        });
                    });
                });
            }
            // Call the fetchPokemonData function to populate the table
            fetchPokemonData();
        });
    </script>
    <script>
        $(document).ready(function () {
            $("#nameHeader").click(function () {
                sortTableByName();
            });
        });
        function sortTableByName() {
            var table, rows, switching, i, x, y, shouldSwitch;
            table = document.getElementById("pokemonTable");
            switching = true;
            while (switching) {
                switching = false;
                rows = table.getElementsByTagName("tr");
                for (i = 1; i < rows.length - 1; i++) {
                    shouldSwitch = false;
                    x = rows[i].getElementsByTagName("td")[1]; // Use index 1 for Name column
                    y = rows[i + 1].getElementsByTagName("td")[1]; // Use index 1 for Name column
                    if (x.innerHTML.toLowerCase() > y.innerHTML.toLowerCase()) {
                        shouldSwitch = true;
                        break;
                    }
                }
                if (shouldSwitch) {
                    rows[i].parentNode.insertBefore(rows[i + 1], rows[i]);
                    switching = true;
                }
            }
        }
    </script>

    <h1>Pokemon Data</h1>
    <table id="pokemonTable">
        <thead>
            <tr>
                <th>ID</th>
                <th id="nameHeader">Name</th>
                <th>Type</th>
                <th>Abilities</th>
                <th>Image</th>
            </tr>
        </thead>
        <tbody>
            <!-- Pokemon data will be inserted here -->
        </tbody>
    </table>
</body>
</html>