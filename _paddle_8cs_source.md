<div id="top">

<div id="titlearea">

<table data-cellspacing="0" data-cellpadding="0">
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr id="projectrow" class="odd">
<td id="projectalign"><div id="projectname">
PongExample<span id="projectnumber"> 1.0.0</span>
</div></td>
</tr>
</tbody>
</table>

</div>

<div id="nav-path" class="navpath">

- <a href="dir_1dcde7ea5adb4470e937f2f1c0036389.html"
  class="el">FurkanIntern</a>
- <a href="dir_db18fc5b59b71647f21f3d49fd35b7b1.html"
  class="el">Internship</a>
- <a href="dir_7f2202f332a95df5c6e50699b596c7b9.html" class="el">Pong
  Staj</a>
- <a href="dir_b7568e80c0eb65df54ebd3d006b23e5e.html"
  class="el">Assets</a>
- <a href="dir_97d71e10d40891aefe860af68a8d9ea5.html"
  class="el">Scripts</a>

</div>

</div>

<div class="header">

<div class="headertitle">

<div class="title">

Paddle.cs

</div>

</div>

</div>

<div class="contents">

[Go to the documentation of this file.](_paddle_8cs.html)

<div class="fragment">

<div class="line">

<span id="l00001"></span><span class="lineno">
1</span><span class="keyword">using </span>System;

</div>

<div class="line">

<span id="l00002"></span><span class="lineno">
2</span><span class="keyword">using </span>System.Collections;

</div>

<div class="line">

<span id="l00003"></span><span class="lineno">
3</span><span class="keyword">using </span>System.Collections.Generic;

</div>

<div class="line">

<span id="l00004"></span><span class="lineno">
4</span><span class="keyword">using </span>UnityEngine;

</div>

<div id="foldopen00008" class="foldopen" data-start="{" end="};">

<div class="line">

<span id="l00008"></span><span class="lineno">
<a href="class_paddle.html" class="line">8</a></span><span class="keyword">public</span>
<span class="keyword">class
</span><a href="class_paddle.html" class="code hl_class">Paddle</a> :
MonoBehaviour

</div>

<div class="line">

<span id="l00009"></span><span class="lineno"> 9</span>{

</div>

<div class="line">

<span id="l00010"></span><span class="lineno">
<a href="class_paddle.html#a25f7d923692a3ad5c5c394961a847a3a"
class="line">10</a></span> <span class="keyword">public</span>
<span class="keywordtype">float</span>
<a href="class_paddle.html#a25f7d923692a3ad5c5c394961a847a3a"
class="code hl_variable">speed</a> = 5.0f; <span class="comment">//
Paddle'ın hızı</span>

</div>

<div class="line">

<span id="l00011"></span><span class="lineno"> 11</span>
<span class="keyword">private</span>
<span class="keywordtype">void</span> Start()

</div>

<div class="line">

<span id="l00012"></span><span class="lineno"> 12</span> {

</div>

<div class="line">

<span id="l00013"></span><span class="lineno">
13</span><span class="preprocessor"> \#region example1</span>

</div>

<div class="line">

<span id="l00014"></span><span class="lineno"> 14</span>

</div>

<div class="line">

<span id="l00015"></span><span class="lineno"> 15</span>
Debug.Log(<span class="stringliteral">"DEBUG"</span>);

</div>

<div class="line">

<span id="l00016"></span><span class="lineno"> 16</span>

</div>

<div class="line">

<span id="l00017"></span><span class="lineno">
17</span><span class="preprocessor"> \#endregion</span>

</div>

<div class="line">

<span id="l00018"></span><span class="lineno"> 18</span> }

</div>

<div class="line">

<span id="l00019"></span><span class="lineno"> 19</span>

</div>

<div class="line">

<span id="l00020"></span><span class="lineno"> 20</span>
<span class="keywordtype">void</span> Update()

</div>

<div class="line">

<span id="l00021"></span><span class="lineno"> 21</span> {

</div>

<div class="line">

<span id="l00022"></span><span class="lineno"> 22</span>
<span class="comment">// Eğer yukarı hareket tuşuna basılırsa, paddle'ı
yukarı hareket ettir.</span>

</div>

<div class="line">

<span id="l00023"></span><span class="lineno"> 23</span>
<span class="keywordflow">if</span> (Input.GetKey(KeyCode.W) \|\|
Input.GetKey(KeyCode.UpArrow))

</div>

<div class="line">

<span id="l00024"></span><span class="lineno"> 24</span> {

</div>

<div class="line">

<span id="l00025"></span><span class="lineno"> 25</span>
transform.Translate(Vector2.up \*
<a href="class_paddle.html#a25f7d923692a3ad5c5c394961a847a3a"
class="code hl_variable">speed</a> \* Time.deltaTime);

</div>

<div class="line">

<span id="l00026"></span><span class="lineno"> 26</span> }

</div>

<div class="line">

<span id="l00027"></span><span class="lineno"> 27</span>

</div>

<div class="line">

<span id="l00028"></span><span class="lineno"> 28</span>
<span class="comment">// Eğer aşağı hareket tuşuna basılırsa, paddle'ı
aşağı hareket ettir.</span>

</div>

<div class="line">

<span id="l00029"></span><span class="lineno"> 29</span>
<span class="keywordflow">if</span> (Input.GetKey(KeyCode.S) \|\|
Input.GetKey(KeyCode.DownArrow))

</div>

<div class="line">

<span id="l00030"></span><span class="lineno"> 30</span> {

</div>

<div class="line">

<span id="l00031"></span><span class="lineno"> 31</span>
transform.Translate(Vector2.down \*
<a href="class_paddle.html#a25f7d923692a3ad5c5c394961a847a3a"
class="code hl_variable">speed</a> \* Time.deltaTime);

</div>

<div class="line">

<span id="l00032"></span><span class="lineno"> 32</span> }

</div>

<div class="line">

<span id="l00033"></span><span class="lineno"> 33</span> }

</div>

<div class="line">

<span id="l00034"></span><span class="lineno"> 34</span>}

</div>

</div>

<div class="line">

<span id="l00063"></span><span class="lineno"> 63</span>

</div>

<div class="line">

<span id="l00066"></span><span class="lineno"> 66</span>

</div>

<div id="aclass_paddle_html" class="ttc">

<div class="ttname">

[Paddle](class_paddle.html)

</div>

<div class="ttdoc">

This Class performs Paddle Movement.

</div>

<div class="ttdef">

**Definition** [Paddle.cs:9](_paddle_8cs_source.html#l00008)

</div>

</div>

<div id="aclass_paddle_html_a25f7d923692a3ad5c5c394961a847a3a"
class="ttc">

<div class="ttname">

[Paddle.speed](class_paddle.html#a25f7d923692a3ad5c5c394961a847a3a)

</div>

<div class="ttdeci">

float speed

</div>

<div class="ttdef">

**Definition** [Paddle.cs:10](_paddle_8cs_source.html#l00010)

</div>

</div>

</div>

</div>

------------------------------------------------------------------------

<span class="small">Generated
by [<img src="doxygen.svg" class="footer" width="104" height="31"
alt="doxygen" />](https://www.doxygen.org/index.html) 1.9.8</span>
