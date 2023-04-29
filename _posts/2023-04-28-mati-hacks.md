---
toc: true
layout: post
Badges: true
comments: false
author: Mati Danish
categories: [fastpages, markdown]
title: Zestys
---

# Create buttons similar to the ones above that allow you to multiply binary numbers and returns the desired result in both binary and decimal in HTML and js
```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8">
    <title>Binary Multiplication</title>
  </head>
  <body>
    <h1>Binary Multiplication</h1>
    <form>
      <label for="binary1">Binary 1:</label>
      <input type="text" id="binary1" name="binary1" placeholder="Enter binary number 1"><br><br>
      <label for="binary2">Binary 2:</label>
      <input type="text" id="binary2" name="binary2" placeholder="Enter binary number 2"><br><br>
      <button type="button" onclick="multiplyBinary()">Multiply</button><br><br>
      <label for="resultBinary">Result in Binary:</label>
      <input type="text" id="resultBinary" name="resultBinary" readonly><br><br>
      <label for="resultDecimal">Result in Decimal:</label>
      <input type="text" id="resultDecimal" name="resultDecimal" readonly><br><br>
    </form>
    
    <script>
      function multiplyBinary() {
        // Get binary numbers from input fields
        var binary1 = document.getElementById("binary1").value;
        var binary2 = document.getElementById("binary2").value;
        
        // Convert binary numbers to decimal
        var decimal1 = parseInt(binary1, 2);
        var decimal2 = parseInt(binary2, 2);
        
        // Multiply decimal numbers
        var resultDecimal = decimal1 * decimal2;
        
        // Convert decimal result to binary
        var resultBinary = resultDecimal.toString(2);
        
        // Display results in output fields
        document.getElementById("resultBinary").value = resultBinary;
        document.getElementById("resultDecimal").value = resultDecimal;
      }
    </script>
  </body>
</html>
```




# Binary Logic

![image](/Danish_Cookies/images/Mati-quiz%232.png)



# Logic Gate

1. Logic gates can be combined in various ways to implement different computer functions, such as arithmetic operations, memory storage, and control flow. For example, an arithmetic logic unit (ALU) can be constructed using logic gates to perform arithmetic and logic operations on binary data.

2. Boolean operations are mathematical operations performed on Boolean variables or expressions, whereas logic gates are physical devices or digital circuits that implement Boolean operations using electronic or optical signals. In other words, Boolean operations are an abstract concept, while logic gates are a concrete implementation of those operations in hardware.

See image named (Mati-quiz#2)

![image](/Danish_Cookies/images/Mati-quiz%231.png)

# Fetching

``` html

<!DOCTYPE html>
<html>
<head>
	<title>Filter Data Example</title>
	<script>
		function filterData() {
			// Get the input value
			var input = document.getElementById("filterInput").value.toLowerCase();

			// Get the table rows
			var rows = document.getElementsByTagName("tr");

			// Loop through the rows
			for (var i = 1; i < rows.length; i++) {
				var row = rows[i];
				var cells = row.getElementsByTagName("td");

				// Hide the row if the input is not found in any of the cells
				var found = false;
				for (var j = 0; j < cells.length; j++) {
					var cell = cells[j];
					if (cell.innerHTML.toLowerCase().indexOf(input) > -1) {
						found = true;
						break;
					}
				}
				if (!found) {
					row.style.display = "none";
				} else {
					row.style.display = "";
				}
			}
		}
	</script>
</head>
<body>
	<h2>Filter Data Example</h2>
	<p>Enter text to filter the table:</p>
	<input type="text" id="filterInput" onkeyup="filterData()">
	<table>
		<tr>
			<th>Column 1</th>
			<th>Column 2</th>
			<th>Column 3</th>
		</tr>
		<tr>
			<td>Row 1, Column 1</td>
			<td>Row 1, Column 2</td>
			<td>Row 1, Column 3</td>
		</tr>
		<tr>
			<td>Row 2, Column 1</td>
			<td>Row 2, Column 2</td>
			<td>Row 2, Column 3</td>
		</tr>
		<tr>
			<td>Row 3, Column 1</td>
			<td>Row 3, Column 2</td>
			<td>Row 3, Column 3</td>
		</tr>
	</table>
</body>
</html>

```


# github pages

One alternative to Github Pages is Netlify, which offers several benefits and advantages over other hosting service websites. One feature that sets Netlify apart is its continuous deployment system, which allows developers to deploy their sites automatically whenever they push changes to their code repository. Additionally, Netlify offers features such as serverless functions, form handling, and password protection for static sites, which make it a powerful and versatile hosting solution. Netlify also has a user-friendly interface and extensive documentation, which makes it easy for developers to set up and manage their sites.




```python
import pandas as pd

data = {
    'Name': ['Dillon', 'Noor', 'Steven', 'Lucas', 'Harsha', 'Varalu', 'Ryan', 'Emaad'],
    'Age': [24, 31, 42, 27, 29, 26, 90, 15],
    'Gender': ['M', 'M', 'M', 'M', 'F', 'F', 'F', 'F'],
    'Grade': ['A', 'B', 'A', 'D', 'C', 'F', 'B', 'A']
}

df = pd.DataFrame(data)

print(df.describe())


print(df['Gender'].value_counts())
print(df['Grade'].value_counts())

print(df.sort_values('Age'))
```


output: 
```zsh
             Age
count   8.000000
mean   33.625000
std    23.332019
min    15.000000
25%    25.250000
50%    28.000000
75%    36.750000
max    90.000000

F    4
M    4
Name: Gender, dtype: int64

A    3
B    2
F    1
C    1
D    1
Name: Grade, dtype: int64

     Name  Age Gender Grade
7   Emaad   15      F     A
0  Dillon    24      M     A
4  Harsha    29      F     C
3   Lucas    27      M     D
5  Varalu    26      F     F
1    Noor    31      M     B
2  Steven    42      M     A
6    Ryan    90      F     B
```

# no hacks were mentioned for Data Compression



