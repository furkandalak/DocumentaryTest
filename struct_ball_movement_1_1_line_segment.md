::: {#top}
::: {#titlearea}
+-----------------------------------------------------------------------+
| ::: {#projectname}                                                    |
| PongExample[ 1.0.0]{#projectnumber}                                   |
| :::                                                                   |
+-----------------------------------------------------------------------+
:::

::: {#nav-path .navpath}
-   [BallMovement](class_ball_movement.html){.el}
-   [LineSegment](struct_ball_movement_1_1_line_segment.html){.el}
:::
:::

::: header
::: summary
[Public Member Functions](#pub-methods) \| [Public
Attributes](#pub-attribs) \| [List of all
members](struct_ball_movement_1_1_line_segment-members.html)
:::

::: headertitle
::: title
BallMovement.LineSegment Struct Reference
:::
:::
:::

::: contents
Calculates two line segmentation.
[More\...](struct_ball_movement_1_1_line_segment.html#details)

+-----------------------------------+-----------------------------------+
| ## []{#pub-method                 |                                   |
| s} Public Member Functions {#publ |                                   |
| ic-member-functions .groupheader} |                                   |
+-----------------------------------+-----------------------------------+
|                                   | [LineSegment](struct_ball_move    |
|                                   | ment_1_1_line_segment.html#ad2b56 |
|                                   | 7b007687d6235085bfb628f6fe8){.el} |
|                                   | (Vector3                          |
|                                   | [start](struct_ball_movem         |
|                                   | ent_1_1_line_segment.html#ab6925c |
|                                   | 20f22c7ed443f2a1710866c9e5){.el}, |
|                                   | Vector3                           |
|                                   | [end](struct_ball_movem           |
|                                   | ent_1_1_line_segment.html#a69fc40 |
|                                   | fa8c0df4a8c088a9fdd6c97449){.el}, |
|                                   | Vector3                           |
|                                   | [normal](struct_ball_movem        |
|                                   | ent_1_1_line_segment.html#a9c4654 |
|                                   | ac7f753bf2b97cad21ffc4c04c){.el}) |
+-----------------------------------+-----------------------------------+
|                                   |                                   |
+-----------------------------------+-----------------------------------+

+-----------------------------------+-----------------------------------+
| ## []                             |                                   |
| {#pub-attribs} Public Attributes  |                                   |
| {#public-attributes .groupheader} |                                   |
+-----------------------------------+-----------------------------------+
| Vector3                           | [start](struct_ball_move          |
|                                   | ment_1_1_line_segment.html#ab6925 |
|                                   | c20f22c7ed443f2a1710866c9e5){.el} |
+-----------------------------------+-----------------------------------+
|                                   |                                   |
+-----------------------------------+-----------------------------------+
| Vector3                           | [end](struct_ball_move            |
|                                   | ment_1_1_line_segment.html#a69fc4 |
|                                   | 0fa8c0df4a8c088a9fdd6c97449){.el} |
+-----------------------------------+-----------------------------------+
|                                   |                                   |
+-----------------------------------+-----------------------------------+
| Vector3                           | [normal](struct_ball_move         |
|                                   | ment_1_1_line_segment.html#a9c465 |
|                                   | 4ac7f753bf2b97cad21ffc4c04c){.el} |
+-----------------------------------+-----------------------------------+
|                                   |                                   |
+-----------------------------------+-----------------------------------+

[]{#details}

## Detailed Description {#detailed-description .groupheader}

::: textblock
Calculates two line segmentation.

Parameters

:   ------------------- -----------------------------
      p1                  First point of firt line
      p2                  Second point of first line
      q1                  First point of second line
      q2                  Second point of second line
      intersectionPoint   Returns if intersect
      ------------------- -----------------------------

```{=html}
<!-- -->
```

Returns
:   Bool

Definition at line [161](_ball_movement_8cs_source.html#l00161){.el} of
file [BallMovement.cs](_ball_movement_8cs_source.html){.el}.
:::

## Constructor & Destructor Documentation {#constructor-destructor-documentation .groupheader}

[]{#ad2b567b007687d6235085bfb628f6fe8}

## [[◆ ](#ad2b567b007687d6235085bfb628f6fe8)]{.permalink}LineSegment() {#linesegment .memtitle}

::: memitem
::: memproto
+-----------------------------------+-----------------------------------+
|                                   | [[inline]{.mlabel}]{.mlabels}     |
|  -------------------------------- |                                   |
| ------ --- ---------- ----------- |                                   |
|   BallMovement.LineSegment.Line   |                                   |
| Segment   (   Vector3    *start*, |                                   |
|                                   |                                   |
|                 Vector3    *end*, |                                   |
|                                   |                                   |
|              Vector3    *normal*  |                                   |
|                                   |                                   |
|                   )               |                                   |
|                                   |                                   |
|  -------------------------------- |                                   |
| ------ --- ---------- ----------- |                                   |
+-----------------------------------+-----------------------------------+
:::

::: memdoc
Definition at line [167](_ball_movement_8cs_source.html#l00167){.el} of
file [BallMovement.cs](_ball_movement_8cs_source.html){.el}.
:::
:::

## Member Data Documentation {#member-data-documentation .groupheader}

[]{#a69fc40fa8c0df4a8c088a9fdd6c97449}

## [[◆ ](#a69fc40fa8c0df4a8c088a9fdd6c97449)]{.permalink}end {#end .memtitle}

::: memitem
::: memproto
  --------------------------------------
  Vector3 BallMovement.LineSegment.end
  --------------------------------------
:::

::: memdoc
Definition at line [164](_ball_movement_8cs_source.html#l00164){.el} of
file [BallMovement.cs](_ball_movement_8cs_source.html){.el}.
:::
:::

[]{#a9c4654ac7f753bf2b97cad21ffc4c04c}

## [[◆ ](#a9c4654ac7f753bf2b97cad21ffc4c04c)]{.permalink}normal {#normal .memtitle}

::: memitem
::: memproto
  -----------------------------------------
  Vector3 BallMovement.LineSegment.normal
  -----------------------------------------
:::

::: memdoc
Definition at line [165](_ball_movement_8cs_source.html#l00165){.el} of
file [BallMovement.cs](_ball_movement_8cs_source.html){.el}.
:::
:::

[]{#ab6925c20f22c7ed443f2a1710866c9e5}

## [[◆ ](#ab6925c20f22c7ed443f2a1710866c9e5)]{.permalink}start {#start .memtitle}

::: memitem
::: memproto
  ----------------------------------------
  Vector3 BallMovement.LineSegment.start
  ----------------------------------------
:::

::: memdoc
Definition at line [163](_ball_movement_8cs_source.html#l00163){.el} of
file [BallMovement.cs](_ball_movement_8cs_source.html){.el}.
:::
:::

------------------------------------------------------------------------

The documentation for this struct was generated from the following file:

-   C:/Users/dalakgames/Desktop/FurkanIntern/Internship/Pong
    Staj/Assets/Scripts/[BallMovement.cs](_ball_movement_8cs_source.html){.el}
:::

------------------------------------------------------------------------

[Generated by [![doxygen](doxygen.svg){.footer width="104"
height="31"}](https://www.doxygen.org/index.html) 1.9.8]{.small}
