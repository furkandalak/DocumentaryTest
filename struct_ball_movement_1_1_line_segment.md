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

- <a href="class_ball_movement.html" class="el">BallMovement</a>
- <a href="struct_ball_movement_1_1_line_segment.html"
  class="el">LineSegment</a>

</div>

</div>

<div class="header">

<div class="summary">

[Public Member Functions](#pub-methods) \| [Public
Attributes](#pub-attribs) \| [List of all
members](struct_ball_movement_1_1_line_segment-members.html)

</div>

<div class="headertitle">

<div class="title">

BallMovement.LineSegment Struct Reference

</div>

</div>

</div>

<div class="contents">

Calculates two line segmentation.
[More...](struct_ball_movement_1_1_line_segment.html#details)

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
<tr id="r_ad2b567b007687d6235085bfb628f6fe8"
class="even memitem:ad2b567b007687d6235085bfb628f6fe8">
<td class="memItemLeft" style="text-align: right;"
data-valign="top"> </td>
<td class="memItemRight" data-valign="bottom"><a
href="struct_ball_movement_1_1_line_segment.html#ad2b567b007687d6235085bfb628f6fe8"
class="el">LineSegment</a> (Vector3 <a
href="struct_ball_movement_1_1_line_segment.html#ab6925c20f22c7ed443f2a1710866c9e5"
class="el">start</a>, Vector3 <a
href="struct_ball_movement_1_1_line_segment.html#a69fc40fa8c0df4a8c088a9fdd6c97449"
class="el">end</a>, Vector3 <a
href="struct_ball_movement_1_1_line_segment.html#a9c4654ac7f753bf2b97cad21ffc4c04c"
class="el">normal</a>)</td>
</tr>
<tr class="odd separator:ad2b567b007687d6235085bfb628f6fe8">
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
<td colspan="2"><h2 id="public-attributes" class="groupheader"><span
id="pub-attribs"></span> Public Attributes</h2></td>
</tr>
<tr id="r_ab6925c20f22c7ed443f2a1710866c9e5"
class="even memitem:ab6925c20f22c7ed443f2a1710866c9e5">
<td class="memItemLeft" style="text-align: right;"
data-valign="top">Vector3 </td>
<td class="memItemRight" data-valign="bottom"><a
href="struct_ball_movement_1_1_line_segment.html#ab6925c20f22c7ed443f2a1710866c9e5"
class="el">start</a></td>
</tr>
<tr class="odd separator:ab6925c20f22c7ed443f2a1710866c9e5">
<td colspan="2" class="memSeparator"> </td>
</tr>
<tr id="r_a69fc40fa8c0df4a8c088a9fdd6c97449"
class="even memitem:a69fc40fa8c0df4a8c088a9fdd6c97449">
<td class="memItemLeft" style="text-align: right;"
data-valign="top">Vector3 </td>
<td class="memItemRight" data-valign="bottom"><a
href="struct_ball_movement_1_1_line_segment.html#a69fc40fa8c0df4a8c088a9fdd6c97449"
class="el">end</a></td>
</tr>
<tr class="odd separator:a69fc40fa8c0df4a8c088a9fdd6c97449">
<td colspan="2" class="memSeparator"> </td>
</tr>
<tr id="r_a9c4654ac7f753bf2b97cad21ffc4c04c"
class="even memitem:a9c4654ac7f753bf2b97cad21ffc4c04c">
<td class="memItemLeft" style="text-align: right;"
data-valign="top">Vector3 </td>
<td class="memItemRight" data-valign="bottom"><a
href="struct_ball_movement_1_1_line_segment.html#a9c4654ac7f753bf2b97cad21ffc4c04c"
class="el">normal</a></td>
</tr>
<tr class="odd separator:a9c4654ac7f753bf2b97cad21ffc4c04c">
<td colspan="2" class="memSeparator"> </td>
</tr>
</tbody>
</table>

<span id="details"></span>

## Detailed Description

<div class="textblock">

Calculates two line segmentation.

Parameters  
|                   |                             |
|-------------------|-----------------------------|
| p1                | First point of firt line    |
| p2                | Second point of first line  |
| q1                | First point of second line  |
| q2                | Second point of second line |
| intersectionPoint | Returns if intersect        |

<!-- -->

Returns  
Bool

Definition at line
<a href="_ball_movement_8cs_source.html#l00161" class="el">161</a> of
file
<a href="_ball_movement_8cs_source.html" class="el">BallMovement.cs</a>.

</div>

## Constructor & Destructor Documentation

<span id="ad2b567b007687d6235085bfb628f6fe8"></span>

## <span class="permalink">[◆ ](#ad2b567b007687d6235085bfb628f6fe8)</span>LineSegment()

<div class="memitem">

<div class="memproto">

|                                      |     |          |           |
|--------------------------------------|-----|----------|-----------|
| BallMovement.LineSegment.LineSegment | (   | Vector3  | *start*,  |
|                                      |     | Vector3  | *end*,    |
|                                      |     | Vector3  | *normal*  |
|                                      | )   |          |           |

</div>

<div class="memdoc">

Definition at line
<a href="_ball_movement_8cs_source.html#l00167" class="el">167</a> of
file
<a href="_ball_movement_8cs_source.html" class="el">BallMovement.cs</a>.

</div>

</div>

## Member Data Documentation

<span id="a69fc40fa8c0df4a8c088a9fdd6c97449"></span>

## <span class="permalink">[◆ ](#a69fc40fa8c0df4a8c088a9fdd6c97449)</span>end

<div class="memitem">

<div class="memproto">

|                                      |
|--------------------------------------|
| Vector3 BallMovement.LineSegment.end |

</div>

<div class="memdoc">

Definition at line
<a href="_ball_movement_8cs_source.html#l00164" class="el">164</a> of
file
<a href="_ball_movement_8cs_source.html" class="el">BallMovement.cs</a>.

</div>

</div>

<span id="a9c4654ac7f753bf2b97cad21ffc4c04c"></span>

## <span class="permalink">[◆ ](#a9c4654ac7f753bf2b97cad21ffc4c04c)</span>normal

<div class="memitem">

<div class="memproto">

|                                         |
|-----------------------------------------|
| Vector3 BallMovement.LineSegment.normal |

</div>

<div class="memdoc">

Definition at line
<a href="_ball_movement_8cs_source.html#l00165" class="el">165</a> of
file
<a href="_ball_movement_8cs_source.html" class="el">BallMovement.cs</a>.

</div>

</div>

<span id="ab6925c20f22c7ed443f2a1710866c9e5"></span>

## <span class="permalink">[◆ ](#ab6925c20f22c7ed443f2a1710866c9e5)</span>start

<div class="memitem">

<div class="memproto">

|                                        |
|----------------------------------------|
| Vector3 BallMovement.LineSegment.start |

</div>

<div class="memdoc">

Definition at line
<a href="_ball_movement_8cs_source.html#l00163" class="el">163</a> of
file
<a href="_ball_movement_8cs_source.html" class="el">BallMovement.cs</a>.

</div>

</div>

------------------------------------------------------------------------

The documentation for this struct was generated from the following file:

- C:/Users/dalakgames/Desktop/FurkanIntern/Internship/Pong
  Staj/Assets/Scripts/<a href="_ball_movement_8cs_source.html" class="el">BallMovement.cs</a>

</div>

------------------------------------------------------------------------

<span class="small">Generated
by [<img src="doxygen.svg" class="footer" width="104" height="31"
alt="doxygen" />](https://www.doxygen.org/index.html) 1.9.8</span>
