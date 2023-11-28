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

</div>

<div class="header">

<div class="summary">

[Data Structures](#nested-classes) \| [Public Member
Functions](#pub-methods) \| [Data Fields](#pub-attribs)

</div>

<div class="headertitle">

<div class="title">

BallMovement Class Reference

</div>

</div>

</div>

<div class="contents">

This Class controls Ball Movement and Segment Intersections.
[More...](class_ball_movement.html#details)

<table class="memberdecls">
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd heading">
<td colspan="2"><h2 id="data-structures" class="groupheader"><span
id="nested-classes"></span> Data Structures</h2></td>
</tr>
<tr class="even memitem:">
<td class="memItemLeft" style="text-align: right;"
data-valign="top">struct  </td>
<td class="memItemRight" data-valign="bottom"><a
href="struct_ball_movement_1_1_line_segment.html"
class="el">LineSegment</a></td>
</tr>
<tr class="odd memdesc:">
<td class="mdescLeft"> </td>
<td class="mdescRight">Calculates two line segmentation. <a
href="struct_ball_movement_1_1_line_segment.html#details">More...</a><br />
</td>
</tr>
<tr class="even separator:">
<td colspan="2" class="memSeparator"> </td>
</tr>
</tbody>
</table>

<table class="memberdecls">
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd heading">
<td colspan="2"><h2 id="public-member-functions"
class="groupheader"><span id="pub-methods"></span> Public Member
Functions</h2></td>
</tr>
<tr id="r_a2c6180a5d985ce8c7c39596ab9e5d9a3"
class="even memitem:a2c6180a5d985ce8c7c39596ab9e5d9a3">
<td class="memItemLeft" style="text-align: right;"
data-valign="top">bool </td>
<td class="memItemRight" data-valign="bottom"><a
href="class_ball_movement.html#a2c6180a5d985ce8c7c39596ab9e5d9a3"
class="el">LineSegmentIntersection</a> (Vector3 p1, Vector3 p2, Vector3
q1, Vector3 q2, out Vector3 intersectionPoint)</td>
</tr>
<tr class="odd separator:a2c6180a5d985ce8c7c39596ab9e5d9a3">
<td colspan="2" class="memSeparator"> </td>
</tr>
</tbody>
</table>

<table class="memberdecls">
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd heading">
<td colspan="2"><h2 id="data-fields" class="groupheader"><span
id="pub-attribs"></span> Data Fields</h2></td>
</tr>
<tr id="r_ab2657ddd68ebf02876c11212145fcfdb"
class="even memitem:ab2657ddd68ebf02876c11212145fcfdb">
<td class="memItemLeft" style="text-align: right;"
data-valign="top">Transform </td>
<td class="memItemRight" data-valign="bottom"><a
href="class_ball_movement.html#ab2657ddd68ebf02876c11212145fcfdb"
class="el">ball</a></td>
</tr>
<tr class="odd separator:ab2657ddd68ebf02876c11212145fcfdb">
<td colspan="2" class="memSeparator"> </td>
</tr>
<tr id="r_afc7bd1ba11daafd6825473d72337f708"
class="even memitem:afc7bd1ba11daafd6825473d72337f708">
<td class="memItemLeft" style="text-align: right;"
data-valign="top">Transform </td>
<td class="memItemRight" data-valign="bottom"><a
href="class_ball_movement.html#afc7bd1ba11daafd6825473d72337f708"
class="el">paddle1</a></td>
</tr>
<tr class="odd separator:afc7bd1ba11daafd6825473d72337f708">
<td colspan="2" class="memSeparator"> </td>
</tr>
<tr id="r_ae6fbc952b54fb915ac79385d0a55ecc0"
class="even memitem:ae6fbc952b54fb915ac79385d0a55ecc0">
<td class="memItemLeft" style="text-align: right;"
data-valign="top">Transform </td>
<td class="memItemRight" data-valign="bottom"><a
href="class_ball_movement.html#ae6fbc952b54fb915ac79385d0a55ecc0"
class="el">paddle2</a></td>
</tr>
<tr class="odd separator:ae6fbc952b54fb915ac79385d0a55ecc0">
<td colspan="2" class="memSeparator"> </td>
</tr>
<tr id="r_aa33416010b3040ac39e7b02bfa7aa95a"
class="even memitem:aa33416010b3040ac39e7b02bfa7aa95a">
<td class="memItemLeft" style="text-align: right;"
data-valign="top">float </td>
<td class="memItemRight" data-valign="bottom"><a
href="class_ball_movement.html#aa33416010b3040ac39e7b02bfa7aa95a"
class="el">edgeFollow</a> = 11f</td>
</tr>
<tr class="odd separator:aa33416010b3040ac39e7b02bfa7aa95a">
<td colspan="2" class="memSeparator"> </td>
</tr>
<tr id="r_ae5be514e8f3c1b3af767d5a8627c9277"
class="even memitem:ae5be514e8f3c1b3af767d5a8627c9277">
<td class="memItemLeft" style="text-align: right;"
data-valign="top">float </td>
<td class="memItemRight" data-valign="bottom"><a
href="class_ball_movement.html#ae5be514e8f3c1b3af767d5a8627c9277"
class="el">speed</a> = 5f</td>
</tr>
<tr class="odd separator:ae5be514e8f3c1b3af767d5a8627c9277">
<td colspan="2" class="memSeparator"> </td>
</tr>
<tr id="r_ac6a63f2cbb61ce14dda95621177ee843"
class="even memitem:ac6a63f2cbb61ce14dda95621177ee843">
<td class="memItemLeft" style="text-align: right;"
data-valign="top">Vector2 </td>
<td class="memItemRight" data-valign="bottom"><a
href="class_ball_movement.html#ac6a63f2cbb61ce14dda95621177ee843"
class="el">direction</a></td>
</tr>
<tr class="odd separator:ac6a63f2cbb61ce14dda95621177ee843">
<td colspan="2" class="memSeparator"> </td>
</tr>
<tr id="r_a5866f553f594be14a85c88de4fcdf36f"
class="even memitem:a5866f553f594be14a85c88de4fcdf36f">
<td class="memItemLeft" style="text-align: right;"
data-valign="top">Font </td>
<td class="memItemRight" data-valign="bottom"><a
href="class_ball_movement.html#a5866f553f594be14a85c88de4fcdf36f"
class="el">font</a></td>
</tr>
<tr class="odd separator:a5866f553f594be14a85c88de4fcdf36f">
<td colspan="2" class="memSeparator"> </td>
</tr>
</tbody>
</table>

<span id="details"></span>

## Detailed Description

<div class="textblock">

This Class controls Ball Movement and Segment Intersections.

Definition at line
<a href="_ball_movement_8cs_source.html#l00012" class="el">12</a> of
file
<a href="_ball_movement_8cs_source.html" class="el">BallMovement.cs</a>.

</div>

## Member Function Documentation

<span id="a2c6180a5d985ce8c7c39596ab9e5d9a3"></span>

## <span class="permalink">[◆ ](#a2c6180a5d985ce8c7c39596ab9e5d9a3)</span>LineSegmentIntersection()

<div class="memitem">

<div class="memproto">

<table class="mlabels">
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td class="mlabels-left"><table class="memname">
<tbody>
<tr class="odd">
<td class="memname">bool BallMovement.LineSegmentIntersection</td>
<td>(</td>
<td class="paramtype">Vector3 </td>
<td class="paramname"><em>p1</em>,</td>
</tr>
<tr class="even">
<td class="paramkey"></td>
<td></td>
<td class="paramtype">Vector3 </td>
<td class="paramname"><em>p2</em>,</td>
</tr>
<tr class="odd">
<td class="paramkey"></td>
<td></td>
<td class="paramtype">Vector3 </td>
<td class="paramname"><em>q1</em>,</td>
</tr>
<tr class="even">
<td class="paramkey"></td>
<td></td>
<td class="paramtype">Vector3 </td>
<td class="paramname"><em>q2</em>,</td>
</tr>
<tr class="odd">
<td class="paramkey"></td>
<td></td>
<td class="paramtype">out Vector3 </td>
<td class="paramname"><em>intersectionPoint</em> </td>
</tr>
<tr class="even">
<td></td>
<td>)</td>
<td></td>
<td></td>
</tr>
</tbody>
</table></td>
<td class="mlabels-right"><span class="mlabels"><span
class="mlabel">inline</span></span></td>
</tr>
</tbody>
</table>

</div>

<div class="memdoc">

Definition at line
<a href="_ball_movement_8cs_source.html#l00175" class="el">175</a> of
file
<a href="_ball_movement_8cs_source.html" class="el">BallMovement.cs</a>.

</div>

</div>

## Field Documentation

<span id="ab2657ddd68ebf02876c11212145fcfdb"></span>

## <span class="permalink">[◆ ](#ab2657ddd68ebf02876c11212145fcfdb)</span>ball

<div class="memitem">

<div class="memproto">

|                             |
|-----------------------------|
| Transform BallMovement.ball |

</div>

<div class="memdoc">

Definition at line
<a href="_ball_movement_8cs_source.html#l00014" class="el">14</a> of
file
<a href="_ball_movement_8cs_source.html" class="el">BallMovement.cs</a>.

</div>

</div>

<span id="ac6a63f2cbb61ce14dda95621177ee843"></span>

## <span class="permalink">[◆ ](#ac6a63f2cbb61ce14dda95621177ee843)</span>direction

<div class="memitem">

<div class="memproto">

|                                |
|--------------------------------|
| Vector2 BallMovement.direction |

</div>

<div class="memdoc">

Definition at line
<a href="_ball_movement_8cs_source.html#l00020" class="el">20</a> of
file
<a href="_ball_movement_8cs_source.html" class="el">BallMovement.cs</a>.

</div>

</div>

<span id="aa33416010b3040ac39e7b02bfa7aa95a"></span>

## <span class="permalink">[◆ ](#aa33416010b3040ac39e7b02bfa7aa95a)</span>edgeFollow

<div class="memitem">

<div class="memproto">

|                                     |
|-------------------------------------|
| float BallMovement.edgeFollow = 11f |

</div>

<div class="memdoc">

Definition at line
<a href="_ball_movement_8cs_source.html#l00018" class="el">18</a> of
file
<a href="_ball_movement_8cs_source.html" class="el">BallMovement.cs</a>.

</div>

</div>

<span id="a5866f553f594be14a85c88de4fcdf36f"></span>

## <span class="permalink">[◆ ](#a5866f553f594be14a85c88de4fcdf36f)</span>font

<div class="memitem">

<div class="memproto">

|                        |
|------------------------|
| Font BallMovement.font |

</div>

<div class="memdoc">

Definition at line
<a href="_ball_movement_8cs_source.html#l00229" class="el">229</a> of
file
<a href="_ball_movement_8cs_source.html" class="el">BallMovement.cs</a>.

</div>

</div>

<span id="afc7bd1ba11daafd6825473d72337f708"></span>

## <span class="permalink">[◆ ](#afc7bd1ba11daafd6825473d72337f708)</span>paddle1

<div class="memitem">

<div class="memproto">

|                                |
|--------------------------------|
| Transform BallMovement.paddle1 |

</div>

<div class="memdoc">

Definition at line
<a href="_ball_movement_8cs_source.html#l00015" class="el">15</a> of
file
<a href="_ball_movement_8cs_source.html" class="el">BallMovement.cs</a>.

</div>

</div>

<span id="ae6fbc952b54fb915ac79385d0a55ecc0"></span>

## <span class="permalink">[◆ ](#ae6fbc952b54fb915ac79385d0a55ecc0)</span>paddle2

<div class="memitem">

<div class="memproto">

|                                |
|--------------------------------|
| Transform BallMovement.paddle2 |

</div>

<div class="memdoc">

Definition at line
<a href="_ball_movement_8cs_source.html#l00016" class="el">16</a> of
file
<a href="_ball_movement_8cs_source.html" class="el">BallMovement.cs</a>.

</div>

</div>

<span id="ae5be514e8f3c1b3af767d5a8627c9277"></span>

## <span class="permalink">[◆ ](#ae5be514e8f3c1b3af767d5a8627c9277)</span>speed

<div class="memitem">

<div class="memproto">

|                               |
|-------------------------------|
| float BallMovement.speed = 5f |

</div>

<div class="memdoc">

Definition at line
<a href="_ball_movement_8cs_source.html#l00019" class="el">19</a> of
file
<a href="_ball_movement_8cs_source.html" class="el">BallMovement.cs</a>.

</div>

</div>

------------------------------------------------------------------------

The documentation for this class was generated from the following file:

- C:/Users/dalakgames/Desktop/FurkanIntern/Internship/Pong
  Staj/Assets/Scripts/<a href="_ball_movement_8cs_source.html" class="el">BallMovement.cs</a>

</div>

------------------------------------------------------------------------

<span class="small">Generated
by [<img src="doxygen.svg" class="footer" width="104" height="31"
alt="doxygen" />](https://www.doxygen.org/index.html) 1.9.8</span>
