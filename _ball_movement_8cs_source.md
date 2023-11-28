::: {#top}
::: {#titlearea}
+-----------------------------------+-----------------------------------+
| ::: {#projectname}                | :::                               |
| Po                                | {#MSearchBox .MSearchBoxInactive} |
| ngExample[ 1.0.0]{#projectnumber} | [ [ ]{#MSearchSelect              |
| :::                               | onmouseover="retur                |
|                                   | n searchBox.OnSearchSelectShow()" |
|                                   | onmouseout="return                |
|                                   |  searchBox.OnSearchSelectHide()"} |
|                                   | ]{.left}[                         |
|                                   | [![](s                            |
|                                   | earch/close.svg){#MSearchCloseImg |
|                                   | bord                              |
|                                   | er="0"}](javascript:searchBox.Clo |
|                                   | seResultsWindow()){#MSearchClose} |
|                                   | ]{.right}                         |
|                                   | :::                               |
+-----------------------------------+-----------------------------------+
:::
:::

::: {#side-nav .ui-resizable .side-nav-resizable}
::: {#nav-tree}
::: {#nav-tree-contents}
::: {#nav-sync .sync}
:::
:::
:::

::: {#splitbar .ui-resizable-handle style="-moz-user-select:none;"}
:::
:::

::: {#doc-content}
::: {#MSearchSelectWindow onmouseover="return searchBox.OnSearchSelectShow()" onmouseout="return searchBox.OnSearchSelectHide()" onkeydown="return searchBox.OnSearchSelectKey(event)"}
:::

::: {#MSearchResultsWindow}
::: {#MSearchResults}
::: SRPage
::: {#SRIndex}
::: {#SRResults}
:::

::: {#Loading .SRStatus}
Loading\...
:::

::: {#Searching .SRStatus}
Searching\...
:::

::: {#NoMatches .SRStatus}
No Matches
:::
:::
:::
:::
:::

::: header
::: headertitle
::: title
BallMovement.cs
:::
:::
:::

::: contents
[Go to the documentation of this file.](_ball_movement_8cs.html)

::: fragment
::: line
[]{#l00001}[ 1]{.lineno}[using ]{.keyword}System;
:::

::: line
[]{#l00002}[ 2]{.lineno}[using ]{.keyword}System.Collections;
:::

::: line
[]{#l00003}[ 3]{.lineno}[using ]{.keyword}System.Collections.Generic;
:::

::: line
[]{#l00004}[ 4]{.lineno}[using ]{.keyword}System.Threading.Tasks;
:::

::: line
[]{#l00005}[ 5]{.lineno}[using ]{.keyword}UnityEngine;
:::

::: line
[]{#l00006}[ 6]{.lineno}[using ]{.keyword}UnityEngine.Assertions.Must;
:::

::: line
[]{#l00007}[
[7](_ball_movement_8cs.html#a832e8f52fca5a678819ec96269dcb532){.line}]{.lineno}[using
]{.keyword}[Random](_ball_movement_8cs.html#a832e8f52fca5a678819ec96269dcb532){.code
.hl_typedef} = UnityEngine.Random;
:::

::: line
[]{#l00008}[ 8]{.lineno}
:::

::: {#foldopen00012 .foldopen data-start="{" end="};"}
::: line
[]{#l00012}[
[12](class_ball_movement.html){.line}]{.lineno}[public]{.keyword} [class
]{.keyword}[BallMovement](class_ball_movement.html){.code .hl_class} :
MonoBehaviour
:::

::: line
[]{#l00013}[ 13]{.lineno}{
:::

::: line
[]{#l00014}[
[14](class_ball_movement.html#ab2657ddd68ebf02876c11212145fcfdb){.line}]{.lineno}
[public]{.keyword} Transform
[ball](class_ball_movement.html#ab2657ddd68ebf02876c11212145fcfdb){.code
.hl_variable};
:::

::: line
[]{#l00015}[
[15](class_ball_movement.html#afc7bd1ba11daafd6825473d72337f708){.line}]{.lineno}
[public]{.keyword} Transform
[paddle1](class_ball_movement.html#afc7bd1ba11daafd6825473d72337f708){.code
.hl_variable};
:::

::: line
[]{#l00016}[
[16](class_ball_movement.html#ae6fbc952b54fb915ac79385d0a55ecc0){.line}]{.lineno}
[public]{.keyword} Transform
[paddle2](class_ball_movement.html#ae6fbc952b54fb915ac79385d0a55ecc0){.code
.hl_variable};
:::

::: line
[]{#l00017}[ 17]{.lineno}
:::

::: line
[]{#l00018}[
[18](class_ball_movement.html#aa33416010b3040ac39e7b02bfa7aa95a){.line}]{.lineno}
[public]{.keyword} [float]{.keywordtype}
[edgeFollow](class_ball_movement.html#aa33416010b3040ac39e7b02bfa7aa95a){.code
.hl_variable} = 11f;
:::

::: line
[]{#l00019}[
[19](class_ball_movement.html#ae5be514e8f3c1b3af767d5a8627c9277){.line}]{.lineno}
[public]{.keyword} [float]{.keywordtype}
[speed](class_ball_movement.html#ae5be514e8f3c1b3af767d5a8627c9277){.code
.hl_variable} = 5f;
:::

::: line
[]{#l00020}[
[20](class_ball_movement.html#ac6a63f2cbb61ce14dda95621177ee843){.line}]{.lineno}
[public]{.keyword} Vector2
[direction](class_ball_movement.html#ac6a63f2cbb61ce14dda95621177ee843){.code
.hl_variable};
:::

::: line
[]{#l00021}[ 21]{.lineno}
:::

::: line
[]{#l00022}[ 22]{.lineno} [private]{.keyword} [int]{.keywordtype} score1
= 0;
:::

::: line
[]{#l00023}[ 23]{.lineno} [private]{.keyword} [int]{.keywordtype} score2
= 0;
:::

::: line
[]{#l00024}[ 24]{.lineno}
:::

::: line
[]{#l00025}[ 25]{.lineno} [private]{.keyword} Vector3 ballVelocity;
:::

::: line
[]{#l00026}[ 26]{.lineno} [private]{.keyword} List\<LineSegment\>
lineSegments;
:::

::: line
[]{#l00027}[ 27]{.lineno}
:::

::: line
[]{#l00028}[ 28]{.lineno}
:::

::: line
[]{#l00029}[ 29]{.lineno} [enum]{.keyword} SegmentName
:::

::: line
[]{#l00030}[ 30]{.lineno} {
:::

::: line
[]{#l00031}[ 31]{.lineno} LeftPaddle = 0,
:::

::: line
[]{#l00032}[ 32]{.lineno} RightPaddle = 1,
:::

::: line
[]{#l00033}[ 33]{.lineno} TopWall = 2,
:::

::: line
[]{#l00034}[ 34]{.lineno} BottomWall = 3,
:::

::: line
[]{#l00035}[ 35]{.lineno} }
:::

::: line
[]{#l00036}[ 36]{.lineno}
:::

::: line
[]{#l00037}[ 37]{.lineno} [void]{.keywordtype} Start()
:::

::: line
[]{#l00038}[ 38]{.lineno} {
:::

::: line
[]{#l00039}[ 39]{.lineno} [//Rastgele direction ayarla]{.comment}
:::

::: line
[]{#l00040}[ 40]{.lineno}
[direction](class_ball_movement.html#ac6a63f2cbb61ce14dda95621177ee843){.code
.hl_variable} = [new]{.keyword}
Vector3([Random](_ball_movement_8cs.html#a832e8f52fca5a678819ec96269dcb532){.code
.hl_typedef}.Range(0, 2) == 0 ? -1 : 1,
[Random](_ball_movement_8cs.html#a832e8f52fca5a678819ec96269dcb532){.code
.hl_typedef}.Range(0, 2) == 0 ? -1 : 1, 0);
:::

::: line
[]{#l00041}[ 41]{.lineno}
:::

::: line
[]{#l00042}[ 42]{.lineno} [//Collision lineları ayarla]{.comment}
:::

::: line
[]{#l00043}[ 43]{.lineno} Vector3 paddle1TopEdge = paddle1.position -
[new]{.keyword} Vector3(0,
[paddle1](class_ball_movement.html#afc7bd1ba11daafd6825473d72337f708){.code
.hl_variable}.transform.localScale.y / 2, 0);
:::

::: line
[]{#l00044}[ 44]{.lineno} Vector3 paddle1BottomEdge = paddle1.position +
[new]{.keyword} Vector3(0,
[paddle1](class_ball_movement.html#afc7bd1ba11daafd6825473d72337f708){.code
.hl_variable}.transform.localScale.y / 2, 0);
:::

::: line
[]{#l00045}[ 45]{.lineno} Vector3 paddle2TopEdge = paddle2.position -
[new]{.keyword} Vector3(0,
[paddle2](class_ball_movement.html#ae6fbc952b54fb915ac79385d0a55ecc0){.code
.hl_variable}.transform.localScale.y / 2, 0);
:::

::: line
[]{#l00046}[ 46]{.lineno} Vector3 paddle2BottomEdge = paddle2.position +
[new]{.keyword} Vector3(0,
[paddle2](class_ball_movement.html#ae6fbc952b54fb915ac79385d0a55ecc0){.code
.hl_variable}.transform.localScale.y / 2, 0);
:::

::: line
[]{#l00047}[ 47]{.lineno}
:::

::: line
[]{#l00048}[ 48]{.lineno} Vector3 topLeft = [new]{.keyword}
Vector3(+[edgeFollow](class_ball_movement.html#aa33416010b3040ac39e7b02bfa7aa95a){.code
.hl_variable}, 5, 0);
:::

::: line
[]{#l00049}[ 49]{.lineno} Vector3 topRight = [new]{.keyword}
Vector3(-[edgeFollow](class_ball_movement.html#aa33416010b3040ac39e7b02bfa7aa95a){.code
.hl_variable}, 5, 0);
:::

::: line
[]{#l00050}[ 50]{.lineno}
:::

::: line
[]{#l00051}[ 51]{.lineno} Vector3 bottomLeft = [new]{.keyword}
Vector3(+[edgeFollow](class_ball_movement.html#aa33416010b3040ac39e7b02bfa7aa95a){.code
.hl_variable}, -5, 0);
:::

::: line
[]{#l00052}[ 52]{.lineno} Vector3 bottomRight = [new]{.keyword}
Vector3(-[edgeFollow](class_ball_movement.html#aa33416010b3040ac39e7b02bfa7aa95a){.code
.hl_variable}, -5, 0);
:::

::: line
[]{#l00053}[ 53]{.lineno}
:::

::: line
[]{#l00054}[ 54]{.lineno} Vector3 leftScoreTop = [new]{.keyword}
Vector3(-11, -5, 0);
:::

::: line
[]{#l00055}[ 55]{.lineno} Vector3 leftScoreBottom = [new]{.keyword}
Vector3(-11, 5, 0);
:::

::: line
[]{#l00056}[ 56]{.lineno}
:::

::: line
[]{#l00057}[ 57]{.lineno} Vector3 rightScoreTop = [new]{.keyword}
Vector3(11, -5, 0);
:::

::: line
[]{#l00058}[ 58]{.lineno} Vector3 rightScoreBottom = [new]{.keyword}
Vector3(11, 5, 0);
:::

::: line
[]{#l00059}[ 59]{.lineno}
:::

::: line
[]{#l00060}[ 60]{.lineno} lineSegments = [new]{.keyword}
List\<LineSegment\>
:::

::: line
[]{#l00061}[ 61]{.lineno} {
:::

::: line
[]{#l00062}[ 62]{.lineno} [new]{.keyword} LineSegment(paddle1BottomEdge,
paddle1TopEdge, Vector3.right),
:::

::: line
[]{#l00063}[ 63]{.lineno} [new]{.keyword} LineSegment(paddle2BottomEdge,
paddle2TopEdge, Vector3.left),
:::

::: line
[]{#l00064}[ 64]{.lineno} [new]{.keyword} LineSegment(topLeft, topRight,
Vector3.down),
:::

::: line
[]{#l00065}[ 65]{.lineno} [new]{.keyword} LineSegment(bottomLeft,
bottomRight, Vector3.up),
:::

::: line
[]{#l00066}[ 66]{.lineno} [new]{.keyword} LineSegment(leftScoreTop,
leftScoreBottom, Vector3.right),
:::

::: line
[]{#l00067}[ 67]{.lineno} [new]{.keyword} LineSegment(rightScoreTop,
rightScoreBottom, Vector3.left),
:::

::: line
[]{#l00068}[ 68]{.lineno} };
:::

::: line
[]{#l00069}[ 69]{.lineno} }
:::

::: line
[]{#l00070}[ 70]{.lineno}
:::

::: line
[]{#l00071}[ 71]{.lineno} [void]{.keywordtype} Update()
:::

::: line
[]{#l00072}[ 72]{.lineno} {
:::

::: line
[]{#l00073}[ 73]{.lineno} [// Topun bir sonraki pozisyonunu tahmin
et]{.comment}
:::

::: line
[]{#l00074}[ 74]{.lineno} Vector3 ballVelocity =
[direction](class_ball_movement.html#ac6a63f2cbb61ce14dda95621177ee843){.code
.hl_variable} \*
[speed](class_ball_movement.html#ae5be514e8f3c1b3af767d5a8627c9277){.code
.hl_variable};
:::

::: line
[]{#l00075}[ 75]{.lineno}
:::

::: line
[]{#l00076}[ 76]{.lineno} Vector3 nextPosition = ball.position +
ballVelocity \* Time.deltaTime;
:::

::: line
[]{#l00077}[ 77]{.lineno}
:::

::: line
[]{#l00078}[ 78]{.lineno} [// Paddle\'ın kenarlarını ve ekranın
kenarlarını temsil eden çizgi parçalarını oluştur]{.comment}
:::

::: line
[]{#l00079}[ 79]{.lineno}
:::

::: line
[]{#l00080}[ 80]{.lineno} var leftPaddleSegment =
lineSegments\[(int)SegmentName.LeftPaddle\];
:::

::: line
[]{#l00081}[ 81]{.lineno} leftPaddleSegment.start = paddle1.position -
[new]{.keyword} Vector3(0,
[paddle1](class_ball_movement.html#afc7bd1ba11daafd6825473d72337f708){.code
.hl_variable}.transform.localScale.y / 2, 0);
:::

::: line
[]{#l00082}[ 82]{.lineno} leftPaddleSegment.end = paddle1.position +
[new]{.keyword} Vector3(0,
[paddle1](class_ball_movement.html#afc7bd1ba11daafd6825473d72337f708){.code
.hl_variable}.transform.localScale.y / 2, 0);
:::

::: line
[]{#l00083}[ 83]{.lineno} lineSegments\[(int)SegmentName.LeftPaddle\] =
leftPaddleSegment;
:::

::: line
[]{#l00084}[ 84]{.lineno}
:::

::: line
[]{#l00085}[ 85]{.lineno} var rightPaddleSegment =
lineSegments\[(int)SegmentName.RightPaddle\];
:::

::: line
[]{#l00086}[ 86]{.lineno} rightPaddleSegment.start = paddle2.position -
[new]{.keyword} Vector3(0,
[paddle2](class_ball_movement.html#ae6fbc952b54fb915ac79385d0a55ecc0){.code
.hl_variable}.transform.localScale.y / 2, 0);
:::

::: line
[]{#l00087}[ 87]{.lineno} rightPaddleSegment.end = paddle2.position +
[new]{.keyword} Vector3(0,
[paddle2](class_ball_movement.html#ae6fbc952b54fb915ac79385d0a55ecc0){.code
.hl_variable}.transform.localScale.y / 2, 0);
:::

::: line
[]{#l00088}[ 88]{.lineno} lineSegments\[(int)SegmentName.RightPaddle\] =
rightPaddleSegment;
:::

::: line
[]{#l00089}[ 89]{.lineno}
:::

::: line
[]{#l00090}[ 90]{.lineno}
:::

::: line
[]{#l00091}[ 91]{.lineno} [// Topun hareketini temsil eden çizgi
parçasını oluştur]{.comment}
:::

::: line
[]{#l00092}[ 92]{.lineno} Vector3 ballStart =
[ball](class_ball_movement.html#ab2657ddd68ebf02876c11212145fcfdb){.code
.hl_variable}.position;
:::

::: line
[]{#l00093}[ 93]{.lineno} Vector3 ballEnd = nextPosition;
:::

::: line
[]{#l00094}[ 94]{.lineno}
:::

::: line
[]{#l00095}[ 95]{.lineno} Debug.DrawLine(ballStart, ballEnd, Color.red);
:::

::: line
[]{#l00096}[ 96]{.lineno}
:::

::: line
[]{#l00097}[ 97]{.lineno}
:::

::: line
[]{#l00098}[ 98]{.lineno} [// Topun hareket çizgisi ile paddle\'ın
kenarları ve ekranın kenarları arasında kesişme kontrolü yap]{.comment}
:::

::: line
[]{#l00099}[ 99]{.lineno}
:::

::: line
[]{#l00100}[ 100]{.lineno} [foreach]{.keywordflow} (var lineSegment
[in]{.keywordflow} lineSegments)
:::

::: line
[]{#l00101}[ 101]{.lineno} {
:::

::: line
[]{#l00102}[ 102]{.lineno} Debug.DrawLine(lineSegment.start,
lineSegment.end, Color.red);
:::

::: line
[]{#l00103}[ 103]{.lineno} }
:::

::: line
[]{#l00104}[ 104]{.lineno}
:::

::: line
[]{#l00105}[ 105]{.lineno}
:::

::: line
[]{#l00106}[ 106]{.lineno} [foreach]{.keywordflow} (var lineSegment
[in]{.keywordflow} lineSegments)
:::

::: line
[]{#l00107}[ 107]{.lineno} {
:::

::: line
[]{#l00108}[ 108]{.lineno} [if]{.keywordflow}
([LineSegmentIntersection](class_ball_movement.html#a2c6180a5d985ce8c7c39596ab9e5d9a3){.code
.hl_function}(ballStart, ballEnd, lineSegment.start, lineSegment.end,
out Vector3 intersectionPoint))
:::

::: line
[]{#l00109}[ 109]{.lineno} {
:::

::: line
[]{#l00110}[ 110]{.lineno}
[direction](class_ball_movement.html#ac6a63f2cbb61ce14dda95621177ee843){.code
.hl_variable} =
Vector3.Reflect([direction](class_ball_movement.html#ac6a63f2cbb61ce14dda95621177ee843){.code
.hl_variable}, lineSegment.normal);
:::

::: line
[]{#l00111}[ 111]{.lineno} [if]{.keywordflow} (intersectionPoint.x \<=
-11f)
:::

::: line
[]{#l00112}[ 112]{.lineno} {
:::

::: line
[]{#l00113}[ 113]{.lineno} score1 += 1;
:::

::: line
[]{#l00114}[ 114]{.lineno} intersectionPoint = [new]{.keyword}
Vector3(0, 0, 0);
:::

::: line
[]{#l00115}[ 115]{.lineno}
[direction](class_ball_movement.html#ac6a63f2cbb61ce14dda95621177ee843){.code
.hl_variable} = [new]{.keyword} Vector3(1,
[Random](_ball_movement_8cs.html#a832e8f52fca5a678819ec96269dcb532){.code
.hl_typedef}.Range(0, 2) == 0 ? -1 : 1, 0);
:::

::: line
[]{#l00116}[ 116]{.lineno} }
:::

::: line
[]{#l00117}[ 117]{.lineno}
:::

::: line
[]{#l00118}[ 118]{.lineno} [if]{.keywordflow} (intersectionPoint.x \>=
11f)
:::

::: line
[]{#l00119}[ 119]{.lineno} {
:::

::: line
[]{#l00120}[ 120]{.lineno} score2 += 1;
:::

::: line
[]{#l00121}[ 121]{.lineno} intersectionPoint = [new]{.keyword}
Vector3(0, 0, 0);
:::

::: line
[]{#l00122}[ 122]{.lineno}
[direction](class_ball_movement.html#ac6a63f2cbb61ce14dda95621177ee843){.code
.hl_variable} = [new]{.keyword} Vector3(-1,
[Random](_ball_movement_8cs.html#a832e8f52fca5a678819ec96269dcb532){.code
.hl_typedef}.Range(0, 2) == 0 ? -1 : 1, 0);
:::

::: line
[]{#l00123}[ 123]{.lineno} }
:::

::: line
[]{#l00124}[ 124]{.lineno}
:::

::: line
[]{#l00125}[ 125]{.lineno} Debug.DrawLine(lineSegment.start,
lineSegment.end, Color.green);
:::

::: line
[]{#l00126}[ 126]{.lineno}
:::

::: line
[]{#l00127}[ 127]{.lineno}
Debug.DrawLine([ball](class_ball_movement.html#ab2657ddd68ebf02876c11212145fcfdb){.code
.hl_variable}.position, intersectionPoint, Color.blue);
:::

::: line
[]{#l00128}[ 128]{.lineno}
:::

::: line
[]{#l00129}[ 129]{.lineno}
:::

::: line
[]{#l00130}[ 130]{.lineno} [// Çarpışma noktasının biraz ötesine
yerleştirerek, topun çarpışma noktasında sıkışmasını önler]{.comment}
:::

::: line
[]{#l00131}[ 131]{.lineno} [float]{.keywordtype} distanceToMove = .1f;
:::

::: line
[]{#l00132}[ 132]{.lineno} nextPosition = intersectionPoint +
(Vector3)lineSegment.normal \* distanceToMove;
:::

::: line
[]{#l00133}[ 133]{.lineno} [// Topu hareket ettir]{.comment}
:::

::: line
[]{#l00134}[ 134]{.lineno} Debug.DrawLine(nextPosition,
intersectionPoint, Color.green);
:::

::: line
[]{#l00135}[ 135]{.lineno} [break]{.keywordflow};
:::

::: line
[]{#l00136}[ 136]{.lineno} }
:::

::: line
[]{#l00137}[ 137]{.lineno} }
:::

::: line
[]{#l00138}[ 138]{.lineno}
:::

::: line
[]{#l00139}[ 139]{.lineno}
:::

::: line
[]{#l00140}[ 140]{.lineno}
:::

::: line
[]{#l00141}[ 141]{.lineno}
:::

::: line
[]{#l00142}[ 142]{.lineno} [// Topu hareket ettir]{.comment}
:::

::: line
[]{#l00143}[ 143]{.lineno} ball.position = nextPosition;
:::

::: line
[]{#l00144}[ 144]{.lineno} }
:::

::: line
[]{#l00145}[ 145]{.lineno}
:::

::: line
[]{#l00146}[ 146]{.lineno} [private]{.keyword} [void]{.keywordtype}
OnDrawGizmosSelected()
:::

::: line
[]{#l00147}[ 147]{.lineno} {
:::

::: line
[]{#l00148}[ 148]{.lineno}
Gizmos.DrawRay([ball](class_ball_movement.html#ab2657ddd68ebf02876c11212145fcfdb){.code
.hl_variable}.transform.position,
[direction](class_ball_movement.html#ac6a63f2cbb61ce14dda95621177ee843){.code
.hl_variable});
:::

::: line
[]{#l00149}[ 149]{.lineno} }
:::

::: line
[]{#l00150}[ 150]{.lineno}
:::

::: line
[]{#l00160}[ 160]{.lineno}
:::

::: {#foldopen00161 .foldopen data-start="{" end="};"}
::: line
[]{#l00161}[
[161](struct_ball_movement_1_1_line_segment.html){.line}]{.lineno}
[public]{.keyword} [struct
]{.keyword}[LineSegment](struct_ball_movement_1_1_line_segment.html){.code
.hl_struct}
:::

::: line
[]{#l00162}[ 162]{.lineno} {
:::

::: line
[]{#l00163}[
[163](struct_ball_movement_1_1_line_segment.html#ab6925c20f22c7ed443f2a1710866c9e5){.line}]{.lineno}
[public]{.keyword} Vector3
[start](struct_ball_movement_1_1_line_segment.html#ab6925c20f22c7ed443f2a1710866c9e5){.code
.hl_variable};
:::

::: line
[]{#l00164}[
[164](struct_ball_movement_1_1_line_segment.html#a69fc40fa8c0df4a8c088a9fdd6c97449){.line}]{.lineno}
[public]{.keyword} Vector3
[end](struct_ball_movement_1_1_line_segment.html#a69fc40fa8c0df4a8c088a9fdd6c97449){.code
.hl_variable};
:::

::: line
[]{#l00165}[
[165](struct_ball_movement_1_1_line_segment.html#a9c4654ac7f753bf2b97cad21ffc4c04c){.line}]{.lineno}
[public]{.keyword} Vector3
[normal](struct_ball_movement_1_1_line_segment.html#a9c4654ac7f753bf2b97cad21ffc4c04c){.code
.hl_variable};
:::

::: line
[]{#l00166}[ 166]{.lineno}
:::

::: {#foldopen00167 .foldopen data-start="{" end="}"}
::: line
[]{#l00167}[
[167](struct_ball_movement_1_1_line_segment.html#ad2b567b007687d6235085bfb628f6fe8){.line}]{.lineno}
[public]{.keyword}
[LineSegment](struct_ball_movement_1_1_line_segment.html#ad2b567b007687d6235085bfb628f6fe8){.code
.hl_function}(Vector3
[start](struct_ball_movement_1_1_line_segment.html#ab6925c20f22c7ed443f2a1710866c9e5){.code
.hl_variable}, Vector3
[end](struct_ball_movement_1_1_line_segment.html#a69fc40fa8c0df4a8c088a9fdd6c97449){.code
.hl_variable}, Vector3
[normal](struct_ball_movement_1_1_line_segment.html#a9c4654ac7f753bf2b97cad21ffc4c04c){.code
.hl_variable})
:::

::: line
[]{#l00168}[ 168]{.lineno} {
:::

::: line
[]{#l00169}[ 169]{.lineno} this.start =
[start](struct_ball_movement_1_1_line_segment.html#ab6925c20f22c7ed443f2a1710866c9e5){.code
.hl_variable};
:::

::: line
[]{#l00170}[ 170]{.lineno} this.end =
[end](struct_ball_movement_1_1_line_segment.html#a69fc40fa8c0df4a8c088a9fdd6c97449){.code
.hl_variable};
:::

::: line
[]{#l00171}[ 171]{.lineno} this.normal =
[normal](struct_ball_movement_1_1_line_segment.html#a9c4654ac7f753bf2b97cad21ffc4c04c){.code
.hl_variable};
:::

::: line
[]{#l00172}[ 172]{.lineno} }
:::
:::

::: line
[]{#l00173}[ 173]{.lineno} }
:::
:::

::: line
[]{#l00174}[ 174]{.lineno}
:::

::: {#foldopen00175 .foldopen data-start="{" end="}"}
::: line
[]{#l00175}[
[175](class_ball_movement.html#a2c6180a5d985ce8c7c39596ab9e5d9a3){.line}]{.lineno}
[public]{.keyword} [bool]{.keywordtype}
[LineSegmentIntersection](class_ball_movement.html#a2c6180a5d985ce8c7c39596ab9e5d9a3){.code
.hl_function}(Vector3 p1, Vector3 p2, Vector3 q1, Vector3 q2, out
Vector3 intersectionPoint)
:::

::: line
[]{#l00176}[ 176]{.lineno} {
:::

::: line
[]{#l00177}[ 177]{.lineno} Vector3 r = p2 - p1;
:::

::: line
[]{#l00178}[ 178]{.lineno} Vector3 s = q2 - q1;
:::

::: line
[]{#l00179}[ 179]{.lineno}
:::

::: line
[]{#l00180}[ 180]{.lineno} [float]{.keywordtype} d = r.x \* s.y - r.y \*
s.x;
:::

::: line
[]{#l00181}[ 181]{.lineno} [float]{.keywordtype} u = ((q1.x - p1.x) \*
r.y - (q1.y - p1.y) \* r.x) / d;
:::

::: line
[]{#l00182}[ 182]{.lineno} [float]{.keywordtype} t = ((q1.x - p1.x) \*
s.y - (q1.y - p1.y) \* s.x) / d;
:::

::: line
[]{#l00183}[ 183]{.lineno} [if]{.keywordflow} ((0 \<= u && u \<= 1 && 0
\<= t && t \<= 1))
:::

::: line
[]{#l00184}[ 184]{.lineno} {
:::

::: line
[]{#l00185}[ 185]{.lineno} intersectionPoint = p1 + t \* r;
:::

::: line
[]{#l00186}[ 186]{.lineno} [return]{.keywordflow} [true]{.keyword};
:::

::: line
[]{#l00187}[ 187]{.lineno} }
:::

::: line
[]{#l00188}[ 188]{.lineno}
:::

::: line
[]{#l00189}[ 189]{.lineno} intersectionPoint = [default]{.keywordflow};
:::

::: line
[]{#l00190}[ 190]{.lineno} [return]{.keywordflow} [false]{.keyword};
:::

::: line
[]{#l00191}[ 191]{.lineno} }
:::
:::

::: line
[]{#l00192}[ 192]{.lineno}
:::

::: line
[]{#l00193}[ 193]{.lineno} [bool]{.keywordtype}
LineSegmentIntersectionOriginal(Vector3 p1, Vector3 p2, Vector3 q1,
Vector3 q2, out Vector3 intersectionPoint)
:::

::: line
[]{#l00194}[ 194]{.lineno} {
:::

::: line
[]{#l00195}[ 195]{.lineno} [float]{.keywordtype} A1 = p2.y - p1.y;
:::

::: line
[]{#l00196}[ 196]{.lineno} [float]{.keywordtype} B1 = p1.x - p2.x;
:::

::: line
[]{#l00197}[ 197]{.lineno} [float]{.keywordtype} C1 = A1 \* p1.x + B1 \*
p1.y;
:::

::: line
[]{#l00198}[ 198]{.lineno}
:::

::: line
[]{#l00199}[ 199]{.lineno} [float]{.keywordtype} A2 = q2.y - q1.y;
:::

::: line
[]{#l00200}[ 200]{.lineno} [float]{.keywordtype} B2 = q1.x - q2.x;
:::

::: line
[]{#l00201}[ 201]{.lineno} [float]{.keywordtype} C2 = A2 \* q1.x + B2 \*
q1.y;
:::

::: line
[]{#l00202}[ 202]{.lineno}
:::

::: line
[]{#l00203}[ 203]{.lineno} [float]{.keywordtype} det = A1 \* B2 - A2 \*
B1;
:::

::: line
[]{#l00204}[ 204]{.lineno}
:::

::: line
[]{#l00205}[ 205]{.lineno} [if]{.keywordflow} (Mathf.Abs(det) \<
0.0001f)
:::

::: line
[]{#l00206}[ 206]{.lineno} {
:::

::: line
[]{#l00207}[ 207]{.lineno} [// Çizgiler paralelse]{.comment}
:::

::: line
[]{#l00208}[ 208]{.lineno} intersectionPoint = Vector3.zero;
:::

::: line
[]{#l00209}[ 209]{.lineno} [return]{.keywordflow} [false]{.keyword};
:::

::: line
[]{#l00210}[ 210]{.lineno} }
:::

::: line
[]{#l00211}[ 211]{.lineno}
:::

::: line
[]{#l00212}[ 212]{.lineno} [float]{.keywordtype} x = (B2 \* C1 - B1 \*
C2) / det;
:::

::: line
[]{#l00213}[ 213]{.lineno} [float]{.keywordtype} y = (A1 \* C2 - A2 \*
C1) / det;
:::

::: line
[]{#l00214}[ 214]{.lineno} [//Debug.Log(x);]{.comment}
:::

::: line
[]{#l00215}[ 215]{.lineno} [//Debug.Log(y);]{.comment}
:::

::: line
[]{#l00216}[ 216]{.lineno} [if]{.keywordflow} ((x \>= Mathf.Min(p1.x,
p2.x) && x \<= Mathf.Max(p1.x, p2.x)) &&
:::

::: line
[]{#l00217}[ 217]{.lineno} (y \>= Mathf.Min(p1.y, p2.y) && y \<=
Mathf.Max(p1.y, p2.y)) &&
:::

::: line
[]{#l00218}[ 218]{.lineno} (x \>= Mathf.Min(q1.x, q2.x) && x \<=
Mathf.Max(q1.x, q2.x)) &&
:::

::: line
[]{#l00219}[ 219]{.lineno} (y \>= Mathf.Min(q1.y, q2.y) && y \<=
Mathf.Max(q1.y, q2.y)))
:::

::: line
[]{#l00220}[ 220]{.lineno} {
:::

::: line
[]{#l00221}[ 221]{.lineno} intersectionPoint = [new]{.keyword}
Vector3(x, y, 0);
:::

::: line
[]{#l00222}[ 222]{.lineno} [return]{.keywordflow} [true]{.keyword};
:::

::: line
[]{#l00223}[ 223]{.lineno} }
:::

::: line
[]{#l00224}[ 224]{.lineno}
:::

::: line
[]{#l00225}[ 225]{.lineno} intersectionPoint = Vector3.zero;
:::

::: line
[]{#l00226}[ 226]{.lineno} [return]{.keywordflow} [false]{.keyword};
:::

::: line
[]{#l00227}[ 227]{.lineno} }
:::

::: line
[]{#l00228}[ 228]{.lineno}
:::

::: line
[]{#l00229}[
[229](class_ball_movement.html#a5866f553f594be14a85c88de4fcdf36f){.line}]{.lineno}
[public]{.keyword} Font
[font](class_ball_movement.html#a5866f553f594be14a85c88de4fcdf36f){.code
.hl_variable};
:::

::: line
[]{#l00230}[ 230]{.lineno} [private]{.keyword} [void]{.keywordtype}
OnGUI()
:::

::: line
[]{#l00231}[ 231]{.lineno} {
:::

::: line
[]{#l00232}[ 232]{.lineno} GUI.skin.font =
[font](class_ball_movement.html#a5866f553f594be14a85c88de4fcdf36f){.code
.hl_variable};
:::

::: line
[]{#l00233}[ 233]{.lineno} GUIStyle style = [new]{.keyword}
GUIStyle(GUI.skin.label);
:::

::: line
[]{#l00234}[ 234]{.lineno} style.alignment = TextAnchor.MiddleCenter;
:::

::: line
[]{#l00235}[ 235]{.lineno}
:::

::: line
[]{#l00236}[ 236]{.lineno} GUI.Label([new]{.keyword} Rect(Screen.width /
2 - 125 - 50, -50, 250, 250), score2.ToString(), style);
:::

::: line
[]{#l00237}[ 237]{.lineno} GUI.Label([new]{.keyword} Rect(Screen.width /
2 - 125 + 50, -50, 250, 250), score1.ToString(), style);
:::

::: line
[]{#l00238}[ 238]{.lineno} }
:::

::: line
[]{#l00239}[ 239]{.lineno}}
:::
:::

::: {#a_ball_movement_8cs_html_a832e8f52fca5a678819ec96269dcb532 .ttc}
::: ttname
[Random](_ball_movement_8cs.html#a832e8f52fca5a678819ec96269dcb532)
:::

::: ttdeci
UnityEngine.Random Random
:::

::: ttdef
**Definition**
[BallMovement.cs:7](_ball_movement_8cs_source.html#l00007)
:::
:::

::: {#aclass_ball_movement_html .ttc}
::: ttname
[BallMovement](class_ball_movement.html)
:::

::: ttdoc
This Class controls Ball Movement and Segment Intersections.
:::

::: ttdef
**Definition**
[BallMovement.cs:13](_ball_movement_8cs_source.html#l00012)
:::
:::

::: {#aclass_ball_movement_html_a2c6180a5d985ce8c7c39596ab9e5d9a3 .ttc}
::: ttname
[BallMovement.LineSegmentIntersection](class_ball_movement.html#a2c6180a5d985ce8c7c39596ab9e5d9a3)
:::

::: ttdeci
bool LineSegmentIntersection(Vector3 p1, Vector3 p2, Vector3 q1, Vector3
q2, out Vector3 intersectionPoint)
:::

::: ttdef
**Definition**
[BallMovement.cs:175](_ball_movement_8cs_source.html#l00175)
:::
:::

::: {#aclass_ball_movement_html_a5866f553f594be14a85c88de4fcdf36f .ttc}
::: ttname
[BallMovement.font](class_ball_movement.html#a5866f553f594be14a85c88de4fcdf36f)
:::

::: ttdeci
Font font
:::

::: ttdef
**Definition**
[BallMovement.cs:229](_ball_movement_8cs_source.html#l00229)
:::
:::

::: {#aclass_ball_movement_html_aa33416010b3040ac39e7b02bfa7aa95a .ttc}
::: ttname
[BallMovement.edgeFollow](class_ball_movement.html#aa33416010b3040ac39e7b02bfa7aa95a)
:::

::: ttdeci
float edgeFollow
:::

::: ttdef
**Definition**
[BallMovement.cs:18](_ball_movement_8cs_source.html#l00018)
:::
:::

::: {#aclass_ball_movement_html_ab2657ddd68ebf02876c11212145fcfdb .ttc}
::: ttname
[BallMovement.ball](class_ball_movement.html#ab2657ddd68ebf02876c11212145fcfdb)
:::

::: ttdeci
Transform ball
:::

::: ttdef
**Definition**
[BallMovement.cs:14](_ball_movement_8cs_source.html#l00014)
:::
:::

::: {#aclass_ball_movement_html_ac6a63f2cbb61ce14dda95621177ee843 .ttc}
::: ttname
[BallMovement.direction](class_ball_movement.html#ac6a63f2cbb61ce14dda95621177ee843)
:::

::: ttdeci
Vector2 direction
:::

::: ttdef
**Definition**
[BallMovement.cs:20](_ball_movement_8cs_source.html#l00020)
:::
:::

::: {#aclass_ball_movement_html_ae5be514e8f3c1b3af767d5a8627c9277 .ttc}
::: ttname
[BallMovement.speed](class_ball_movement.html#ae5be514e8f3c1b3af767d5a8627c9277)
:::

::: ttdeci
float speed
:::

::: ttdef
**Definition**
[BallMovement.cs:19](_ball_movement_8cs_source.html#l00019)
:::
:::

::: {#aclass_ball_movement_html_ae6fbc952b54fb915ac79385d0a55ecc0 .ttc}
::: ttname
[BallMovement.paddle2](class_ball_movement.html#ae6fbc952b54fb915ac79385d0a55ecc0)
:::

::: ttdeci
Transform paddle2
:::

::: ttdef
**Definition**
[BallMovement.cs:16](_ball_movement_8cs_source.html#l00016)
:::
:::

::: {#aclass_ball_movement_html_afc7bd1ba11daafd6825473d72337f708 .ttc}
::: ttname
[BallMovement.paddle1](class_ball_movement.html#afc7bd1ba11daafd6825473d72337f708)
:::

::: ttdeci
Transform paddle1
:::

::: ttdef
**Definition**
[BallMovement.cs:15](_ball_movement_8cs_source.html#l00015)
:::
:::

::: {#astruct_ball_movement_1_1_line_segment_html .ttc}
::: ttname
[BallMovement.LineSegment](struct_ball_movement_1_1_line_segment.html)
:::

::: ttdoc
Calculates two line segmentation.
:::

::: ttdef
**Definition**
[BallMovement.cs:162](_ball_movement_8cs_source.html#l00161)
:::
:::

::: {#astruct_ball_movement_1_1_line_segment_html_a69fc40fa8c0df4a8c088a9fdd6c97449 .ttc}
::: ttname
[BallMovement.LineSegment.end](struct_ball_movement_1_1_line_segment.html#a69fc40fa8c0df4a8c088a9fdd6c97449)
:::

::: ttdeci
Vector3 end
:::

::: ttdef
**Definition**
[BallMovement.cs:164](_ball_movement_8cs_source.html#l00164)
:::
:::

::: {#astruct_ball_movement_1_1_line_segment_html_a9c4654ac7f753bf2b97cad21ffc4c04c .ttc}
::: ttname
[BallMovement.LineSegment.normal](struct_ball_movement_1_1_line_segment.html#a9c4654ac7f753bf2b97cad21ffc4c04c)
:::

::: ttdeci
Vector3 normal
:::

::: ttdef
**Definition**
[BallMovement.cs:165](_ball_movement_8cs_source.html#l00165)
:::
:::

::: {#astruct_ball_movement_1_1_line_segment_html_ab6925c20f22c7ed443f2a1710866c9e5 .ttc}
::: ttname
[BallMovement.LineSegment.start](struct_ball_movement_1_1_line_segment.html#ab6925c20f22c7ed443f2a1710866c9e5)
:::

::: ttdeci
Vector3 start
:::

::: ttdef
**Definition**
[BallMovement.cs:163](_ball_movement_8cs_source.html#l00163)
:::
:::

::: {#astruct_ball_movement_1_1_line_segment_html_ad2b567b007687d6235085bfb628f6fe8 .ttc}
::: ttname
[BallMovement.LineSegment.LineSegment](struct_ball_movement_1_1_line_segment.html#ad2b567b007687d6235085bfb628f6fe8)
:::

::: ttdeci
LineSegment(Vector3 start, Vector3 end, Vector3 normal)
:::

::: ttdef
**Definition**
[BallMovement.cs:167](_ball_movement_8cs_source.html#l00167)
:::
:::
:::
:::
:::

::: {#nav-path .navpath}
-   [FurkanIntern](dir_1dcde7ea5adb4470e937f2f1c0036389.html){.el}
-   [Internship](dir_db18fc5b59b71647f21f3d49fd35b7b1.html){.el}
-   [Pong Staj](dir_7f2202f332a95df5c6e50699b596c7b9.html){.el}
-   [Assets](dir_b7568e80c0eb65df54ebd3d006b23e5e.html){.el}
-   [Scripts](dir_97d71e10d40891aefe860af68a8d9ea5.html){.el}
-   [BallMovement.cs](_ball_movement_8cs.html){.el}
-   Generated by [![doxygen](doxygen.svg){.footer width="104"
    height="31"}](https://www.doxygen.org/index.html) 1.9.8
:::
