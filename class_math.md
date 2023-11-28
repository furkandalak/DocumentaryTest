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
[Public Member Functions](#pub-methods)
:::

::: headertitle
::: title
Math Class Reference
:::
:::
:::

::: contents
Makes some calculating. [More\...](class_math.html#details)

+-----------------------------------+-----------------------------------+
| ## []{#pub-method                 |                                   |
| s} Public Member Functions {#publ |                                   |
| ic-member-functions .groupheader} |                                   |
+-----------------------------------+-----------------------------------+
| int                               | [AddTw                            |
|                                   | oIntegers](class_math.html#a7c871 |
|                                   | f51dfc34ae986cd577e732183ae){.el} |
|                                   | (int a, int b)                    |
+-----------------------------------+-----------------------------------+
|                                   | Adds two Integers.\               |
+-----------------------------------+-----------------------------------+
|                                   |                                   |
+-----------------------------------+-----------------------------------+
| int                               | [SubTw                            |
|                                   | oIntegers](class_math.html#a62b01 |
|                                   | 1a90e95facd6ee112bd171bccc0){.el} |
|                                   | (int a, int b)                    |
+-----------------------------------+-----------------------------------+
|                                   | Substracts two Integers.\         |
+-----------------------------------+-----------------------------------+
|                                   |                                   |
+-----------------------------------+-----------------------------------+
| int                               | [MultiTw                          |
|                                   | oIntegers](class_math.html#a56e40 |
|                                   | 797c0abd636af35283f35748f59){.el} |
|                                   | (int a, int b)                    |
+-----------------------------------+-----------------------------------+
|                                   | Multiplies two Integers.\         |
+-----------------------------------+-----------------------------------+
|                                   |                                   |
+-----------------------------------+-----------------------------------+
| void                              | [Update](class_math.html#a5f89b   |
|                                   | 21d11567863daecedba91addc11){.el} |
|                                   | ()                                |
+-----------------------------------+-----------------------------------+
|                                   |                                   |
+-----------------------------------+-----------------------------------+

[]{#details}

## Detailed Description {#detailed-description .groupheader}

::: textblock
Makes some calculating.

# []{#name .anchor} \"NAME\"

Makes calculations for some basic
*[Math](class_math.html "Makes some calculating."){.el}* stuff.

Note
:   Check Examples from [here](_math-example.html){.el}

```{=html}
<!-- -->
```

See also
:   [Extra](_extra-example.html){.el}

Definition at line [42](_f_p_s_8cs_source.html#l00042){.el} of file
[FPS.cs](_f_p_s_8cs_source.html){.el}.
:::

## Member Function Documentation {#member-function-documentation .groupheader}

[]{#a7c871f51dfc34ae986cd577e732183ae}

## [[◆ ](#a7c871f51dfc34ae986cd577e732183ae)]{.permalink}AddTwoIntegers() {#addtwointegers .memtitle}

::: memitem
::: memproto
+-----------------------------------+-----------------------------------+
|   ----------                      | [[inline]{.mlabel}]{.mlabels}     |
| --------------- --- ------ ------ |                                   |
|   int Math                        |                                   |
| .AddTwoIntegers   (   int    *a*, |                                   |
|                                   |                                   |
|                       int    *b*  |                                   |
|                                   |                                   |
|                       )           |                                   |
|   ----------                      |                                   |
| --------------- --- ------ ------ |                                   |
+-----------------------------------+-----------------------------------+
:::

::: memdoc
Adds two Integers.

Parameters

:   --- ------------
      a   an Integer
      b   an Integer
      --- ------------

```{=html}
<!-- -->
```

Returns
:   int (a + b)

Definition at line [47](_f_p_s_8cs_source.html#l00047){.el} of file
[FPS.cs](_f_p_s_8cs_source.html){.el}.
:::
:::

[]{#a56e40797c0abd636af35283f35748f59}

## [[◆ ](#a56e40797c0abd636af35283f35748f59)]{.permalink}MultiTwoIntegers() {#multitwointegers .memtitle}

::: memitem
::: memproto
+-----------------------------------+-----------------------------------+
|   ------------                    | [[inline]{.mlabel}]{.mlabels}     |
| --------------- --- ------ ------ |                                   |
|   int Math.M                      |                                   |
| ultiTwoIntegers   (   int    *a*, |                                   |
|                                   |                                   |
|                       int    *b*  |                                   |
|                                   |                                   |
|                       )           |                                   |
|   ------------                    |                                   |
| --------------- --- ------ ------ |                                   |
+-----------------------------------+-----------------------------------+
:::

::: memdoc
Multiplies two Integers.

Parameters

:   --- ------------
      a   an Integer
      b   an Integer
      --- ------------

```{=html}
<!-- -->
```

Returns
:   int (a \* b)

```{=html}
<!-- -->
```

Note
:   It uses
    [Math.AddTwoIntegers()](class_math.html#a7c871f51dfc34ae986cd577e732183ae "Adds two Integers."){.el}
    with for loop

```{=html}
<!-- -->
```

Attention
:   Not Tested Yet

```{=html}
<!-- -->
```

Warning
:   Do not use **0** as a parameter

Definition at line [70](_f_p_s_8cs_source.html#l00070){.el} of file
[FPS.cs](_f_p_s_8cs_source.html){.el}.
:::
:::

[]{#a62b011a90e95facd6ee112bd171bccc0}

## [[◆ ](#a62b011a90e95facd6ee112bd171bccc0)]{.permalink}SubTwoIntegers() {#subtwointegers .memtitle}

::: memitem
::: memproto
+-----------------------------------+-----------------------------------+
|   ----------                      | [[inline]{.mlabel}]{.mlabels}     |
| --------------- --- ------ ------ |                                   |
|   int Math                        |                                   |
| .SubTwoIntegers   (   int    *a*, |                                   |
|                                   |                                   |
|                       int    *b*  |                                   |
|                                   |                                   |
|                       )           |                                   |
|   ----------                      |                                   |
| --------------- --- ------ ------ |                                   |
+-----------------------------------+-----------------------------------+
:::

::: memdoc
Substracts two Integers.

Parameters

:   --- ------------
      a   an Integer
      b   an Integer
      --- ------------

```{=html}
<!-- -->
```

Returns
:   int (a - b)

Definition at line [57](_f_p_s_8cs_source.html#l00057){.el} of file
[FPS.cs](_f_p_s_8cs_source.html){.el}.
:::
:::

[]{#a5f89b21d11567863daecedba91addc11}

## [[◆ ](#a5f89b21d11567863daecedba91addc11)]{.permalink}Update() {#update .memtitle}

::: memitem
::: memproto
+-----------------------------------+-----------------------------------+
|                                   | [[inline]{.mlabel}]{.mlabels}     |
|  ------------------ --- -- --- -- |                                   |
|   void Math.Update   (      )     |                                   |
|                                   |                                   |
|  ------------------ --- -- --- -- |                                   |
+-----------------------------------+-----------------------------------+
:::

::: memdoc
Definition at line [80](_f_p_s_8cs_source.html#l00080){.el} of file
[FPS.cs](_f_p_s_8cs_source.html){.el}.
:::
:::

------------------------------------------------------------------------

The documentation for this class was generated from the following file:

-   C:/Users/dalakgames/Desktop/FurkanIntern/Internship/Pong
    Staj/Assets/Scripts/[FPS.cs](_f_p_s_8cs_source.html){.el}
:::

------------------------------------------------------------------------

[Generated by [![doxygen](doxygen.svg){.footer width="104"
height="31"}](https://www.doxygen.org/index.html) 1.9.8]{.small}
