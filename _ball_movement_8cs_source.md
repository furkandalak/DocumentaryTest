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

BallMovement.cs

</div>

</div>

</div>

<div class="contents">

[Go to the documentation of this file.](_ball_movement_8cs.html)

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
4</span><span class="keyword">using </span>System.Threading.Tasks;

</div>

<div class="line">

<span id="l00005"></span><span class="lineno">
5</span><span class="keyword">using </span>UnityEngine;

</div>

<div class="line">

<span id="l00006"></span><span class="lineno">
6</span><span class="keyword">using </span>UnityEngine.Assertions.Must;

</div>

<div class="line">

<span id="l00007"></span><span class="lineno">
<a href="_ball_movement_8cs.html#a832e8f52fca5a678819ec96269dcb532"
class="line">7</a></span><span class="keyword">using
</span><a href="_ball_movement_8cs.html#a832e8f52fca5a678819ec96269dcb532"
class="code hl_typedef">Random</a> = UnityEngine.Random;

</div>

<div class="line">

<span id="l00008"></span><span class="lineno"> 8</span>

</div>

<div id="foldopen00012" class="foldopen" data-start="{" end="};">

<div class="line">

<span id="l00012"></span><span class="lineno">
<a href="class_ball_movement.html" class="line">12</a></span><span class="keyword">public</span>
<span class="keyword">class </span><a href="class_ball_movement.html"
class="code hl_class">BallMovement</a> : MonoBehaviour

</div>

<div class="line">

<span id="l00013"></span><span class="lineno"> 13</span>{

</div>

<div class="line">

<span id="l00014"></span><span class="lineno">
<a href="class_ball_movement.html#ab2657ddd68ebf02876c11212145fcfdb"
class="line">14</a></span> <span class="keyword">public</span> Transform
<a href="class_ball_movement.html#ab2657ddd68ebf02876c11212145fcfdb"
class="code hl_variable">ball</a>;

</div>

<div class="line">

<span id="l00015"></span><span class="lineno">
<a href="class_ball_movement.html#afc7bd1ba11daafd6825473d72337f708"
class="line">15</a></span> <span class="keyword">public</span> Transform
<a href="class_ball_movement.html#afc7bd1ba11daafd6825473d72337f708"
class="code hl_variable">paddle1</a>;

</div>

<div class="line">

<span id="l00016"></span><span class="lineno">
<a href="class_ball_movement.html#ae6fbc952b54fb915ac79385d0a55ecc0"
class="line">16</a></span> <span class="keyword">public</span> Transform
<a href="class_ball_movement.html#ae6fbc952b54fb915ac79385d0a55ecc0"
class="code hl_variable">paddle2</a>;

</div>

<div class="line">

<span id="l00017"></span><span class="lineno"> 17</span>

</div>

<div class="line">

<span id="l00018"></span><span class="lineno">
<a href="class_ball_movement.html#aa33416010b3040ac39e7b02bfa7aa95a"
class="line">18</a></span> <span class="keyword">public</span>
<span class="keywordtype">float</span>
<a href="class_ball_movement.html#aa33416010b3040ac39e7b02bfa7aa95a"
class="code hl_variable">edgeFollow</a> = 11f;

</div>

<div class="line">

<span id="l00019"></span><span class="lineno">
<a href="class_ball_movement.html#ae5be514e8f3c1b3af767d5a8627c9277"
class="line">19</a></span> <span class="keyword">public</span>
<span class="keywordtype">float</span>
<a href="class_ball_movement.html#ae5be514e8f3c1b3af767d5a8627c9277"
class="code hl_variable">speed</a> = 5f;

</div>

<div class="line">

<span id="l00020"></span><span class="lineno">
<a href="class_ball_movement.html#ac6a63f2cbb61ce14dda95621177ee843"
class="line">20</a></span> <span class="keyword">public</span> Vector2
<a href="class_ball_movement.html#ac6a63f2cbb61ce14dda95621177ee843"
class="code hl_variable">direction</a>;

</div>

<div class="line">

<span id="l00021"></span><span class="lineno"> 21</span>

</div>

<div class="line">

<span id="l00022"></span><span class="lineno"> 22</span>
<span class="keyword">private</span>
<span class="keywordtype">int</span> score1 = 0;

</div>

<div class="line">

<span id="l00023"></span><span class="lineno"> 23</span>
<span class="keyword">private</span>
<span class="keywordtype">int</span> score2 = 0;

</div>

<div class="line">

<span id="l00024"></span><span class="lineno"> 24</span>

</div>

<div class="line">

<span id="l00025"></span><span class="lineno"> 25</span>
<span class="keyword">private</span> Vector3 ballVelocity;

</div>

<div class="line">

<span id="l00026"></span><span class="lineno"> 26</span>
<span class="keyword">private</span> List\<LineSegment\> lineSegments;

</div>

<div class="line">

<span id="l00027"></span><span class="lineno"> 27</span>

</div>

<div class="line">

<span id="l00028"></span><span class="lineno"> 28</span>

</div>

<div class="line">

<span id="l00029"></span><span class="lineno"> 29</span>
<span class="keyword">enum</span> SegmentName

</div>

<div class="line">

<span id="l00030"></span><span class="lineno"> 30</span> {

</div>

<div class="line">

<span id="l00031"></span><span class="lineno"> 31</span> LeftPaddle = 0,

</div>

<div class="line">

<span id="l00032"></span><span class="lineno"> 32</span> RightPaddle =
1,

</div>

<div class="line">

<span id="l00033"></span><span class="lineno"> 33</span> TopWall = 2,

</div>

<div class="line">

<span id="l00034"></span><span class="lineno"> 34</span> BottomWall = 3,

</div>

<div class="line">

<span id="l00035"></span><span class="lineno"> 35</span> }

</div>

<div class="line">

<span id="l00036"></span><span class="lineno"> 36</span>

</div>

<div class="line">

<span id="l00037"></span><span class="lineno"> 37</span>
<span class="keywordtype">void</span> Start()

</div>

<div class="line">

<span id="l00038"></span><span class="lineno"> 38</span> {

</div>

<div class="line">

<span id="l00039"></span><span class="lineno"> 39</span>
<span class="comment">//Rastgele direction ayarla</span>

</div>

<div class="line">

<span id="l00040"></span><span class="lineno"> 40</span>
<a href="class_ball_movement.html#ac6a63f2cbb61ce14dda95621177ee843"
class="code hl_variable">direction</a> =
<span class="keyword">new</span>
Vector3(<a href="_ball_movement_8cs.html#a832e8f52fca5a678819ec96269dcb532"
class="code hl_typedef">Random</a>.Range(0, 2) == 0 ? -1 : 1,
<a href="_ball_movement_8cs.html#a832e8f52fca5a678819ec96269dcb532"
class="code hl_typedef">Random</a>.Range(0, 2) == 0 ? -1 : 1, 0);

</div>

<div class="line">

<span id="l00041"></span><span class="lineno"> 41</span>

</div>

<div class="line">

<span id="l00042"></span><span class="lineno"> 42</span>
<span class="comment">//Collision lineları ayarla</span>

</div>

<div class="line">

<span id="l00043"></span><span class="lineno"> 43</span> Vector3
paddle1TopEdge = paddle1.position - <span class="keyword">new</span>
Vector3(0,
<a href="class_ball_movement.html#afc7bd1ba11daafd6825473d72337f708"
class="code hl_variable">paddle1</a>.transform.localScale.y / 2, 0);

</div>

<div class="line">

<span id="l00044"></span><span class="lineno"> 44</span> Vector3
paddle1BottomEdge = paddle1.position + <span class="keyword">new</span>
Vector3(0,
<a href="class_ball_movement.html#afc7bd1ba11daafd6825473d72337f708"
class="code hl_variable">paddle1</a>.transform.localScale.y / 2, 0);

</div>

<div class="line">

<span id="l00045"></span><span class="lineno"> 45</span> Vector3
paddle2TopEdge = paddle2.position - <span class="keyword">new</span>
Vector3(0,
<a href="class_ball_movement.html#ae6fbc952b54fb915ac79385d0a55ecc0"
class="code hl_variable">paddle2</a>.transform.localScale.y / 2, 0);

</div>

<div class="line">

<span id="l00046"></span><span class="lineno"> 46</span> Vector3
paddle2BottomEdge = paddle2.position + <span class="keyword">new</span>
Vector3(0,
<a href="class_ball_movement.html#ae6fbc952b54fb915ac79385d0a55ecc0"
class="code hl_variable">paddle2</a>.transform.localScale.y / 2, 0);

</div>

<div class="line">

<span id="l00047"></span><span class="lineno"> 47</span>

</div>

<div class="line">

<span id="l00048"></span><span class="lineno"> 48</span> Vector3 topLeft
= <span class="keyword">new</span>
Vector3(+<a href="class_ball_movement.html#aa33416010b3040ac39e7b02bfa7aa95a"
class="code hl_variable">edgeFollow</a>, 5, 0);

</div>

<div class="line">

<span id="l00049"></span><span class="lineno"> 49</span> Vector3
topRight = <span class="keyword">new</span>
Vector3(-<a href="class_ball_movement.html#aa33416010b3040ac39e7b02bfa7aa95a"
class="code hl_variable">edgeFollow</a>, 5, 0);

</div>

<div class="line">

<span id="l00050"></span><span class="lineno"> 50</span>

</div>

<div class="line">

<span id="l00051"></span><span class="lineno"> 51</span> Vector3
bottomLeft = <span class="keyword">new</span>
Vector3(+<a href="class_ball_movement.html#aa33416010b3040ac39e7b02bfa7aa95a"
class="code hl_variable">edgeFollow</a>, -5, 0);

</div>

<div class="line">

<span id="l00052"></span><span class="lineno"> 52</span> Vector3
bottomRight = <span class="keyword">new</span>
Vector3(-<a href="class_ball_movement.html#aa33416010b3040ac39e7b02bfa7aa95a"
class="code hl_variable">edgeFollow</a>, -5, 0);

</div>

<div class="line">

<span id="l00053"></span><span class="lineno"> 53</span>

</div>

<div class="line">

<span id="l00054"></span><span class="lineno"> 54</span> Vector3
leftScoreTop = <span class="keyword">new</span> Vector3(-11, -5, 0);

</div>

<div class="line">

<span id="l00055"></span><span class="lineno"> 55</span> Vector3
leftScoreBottom = <span class="keyword">new</span> Vector3(-11, 5, 0);

</div>

<div class="line">

<span id="l00056"></span><span class="lineno"> 56</span>

</div>

<div class="line">

<span id="l00057"></span><span class="lineno"> 57</span> Vector3
rightScoreTop = <span class="keyword">new</span> Vector3(11, -5, 0);

</div>

<div class="line">

<span id="l00058"></span><span class="lineno"> 58</span> Vector3
rightScoreBottom = <span class="keyword">new</span> Vector3(11, 5, 0);

</div>

<div class="line">

<span id="l00059"></span><span class="lineno"> 59</span>

</div>

<div class="line">

<span id="l00060"></span><span class="lineno"> 60</span> lineSegments =
<span class="keyword">new</span> List\<LineSegment\>

</div>

<div class="line">

<span id="l00061"></span><span class="lineno"> 61</span> {

</div>

<div class="line">

<span id="l00062"></span><span class="lineno"> 62</span>
<span class="keyword">new</span> LineSegment(paddle1BottomEdge,
paddle1TopEdge, Vector3.right),

</div>

<div class="line">

<span id="l00063"></span><span class="lineno"> 63</span>
<span class="keyword">new</span> LineSegment(paddle2BottomEdge,
paddle2TopEdge, Vector3.left),

</div>

<div class="line">

<span id="l00064"></span><span class="lineno"> 64</span>
<span class="keyword">new</span> LineSegment(topLeft, topRight,
Vector3.down),

</div>

<div class="line">

<span id="l00065"></span><span class="lineno"> 65</span>
<span class="keyword">new</span> LineSegment(bottomLeft, bottomRight,
Vector3.up),

</div>

<div class="line">

<span id="l00066"></span><span class="lineno"> 66</span>
<span class="keyword">new</span> LineSegment(leftScoreTop,
leftScoreBottom, Vector3.right),

</div>

<div class="line">

<span id="l00067"></span><span class="lineno"> 67</span>
<span class="keyword">new</span> LineSegment(rightScoreTop,
rightScoreBottom, Vector3.left),

</div>

<div class="line">

<span id="l00068"></span><span class="lineno"> 68</span> };

</div>

<div class="line">

<span id="l00069"></span><span class="lineno"> 69</span> }

</div>

<div class="line">

<span id="l00070"></span><span class="lineno"> 70</span>

</div>

<div class="line">

<span id="l00071"></span><span class="lineno"> 71</span>
<span class="keywordtype">void</span> Update()

</div>

<div class="line">

<span id="l00072"></span><span class="lineno"> 72</span> {

</div>

<div class="line">

<span id="l00073"></span><span class="lineno"> 73</span>
<span class="comment">// Topun bir sonraki pozisyonunu tahmin et</span>

</div>

<div class="line">

<span id="l00074"></span><span class="lineno"> 74</span> Vector3
ballVelocity =
<a href="class_ball_movement.html#ac6a63f2cbb61ce14dda95621177ee843"
class="code hl_variable">direction</a> \*
<a href="class_ball_movement.html#ae5be514e8f3c1b3af767d5a8627c9277"
class="code hl_variable">speed</a>;

</div>

<div class="line">

<span id="l00075"></span><span class="lineno"> 75</span>

</div>

<div class="line">

<span id="l00076"></span><span class="lineno"> 76</span> Vector3
nextPosition = ball.position + ballVelocity \* Time.deltaTime;

</div>

<div class="line">

<span id="l00077"></span><span class="lineno"> 77</span>

</div>

<div class="line">

<span id="l00078"></span><span class="lineno"> 78</span>
<span class="comment">// Paddle'ın kenarlarını ve ekranın kenarlarını
temsil eden çizgi parçalarını oluştur</span>

</div>

<div class="line">

<span id="l00079"></span><span class="lineno"> 79</span>

</div>

<div class="line">

<span id="l00080"></span><span class="lineno"> 80</span> var
leftPaddleSegment = lineSegments\[(int)SegmentName.LeftPaddle\];

</div>

<div class="line">

<span id="l00081"></span><span class="lineno"> 81</span>
leftPaddleSegment.start = paddle1.position -
<span class="keyword">new</span> Vector3(0,
<a href="class_ball_movement.html#afc7bd1ba11daafd6825473d72337f708"
class="code hl_variable">paddle1</a>.transform.localScale.y / 2, 0);

</div>

<div class="line">

<span id="l00082"></span><span class="lineno"> 82</span>
leftPaddleSegment.end = paddle1.position +
<span class="keyword">new</span> Vector3(0,
<a href="class_ball_movement.html#afc7bd1ba11daafd6825473d72337f708"
class="code hl_variable">paddle1</a>.transform.localScale.y / 2, 0);

</div>

<div class="line">

<span id="l00083"></span><span class="lineno"> 83</span>
lineSegments\[(int)SegmentName.LeftPaddle\] = leftPaddleSegment;

</div>

<div class="line">

<span id="l00084"></span><span class="lineno"> 84</span>

</div>

<div class="line">

<span id="l00085"></span><span class="lineno"> 85</span> var
rightPaddleSegment = lineSegments\[(int)SegmentName.RightPaddle\];

</div>

<div class="line">

<span id="l00086"></span><span class="lineno"> 86</span>
rightPaddleSegment.start = paddle2.position -
<span class="keyword">new</span> Vector3(0,
<a href="class_ball_movement.html#ae6fbc952b54fb915ac79385d0a55ecc0"
class="code hl_variable">paddle2</a>.transform.localScale.y / 2, 0);

</div>

<div class="line">

<span id="l00087"></span><span class="lineno"> 87</span>
rightPaddleSegment.end = paddle2.position +
<span class="keyword">new</span> Vector3(0,
<a href="class_ball_movement.html#ae6fbc952b54fb915ac79385d0a55ecc0"
class="code hl_variable">paddle2</a>.transform.localScale.y / 2, 0);

</div>

<div class="line">

<span id="l00088"></span><span class="lineno"> 88</span>
lineSegments\[(int)SegmentName.RightPaddle\] = rightPaddleSegment;

</div>

<div class="line">

<span id="l00089"></span><span class="lineno"> 89</span>

</div>

<div class="line">

<span id="l00090"></span><span class="lineno"> 90</span>

</div>

<div class="line">

<span id="l00091"></span><span class="lineno"> 91</span>
<span class="comment">// Topun hareketini temsil eden çizgi parçasını
oluştur</span>

</div>

<div class="line">

<span id="l00092"></span><span class="lineno"> 92</span> Vector3
ballStart =
<a href="class_ball_movement.html#ab2657ddd68ebf02876c11212145fcfdb"
class="code hl_variable">ball</a>.position;

</div>

<div class="line">

<span id="l00093"></span><span class="lineno"> 93</span> Vector3 ballEnd
= nextPosition;

</div>

<div class="line">

<span id="l00094"></span><span class="lineno"> 94</span>

</div>

<div class="line">

<span id="l00095"></span><span class="lineno"> 95</span>
Debug.DrawLine(ballStart, ballEnd, Color.red);

</div>

<div class="line">

<span id="l00096"></span><span class="lineno"> 96</span>

</div>

<div class="line">

<span id="l00097"></span><span class="lineno"> 97</span>

</div>

<div class="line">

<span id="l00098"></span><span class="lineno"> 98</span>
<span class="comment">// Topun hareket çizgisi ile paddle'ın kenarları
ve ekranın kenarları arasında kesişme kontrolü yap</span>

</div>

<div class="line">

<span id="l00099"></span><span class="lineno"> 99</span>

</div>

<div class="line">

<span id="l00100"></span><span class="lineno"> 100</span>
<span class="keywordflow">foreach</span> (var lineSegment
<span class="keywordflow">in</span> lineSegments)

</div>

<div class="line">

<span id="l00101"></span><span class="lineno"> 101</span> {

</div>

<div class="line">

<span id="l00102"></span><span class="lineno"> 102</span>
Debug.DrawLine(lineSegment.start, lineSegment.end, Color.red);

</div>

<div class="line">

<span id="l00103"></span><span class="lineno"> 103</span> }

</div>

<div class="line">

<span id="l00104"></span><span class="lineno"> 104</span>

</div>

<div class="line">

<span id="l00105"></span><span class="lineno"> 105</span>

</div>

<div class="line">

<span id="l00106"></span><span class="lineno"> 106</span>
<span class="keywordflow">foreach</span> (var lineSegment
<span class="keywordflow">in</span> lineSegments)

</div>

<div class="line">

<span id="l00107"></span><span class="lineno"> 107</span> {

</div>

<div class="line">

<span id="l00108"></span><span class="lineno"> 108</span>
<span class="keywordflow">if</span>
(<a href="class_ball_movement.html#a2c6180a5d985ce8c7c39596ab9e5d9a3"
class="code hl_function">LineSegmentIntersection</a>(ballStart, ballEnd,
lineSegment.start, lineSegment.end, out Vector3 intersectionPoint))

</div>

<div class="line">

<span id="l00109"></span><span class="lineno"> 109</span> {

</div>

<div class="line">

<span id="l00110"></span><span class="lineno"> 110</span>
<a href="class_ball_movement.html#ac6a63f2cbb61ce14dda95621177ee843"
class="code hl_variable">direction</a> =
Vector3.Reflect(<a href="class_ball_movement.html#ac6a63f2cbb61ce14dda95621177ee843"
class="code hl_variable">direction</a>, lineSegment.normal);

</div>

<div class="line">

<span id="l00111"></span><span class="lineno"> 111</span>
<span class="keywordflow">if</span> (intersectionPoint.x \<= -11f)

</div>

<div class="line">

<span id="l00112"></span><span class="lineno"> 112</span> {

</div>

<div class="line">

<span id="l00113"></span><span class="lineno"> 113</span> score1 += 1;

</div>

<div class="line">

<span id="l00114"></span><span class="lineno"> 114</span>
intersectionPoint = <span class="keyword">new</span> Vector3(0, 0, 0);

</div>

<div class="line">

<span id="l00115"></span><span class="lineno"> 115</span>
<a href="class_ball_movement.html#ac6a63f2cbb61ce14dda95621177ee843"
class="code hl_variable">direction</a> =
<span class="keyword">new</span> Vector3(1,
<a href="_ball_movement_8cs.html#a832e8f52fca5a678819ec96269dcb532"
class="code hl_typedef">Random</a>.Range(0, 2) == 0 ? -1 : 1, 0);

</div>

<div class="line">

<span id="l00116"></span><span class="lineno"> 116</span> }

</div>

<div class="line">

<span id="l00117"></span><span class="lineno"> 117</span>

</div>

<div class="line">

<span id="l00118"></span><span class="lineno"> 118</span>
<span class="keywordflow">if</span> (intersectionPoint.x \>= 11f)

</div>

<div class="line">

<span id="l00119"></span><span class="lineno"> 119</span> {

</div>

<div class="line">

<span id="l00120"></span><span class="lineno"> 120</span> score2 += 1;

</div>

<div class="line">

<span id="l00121"></span><span class="lineno"> 121</span>
intersectionPoint = <span class="keyword">new</span> Vector3(0, 0, 0);

</div>

<div class="line">

<span id="l00122"></span><span class="lineno"> 122</span>
<a href="class_ball_movement.html#ac6a63f2cbb61ce14dda95621177ee843"
class="code hl_variable">direction</a> =
<span class="keyword">new</span> Vector3(-1,
<a href="_ball_movement_8cs.html#a832e8f52fca5a678819ec96269dcb532"
class="code hl_typedef">Random</a>.Range(0, 2) == 0 ? -1 : 1, 0);

</div>

<div class="line">

<span id="l00123"></span><span class="lineno"> 123</span> }

</div>

<div class="line">

<span id="l00124"></span><span class="lineno"> 124</span>

</div>

<div class="line">

<span id="l00125"></span><span class="lineno"> 125</span>
Debug.DrawLine(lineSegment.start, lineSegment.end, Color.green);

</div>

<div class="line">

<span id="l00126"></span><span class="lineno"> 126</span>

</div>

<div class="line">

<span id="l00127"></span><span class="lineno"> 127</span>
Debug.DrawLine(<a href="class_ball_movement.html#ab2657ddd68ebf02876c11212145fcfdb"
class="code hl_variable">ball</a>.position, intersectionPoint,
Color.blue);

</div>

<div class="line">

<span id="l00128"></span><span class="lineno"> 128</span>

</div>

<div class="line">

<span id="l00129"></span><span class="lineno"> 129</span>

</div>

<div class="line">

<span id="l00130"></span><span class="lineno"> 130</span>
<span class="comment">// Çarpışma noktasının biraz ötesine
yerleştirerek, topun çarpışma noktasında sıkışmasını önler</span>

</div>

<div class="line">

<span id="l00131"></span><span class="lineno"> 131</span>
<span class="keywordtype">float</span> distanceToMove = .1f;

</div>

<div class="line">

<span id="l00132"></span><span class="lineno"> 132</span> nextPosition =
intersectionPoint + (Vector3)lineSegment.normal \* distanceToMove;

</div>

<div class="line">

<span id="l00133"></span><span class="lineno"> 133</span>
<span class="comment">// Topu hareket ettir</span>

</div>

<div class="line">

<span id="l00134"></span><span class="lineno"> 134</span>
Debug.DrawLine(nextPosition, intersectionPoint, Color.green);

</div>

<div class="line">

<span id="l00135"></span><span class="lineno"> 135</span>
<span class="keywordflow">break</span>;

</div>

<div class="line">

<span id="l00136"></span><span class="lineno"> 136</span> }

</div>

<div class="line">

<span id="l00137"></span><span class="lineno"> 137</span> }

</div>

<div class="line">

<span id="l00138"></span><span class="lineno"> 138</span>

</div>

<div class="line">

<span id="l00139"></span><span class="lineno"> 139</span>

</div>

<div class="line">

<span id="l00140"></span><span class="lineno"> 140</span>

</div>

<div class="line">

<span id="l00141"></span><span class="lineno"> 141</span>

</div>

<div class="line">

<span id="l00142"></span><span class="lineno"> 142</span>
<span class="comment">// Topu hareket ettir</span>

</div>

<div class="line">

<span id="l00143"></span><span class="lineno"> 143</span> ball.position
= nextPosition;

</div>

<div class="line">

<span id="l00144"></span><span class="lineno"> 144</span> }

</div>

<div class="line">

<span id="l00145"></span><span class="lineno"> 145</span>

</div>

<div class="line">

<span id="l00146"></span><span class="lineno"> 146</span>
<span class="keyword">private</span>
<span class="keywordtype">void</span> OnDrawGizmosSelected()

</div>

<div class="line">

<span id="l00147"></span><span class="lineno"> 147</span> {

</div>

<div class="line">

<span id="l00148"></span><span class="lineno"> 148</span>
Gizmos.DrawRay(<a href="class_ball_movement.html#ab2657ddd68ebf02876c11212145fcfdb"
class="code hl_variable">ball</a>.transform.position,
<a href="class_ball_movement.html#ac6a63f2cbb61ce14dda95621177ee843"
class="code hl_variable">direction</a>);

</div>

<div class="line">

<span id="l00149"></span><span class="lineno"> 149</span> }

</div>

<div class="line">

<span id="l00150"></span><span class="lineno"> 150</span>

</div>

<div class="line">

<span id="l00160"></span><span class="lineno"> 160</span>

</div>

<div id="foldopen00161" class="foldopen" data-start="{" end="};">

<div class="line">

<span id="l00161"></span><span class="lineno">
<a href="struct_ball_movement_1_1_line_segment.html"
class="line">161</a></span> <span class="keyword">public</span>
<span class="keyword">struct
</span><a href="struct_ball_movement_1_1_line_segment.html"
class="code hl_struct">LineSegment</a>

</div>

<div class="line">

<span id="l00162"></span><span class="lineno"> 162</span> {

</div>

<div class="line">

<span id="l00163"></span><span class="lineno"> <a
href="struct_ball_movement_1_1_line_segment.html#ab6925c20f22c7ed443f2a1710866c9e5"
class="line">163</a></span> <span class="keyword">public</span> Vector3
<a
href="struct_ball_movement_1_1_line_segment.html#ab6925c20f22c7ed443f2a1710866c9e5"
class="code hl_variable">start</a>;

</div>

<div class="line">

<span id="l00164"></span><span class="lineno"> <a
href="struct_ball_movement_1_1_line_segment.html#a69fc40fa8c0df4a8c088a9fdd6c97449"
class="line">164</a></span> <span class="keyword">public</span> Vector3
<a
href="struct_ball_movement_1_1_line_segment.html#a69fc40fa8c0df4a8c088a9fdd6c97449"
class="code hl_variable">end</a>;

</div>

<div class="line">

<span id="l00165"></span><span class="lineno"> <a
href="struct_ball_movement_1_1_line_segment.html#a9c4654ac7f753bf2b97cad21ffc4c04c"
class="line">165</a></span> <span class="keyword">public</span> Vector3
<a
href="struct_ball_movement_1_1_line_segment.html#a9c4654ac7f753bf2b97cad21ffc4c04c"
class="code hl_variable">normal</a>;

</div>

<div class="line">

<span id="l00166"></span><span class="lineno"> 166</span>

</div>

<div id="foldopen00167" class="foldopen" data-start="{" end="}">

<div class="line">

<span id="l00167"></span><span class="lineno"> <a
href="struct_ball_movement_1_1_line_segment.html#ad2b567b007687d6235085bfb628f6fe8"
class="line">167</a></span> <span class="keyword">public</span> <a
href="struct_ball_movement_1_1_line_segment.html#ad2b567b007687d6235085bfb628f6fe8"
class="code hl_function">LineSegment</a>(Vector3 <a
href="struct_ball_movement_1_1_line_segment.html#ab6925c20f22c7ed443f2a1710866c9e5"
class="code hl_variable">start</a>, Vector3 <a
href="struct_ball_movement_1_1_line_segment.html#a69fc40fa8c0df4a8c088a9fdd6c97449"
class="code hl_variable">end</a>, Vector3 <a
href="struct_ball_movement_1_1_line_segment.html#a9c4654ac7f753bf2b97cad21ffc4c04c"
class="code hl_variable">normal</a>)

</div>

<div class="line">

<span id="l00168"></span><span class="lineno"> 168</span> {

</div>

<div class="line">

<span id="l00169"></span><span class="lineno"> 169</span> this.start =
<a
href="struct_ball_movement_1_1_line_segment.html#ab6925c20f22c7ed443f2a1710866c9e5"
class="code hl_variable">start</a>;

</div>

<div class="line">

<span id="l00170"></span><span class="lineno"> 170</span> this.end = <a
href="struct_ball_movement_1_1_line_segment.html#a69fc40fa8c0df4a8c088a9fdd6c97449"
class="code hl_variable">end</a>;

</div>

<div class="line">

<span id="l00171"></span><span class="lineno"> 171</span> this.normal =
<a
href="struct_ball_movement_1_1_line_segment.html#a9c4654ac7f753bf2b97cad21ffc4c04c"
class="code hl_variable">normal</a>;

</div>

<div class="line">

<span id="l00172"></span><span class="lineno"> 172</span> }

</div>

</div>

<div class="line">

<span id="l00173"></span><span class="lineno"> 173</span> }

</div>

</div>

<div class="line">

<span id="l00174"></span><span class="lineno"> 174</span>

</div>

<div id="foldopen00175" class="foldopen" data-start="{" end="}">

<div class="line">

<span id="l00175"></span><span class="lineno">
<a href="class_ball_movement.html#a2c6180a5d985ce8c7c39596ab9e5d9a3"
class="line">175</a></span> <span class="keyword">public</span>
<span class="keywordtype">bool</span>
<a href="class_ball_movement.html#a2c6180a5d985ce8c7c39596ab9e5d9a3"
class="code hl_function">LineSegmentIntersection</a>(Vector3 p1, Vector3
p2, Vector3 q1, Vector3 q2, out Vector3 intersectionPoint)

</div>

<div class="line">

<span id="l00176"></span><span class="lineno"> 176</span> {

</div>

<div class="line">

<span id="l00177"></span><span class="lineno"> 177</span> Vector3 r =
p2 - p1;

</div>

<div class="line">

<span id="l00178"></span><span class="lineno"> 178</span> Vector3 s =
q2 - q1;

</div>

<div class="line">

<span id="l00179"></span><span class="lineno"> 179</span>

</div>

<div class="line">

<span id="l00180"></span><span class="lineno"> 180</span>
<span class="keywordtype">float</span> d = r.x \* s.y - r.y \* s.x;

</div>

<div class="line">

<span id="l00181"></span><span class="lineno"> 181</span>
<span class="keywordtype">float</span> u = ((q1.x - p1.x) \* r.y -
(q1.y - p1.y) \* r.x) / d;

</div>

<div class="line">

<span id="l00182"></span><span class="lineno"> 182</span>
<span class="keywordtype">float</span> t = ((q1.x - p1.x) \* s.y -
(q1.y - p1.y) \* s.x) / d;

</div>

<div class="line">

<span id="l00183"></span><span class="lineno"> 183</span>
<span class="keywordflow">if</span> ((0 \<= u && u \<= 1 && 0 \<= t && t
\<= 1))

</div>

<div class="line">

<span id="l00184"></span><span class="lineno"> 184</span> {

</div>

<div class="line">

<span id="l00185"></span><span class="lineno"> 185</span>
intersectionPoint = p1 + t \* r;

</div>

<div class="line">

<span id="l00186"></span><span class="lineno"> 186</span>
<span class="keywordflow">return</span>
<span class="keyword">true</span>;

</div>

<div class="line">

<span id="l00187"></span><span class="lineno"> 187</span> }

</div>

<div class="line">

<span id="l00188"></span><span class="lineno"> 188</span>

</div>

<div class="line">

<span id="l00189"></span><span class="lineno"> 189</span>
intersectionPoint = <span class="keywordflow">default</span>;

</div>

<div class="line">

<span id="l00190"></span><span class="lineno"> 190</span>
<span class="keywordflow">return</span>
<span class="keyword">false</span>;

</div>

<div class="line">

<span id="l00191"></span><span class="lineno"> 191</span> }

</div>

</div>

<div class="line">

<span id="l00192"></span><span class="lineno"> 192</span>

</div>

<div class="line">

<span id="l00193"></span><span class="lineno"> 193</span>
<span class="keywordtype">bool</span>
LineSegmentIntersectionOriginal(Vector3 p1, Vector3 p2, Vector3 q1,
Vector3 q2, out Vector3 intersectionPoint)

</div>

<div class="line">

<span id="l00194"></span><span class="lineno"> 194</span> {

</div>

<div class="line">

<span id="l00195"></span><span class="lineno"> 195</span>
<span class="keywordtype">float</span> A1 = p2.y - p1.y;

</div>

<div class="line">

<span id="l00196"></span><span class="lineno"> 196</span>
<span class="keywordtype">float</span> B1 = p1.x - p2.x;

</div>

<div class="line">

<span id="l00197"></span><span class="lineno"> 197</span>
<span class="keywordtype">float</span> C1 = A1 \* p1.x + B1 \* p1.y;

</div>

<div class="line">

<span id="l00198"></span><span class="lineno"> 198</span>

</div>

<div class="line">

<span id="l00199"></span><span class="lineno"> 199</span>
<span class="keywordtype">float</span> A2 = q2.y - q1.y;

</div>

<div class="line">

<span id="l00200"></span><span class="lineno"> 200</span>
<span class="keywordtype">float</span> B2 = q1.x - q2.x;

</div>

<div class="line">

<span id="l00201"></span><span class="lineno"> 201</span>
<span class="keywordtype">float</span> C2 = A2 \* q1.x + B2 \* q1.y;

</div>

<div class="line">

<span id="l00202"></span><span class="lineno"> 202</span>

</div>

<div class="line">

<span id="l00203"></span><span class="lineno"> 203</span>
<span class="keywordtype">float</span> det = A1 \* B2 - A2 \* B1;

</div>

<div class="line">

<span id="l00204"></span><span class="lineno"> 204</span>

</div>

<div class="line">

<span id="l00205"></span><span class="lineno"> 205</span>
<span class="keywordflow">if</span> (Mathf.Abs(det) \< 0.0001f)

</div>

<div class="line">

<span id="l00206"></span><span class="lineno"> 206</span> {

</div>

<div class="line">

<span id="l00207"></span><span class="lineno"> 207</span>
<span class="comment">// Çizgiler paralelse</span>

</div>

<div class="line">

<span id="l00208"></span><span class="lineno"> 208</span>
intersectionPoint = Vector3.zero;

</div>

<div class="line">

<span id="l00209"></span><span class="lineno"> 209</span>
<span class="keywordflow">return</span>
<span class="keyword">false</span>;

</div>

<div class="line">

<span id="l00210"></span><span class="lineno"> 210</span> }

</div>

<div class="line">

<span id="l00211"></span><span class="lineno"> 211</span>

</div>

<div class="line">

<span id="l00212"></span><span class="lineno"> 212</span>
<span class="keywordtype">float</span> x = (B2 \* C1 - B1 \* C2) / det;

</div>

<div class="line">

<span id="l00213"></span><span class="lineno"> 213</span>
<span class="keywordtype">float</span> y = (A1 \* C2 - A2 \* C1) / det;

</div>

<div class="line">

<span id="l00214"></span><span class="lineno"> 214</span>
<span class="comment">//Debug.Log(x);</span>

</div>

<div class="line">

<span id="l00215"></span><span class="lineno"> 215</span>
<span class="comment">//Debug.Log(y);</span>

</div>

<div class="line">

<span id="l00216"></span><span class="lineno"> 216</span>
<span class="keywordflow">if</span> ((x \>= Mathf.Min(p1.x, p2.x) && x
\<= Mathf.Max(p1.x, p2.x)) &&

</div>

<div class="line">

<span id="l00217"></span><span class="lineno"> 217</span> (y \>=
Mathf.Min(p1.y, p2.y) && y \<= Mathf.Max(p1.y, p2.y)) &&

</div>

<div class="line">

<span id="l00218"></span><span class="lineno"> 218</span> (x \>=
Mathf.Min(q1.x, q2.x) && x \<= Mathf.Max(q1.x, q2.x)) &&

</div>

<div class="line">

<span id="l00219"></span><span class="lineno"> 219</span> (y \>=
Mathf.Min(q1.y, q2.y) && y \<= Mathf.Max(q1.y, q2.y)))

</div>

<div class="line">

<span id="l00220"></span><span class="lineno"> 220</span> {

</div>

<div class="line">

<span id="l00221"></span><span class="lineno"> 221</span>
intersectionPoint = <span class="keyword">new</span> Vector3(x, y, 0);

</div>

<div class="line">

<span id="l00222"></span><span class="lineno"> 222</span>
<span class="keywordflow">return</span>
<span class="keyword">true</span>;

</div>

<div class="line">

<span id="l00223"></span><span class="lineno"> 223</span> }

</div>

<div class="line">

<span id="l00224"></span><span class="lineno"> 224</span>

</div>

<div class="line">

<span id="l00225"></span><span class="lineno"> 225</span>
intersectionPoint = Vector3.zero;

</div>

<div class="line">

<span id="l00226"></span><span class="lineno"> 226</span>
<span class="keywordflow">return</span>
<span class="keyword">false</span>;

</div>

<div class="line">

<span id="l00227"></span><span class="lineno"> 227</span> }

</div>

<div class="line">

<span id="l00228"></span><span class="lineno"> 228</span>

</div>

<div class="line">

<span id="l00229"></span><span class="lineno">
<a href="class_ball_movement.html#a5866f553f594be14a85c88de4fcdf36f"
class="line">229</a></span> <span class="keyword">public</span> Font
<a href="class_ball_movement.html#a5866f553f594be14a85c88de4fcdf36f"
class="code hl_variable">font</a>;

</div>

<div class="line">

<span id="l00230"></span><span class="lineno"> 230</span>
<span class="keyword">private</span>
<span class="keywordtype">void</span> OnGUI()

</div>

<div class="line">

<span id="l00231"></span><span class="lineno"> 231</span> {

</div>

<div class="line">

<span id="l00232"></span><span class="lineno"> 232</span> GUI.skin.font
= <a href="class_ball_movement.html#a5866f553f594be14a85c88de4fcdf36f"
class="code hl_variable">font</a>;

</div>

<div class="line">

<span id="l00233"></span><span class="lineno"> 233</span> GUIStyle style
= <span class="keyword">new</span> GUIStyle(GUI.skin.label);

</div>

<div class="line">

<span id="l00234"></span><span class="lineno"> 234</span>
style.alignment = TextAnchor.MiddleCenter;

</div>

<div class="line">

<span id="l00235"></span><span class="lineno"> 235</span>

</div>

<div class="line">

<span id="l00236"></span><span class="lineno"> 236</span>
GUI.Label(<span class="keyword">new</span> Rect(Screen.width / 2 - 125 -
50, -50, 250, 250), score2.ToString(), style);

</div>

<div class="line">

<span id="l00237"></span><span class="lineno"> 237</span>
GUI.Label(<span class="keyword">new</span> Rect(Screen.width / 2 - 125 +
50, -50, 250, 250), score1.ToString(), style);

</div>

<div class="line">

<span id="l00238"></span><span class="lineno"> 238</span> }

</div>

<div class="line">

<span id="l00239"></span><span class="lineno"> 239</span>}

</div>

</div>

<div id="a_ball_movement_8cs_html_a832e8f52fca5a678819ec96269dcb532"
class="ttc">

<div class="ttname">

[Random](_ball_movement_8cs.html#a832e8f52fca5a678819ec96269dcb532)

</div>

<div class="ttdeci">

UnityEngine.Random Random

</div>

<div class="ttdef">

**Definition**
[BallMovement.cs:7](_ball_movement_8cs_source.html#l00007)

</div>

</div>

<div id="aclass_ball_movement_html" class="ttc">

<div class="ttname">

[BallMovement](class_ball_movement.html)

</div>

<div class="ttdoc">

This Class controls Ball Movement and Segment Intersections.

</div>

<div class="ttdef">

**Definition**
[BallMovement.cs:13](_ball_movement_8cs_source.html#l00012)

</div>

</div>

<div id="aclass_ball_movement_html_a2c6180a5d985ce8c7c39596ab9e5d9a3"
class="ttc">

<div class="ttname">

[BallMovement.LineSegmentIntersection](class_ball_movement.html#a2c6180a5d985ce8c7c39596ab9e5d9a3)

</div>

<div class="ttdeci">

bool LineSegmentIntersection(Vector3 p1, Vector3 p2, Vector3 q1, Vector3
q2, out Vector3 intersectionPoint)

</div>

<div class="ttdef">

**Definition**
[BallMovement.cs:175](_ball_movement_8cs_source.html#l00175)

</div>

</div>

<div id="aclass_ball_movement_html_a5866f553f594be14a85c88de4fcdf36f"
class="ttc">

<div class="ttname">

[BallMovement.font](class_ball_movement.html#a5866f553f594be14a85c88de4fcdf36f)

</div>

<div class="ttdeci">

Font font

</div>

<div class="ttdef">

**Definition**
[BallMovement.cs:229](_ball_movement_8cs_source.html#l00229)

</div>

</div>

<div id="aclass_ball_movement_html_aa33416010b3040ac39e7b02bfa7aa95a"
class="ttc">

<div class="ttname">

[BallMovement.edgeFollow](class_ball_movement.html#aa33416010b3040ac39e7b02bfa7aa95a)

</div>

<div class="ttdeci">

float edgeFollow

</div>

<div class="ttdef">

**Definition**
[BallMovement.cs:18](_ball_movement_8cs_source.html#l00018)

</div>

</div>

<div id="aclass_ball_movement_html_ab2657ddd68ebf02876c11212145fcfdb"
class="ttc">

<div class="ttname">

[BallMovement.ball](class_ball_movement.html#ab2657ddd68ebf02876c11212145fcfdb)

</div>

<div class="ttdeci">

Transform ball

</div>

<div class="ttdef">

**Definition**
[BallMovement.cs:14](_ball_movement_8cs_source.html#l00014)

</div>

</div>

<div id="aclass_ball_movement_html_ac6a63f2cbb61ce14dda95621177ee843"
class="ttc">

<div class="ttname">

[BallMovement.direction](class_ball_movement.html#ac6a63f2cbb61ce14dda95621177ee843)

</div>

<div class="ttdeci">

Vector2 direction

</div>

<div class="ttdef">

**Definition**
[BallMovement.cs:20](_ball_movement_8cs_source.html#l00020)

</div>

</div>

<div id="aclass_ball_movement_html_ae5be514e8f3c1b3af767d5a8627c9277"
class="ttc">

<div class="ttname">

[BallMovement.speed](class_ball_movement.html#ae5be514e8f3c1b3af767d5a8627c9277)

</div>

<div class="ttdeci">

float speed

</div>

<div class="ttdef">

**Definition**
[BallMovement.cs:19](_ball_movement_8cs_source.html#l00019)

</div>

</div>

<div id="aclass_ball_movement_html_ae6fbc952b54fb915ac79385d0a55ecc0"
class="ttc">

<div class="ttname">

[BallMovement.paddle2](class_ball_movement.html#ae6fbc952b54fb915ac79385d0a55ecc0)

</div>

<div class="ttdeci">

Transform paddle2

</div>

<div class="ttdef">

**Definition**
[BallMovement.cs:16](_ball_movement_8cs_source.html#l00016)

</div>

</div>

<div id="aclass_ball_movement_html_afc7bd1ba11daafd6825473d72337f708"
class="ttc">

<div class="ttname">

[BallMovement.paddle1](class_ball_movement.html#afc7bd1ba11daafd6825473d72337f708)

</div>

<div class="ttdeci">

Transform paddle1

</div>

<div class="ttdef">

**Definition**
[BallMovement.cs:15](_ball_movement_8cs_source.html#l00015)

</div>

</div>

<div id="astruct_ball_movement_1_1_line_segment_html" class="ttc">

<div class="ttname">

[BallMovement.LineSegment](struct_ball_movement_1_1_line_segment.html)

</div>

<div class="ttdoc">

Calculates two line segmentation.

</div>

<div class="ttdef">

**Definition**
[BallMovement.cs:162](_ball_movement_8cs_source.html#l00161)

</div>

</div>

<div id="astruct_ball_movement_1_1_line_segment_html_a69fc40fa8c0df4a8c088a9fdd6c97449"
class="ttc">

<div class="ttname">

[BallMovement.LineSegment.end](struct_ball_movement_1_1_line_segment.html#a69fc40fa8c0df4a8c088a9fdd6c97449)

</div>

<div class="ttdeci">

Vector3 end

</div>

<div class="ttdef">

**Definition**
[BallMovement.cs:164](_ball_movement_8cs_source.html#l00164)

</div>

</div>

<div id="astruct_ball_movement_1_1_line_segment_html_a9c4654ac7f753bf2b97cad21ffc4c04c"
class="ttc">

<div class="ttname">

[BallMovement.LineSegment.normal](struct_ball_movement_1_1_line_segment.html#a9c4654ac7f753bf2b97cad21ffc4c04c)

</div>

<div class="ttdeci">

Vector3 normal

</div>

<div class="ttdef">

**Definition**
[BallMovement.cs:165](_ball_movement_8cs_source.html#l00165)

</div>

</div>

<div id="astruct_ball_movement_1_1_line_segment_html_ab6925c20f22c7ed443f2a1710866c9e5"
class="ttc">

<div class="ttname">

[BallMovement.LineSegment.start](struct_ball_movement_1_1_line_segment.html#ab6925c20f22c7ed443f2a1710866c9e5)

</div>

<div class="ttdeci">

Vector3 start

</div>

<div class="ttdef">

**Definition**
[BallMovement.cs:163](_ball_movement_8cs_source.html#l00163)

</div>

</div>

<div id="astruct_ball_movement_1_1_line_segment_html_ad2b567b007687d6235085bfb628f6fe8"
class="ttc">

<div class="ttname">

[BallMovement.LineSegment.LineSegment](struct_ball_movement_1_1_line_segment.html#ad2b567b007687d6235085bfb628f6fe8)

</div>

<div class="ttdeci">

LineSegment(Vector3 start, Vector3 end, Vector3 normal)

</div>

<div class="ttdef">

**Definition**
[BallMovement.cs:167](_ball_movement_8cs_source.html#l00167)

</div>

</div>

</div>

</div>

------------------------------------------------------------------------

<span class="small">Generated
by [<img src="doxygen.svg" class="footer" width="104" height="31"
alt="doxygen" />](https://www.doxygen.org/index.html) 1.9.8</span>
