---
keywords: fastai
description: Practice with identifying and correcting code blocks
title: Big Idea 1 'Identifying and Correcting Errors'
layout: default
badges: false
permalink: /collegeboard/error
image: /images/apcsp.png
categories: [1.B, 4.C]
type: ap
week: 7
nb_path: _notebooks/2022-10-03-AP-error_testing.ipynb
layout: notebook
---

<!--
#################################################
### THIS FILE WAS AUTOGENERATED! DO NOT EDIT! ###
#################################################
# file to edit: _notebooks/2022-10-03-AP-error_testing.ipynb
-->

<div class="container" id="notebook-container">
        
<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p><a href="https://apclassroom.collegeboard.org/103/home?unit=1">College Board Big Idea 1</a></p>
<h2 id="Identifying-and-Correcting-Errors-(Unit-1.4)">Identifying and Correcting Errors (Unit 1.4)<a class="anchor-link" href="#Identifying-and-Correcting-Errors-(Unit-1.4)"> </a></h2><blockquote><p>Become familiar with types of errors and strategies to fixing them</p>
<ul>
<li>Lightly Review Videos and take notes on topics with Blog</li>
<li>Complete assigned MCQ questions</li>
</ul>
</blockquote>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="Here-are-some-code-segments-you-can-practice-fixing:">Here are some code segments you can practice fixing:<a class="anchor-link" href="#Here-are-some-code-segments-you-can-practice-fixing:"> </a></h1>
</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">alphabet</span> <span class="o">=</span> <span class="s2">&quot;abcdefghijklmnopqrstuvwxyz&quot;</span>

<span class="n">alphabetList</span> <span class="o">=</span> <span class="p">[]</span>

<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="n">alphabet</span><span class="p">:</span>
    <span class="n">alphabetList</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="n">i</span><span class="p">)</span>

<span class="nb">print</span><span class="p">(</span><span class="n">alphabetList</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">

<div class="output_subarea output_stream output_stdout output_text">
<pre>[&#39;a&#39;, &#39;b&#39;, &#39;c&#39;, &#39;d&#39;, &#39;e&#39;, &#39;f&#39;, &#39;g&#39;, &#39;h&#39;, &#39;i&#39;, &#39;j&#39;, &#39;k&#39;, &#39;l&#39;, &#39;m&#39;, &#39;n&#39;, &#39;o&#39;, &#39;p&#39;, &#39;q&#39;, &#39;r&#39;, &#39;s&#39;, &#39;t&#39;, &#39;u&#39;, &#39;v&#39;, &#39;w&#39;, &#39;x&#39;, &#39;y&#39;, &#39;z&#39;]
</pre>
</div>
</div>

</div>
</div>

</div>
    {% endraw %}

<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>The intended outcome is to determine where the letter is in the alphabet using a while loop</p>
<ul>
<li>What is a good test case to check the current outcome? Why?</li>
<li>Make changes to get the intended outcome.</li>
</ul>

</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">letter</span> <span class="o">=</span> <span class="nb">input</span><span class="p">(</span><span class="s2">&quot;What letter would you like to check?&quot;</span><span class="p">)</span>

<span class="n">i</span> <span class="o">=</span> <span class="o">+</span><span class="mi">1</span>


<span class="k">while</span> <span class="n">i</span> <span class="o">&lt;</span> <span class="mi">26</span><span class="p">:</span>
    <span class="k">if</span> <span class="n">alphabetList</span><span class="p">[</span><span class="n">i</span><span class="p">]</span> <span class="o">==</span> <span class="n">letter</span><span class="p">:</span>
        <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;The letter &quot;</span> <span class="o">+</span> <span class="n">letter</span> <span class="o">+</span> <span class="s2">&quot; is the &quot;</span> <span class="o">+</span> <span class="nb">str</span><span class="p">(</span><span class="n">i</span> <span class="o">+</span> <span class="mi">1</span><span class="p">)</span> <span class="o">+</span> <span class="s2">&quot; letter in the alphabet&quot;</span><span class="p">)</span>
    <span class="n">i</span> <span class="o">+=</span> <span class="mi">1</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">

<div class="output_subarea output_stream output_stdout output_text">
<pre>The letter c is the 3 letter in the alphabet
</pre>
</div>
</div>

</div>
</div>

</div>
    {% endraw %}

<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>The intended outcome is to determine where the letter is in the alphabet using a for loop</p>
<ul>
<li>What is a good test case to check the current outcome? Why?</li>
<li>Make changes to get the intended outcome.</li>
</ul>

</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">count</span> <span class="o">=</span> <span class="mi">0</span>

<span class="n">letter</span> <span class="o">=</span> <span class="nb">input</span><span class="p">(</span><span class="s2">&quot;What letter would you like to check?&quot;</span><span class="p">)</span>

<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="n">alphabetList</span><span class="p">:</span>
    <span class="n">count</span> <span class="o">=</span> <span class="n">count</span> <span class="o">+</span><span class="mi">1</span>
    <span class="k">if</span> <span class="n">i</span> <span class="o">==</span> <span class="n">letter</span><span class="p">:</span>
        <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;The letter &quot;</span> <span class="o">+</span> <span class="n">letter</span> <span class="o">+</span> <span class="s2">&quot; is the &quot;</span> <span class="o">+</span> <span class="nb">str</span><span class="p">(</span><span class="n">count</span><span class="p">)</span> <span class="o">+</span> <span class="s2">&quot; letter in the alphabet&quot;</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">

<div class="output_subarea output_stream output_stdout output_text">
<pre>The letter z is the 26 letter in the alphabet
</pre>
</div>
</div>

</div>
</div>

</div>
    {% endraw %}

<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>This code outputs the even numbers from 0 - 10 using a while loop.</p>
<ul>
<li>Analyze this code to determine what can be changed to get the outcome to be odd numbers. (Code block below)</li>
</ul>

</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">evens</span> <span class="o">=</span> <span class="p">[]</span>
<span class="n">i</span> <span class="o">=</span> <span class="mi">1</span>

<span class="k">while</span> <span class="n">i</span> <span class="o">&lt;=</span> <span class="mi">10</span><span class="p">:</span>
    <span class="n">evens</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="n">i</span><span class="p">)</span>
    <span class="n">i</span> <span class="o">+=</span> <span class="mi">2</span>

<span class="nb">print</span><span class="p">(</span><span class="n">evens</span><span class="p">)</span>    
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">

<div class="output_subarea output_stream output_stdout output_text">
<pre>[1, 3, 5, 7, 9]
</pre>
</div>
</div>

</div>
</div>

</div>
    {% endraw %}

<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>This code should output the odd numbers from 0 - 10 using a while loop.</p>

</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">odds</span> <span class="o">=</span> <span class="p">[]</span>
<span class="n">i</span> <span class="o">=</span> <span class="mi">0</span>

<span class="k">while</span> <span class="n">i</span> <span class="o">&lt;=</span> <span class="mi">10</span><span class="p">:</span>
    <span class="n">odds</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="n">i</span><span class="p">)</span>
    <span class="n">i</span> <span class="o">+=</span> <span class="mi">2</span>

<span class="nb">print</span><span class="p">(</span><span class="n">odds</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">

<div class="output_subarea output_stream output_stdout output_text">
<pre>[0, 2, 4, 6, 8, 10]
</pre>
</div>
</div>

</div>
</div>

</div>
    {% endraw %}

<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>This code outputs the even numbers from 0 - 10 using a for loop.</p>
<ul>
<li>Analyze this code to determine what can be changed to get the outcome to be odd numbers. (Code block below)</li>
</ul>

</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">numbers</span> <span class="o">=</span> <span class="p">[</span><span class="mi">0</span><span class="p">,</span><span class="mi">1</span><span class="p">,</span><span class="mi">2</span><span class="p">,</span><span class="mi">3</span><span class="p">,</span><span class="mi">4</span><span class="p">,</span><span class="mi">5</span><span class="p">,</span><span class="mi">6</span><span class="p">,</span><span class="mi">7</span><span class="p">,</span><span class="mi">8</span><span class="p">,</span><span class="mi">9</span><span class="p">,</span><span class="mi">10</span><span class="p">]</span>
<span class="n">evens</span> <span class="o">=</span> <span class="p">[]</span>

<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="n">numbers</span><span class="p">:</span>
    <span class="k">if</span> <span class="p">(</span><span class="n">numbers</span><span class="p">[</span><span class="n">i</span><span class="p">]</span> <span class="o">%</span> <span class="mi">2</span> <span class="o">==</span> <span class="mi">0</span><span class="p">):</span>
        <span class="n">evens</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="n">numbers</span><span class="p">[</span><span class="n">i</span><span class="p">])</span>

<span class="nb">print</span><span class="p">(</span><span class="n">evens</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">

<div class="output_subarea output_stream output_stdout output_text">
<pre>[0, 2, 4, 6, 8, 10]
</pre>
</div>
</div>

</div>
</div>

</div>
    {% endraw %}

<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>This code should output the odd numbers from 0 - 10 using a for loop.</p>

</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">numbers</span> <span class="o">=</span> <span class="p">[</span><span class="mi">0</span><span class="p">,</span><span class="mi">1</span><span class="p">,</span><span class="mi">2</span><span class="p">,</span><span class="mi">3</span><span class="p">,</span><span class="mi">4</span><span class="p">,</span><span class="mi">5</span><span class="p">,</span><span class="mi">6</span><span class="p">,</span><span class="mi">7</span><span class="p">,</span><span class="mi">8</span><span class="p">,</span><span class="mi">9</span><span class="p">,</span><span class="mi">10</span><span class="p">]</span>
<span class="n">odds</span> <span class="o">=</span> <span class="p">[]</span>

<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="n">numbers</span><span class="p">:</span>
    <span class="k">if</span> <span class="p">(</span><span class="n">numbers</span><span class="p">[</span><span class="n">i</span><span class="p">]</span> <span class="o">%</span> <span class="mi">2</span> <span class="o">==</span> <span class="mi">1</span><span class="p">):</span>
        <span class="n">odds</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="n">numbers</span><span class="p">[</span><span class="n">i</span><span class="p">])</span>

<span class="nb">print</span><span class="p">(</span><span class="n">odds</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">

<div class="output_subarea output_stream output_stdout output_text">
<pre>[1, 3, 5, 7, 9]
</pre>
</div>
</div>

</div>
</div>

</div>
    {% endraw %}

<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>The intended outcome is printing a number between 1 and 100 once, if it is a multiple of 2 or 5</p>
<ul>
<li>What values are outputted incorrectly. Why?</li>
<li>Make changes to get the intended outcome.</li>
</ul>

</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">numbers</span> <span class="o">=</span> <span class="p">[]</span>
<span class="n">newNumbers</span> <span class="o">=</span> <span class="p">[]</span>
<span class="n">i</span> <span class="o">=</span> <span class="mi">0</span>

<span class="k">while</span> <span class="n">i</span> <span class="o">&lt;</span> <span class="mi">100</span><span class="p">:</span>
    <span class="n">numbers</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="n">i</span><span class="p">)</span>
    <span class="n">i</span> <span class="o">+=</span> <span class="mi">1</span>

<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="n">numbers</span><span class="p">:</span>
    <span class="k">if</span> <span class="n">numbers</span><span class="p">[</span><span class="n">i</span><span class="p">]</span> <span class="o">%</span> <span class="mi">5</span> <span class="o">==</span> <span class="mi">0</span><span class="p">:</span>
        <span class="n">newNumbers</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="n">numbers</span><span class="p">[</span><span class="n">i</span><span class="p">])</span>
    <span class="k">if</span> <span class="n">numbers</span><span class="p">[</span><span class="n">i</span><span class="p">]</span> <span class="o">%</span> <span class="mi">2</span> <span class="o">==</span> <span class="mi">1</span><span class="p">:</span>
        <span class="n">newNumbers</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="n">numbers</span><span class="p">[</span><span class="n">i</span><span class="p">])</span>

<span class="nb">print</span><span class="p">(</span><span class="n">newNumbers</span><span class="p">)</span> 
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">

<div class="output_subarea output_stream output_stdout output_text">
<pre>[0, 1, 3, 5, 5, 7, 9, 10, 11, 13, 15, 15, 17, 19, 20, 21, 23, 25, 25, 27, 29, 30, 31, 33, 35, 35, 37, 39, 40, 41, 43, 45, 45, 47, 49, 50, 51, 53, 55, 55, 57, 59, 60, 61, 63, 65, 65, 67, 69, 70, 71, 73, 75, 75, 77, 79, 80, 81, 83, 85, 85, 87, 89, 90, 91, 93, 95, 95, 97, 99]
</pre>
</div>
</div>

</div>
</div>

</div>
    {% endraw %}

<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="Challenge">Challenge<a class="anchor-link" href="#Challenge"> </a></h1>
</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">menu</span> <span class="o">=</span>  <span class="p">{</span><span class="s2">&quot;burger&quot;</span><span class="p">:</span> <span class="mf">3.99</span><span class="p">,</span>
         <span class="s2">&quot;fries&quot;</span><span class="p">:</span> <span class="mf">1.99</span><span class="p">,</span>
         <span class="s2">&quot;drink&quot;</span><span class="p">:</span> <span class="mf">0.99</span><span class="p">}</span>
<span class="nb">print</span> <span class="p">(</span><span class="n">menu</span><span class="p">)</span>

<span class="n">order</span><span class="o">=</span> <span class="nb">input</span><span class="p">(</span><span class="s2">&quot;What can i get for you? &gt;&gt;&quot;</span><span class="p">)</span>

<span class="k">if</span> <span class="n">order</span> <span class="o">==</span> <span class="s2">&quot;burger&quot;</span><span class="p">:</span>
    <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;you ordered burger, your total is $3.99&quot;</span><span class="p">)</span>
<span class="k">elif</span> <span class="n">order</span> <span class="o">==</span> <span class="s2">&quot;fries&quot;</span><span class="p">:</span>
    <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;you ordered fries, your total is $1.99&quot;</span><span class="p">)</span>
<span class="k">elif</span> <span class="n">order</span> <span class="o">==</span> <span class="s2">&quot;drink&quot;</span><span class="p">:</span>
    <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;you ordered a drink, your total is $0.99&quot;</span><span class="p">)</span>
<span class="k">elif</span> <span class="n">order</span> <span class="o">!=</span> <span class="s2">&quot;burger&quot;</span> <span class="ow">or</span> <span class="s2">&quot;fries&quot;</span> <span class="ow">or</span> <span class="s2">&quot;drink&quot;</span><span class="p">:</span>
    <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;That item is not on the menu, try re-order&quot;</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">

<div class="output_subarea output_stream output_stdout output_text">
<pre>{&#39;burger&#39;: 3.99, &#39;fries&#39;: 1.99, &#39;drink&#39;: 0.99}
you ordered a drink, your total is $0.99
</pre>
</div>
</div>

</div>
</div>

</div>
    {% endraw %}

<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Hacks">Hacks<a class="anchor-link" href="#Hacks"> </a></h2><blockquote><p>Now is a good time to think about Testing of your teams final project...</p>
<ul>
<li>What errors may arise in your project?</li>
<li>What are some test cases that can be used?</li>
<li>Make sure to document any bugs you encounter and how you solved the problem.</li>
<li>What are ???single??? tests that you will perform on your project? Or, your part of the project?<ul>
<li>As Hack Design and Test plan action ??? Divide these ???single??? tests into Issues for Scrum Board prior to coding. FYI, related tests could be in same Issue by using markdown checkboxes to separate tests.</li>
</ul>
</li>
</ul>
</blockquote>

</div>
</div>
</div>
</div>
 

