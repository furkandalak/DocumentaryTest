::: {#top}
::: {#titlearea}
+-----------------------------------------------------------------------+
| ::: {#projectname}                                                    |
| PongExample[ 1.0.0]{#projectnumber}                                   |
| :::                                                                   |
+-----------------------------------------------------------------------+
:::
:::

::: header
::: summary
[Data Structures](#nested-classes) \| [Public Member
Functions](#pub-methods) \| [Data Fields](#pub-attribs)
:::

::: headertitle
::: title
BallMovement Class Reference
:::
:::
:::

::: contents
This Class controls Ball Movement and Segment Intersections.
[More\...](class_ball_movement.html#details)

+-----------------------------------+-----------------------------------+
| ## [                              |                                   |
| ]{#nested-classes} Data Structure |                                   |
| s {#data-structures .groupheader} |                                   |
+-----------------------------------+-----------------------------------+
| struct                            | [LineSegment](struct_ball_mov     |
|                                   | ement_1_1_line_segment.html){.el} |
+-----------------------------------+-----------------------------------+
|                                   | Calculates two line segmentation. |
|                                   | [More\...](struct_ball_movemen    |
|                                   | t_1_1_line_segment.html#details)\ |
+-----------------------------------+-----------------------------------+
|                                   |                                   |
+-----------------------------------+-----------------------------------+

+-----------------------------------+-----------------------------------+
| ## []{#pub-method                 |                                   |
| s} Public Member Functions {#publ |                                   |
| ic-member-functions .groupheader} |                                   |
+-----------------------------------+-----------------------------------+
| bool                              | [LineSegmentIntersection          |
|                                   | ](class_ball_movement.html#a2c618 |
|                                   | 0a5d985ce8c7c39596ab9e5d9a3){.el} |
|                                   | (Vector3 p1, Vector3 p2, Vector3  |
|                                   | q1, Vector3 q2, out Vector3       |
|                                   | intersectionPoint)                |
+-----------------------------------+-----------------------------------+
|                                   |                                   |
+-----------------------------------+-----------------------------------+

+-----------------------------------+-----------------------------------+
| ## []{#pub-attribs} Data F        |                                   |
| ields {#data-fields .groupheader} |                                   |
+-----------------------------------+-----------------------------------+
| Transform                         | [ball                             |
|                                   | ](class_ball_movement.html#ab2657 |
|                                   | ddd68ebf02876c11212145fcfdb){.el} |
+-----------------------------------+-----------------------------------+
|                                   |                                   |
+-----------------------------------+-----------------------------------+
| Transform                         | [paddle1                          |
|                                   | ](class_ball_movement.html#afc7bd |
|                                   | 1ba11daafd6825473d72337f708){.el} |
+-----------------------------------+-----------------------------------+
|                                   |                                   |
+-----------------------------------+-----------------------------------+
| Transform                         | [paddle2                          |
|                                   | ](class_ball_movement.html#ae6fbc |
|                                   | 952b54fb915ac79385d0a55ecc0){.el} |
+-----------------------------------+-----------------------------------+
|                                   |                                   |
+-----------------------------------+-----------------------------------+
| float                             | [edgeFollow                       |
|                                   | ](class_ball_movement.html#aa3341 |
|                                   | 6010b3040ac39e7b02bfa7aa95a){.el} |
|                                   | = 11f                             |
+-----------------------------------+-----------------------------------+
|                                   |                                   |
+-----------------------------------+-----------------------------------+
| float                             | [speed                            |
|                                   | ](class_ball_movement.html#ae5be5 |
|                                   | 14e8f3c1b3af767d5a8627c9277){.el} |
|                                   | = 5f                              |
+-----------------------------------+-----------------------------------+
|                                   |                                   |
+-----------------------------------+-----------------------------------+
| Vector2                           | [direction                        |
|                                   | ](class_ball_movement.html#ac6a63 |
|                                   | f2cbb61ce14dda95621177ee843){.el} |
+-----------------------------------+-----------------------------------+
|                                   |                                   |
+-----------------------------------+-----------------------------------+
| Font                              | [font                             |
|                                   | ](class_ball_movement.html#a5866f |
|                                   | 553f594be14a85c88de4fcdf36f){.el} |
+-----------------------------------+-----------------------------------+
|                                   |                                   |
+-----------------------------------+-----------------------------------+

[]{#details}

## Detailed Description {#detailed-description .groupheader}

::: textblock
This Class controls Ball Movement and Segment Intersections.

Definition at line [12](_ball_movement_8cs_source.html#l00012){.el} of
file [BallMovement.cs](_ball_movement_8cs_source.html){.el}.
:::

## Member Function Documentation {#member-function-documentation .groupheader}

[]{#a2c6180a5d985ce8c7c39596ab9e5d9a3}

## [[◆ ](#a2c6180a5d985ce8c7c39596ab9e5d9a3)]{.permalink}LineSegmentIntersection() {#linesegmentintersection .memtitle}

::: memitem
::: memproto
+-----------------------------------+-----------------------------------+
|   -------------------             | [[inline]{.mlabel}]{.mlabels}     |
| ------------------------ --- ---- |                                   |
| ---------- ---------------------- |                                   |
|   bo                              |                                   |
| ol BallMovement.LineSegmentInters |                                   |
| ection   (   Vector3        *p1*, |                                   |
|                                   |                                   |
|                                   |                                   |
|              Vector3        *p2*, |                                   |
|                                   |                                   |
|                                   |                                   |
|              Vector3        *q1*, |                                   |
|                                   |                                   |
|                                   |                                   |
|              Vector3        *q2*, |                                   |
|                                   |                                   |
|                                ou |                                   |
| t Vector3    *intersectionPoint*  |                                   |
|                                   |                                   |
|               )                   |                                   |
|   -------------------             |                                   |
| ------------------------ --- ---- |                                   |
| ---------- ---------------------- |                                   |
+-----------------------------------+-----------------------------------+
:::

::: memdoc
Definition at line [175](_ball_movement_8cs_source.html#l00175){.el} of
file [BallMovement.cs](_ball_movement_8cs_source.html){.el}.
:::
:::

## Field Documentation {#field-documentation .groupheader}

[]{#ab2657ddd68ebf02876c11212145fcfdb}

## [[◆ ](#ab2657ddd68ebf02876c11212145fcfdb)]{.permalink}ball {#ball .memtitle}

::: memitem
::: memproto
  -----------------------------
  Transform BallMovement.ball
  -----------------------------
:::

::: memdoc
Definition at line [14](_ball_movement_8cs_source.html#l00014){.el} of
file [BallMovement.cs](_ball_movement_8cs_source.html){.el}.
:::
:::

[]{#ac6a63f2cbb61ce14dda95621177ee843}

## [[◆ ](#ac6a63f2cbb61ce14dda95621177ee843)]{.permalink}direction {#direction .memtitle}

::: memitem
::: memproto
  --------------------------------
  Vector2 BallMovement.direction
  --------------------------------
:::

::: memdoc
Definition at line [20](_ball_movement_8cs_source.html#l00020){.el} of
file [BallMovement.cs](_ball_movement_8cs_source.html){.el}.
:::
:::

[]{#aa33416010b3040ac39e7b02bfa7aa95a}

## [[◆ ](#aa33416010b3040ac39e7b02bfa7aa95a)]{.permalink}edgeFollow {#edgefollow .memtitle}

::: memitem
::: memproto
  -------------------------------------
  float BallMovement.edgeFollow = 11f
  -------------------------------------
:::

::: memdoc
Definition at line [18](_ball_movement_8cs_source.html#l00018){.el} of
file [BallMovement.cs](_ball_movement_8cs_source.html){.el}.
:::
:::

[]{#a5866f553f594be14a85c88de4fcdf36f}

## [[◆ ](#a5866f553f594be14a85c88de4fcdf36f)]{.permalink}font {#font .memtitle}

::: memitem
::: memproto
  ------------------------
  Font BallMovement.font
  ------------------------
:::

::: memdoc
Definition at line [229](_ball_movement_8cs_source.html#l00229){.el} of
file [BallMovement.cs](_ball_movement_8cs_source.html){.el}.
:::
:::

[]{#afc7bd1ba11daafd6825473d72337f708}

## [[◆ ](#afc7bd1ba11daafd6825473d72337f708)]{.permalink}paddle1 {#paddle1 .memtitle}

::: memitem
::: memproto
  --------------------------------
  Transform BallMovement.paddle1
  --------------------------------
:::

::: memdoc
Definition at line [15](_ball_movement_8cs_source.html#l00015){.el} of
file [BallMovement.cs](_ball_movement_8cs_source.html){.el}.
:::
:::

[]{#ae6fbc952b54fb915ac79385d0a55ecc0}

## [[◆ ](#ae6fbc952b54fb915ac79385d0a55ecc0)]{.permalink}paddle2 {#paddle2 .memtitle}

::: memitem
::: memproto
  --------------------------------
  Transform BallMovement.paddle2
  --------------------------------
:::

::: memdoc
Definition at line [16](_ball_movement_8cs_source.html#l00016){.el} of
file [BallMovement.cs](_ball_movement_8cs_source.html){.el}.
:::
:::

[]{#ae5be514e8f3c1b3af767d5a8627c9277}

## [[◆ ](#ae5be514e8f3c1b3af767d5a8627c9277)]{.permalink}speed {#speed .memtitle}

::: memitem
::: memproto
  -------------------------------
  float BallMovement.speed = 5f
  -------------------------------
:::

::: memdoc
Definition at line [19](_ball_movement_8cs_source.html#l00019){.el} of
file [BallMovement.cs](_ball_movement_8cs_source.html){.el}.
:::
:::

------------------------------------------------------------------------

The documentation for this class was generated from the following file:

-   C:/Users/dalakgames/Desktop/FurkanIntern/Internship/Pong
    Staj/Assets/Scripts/[BallMovement.cs](_ball_movement_8cs_source.html){.el}
:::

------------------------------------------------------------------------

[Generated by [![doxygen](doxygen.svg){.footer width="104"
height="31"}](https://www.doxygen.org/index.html) 1.9.8]{.small}
