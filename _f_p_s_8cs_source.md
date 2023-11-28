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

FPS.cs

</div>

</div>

</div>

<div class="contents">

[Go to the documentation of this file.](_f_p_s_8cs.html)

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
<a href="class_f_p_s.html" class="line">8</a></span><span class="keyword">public</span>
<span class="keyword">class
</span><a href="class_f_p_s.html" class="code hl_class">FPS</a> :
MonoBehaviour

</div>

<div class="line">

<span id="l00009"></span><span class="lineno"> 9</span>{

</div>

<div class="line">

<span id="l00010"></span><span class="lineno"> 10</span>
<span class="keywordtype">void</span> Update()

</div>

<div class="line">

<span id="l00011"></span><span class="lineno"> 11</span> {

</div>

<div class="line">

<span id="l00012"></span><span class="lineno"> 12</span>
<span class="keywordflow">if</span> (Input.GetKeyDown(KeyCode.Alpha1))

</div>

<div class="line">

<span id="l00013"></span><span class="lineno"> 13</span> {

</div>

<div class="line">

<span id="l00014"></span><span class="lineno"> 14</span>
Application.targetFrameRate = 15;

</div>

<div class="line">

<span id="l00015"></span><span class="lineno"> 15</span> }

</div>

<div class="line">

<span id="l00016"></span><span class="lineno"> 16</span>
<span class="keywordflow">if</span> (Input.GetKeyDown(KeyCode.Alpha2))

</div>

<div class="line">

<span id="l00017"></span><span class="lineno"> 17</span> {

</div>

<div class="line">

<span id="l00018"></span><span class="lineno"> 18</span>
Application.targetFrameRate = 30;

</div>

<div class="line">

<span id="l00019"></span><span class="lineno"> 19</span> }

</div>

<div class="line">

<span id="l00020"></span><span class="lineno"> 20</span>
<span class="keywordflow">if</span> (Input.GetKeyDown(KeyCode.Alpha3))

</div>

<div class="line">

<span id="l00021"></span><span class="lineno"> 21</span> {

</div>

<div class="line">

<span id="l00022"></span><span class="lineno"> 22</span>
Application.targetFrameRate = 60;

</div>

<div class="line">

<span id="l00023"></span><span class="lineno"> 23</span> }

</div>

<div class="line">

<span id="l00024"></span><span class="lineno"> 24</span>
<span class="keywordflow">if</span> (Input.GetKeyDown(KeyCode.Alpha4))

</div>

<div class="line">

<span id="l00025"></span><span class="lineno"> 25</span> {

</div>

<div class="line">

<span id="l00026"></span><span class="lineno"> 26</span>
Application.targetFrameRate = 120;

</div>

<div class="line">

<span id="l00027"></span><span class="lineno"> 27</span> }

</div>

<div class="line">

<span id="l00028"></span><span class="lineno"> 28</span> }

</div>

<div class="line">

<span id="l00029"></span><span class="lineno"> 29</span>

</div>

<div class="line">

<span id="l00030"></span><span class="lineno"> 30</span>

</div>

<div class="line">

<span id="l00031"></span><span class="lineno"> 31</span>}

</div>

</div>

<div class="line">

<span id="l00032"></span><span class="lineno"> 32</span>

</div>

<div id="foldopen00042" class="foldopen" data-start="{" end="};">

<div class="line">

<span id="l00042"></span><span class="lineno">
<a href="class_math.html" class="line">42</a></span><span class="keyword">public</span>
<span class="keyword">class
</span><a href="class_math.html" class="code hl_class">Math</a> :
MonoBehaviour

</div>

<div class="line">

<span id="l00043"></span><span class="lineno"> 43</span>{

</div>

<div id="foldopen00047" class="foldopen" data-start="{" end="}">

<div class="line">

<span id="l00047"></span><span class="lineno">
<a href="class_math.html#a7c871f51dfc34ae986cd577e732183ae"
class="line">47</a></span> <span class="keyword">public</span>
<span class="keywordtype">int</span>
<a href="class_math.html#a7c871f51dfc34ae986cd577e732183ae"
class="code hl_function">AddTwoIntegers</a>(<span class="keywordtype">int</span>
a, <span class="keywordtype">int</span> b)

</div>

<div class="line">

<span id="l00048"></span><span class="lineno"> 48</span> {

</div>

<div class="line">

<span id="l00049"></span><span class="lineno"> 49</span>
<span class="keywordtype">int</span> add = 0;

</div>

<div class="line">

<span id="l00050"></span><span class="lineno"> 50</span> add = a + b;

</div>

<div class="line">

<span id="l00051"></span><span class="lineno"> 51</span>
<span class="keywordflow">return</span> add;

</div>

<div class="line">

<span id="l00052"></span><span class="lineno"> 52</span> }

</div>

</div>

<div class="line">

<span id="l00053"></span><span class="lineno"> 53</span>

</div>

<div id="foldopen00057" class="foldopen" data-start="{" end="}">

<div class="line">

<span id="l00057"></span><span class="lineno">
<a href="class_math.html#a62b011a90e95facd6ee112bd171bccc0"
class="line">57</a></span> <span class="keyword">public</span>
<span class="keywordtype">int</span>
<a href="class_math.html#a62b011a90e95facd6ee112bd171bccc0"
class="code hl_function">SubTwoIntegers</a>(<span class="keywordtype">int</span>
a, <span class="keywordtype">int</span> b)

</div>

<div class="line">

<span id="l00058"></span><span class="lineno"> 58</span> {

</div>

<div class="line">

<span id="l00059"></span><span class="lineno"> 59</span>
<span class="keywordtype">int</span> sub = 0;

</div>

<div class="line">

<span id="l00060"></span><span class="lineno"> 60</span> sub = a - b;

</div>

<div class="line">

<span id="l00061"></span><span class="lineno"> 61</span>
<span class="keywordflow">return</span> sub;

</div>

<div class="line">

<span id="l00062"></span><span class="lineno"> 62</span> }

</div>

</div>

<div class="line">

<span id="l00063"></span><span class="lineno"> 63</span>

</div>

<div id="foldopen00070" class="foldopen" data-start="{" end="}">

<div class="line">

<span id="l00070"></span><span class="lineno">
<a href="class_math.html#a56e40797c0abd636af35283f35748f59"
class="line">70</a></span> <span class="keyword">public</span>
<span class="keywordtype">int</span>
<a href="class_math.html#a56e40797c0abd636af35283f35748f59"
class="code hl_function">MultiTwoIntegers</a>(<span class="keywordtype">int</span>
a, <span class="keywordtype">int</span> b)

</div>

<div class="line">

<span id="l00071"></span><span class="lineno"> 71</span> {

</div>

<div class="line">

<span id="l00072"></span><span class="lineno"> 72</span>
<span class="keywordtype">int</span> mul = 0;

</div>

<div class="line">

<span id="l00073"></span><span class="lineno"> 73</span>
<span class="keywordflow">for</span>
(<span class="keywordtype">int</span> i = 0; i \< a; a++)

</div>

<div class="line">

<span id="l00074"></span><span class="lineno"> 74</span> {

</div>

<div class="line">

<span id="l00075"></span><span class="lineno"> 75</span>
<a href="class_math.html#a7c871f51dfc34ae986cd577e732183ae"
class="code hl_function">AddTwoIntegers</a>(mul, b);

</div>

<div class="line">

<span id="l00076"></span><span class="lineno"> 76</span> }

</div>

<div class="line">

<span id="l00077"></span><span class="lineno"> 77</span>
<span class="keywordflow">return</span> mul;

</div>

<div class="line">

<span id="l00078"></span><span class="lineno"> 78</span> }

</div>

</div>

<div class="line">

<span id="l00079"></span><span class="lineno"> 79</span>

</div>

<div id="foldopen00080" class="foldopen" data-start="{" end="}">

<div class="line">

<span id="l00080"></span><span class="lineno">
<a href="class_math.html#a5f89b21d11567863daecedba91addc11"
class="line">80</a></span> <span class="keyword">public</span>
<span class="keywordtype">void</span>
<a href="class_math.html#a5f89b21d11567863daecedba91addc11"
class="code hl_function">Update</a>()

</div>

<div class="line">

<span id="l00081"></span><span class="lineno"> 81</span> {

</div>

<div class="line">

<span id="l00083"></span><span class="lineno"> 83</span>
<span class="keywordtype">int</span> c =
<a href="class_math.html#a7c871f51dfc34ae986cd577e732183ae"
class="code hl_function">AddTwoIntegers</a>(3, 5);

</div>

<div class="line">

<span id="l00084"></span><span class="lineno"> 84</span> }

</div>

</div>

<div class="line">

<span id="l00085"></span><span class="lineno"> 85</span>}

</div>

</div>

<div class="line">

<span id="l00086"></span><span class="lineno"> 86</span>

</div>

<div class="line">

<span id="l00087"></span><span class="lineno"> 87</span>

</div>

<div class="line">

<span id="l00088"></span><span class="lineno"> 88</span>

</div>

<div id="aclass_f_p_s_html" class="ttc">

<div class="ttname">

[FPS](class_f_p_s.html)

</div>

<div class="ttdoc">

This Class performs FPS changes.

</div>

<div class="ttdef">

**Definition** [FPS.cs:9](_f_p_s_8cs_source.html#l00008)

</div>

</div>

<div id="aclass_math_html" class="ttc">

<div class="ttname">

[Math](class_math.html)

</div>

<div class="ttdoc">

Makes some calculating.

</div>

<div class="ttdef">

**Definition** [FPS.cs:43](_f_p_s_8cs_source.html#l00042)

</div>

</div>

<div id="aclass_math_html_a56e40797c0abd636af35283f35748f59"
class="ttc">

<div class="ttname">

[Math.MultiTwoIntegers](class_math.html#a56e40797c0abd636af35283f35748f59)

</div>

<div class="ttdeci">

int MultiTwoIntegers(int a, int b)

</div>

<div class="ttdoc">

Multiplies two Integers.

</div>

<div class="ttdef">

**Definition** [FPS.cs:70](_f_p_s_8cs_source.html#l00070)

</div>

</div>

<div id="aclass_math_html_a5f89b21d11567863daecedba91addc11"
class="ttc">

<div class="ttname">

[Math.Update](class_math.html#a5f89b21d11567863daecedba91addc11)

</div>

<div class="ttdeci">

void Update()

</div>

<div class="ttdef">

**Definition** [FPS.cs:80](_f_p_s_8cs_source.html#l00080)

</div>

</div>

<div id="aclass_math_html_a62b011a90e95facd6ee112bd171bccc0"
class="ttc">

<div class="ttname">

[Math.SubTwoIntegers](class_math.html#a62b011a90e95facd6ee112bd171bccc0)

</div>

<div class="ttdeci">

int SubTwoIntegers(int a, int b)

</div>

<div class="ttdoc">

Substracts two Integers.

</div>

<div class="ttdef">

**Definition** [FPS.cs:57](_f_p_s_8cs_source.html#l00057)

</div>

</div>

<div id="aclass_math_html_a7c871f51dfc34ae986cd577e732183ae"
class="ttc">

<div class="ttname">

[Math.AddTwoIntegers](class_math.html#a7c871f51dfc34ae986cd577e732183ae)

</div>

<div class="ttdeci">

int AddTwoIntegers(int a, int b)

</div>

<div class="ttdoc">

Adds two Integers.

</div>

<div class="ttdef">

**Definition** [FPS.cs:47](_f_p_s_8cs_source.html#l00047)

</div>

</div>

</div>

</div>

------------------------------------------------------------------------

<span class="small">Generated
by [<img src="doxygen.svg" class="footer" width="104" height="31"
alt="doxygen" />](https://www.doxygen.org/index.html) 1.9.8</span>
