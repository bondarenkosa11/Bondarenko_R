<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml" lang="en" xml:lang="en"><head>

<meta charset="utf-8">
<meta name="generator" content="quarto-1.4.555">

<meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">


<title>readme</title>
<style>
code{white-space: pre-wrap;}
span.smallcaps{font-variant: small-caps;}
div.columns{display: flex; gap: min(4vw, 1.5em);}
div.column{flex: auto; overflow-x: auto;}
div.hanging-indent{margin-left: 1.5em; text-indent: -1.5em;}
ul.task-list{list-style: none;}
ul.task-list li input[type="checkbox"] {
  width: 0.8em;
  margin: 0 0.8em 0.2em -1em; /* quarto-specific, see https://github.com/quarto-dev/quarto-cli/issues/4556 */ 
  vertical-align: middle;
}
/* CSS for syntax highlighting */
pre > code.sourceCode { white-space: pre; position: relative; }
pre > code.sourceCode > span { line-height: 1.25; }
pre > code.sourceCode > span:empty { height: 1.2em; }
.sourceCode { overflow: visible; }
code.sourceCode > span { color: inherit; text-decoration: inherit; }
div.sourceCode { margin: 1em 0; }
pre.sourceCode { margin: 0; }
@media screen {
div.sourceCode { overflow: auto; }
}
@media print {
pre > code.sourceCode { white-space: pre-wrap; }
pre > code.sourceCode > span { text-indent: -5em; padding-left: 5em; }
}
pre.numberSource code
  { counter-reset: source-line 0; }
pre.numberSource code > span
  { position: relative; left: -4em; counter-increment: source-line; }
pre.numberSource code > span > a:first-child::before
  { content: counter(source-line);
    position: relative; left: -1em; text-align: right; vertical-align: baseline;
    border: none; display: inline-block;
    -webkit-touch-callout: none; -webkit-user-select: none;
    -khtml-user-select: none; -moz-user-select: none;
    -ms-user-select: none; user-select: none;
    padding: 0 4px; width: 4em;
  }
pre.numberSource { margin-left: 3em;  padding-left: 4px; }
div.sourceCode
  {   }
@media screen {
pre > code.sourceCode > span > a:first-child::before { text-decoration: underline; }
}
</style>


<script src="readme_files/libs/clipboard/clipboard.min.js"></script>
<script src="readme_files/libs/quarto-html/quarto.js"></script>
<script src="readme_files/libs/quarto-html/popper.min.js"></script>
<script src="readme_files/libs/quarto-html/tippy.umd.min.js"></script>
<script src="readme_files/libs/quarto-html/anchor.min.js"></script>
<link href="readme_files/libs/quarto-html/tippy.css" rel="stylesheet">
<link href="readme_files/libs/quarto-html/quarto-syntax-highlighting.css" rel="stylesheet" id="quarto-text-highlighting-styles">
<script src="readme_files/libs/bootstrap/bootstrap.min.js"></script>
<link href="readme_files/libs/bootstrap/bootstrap-icons.css" rel="stylesheet">
<link href="readme_files/libs/bootstrap/bootstrap.min.css" rel="stylesheet" id="quarto-bootstrap" data-mode="light">


</head>

<body class="fullcontent">

<div id="quarto-content" class="page-columns page-rows-contents page-layout-article">

<main class="content" id="quarto-document-content">




<section id="lab2" class="level1">
<h1>Lab2</h1>
<section id="цель-работы" class="level2">
<h2 class="anchored" data-anchor-id="цель-работы">Цель работы</h2>
<ol type="1">
<li>Развить практические навыки использования языка программирования R для обработки данных</li>
<li>Закрепить знания базовых типов данных языка R</li>
<li>Развить практические навыки использования функций обработки данных пакета dplyr – функции <code>select()</code>, <code>filter()</code>,<code>mutate()</code>, <code>arrange()</code>, <code>group_by()</code></li>
</ol>
</section>
<section id="исходные-данные" class="level2">
<h2 class="anchored" data-anchor-id="исходные-данные">Исходные данные</h2>
</section>
<section id="исходные-данные-1" class="level2">
<h2 class="anchored" data-anchor-id="исходные-данные-1">Исходные данные</h2>
<ol type="1">
<li>Windows 11</li>
<li>Rstudio</li>
<li>Github</li>
<li>Программный пакет dplyr</li>
</ol>
</section>
<section id="план-выполнения-работы" class="level2">
<h2 class="anchored" data-anchor-id="план-выполнения-работы">План выполнения работы</h2>
<ol type="1">
<li>Установить программный пакет dplyr</li>
<li>Проанализировать датасет starwars в рамках пакета dplyr</li>
<li>Выполнить аналитические задания</li>
</ol>
</section>
<section id="содержание-работы" class="level2">
<h2 class="anchored" data-anchor-id="содержание-работы">Содержание Работы</h2>
<section id="шаг-1.-установка-пакета-dplyr" class="level3">
<h3 class="anchored" data-anchor-id="шаг-1.-установка-пакета-dplyr">Шаг 1. Установка пакета dplyr</h3>
<div class="cell">
<div class="sourceCode cell-code" id="cb1"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb1-1"><a href="#cb1-1" aria-hidden="true" tabindex="-1"></a><span class="co">#install.packages("dplyr")</span></span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
</div>
<div class="cell">
<div class="sourceCode cell-code" id="cb2"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb2-1"><a href="#cb2-1" aria-hidden="true" tabindex="-1"></a><span class="fu">library</span>(dplyr)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stderr">
<pre><code>Warning: пакет 'dplyr' был собран под R версии 4.4.2</code></pre>
</div>
<div class="cell-output cell-output-stderr">
<pre><code>
Присоединяю пакет: 'dplyr'</code></pre>
</div>
<div class="cell-output cell-output-stderr">
<pre><code>Следующие объекты скрыты от 'package:stats':

    filter, lag</code></pre>
</div>
<div class="cell-output cell-output-stderr">
<pre><code>Следующие объекты скрыты от 'package:base':

    intersect, setdiff, setequal, union</code></pre>
</div>
</div>
<p><img src="./Images/1.png" class="img-fluid"></p>
</section>
<section id="шаг-2.-анализ-датасета-starwars" class="level3">
<h3 class="anchored" data-anchor-id="шаг-2.-анализ-датасета-starwars">Шаг 2. Анализ датасета starwars</h3>
<div class="cell">
<div class="sourceCode cell-code" id="cb7"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb7-1"><a href="#cb7-1" aria-hidden="true" tabindex="-1"></a>starwars</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre><code># A tibble: 87 × 14
   name     height  mass hair_color skin_color eye_color birth_year sex   gender
   &lt;chr&gt;     &lt;int&gt; &lt;dbl&gt; &lt;chr&gt;      &lt;chr&gt;      &lt;chr&gt;          &lt;dbl&gt; &lt;chr&gt; &lt;chr&gt; 
 1 Luke Sk…    172    77 blond      fair       blue            19   male  mascu…
 2 C-3PO       167    75 &lt;NA&gt;       gold       yellow         112   none  mascu…
 3 R2-D2        96    32 &lt;NA&gt;       white, bl… red             33   none  mascu…
 4 Darth V…    202   136 none       white      yellow          41.9 male  mascu…
 5 Leia Or…    150    49 brown      light      brown           19   fema… femin…
 6 Owen La…    178   120 brown, gr… light      blue            52   male  mascu…
 7 Beru Wh…    165    75 brown      light      blue            47   fema… femin…
 8 R5-D4        97    32 &lt;NA&gt;       white, red red             NA   none  mascu…
 9 Biggs D…    183    84 black      light      brown           24   male  mascu…
10 Obi-Wan…    182    77 auburn, w… fair       blue-gray       57   male  mascu…
# ℹ 77 more rows
# ℹ 5 more variables: homeworld &lt;chr&gt;, species &lt;chr&gt;, films &lt;list&gt;,
#   vehicles &lt;list&gt;, starships &lt;list&gt;</code></pre>
</div>
</div>
<section id="сколько-строк-в-датафрейме" class="level4">
<h4 class="anchored" data-anchor-id="сколько-строк-в-датафрейме">1. Сколько строк в датафрейме?</h4>
<div class="cell">
<div class="sourceCode cell-code" id="cb9"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb9-1"><a href="#cb9-1" aria-hidden="true" tabindex="-1"></a>starwars <span class="sc">%&gt;%</span> <span class="fu">nrow</span>()</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre><code>[1] 87</code></pre>
</div>
</div>
</section>
<section id="сколько-столбцов-в-датафрейме" class="level4">
<h4 class="anchored" data-anchor-id="сколько-столбцов-в-датафрейме">2. Сколько столбцов в датафрейме?</h4>
<div class="cell">
<div class="sourceCode cell-code" id="cb11"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb11-1"><a href="#cb11-1" aria-hidden="true" tabindex="-1"></a>starwars <span class="sc">%&gt;%</span> <span class="fu">ncol</span>()</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre><code>[1] 14</code></pre>
</div>
</div>
</section>
<section id="как-просмотреть-примерный-вид-датафрейма" class="level4">
<h4 class="anchored" data-anchor-id="как-просмотреть-примерный-вид-датафрейма">3.Как просмотреть примерный вид датафрейма?</h4>
<div class="cell">
<div class="sourceCode cell-code" id="cb13"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb13-1"><a href="#cb13-1" aria-hidden="true" tabindex="-1"></a>starwars <span class="sc">%&gt;%</span> <span class="fu">glimpse</span>()</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre><code>Rows: 87
Columns: 14
$ name       &lt;chr&gt; "Luke Skywalker", "C-3PO", "R2-D2", "Darth Vader", "Leia Or…
$ height     &lt;int&gt; 172, 167, 96, 202, 150, 178, 165, 97, 183, 182, 188, 180, 2…
$ mass       &lt;dbl&gt; 77.0, 75.0, 32.0, 136.0, 49.0, 120.0, 75.0, 32.0, 84.0, 77.…
$ hair_color &lt;chr&gt; "blond", NA, NA, "none", "brown", "brown, grey", "brown", N…
$ skin_color &lt;chr&gt; "fair", "gold", "white, blue", "white", "light", "light", "…
$ eye_color  &lt;chr&gt; "blue", "yellow", "red", "yellow", "brown", "blue", "blue",…
$ birth_year &lt;dbl&gt; 19.0, 112.0, 33.0, 41.9, 19.0, 52.0, 47.0, NA, 24.0, 57.0, …
$ sex        &lt;chr&gt; "male", "none", "none", "male", "female", "male", "female",…
$ gender     &lt;chr&gt; "masculine", "masculine", "masculine", "masculine", "femini…
$ homeworld  &lt;chr&gt; "Tatooine", "Tatooine", "Naboo", "Tatooine", "Alderaan", "T…
$ species    &lt;chr&gt; "Human", "Droid", "Droid", "Human", "Human", "Human", "Huma…
$ films      &lt;list&gt; &lt;"A New Hope", "The Empire Strikes Back", "Return of the J…
$ vehicles   &lt;list&gt; &lt;"Snowspeeder", "Imperial Speeder Bike"&gt;, &lt;&gt;, &lt;&gt;, &lt;&gt;, "Imp…
$ starships  &lt;list&gt; &lt;"X-wing", "Imperial shuttle"&gt;, &lt;&gt;, &lt;&gt;, "TIE Advanced x1",…</code></pre>
</div>
</div>
</section>
<section id="сколько-уникальных-рас-персонажей-species-представлено-в-данных" class="level4">
<h4 class="anchored" data-anchor-id="сколько-уникальных-рас-персонажей-species-представлено-в-данных">4. Сколько уникальных рас персонажей (species) представлено в данных?</h4>
<div class="cell">
<div class="sourceCode cell-code" id="cb15"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb15-1"><a href="#cb15-1" aria-hidden="true" tabindex="-1"></a>starwars <span class="sc">%&gt;%</span> <span class="fu">distinct</span>(species) <span class="sc">%&gt;%</span> <span class="fu">nrow</span>()</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre><code>[1] 38</code></pre>
</div>
</div>
</section>
<section id="найти-самого-высокого-персонажа." class="level4">
<h4 class="anchored" data-anchor-id="найти-самого-высокого-персонажа.">5. Найти самого высокого персонажа.</h4>
<div class="cell">
<div class="sourceCode cell-code" id="cb17"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb17-1"><a href="#cb17-1" aria-hidden="true" tabindex="-1"></a>starwars <span class="sc">%&gt;%</span> <span class="fu">arrange</span>(<span class="fu">desc</span>(height)) <span class="sc">%&gt;%</span> <span class="fu">head</span>(<span class="dv">1</span>) <span class="sc">%&gt;%</span> <span class="fu">select</span>(name)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre><code># A tibble: 1 × 1
  name       
  &lt;chr&gt;      
1 Yarael Poof</code></pre>
</div>
</div>
</section>
<section id="найти-всех-персонажей-ниже-170." class="level4">
<h4 class="anchored" data-anchor-id="найти-всех-персонажей-ниже-170.">6. Найти всех персонажей ниже 170.</h4>
<div class="cell">
<div class="sourceCode cell-code" id="cb19"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb19-1"><a href="#cb19-1" aria-hidden="true" tabindex="-1"></a>starwars <span class="sc">%&gt;%</span> <span class="fu">filter</span>(<span class="sc">!</span><span class="fu">is.na</span>(height) <span class="sc">&amp;</span> height <span class="sc">&lt;</span> <span class="dv">170</span>) <span class="sc">%&gt;%</span> <span class="fu">select</span>(name,height) <span class="sc">%&gt;%</span> knitr<span class="sc">::</span><span class="fu">kable</span>()</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output-display">
<table class="caption-top table table-sm table-striped small">
<thead>
<tr class="header">
<th style="text-align: left;">name</th>
<th style="text-align: right;">height</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;">C-3PO</td>
<td style="text-align: right;">167</td>
</tr>
<tr class="even">
<td style="text-align: left;">R2-D2</td>
<td style="text-align: right;">96</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Leia Organa</td>
<td style="text-align: right;">150</td>
</tr>
<tr class="even">
<td style="text-align: left;">Beru Whitesun Lars</td>
<td style="text-align: right;">165</td>
</tr>
<tr class="odd">
<td style="text-align: left;">R5-D4</td>
<td style="text-align: right;">97</td>
</tr>
<tr class="even">
<td style="text-align: left;">Yoda</td>
<td style="text-align: right;">66</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Mon Mothma</td>
<td style="text-align: right;">150</td>
</tr>
<tr class="even">
<td style="text-align: left;">Wicket Systri Warrick</td>
<td style="text-align: right;">88</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Nien Nunb</td>
<td style="text-align: right;">160</td>
</tr>
<tr class="even">
<td style="text-align: left;">Watto</td>
<td style="text-align: right;">137</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Sebulba</td>
<td style="text-align: right;">112</td>
</tr>
<tr class="even">
<td style="text-align: left;">Shmi Skywalker</td>
<td style="text-align: right;">163</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Ratts Tyerel</td>
<td style="text-align: right;">79</td>
</tr>
<tr class="even">
<td style="text-align: left;">Dud Bolt</td>
<td style="text-align: right;">94</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Gasgano</td>
<td style="text-align: right;">122</td>
</tr>
<tr class="even">
<td style="text-align: left;">Ben Quadinaros</td>
<td style="text-align: right;">163</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Cordé</td>
<td style="text-align: right;">157</td>
</tr>
<tr class="even">
<td style="text-align: left;">Barriss Offee</td>
<td style="text-align: right;">166</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Dormé</td>
<td style="text-align: right;">165</td>
</tr>
<tr class="even">
<td style="text-align: left;">Zam Wesell</td>
<td style="text-align: right;">168</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Jocasta Nu</td>
<td style="text-align: right;">167</td>
</tr>
<tr class="even">
<td style="text-align: left;">R4-P17</td>
<td style="text-align: right;">96</td>
</tr>
</tbody>
</table>
</div>
</div>
</section>
<section id="подсчитать-имт-индекс-массы-тела-для-всех-персонажей." class="level4">
<h4 class="anchored" data-anchor-id="подсчитать-имт-индекс-массы-тела-для-всех-персонажей.">7. Подсчитать ИМТ (индекс массы тела) для всех персонажей.</h4>
<div class="cell">
<div class="sourceCode cell-code" id="cb20"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb20-1"><a href="#cb20-1" aria-hidden="true" tabindex="-1"></a>starwars <span class="sc">%&gt;%</span> <span class="fu">mutate</span>(<span class="st">"BMI"</span> <span class="ot">=</span> mass<span class="sc">/</span>(height<span class="sc">*</span>height)) <span class="sc">%&gt;%</span> <span class="fu">select</span>(name,BMI)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre><code># A tibble: 87 × 2
   name                   BMI
   &lt;chr&gt;                &lt;dbl&gt;
 1 Luke Skywalker     0.00260
 2 C-3PO              0.00269
 3 R2-D2              0.00347
 4 Darth Vader        0.00333
 5 Leia Organa        0.00218
 6 Owen Lars          0.00379
 7 Beru Whitesun Lars 0.00275
 8 R5-D4              0.00340
 9 Biggs Darklighter  0.00251
10 Obi-Wan Kenobi     0.00232
# ℹ 77 more rows</code></pre>
</div>
</div>
</section>
<section id="найти-10-самых-вытянутых-персонажей." class="level4">
<h4 class="anchored" data-anchor-id="найти-10-самых-вытянутых-персонажей.">8.Найти 10 самых “вытянутых” персонажей.</h4>
<div class="cell">
<div class="sourceCode cell-code" id="cb22"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb22-1"><a href="#cb22-1" aria-hidden="true" tabindex="-1"></a>starwars <span class="sc">%&gt;%</span> <span class="fu">mutate</span>(<span class="at">Stretching =</span> mass<span class="sc">/</span>height)  <span class="sc">%&gt;%</span> <span class="fu">arrange</span>(<span class="fu">desc</span>(Stretching)) <span class="sc">%&gt;%</span> <span class="fu">head</span>(<span class="dv">10</span>) <span class="sc">%&gt;%</span> <span class="fu">select</span>(name,Stretching) </span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre><code># A tibble: 10 × 2
   name                  Stretching
   &lt;chr&gt;                      &lt;dbl&gt;
 1 Jabba Desilijic Tiure      7.76 
 2 Grievous                   0.736
 3 IG-88                      0.7  
 4 Owen Lars                  0.674
 5 Darth Vader                0.673
 6 Jek Tono Porkins           0.611
 7 Bossk                      0.595
 8 Tarfful                    0.581
 9 Dexter Jettster            0.515
10 Chewbacca                  0.491</code></pre>
</div>
</div>
</section>
<section id="найти-средний-возраст-персонажей-каждой-расы-вселенной-звездных-войн." class="level4">
<h4 class="anchored" data-anchor-id="найти-средний-возраст-персонажей-каждой-расы-вселенной-звездных-войн.">10. Найти средний возраст персонажей каждой расы вселенной Звездных войн.</h4>
<div class="cell">
<div class="sourceCode cell-code" id="cb24"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb24-1"><a href="#cb24-1" aria-hidden="true" tabindex="-1"></a>starwars <span class="sc">%&gt;%</span> <span class="fu">filter</span>(<span class="sc">!</span><span class="fu">is.na</span>(species) <span class="sc">&amp;</span> <span class="sc">!</span><span class="fu">is.na</span>(birth_year)) <span class="sc">%&gt;%</span> <span class="fu">group_by</span>(species) <span class="sc">%&gt;%</span> <span class="fu">summarise</span>(<span class="at">average_age =</span> <span class="fu">mean</span>(birth_year, <span class="at">na.rm =</span> <span class="cn">TRUE</span>)) <span class="sc">%&gt;%</span> knitr<span class="sc">::</span><span class="fu">kable</span>()</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output-display">
<table class="caption-top table table-sm table-striped small">
<thead>
<tr class="header">
<th style="text-align: left;">species</th>
<th style="text-align: right;">average_age</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;">Cerean</td>
<td style="text-align: right;">92.00000</td>
</tr>
<tr class="even">
<td style="text-align: left;">Droid</td>
<td style="text-align: right;">53.33333</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Ewok</td>
<td style="text-align: right;">8.00000</td>
</tr>
<tr class="even">
<td style="text-align: left;">Gungan</td>
<td style="text-align: right;">52.00000</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Human</td>
<td style="text-align: right;">53.74231</td>
</tr>
<tr class="even">
<td style="text-align: left;">Hutt</td>
<td style="text-align: right;">600.00000</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Kel Dor</td>
<td style="text-align: right;">22.00000</td>
</tr>
<tr class="even">
<td style="text-align: left;">Mirialan</td>
<td style="text-align: right;">49.00000</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Mon Calamari</td>
<td style="text-align: right;">41.00000</td>
</tr>
<tr class="even">
<td style="text-align: left;">Rodian</td>
<td style="text-align: right;">44.00000</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Trandoshan</td>
<td style="text-align: right;">53.00000</td>
</tr>
<tr class="even">
<td style="text-align: left;">Twi’lek</td>
<td style="text-align: right;">48.00000</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Wookiee</td>
<td style="text-align: right;">200.00000</td>
</tr>
<tr class="even">
<td style="text-align: left;">Yoda’s species</td>
<td style="text-align: right;">896.00000</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Zabrak</td>
<td style="text-align: right;">54.00000</td>
</tr>
</tbody>
</table>
</div>
</div>
</section>
<section id="найти-самый-распространенный-цвет-глаз-персонажей-вселенной-звездных-войн." class="level4">
<h4 class="anchored" data-anchor-id="найти-самый-распространенный-цвет-глаз-персонажей-вселенной-звездных-войн.">10. Найти самый распространенный цвет глаз персонажей вселенной Звездных войн.</h4>
<div class="cell">
<div class="sourceCode cell-code" id="cb25"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb25-1"><a href="#cb25-1" aria-hidden="true" tabindex="-1"></a>starwars <span class="sc">%&gt;%</span> <span class="fu">filter</span>(<span class="sc">!</span><span class="fu">is.na</span>(eye_color)) <span class="sc">%&gt;%</span> <span class="fu">group_by</span>(eye_color) <span class="sc">%&gt;%</span> <span class="fu">summarise</span>(<span class="at">count =</span> <span class="fu">n</span>()) <span class="sc">%&gt;%</span> <span class="fu">arrange</span>(<span class="fu">desc</span>(count)) <span class="sc">%&gt;%</span> <span class="fu">slice</span>(<span class="dv">1</span>) <span class="sc">%&gt;%</span> knitr<span class="sc">::</span><span class="fu">kable</span>()</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output-display">
<table class="caption-top table table-sm table-striped small">
<thead>
<tr class="header">
<th style="text-align: left;">eye_color</th>
<th style="text-align: right;">count</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;">brown</td>
<td style="text-align: right;">21</td>
</tr>
</tbody>
</table>
</div>
</div>
</section>
<section id="подсчитать-среднюю-длину-имени-в-каждой-расе-вселенной-звездных-войн." class="level4">
<h4 class="anchored" data-anchor-id="подсчитать-среднюю-длину-имени-в-каждой-расе-вселенной-звездных-войн.">11. Подсчитать среднюю длину имени в каждой расе вселенной Звездных войн.</h4>
<div class="cell">
<div class="sourceCode cell-code" id="cb26"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb26-1"><a href="#cb26-1" aria-hidden="true" tabindex="-1"></a>starwars <span class="sc">%&gt;%</span> <span class="fu">filter</span>(<span class="sc">!</span><span class="fu">is.na</span>(species) <span class="sc">&amp;</span> <span class="sc">!</span><span class="fu">is.na</span>(name)) <span class="sc">%&gt;%</span> <span class="fu">mutate</span>(<span class="at">name_length =</span> <span class="fu">nchar</span>(name)) <span class="sc">%&gt;%</span> <span class="fu">group_by</span>(species) <span class="sc">%&gt;%</span> <span class="fu">summarise</span>(<span class="at">len =</span> <span class="fu">mean</span>(name_length, <span class="at">na.rm =</span> <span class="cn">TRUE</span>)) <span class="sc">%&gt;%</span> knitr<span class="sc">::</span><span class="fu">kable</span>()</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output-display">
<table class="caption-top table table-sm table-striped small">
<thead>
<tr class="header">
<th style="text-align: left;">species</th>
<th style="text-align: right;">len</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;">Aleena</td>
<td style="text-align: right;">12.000000</td>
</tr>
<tr class="even">
<td style="text-align: left;">Besalisk</td>
<td style="text-align: right;">15.000000</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Cerean</td>
<td style="text-align: right;">12.000000</td>
</tr>
<tr class="even">
<td style="text-align: left;">Chagrian</td>
<td style="text-align: right;">10.000000</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Clawdite</td>
<td style="text-align: right;">10.000000</td>
</tr>
<tr class="even">
<td style="text-align: left;">Droid</td>
<td style="text-align: right;">4.833333</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Dug</td>
<td style="text-align: right;">7.000000</td>
</tr>
<tr class="even">
<td style="text-align: left;">Ewok</td>
<td style="text-align: right;">21.000000</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Geonosian</td>
<td style="text-align: right;">17.000000</td>
</tr>
<tr class="even">
<td style="text-align: left;">Gungan</td>
<td style="text-align: right;">11.666667</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Human</td>
<td style="text-align: right;">11.342857</td>
</tr>
<tr class="even">
<td style="text-align: left;">Hutt</td>
<td style="text-align: right;">21.000000</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Iktotchi</td>
<td style="text-align: right;">11.000000</td>
</tr>
<tr class="even">
<td style="text-align: left;">Kaleesh</td>
<td style="text-align: right;">8.000000</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Kaminoan</td>
<td style="text-align: right;">7.000000</td>
</tr>
<tr class="even">
<td style="text-align: left;">Kel Dor</td>
<td style="text-align: right;">8.000000</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Mirialan</td>
<td style="text-align: right;">14.000000</td>
</tr>
<tr class="even">
<td style="text-align: left;">Mon Calamari</td>
<td style="text-align: right;">6.000000</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Muun</td>
<td style="text-align: right;">8.000000</td>
</tr>
<tr class="even">
<td style="text-align: left;">Nautolan</td>
<td style="text-align: right;">9.000000</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Neimodian</td>
<td style="text-align: right;">11.000000</td>
</tr>
<tr class="even">
<td style="text-align: left;">Pau’an</td>
<td style="text-align: right;">10.000000</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Quermian</td>
<td style="text-align: right;">11.000000</td>
</tr>
<tr class="even">
<td style="text-align: left;">Rodian</td>
<td style="text-align: right;">6.000000</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Skakoan</td>
<td style="text-align: right;">10.000000</td>
</tr>
<tr class="even">
<td style="text-align: left;">Sullustan</td>
<td style="text-align: right;">9.000000</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Tholothian</td>
<td style="text-align: right;">10.000000</td>
</tr>
<tr class="even">
<td style="text-align: left;">Togruta</td>
<td style="text-align: right;">8.000000</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Toong</td>
<td style="text-align: right;">14.000000</td>
</tr>
<tr class="even">
<td style="text-align: left;">Toydarian</td>
<td style="text-align: right;">5.000000</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Trandoshan</td>
<td style="text-align: right;">5.000000</td>
</tr>
<tr class="even">
<td style="text-align: left;">Twi’lek</td>
<td style="text-align: right;">11.000000</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Vulptereen</td>
<td style="text-align: right;">8.000000</td>
</tr>
<tr class="even">
<td style="text-align: left;">Wookiee</td>
<td style="text-align: right;">8.000000</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Xexto</td>
<td style="text-align: right;">7.000000</td>
</tr>
<tr class="even">
<td style="text-align: left;">Yoda’s species</td>
<td style="text-align: right;">4.000000</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Zabrak</td>
<td style="text-align: right;">9.500000</td>
</tr>
</tbody>
</table>
</div>
</div>
</section>
</section>
</section>
<section id="оценка-результата" class="level2">
<h2 class="anchored" data-anchor-id="оценка-результата">Оценка результата</h2>
<p>В результате практической работы был установлен пакет dplyr. Были выполнены все необходимые аналитические задания для датасета starwars.</p>
</section>
<section id="вывод" class="level2">
<h2 class="anchored" data-anchor-id="вывод">Вывод</h2>
<p>В результате выполнения практической работы были освоены основные инструменты обработки данных пакета dplyr.</p>
</section>
</section>

</main>
<!-- /main column -->
<script id="quarto-html-after-body" type="application/javascript">
window.document.addEventListener("DOMContentLoaded", function (event) {
  const toggleBodyColorMode = (bsSheetEl) => {
    const mode = bsSheetEl.getAttribute("data-mode");
    const bodyEl = window.document.querySelector("body");
    if (mode === "dark") {
      bodyEl.classList.add("quarto-dark");
      bodyEl.classList.remove("quarto-light");
    } else {
      bodyEl.classList.add("quarto-light");
      bodyEl.classList.remove("quarto-dark");
    }
  }
  const toggleBodyColorPrimary = () => {
    const bsSheetEl = window.document.querySelector("link#quarto-bootstrap");
    if (bsSheetEl) {
      toggleBodyColorMode(bsSheetEl);
    }
  }
  toggleBodyColorPrimary();  
  const icon = "";
  const anchorJS = new window.AnchorJS();
  anchorJS.options = {
    placement: 'right',
    icon: icon
  };
  anchorJS.add('.anchored');
  const isCodeAnnotation = (el) => {
    for (const clz of el.classList) {
      if (clz.startsWith('code-annotation-')) {                     
        return true;
      }
    }
    return false;
  }
  const clipboard = new window.ClipboardJS('.code-copy-button', {
    text: function(trigger) {
      const codeEl = trigger.previousElementSibling.cloneNode(true);
      for (const childEl of codeEl.children) {
        if (isCodeAnnotation(childEl)) {
          childEl.remove();
        }
      }
      return codeEl.innerText;
    }
  });
  clipboard.on('success', function(e) {
    // button target
    const button = e.trigger;
    // don't keep focus
    button.blur();
    // flash "checked"
    button.classList.add('code-copy-button-checked');
    var currentTitle = button.getAttribute("title");
    button.setAttribute("title", "Copied!");
    let tooltip;
    if (window.bootstrap) {
      button.setAttribute("data-bs-toggle", "tooltip");
      button.setAttribute("data-bs-placement", "left");
      button.setAttribute("data-bs-title", "Copied!");
      tooltip = new bootstrap.Tooltip(button, 
        { trigger: "manual", 
          customClass: "code-copy-button-tooltip",
          offset: [0, -8]});
      tooltip.show();    
    }
    setTimeout(function() {
      if (tooltip) {
        tooltip.hide();
        button.removeAttribute("data-bs-title");
        button.removeAttribute("data-bs-toggle");
        button.removeAttribute("data-bs-placement");
      }
      button.setAttribute("title", currentTitle);
      button.classList.remove('code-copy-button-checked');
    }, 1000);
    // clear code selection
    e.clearSelection();
  });
    var localhostRegex = new RegExp(/^(?:http|https):\/\/localhost\:?[0-9]*\//);
    var mailtoRegex = new RegExp(/^mailto:/);
      var filterRegex = new RegExp('/' + window.location.host + '/');
    var isInternal = (href) => {
        return filterRegex.test(href) || localhostRegex.test(href) || mailtoRegex.test(href);
    }
    // Inspect non-navigation links and adorn them if external
 	var links = window.document.querySelectorAll('a[href]:not(.nav-link):not(.navbar-brand):not(.toc-action):not(.sidebar-link):not(.sidebar-item-toggle):not(.pagination-link):not(.no-external):not([aria-hidden]):not(.dropdown-item):not(.quarto-navigation-tool)');
    for (var i=0; i<links.length; i++) {
      const link = links[i];
      if (!isInternal(link.href)) {
        // undo the damage that might have been done by quarto-nav.js in the case of
        // links that we want to consider external
        if (link.dataset.originalHref !== undefined) {
          link.href = link.dataset.originalHref;
        }
      }
    }
  function tippyHover(el, contentFn, onTriggerFn, onUntriggerFn) {
    const config = {
      allowHTML: true,
      maxWidth: 500,
      delay: 100,
      arrow: false,
      appendTo: function(el) {
          return el.parentElement;
      },
      interactive: true,
      interactiveBorder: 10,
      theme: 'quarto',
      placement: 'bottom-start',
    };
    if (contentFn) {
      config.content = contentFn;
    }
    if (onTriggerFn) {
      config.onTrigger = onTriggerFn;
    }
    if (onUntriggerFn) {
      config.onUntrigger = onUntriggerFn;
    }
    window.tippy(el, config); 
  }
  const noterefs = window.document.querySelectorAll('a[role="doc-noteref"]');
  for (var i=0; i<noterefs.length; i++) {
    const ref = noterefs[i];
    tippyHover(ref, function() {
      // use id or data attribute instead here
      let href = ref.getAttribute('data-footnote-href') || ref.getAttribute('href');
      try { href = new URL(href).hash; } catch {}
      const id = href.replace(/^#\/?/, "");
      const note = window.document.getElementById(id);
      if (note) {
        return note.innerHTML;
      } else {
        return "";
      }
    });
  }
  const xrefs = window.document.querySelectorAll('a.quarto-xref');
  const processXRef = (id, note) => {
    // Strip column container classes
    const stripColumnClz = (el) => {
      el.classList.remove("page-full", "page-columns");
      if (el.children) {
        for (const child of el.children) {
          stripColumnClz(child);
        }
      }
    }
    stripColumnClz(note)
    if (id === null || id.startsWith('sec-')) {
      // Special case sections, only their first couple elements
      const container = document.createElement("div");
      if (note.children && note.children.length > 2) {
        container.appendChild(note.children[0].cloneNode(true));
        for (let i = 1; i < note.children.length; i++) {
          const child = note.children[i];
          if (child.tagName === "P" && child.innerText === "") {
            continue;
          } else {
            container.appendChild(child.cloneNode(true));
            break;
          }
        }
        if (window.Quarto?.typesetMath) {
          window.Quarto.typesetMath(container);
        }
        return container.innerHTML
      } else {
        if (window.Quarto?.typesetMath) {
          window.Quarto.typesetMath(note);
        }
        return note.innerHTML;
      }
    } else {
      // Remove any anchor links if they are present
      const anchorLink = note.querySelector('a.anchorjs-link');
      if (anchorLink) {
        anchorLink.remove();
      }
      if (window.Quarto?.typesetMath) {
        window.Quarto.typesetMath(note);
      }
      // TODO in 1.5, we should make sure this works without a callout special case
      if (note.classList.contains("callout")) {
        return note.outerHTML;
      } else {
        return note.innerHTML;
      }
    }
  }
  for (var i=0; i<xrefs.length; i++) {
    const xref = xrefs[i];
    tippyHover(xref, undefined, function(instance) {
      instance.disable();
      let url = xref.getAttribute('href');
      let hash = undefined; 
      if (url.startsWith('#')) {
        hash = url;
      } else {
        try { hash = new URL(url).hash; } catch {}
      }
      if (hash) {
        const id = hash.replace(/^#\/?/, "");
        const note = window.document.getElementById(id);
        if (note !== null) {
          try {
            const html = processXRef(id, note.cloneNode(true));
            instance.setContent(html);
          } finally {
            instance.enable();
            instance.show();
          }
        } else {
          // See if we can fetch this
          fetch(url.split('#')[0])
          .then(res => res.text())
          .then(html => {
            const parser = new DOMParser();
            const htmlDoc = parser.parseFromString(html, "text/html");
            const note = htmlDoc.getElementById(id);
            if (note !== null) {
              const html = processXRef(id, note);
              instance.setContent(html);
            } 
          }).finally(() => {
            instance.enable();
            instance.show();
          });
        }
      } else {
        // See if we can fetch a full url (with no hash to target)
        // This is a special case and we should probably do some content thinning / targeting
        fetch(url)
        .then(res => res.text())
        .then(html => {
          const parser = new DOMParser();
          const htmlDoc = parser.parseFromString(html, "text/html");
          const note = htmlDoc.querySelector('main.content');
          if (note !== null) {
            // This should only happen for chapter cross references
            // (since there is no id in the URL)
            // remove the first header
            if (note.children.length > 0 && note.children[0].tagName === "HEADER") {
              note.children[0].remove();
            }
            const html = processXRef(null, note);
            instance.setContent(html);
          } 
        }).finally(() => {
          instance.enable();
          instance.show();
        });
      }
    }, function(instance) {
    });
  }
      let selectedAnnoteEl;
      const selectorForAnnotation = ( cell, annotation) => {
        let cellAttr = 'data-code-cell="' + cell + '"';
        let lineAttr = 'data-code-annotation="' +  annotation + '"';
        const selector = 'span[' + cellAttr + '][' + lineAttr + ']';
        return selector;
      }
      const selectCodeLines = (annoteEl) => {
        const doc = window.document;
        const targetCell = annoteEl.getAttribute("data-target-cell");
        const targetAnnotation = annoteEl.getAttribute("data-target-annotation");
        const annoteSpan = window.document.querySelector(selectorForAnnotation(targetCell, targetAnnotation));
        const lines = annoteSpan.getAttribute("data-code-lines").split(",");
        const lineIds = lines.map((line) => {
          return targetCell + "-" + line;
        })
        let top = null;
        let height = null;
        let parent = null;
        if (lineIds.length > 0) {
            //compute the position of the single el (top and bottom and make a div)
            const el = window.document.getElementById(lineIds[0]);
            top = el.offsetTop;
            height = el.offsetHeight;
            parent = el.parentElement.parentElement;
          if (lineIds.length > 1) {
            const lastEl = window.document.getElementById(lineIds[lineIds.length - 1]);
            const bottom = lastEl.offsetTop + lastEl.offsetHeight;
            height = bottom - top;
          }
          if (top !== null && height !== null && parent !== null) {
            // cook up a div (if necessary) and position it 
            let div = window.document.getElementById("code-annotation-line-highlight");
            if (div === null) {
              div = window.document.createElement("div");
              div.setAttribute("id", "code-annotation-line-highlight");
              div.style.position = 'absolute';
              parent.appendChild(div);
            }
            div.style.top = top - 2 + "px";
            div.style.height = height + 4 + "px";
            div.style.left = 0;
            let gutterDiv = window.document.getElementById("code-annotation-line-highlight-gutter");
            if (gutterDiv === null) {
              gutterDiv = window.document.createElement("div");
              gutterDiv.setAttribute("id", "code-annotation-line-highlight-gutter");
              gutterDiv.style.position = 'absolute';
              const codeCell = window.document.getElementById(targetCell);
              const gutter = codeCell.querySelector('.code-annotation-gutter');
              gutter.appendChild(gutterDiv);
            }
            gutterDiv.style.top = top - 2 + "px";
            gutterDiv.style.height = height + 4 + "px";
          }
          selectedAnnoteEl = annoteEl;
        }
      };
      const unselectCodeLines = () => {
        const elementsIds = ["code-annotation-line-highlight", "code-annotation-line-highlight-gutter"];
        elementsIds.forEach((elId) => {
          const div = window.document.getElementById(elId);
          if (div) {
            div.remove();
          }
        });
        selectedAnnoteEl = undefined;
      };
        // Handle positioning of the toggle
    window.addEventListener(
      "resize",
      throttle(() => {
        elRect = undefined;
        if (selectedAnnoteEl) {
          selectCodeLines(selectedAnnoteEl);
        }
      }, 10)
    );
    function throttle(fn, ms) {
    let throttle = false;
    let timer;
      return (...args) => {
        if(!throttle) { // first call gets through
            fn.apply(this, args);
            throttle = true;
        } else { // all the others get throttled
            if(timer) clearTimeout(timer); // cancel #2
            timer = setTimeout(() => {
              fn.apply(this, args);
              timer = throttle = false;
            }, ms);
        }
      };
    }
      // Attach click handler to the DT
      const annoteDls = window.document.querySelectorAll('dt[data-target-cell]');
      for (const annoteDlNode of annoteDls) {
        annoteDlNode.addEventListener('click', (event) => {
          const clickedEl = event.target;
          if (clickedEl !== selectedAnnoteEl) {
            unselectCodeLines();
            const activeEl = window.document.querySelector('dt[data-target-cell].code-annotation-active');
            if (activeEl) {
              activeEl.classList.remove('code-annotation-active');
            }
            selectCodeLines(clickedEl);
            clickedEl.classList.add('code-annotation-active');
          } else {
            // Unselect the line
            unselectCodeLines();
            clickedEl.classList.remove('code-annotation-active');
          }
        });
      }
  const findCites = (el) => {
    const parentEl = el.parentElement;
    if (parentEl) {
      const cites = parentEl.dataset.cites;
      if (cites) {
        return {
          el,
          cites: cites.split(' ')
        };
      } else {
        return findCites(el.parentElement)
      }
    } else {
      return undefined;
    }
  };
  var bibliorefs = window.document.querySelectorAll('a[role="doc-biblioref"]');
  for (var i=0; i<bibliorefs.length; i++) {
    const ref = bibliorefs[i];
    const citeInfo = findCites(ref);
    if (citeInfo) {
      tippyHover(citeInfo.el, function() {
        var popup = window.document.createElement('div');
        citeInfo.cites.forEach(function(cite) {
          var citeDiv = window.document.createElement('div');
          citeDiv.classList.add('hanging-indent');
          citeDiv.classList.add('csl-entry');
          var biblioDiv = window.document.getElementById('ref-' + cite);
          if (biblioDiv) {
            citeDiv.innerHTML = biblioDiv.innerHTML;
          }
          popup.appendChild(citeDiv);
        });
        return popup.innerHTML;
      });
    }
  }
});
</script>
</div> <!-- /content -->




</body></html>