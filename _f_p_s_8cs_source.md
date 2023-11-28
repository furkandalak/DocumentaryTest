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
FPS.cs
:::
:::
:::

::: contents
[Go to the documentation of this file.](_f_p_s_8cs.html)

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
[]{#l00004}[ 4]{.lineno}[using ]{.keyword}UnityEngine;
:::

::: {#foldopen00008 .foldopen data-start="{" end="};"}
::: line
[]{#l00008}[ [8](class_f_p_s.html){.line}]{.lineno}[public]{.keyword}
[class ]{.keyword}[FPS](class_f_p_s.html){.code .hl_class} :
MonoBehaviour
:::

::: line
[]{#l00009}[ 9]{.lineno}{
:::

::: line
[]{#l00010}[ 10]{.lineno} [void]{.keywordtype} Update()
:::

::: line
[]{#l00011}[ 11]{.lineno} {
:::

::: line
[]{#l00012}[ 12]{.lineno} [if]{.keywordflow}
(Input.GetKeyDown(KeyCode.Alpha1))
:::

::: line
[]{#l00013}[ 13]{.lineno} {
:::

::: line
[]{#l00014}[ 14]{.lineno} Application.targetFrameRate = 15;
:::

::: line
[]{#l00015}[ 15]{.lineno} }
:::

::: line
[]{#l00016}[ 16]{.lineno} [if]{.keywordflow}
(Input.GetKeyDown(KeyCode.Alpha2))
:::

::: line
[]{#l00017}[ 17]{.lineno} {
:::

::: line
[]{#l00018}[ 18]{.lineno} Application.targetFrameRate = 30;
:::

::: line
[]{#l00019}[ 19]{.lineno} }
:::

::: line
[]{#l00020}[ 20]{.lineno} [if]{.keywordflow}
(Input.GetKeyDown(KeyCode.Alpha3))
:::

::: line
[]{#l00021}[ 21]{.lineno} {
:::

::: line
[]{#l00022}[ 22]{.lineno} Application.targetFrameRate = 60;
:::

::: line
[]{#l00023}[ 23]{.lineno} }
:::

::: line
[]{#l00024}[ 24]{.lineno} [if]{.keywordflow}
(Input.GetKeyDown(KeyCode.Alpha4))
:::

::: line
[]{#l00025}[ 25]{.lineno} {
:::

::: line
[]{#l00026}[ 26]{.lineno} Application.targetFrameRate = 120;
:::

::: line
[]{#l00027}[ 27]{.lineno} }
:::

::: line
[]{#l00028}[ 28]{.lineno} }
:::

::: line
[]{#l00029}[ 29]{.lineno}
:::

::: line
[]{#l00030}[ 30]{.lineno}
:::

::: line
[]{#l00031}[ 31]{.lineno}}
:::
:::

::: line
[]{#l00032}[ 32]{.lineno}
:::

::: {#foldopen00042 .foldopen data-start="{" end="};"}
::: line
[]{#l00042}[ [42](class_math.html){.line}]{.lineno}[public]{.keyword}
[class ]{.keyword}[Math](class_math.html){.code .hl_class} :
MonoBehaviour
:::

::: line
[]{#l00043}[ 43]{.lineno}{
:::

::: {#foldopen00047 .foldopen data-start="{" end="}"}
::: line
[]{#l00047}[
[47](class_math.html#a7c871f51dfc34ae986cd577e732183ae){.line}]{.lineno}
[public]{.keyword} [int]{.keywordtype}
[AddTwoIntegers](class_math.html#a7c871f51dfc34ae986cd577e732183ae){.code
.hl_function}([int]{.keywordtype} a, [int]{.keywordtype} b)
:::

::: line
[]{#l00048}[ 48]{.lineno} {
:::

::: line
[]{#l00049}[ 49]{.lineno} [int]{.keywordtype} add = 0;
:::

::: line
[]{#l00050}[ 50]{.lineno} add = a + b;
:::

::: line
[]{#l00051}[ 51]{.lineno} [return]{.keywordflow} add;
:::

::: line
[]{#l00052}[ 52]{.lineno} }
:::
:::

::: line
[]{#l00053}[ 53]{.lineno}
:::

::: {#foldopen00057 .foldopen data-start="{" end="}"}
::: line
[]{#l00057}[
[57](class_math.html#a62b011a90e95facd6ee112bd171bccc0){.line}]{.lineno}
[public]{.keyword} [int]{.keywordtype}
[SubTwoIntegers](class_math.html#a62b011a90e95facd6ee112bd171bccc0){.code
.hl_function}([int]{.keywordtype} a, [int]{.keywordtype} b)
:::

::: line
[]{#l00058}[ 58]{.lineno} {
:::

::: line
[]{#l00059}[ 59]{.lineno} [int]{.keywordtype} sub = 0;
:::

::: line
[]{#l00060}[ 60]{.lineno} sub = a - b;
:::

::: line
[]{#l00061}[ 61]{.lineno} [return]{.keywordflow} sub;
:::

::: line
[]{#l00062}[ 62]{.lineno} }
:::
:::

::: line
[]{#l00063}[ 63]{.lineno}
:::

::: {#foldopen00070 .foldopen data-start="{" end="}"}
::: line
[]{#l00070}[
[70](class_math.html#a56e40797c0abd636af35283f35748f59){.line}]{.lineno}
[public]{.keyword} [int]{.keywordtype}
[MultiTwoIntegers](class_math.html#a56e40797c0abd636af35283f35748f59){.code
.hl_function}([int]{.keywordtype} a, [int]{.keywordtype} b)
:::

::: line
[]{#l00071}[ 71]{.lineno} {
:::

::: line
[]{#l00072}[ 72]{.lineno} [int]{.keywordtype} mul = 0;
:::

::: line
[]{#l00073}[ 73]{.lineno} [for]{.keywordflow} ([int]{.keywordtype} i =
0; i \< a; a++)
:::

::: line
[]{#l00074}[ 74]{.lineno} {
:::

::: line
[]{#l00075}[ 75]{.lineno}
[AddTwoIntegers](class_math.html#a7c871f51dfc34ae986cd577e732183ae){.code
.hl_function}(mul, b);
:::

::: line
[]{#l00076}[ 76]{.lineno} }
:::

::: line
[]{#l00077}[ 77]{.lineno} [return]{.keywordflow} mul;
:::

::: line
[]{#l00078}[ 78]{.lineno} }
:::
:::

::: line
[]{#l00079}[ 79]{.lineno}
:::

::: {#foldopen00080 .foldopen data-start="{" end="}"}
::: line
[]{#l00080}[
[80](class_math.html#a5f89b21d11567863daecedba91addc11){.line}]{.lineno}
[public]{.keyword} [void]{.keywordtype}
[Update](class_math.html#a5f89b21d11567863daecedba91addc11){.code
.hl_function}()
:::

::: line
[]{#l00081}[ 81]{.lineno} {
:::

::: line
[]{#l00083}[ 83]{.lineno} [int]{.keywordtype} c =
[AddTwoIntegers](class_math.html#a7c871f51dfc34ae986cd577e732183ae){.code
.hl_function}(3, 5);
:::

::: line
[]{#l00084}[ 84]{.lineno} }
:::
:::

::: line
[]{#l00085}[ 85]{.lineno}}
:::
:::

::: line
[]{#l00086}[ 86]{.lineno}
:::

::: line
[]{#l00087}[ 87]{.lineno}
:::

::: line
[]{#l00088}[ 88]{.lineno}
:::

::: {#aclass_f_p_s_html .ttc}
::: ttname
[FPS](class_f_p_s.html)
:::

::: ttdoc
This Class performs FPS changes.
:::

::: ttdef
**Definition** [FPS.cs:9](_f_p_s_8cs_source.html#l00008)
:::
:::

::: {#aclass_math_html .ttc}
::: ttname
[Math](class_math.html)
:::

::: ttdoc
Makes some calculating.
:::

::: ttdef
**Definition** [FPS.cs:43](_f_p_s_8cs_source.html#l00042)
:::
:::

::: {#aclass_math_html_a56e40797c0abd636af35283f35748f59 .ttc}
::: ttname
[Math.MultiTwoIntegers](class_math.html#a56e40797c0abd636af35283f35748f59)
:::

::: ttdeci
int MultiTwoIntegers(int a, int b)
:::

::: ttdoc
Multiplies two Integers.
:::

::: ttdef
**Definition** [FPS.cs:70](_f_p_s_8cs_source.html#l00070)
:::
:::

::: {#aclass_math_html_a5f89b21d11567863daecedba91addc11 .ttc}
::: ttname
[Math.Update](class_math.html#a5f89b21d11567863daecedba91addc11)
:::

::: ttdeci
void Update()
:::

::: ttdef
**Definition** [FPS.cs:80](_f_p_s_8cs_source.html#l00080)
:::
:::

::: {#aclass_math_html_a62b011a90e95facd6ee112bd171bccc0 .ttc}
::: ttname
[Math.SubTwoIntegers](class_math.html#a62b011a90e95facd6ee112bd171bccc0)
:::

::: ttdeci
int SubTwoIntegers(int a, int b)
:::

::: ttdoc
Substracts two Integers.
:::

::: ttdef
**Definition** [FPS.cs:57](_f_p_s_8cs_source.html#l00057)
:::
:::

::: {#aclass_math_html_a7c871f51dfc34ae986cd577e732183ae .ttc}
::: ttname
[Math.AddTwoIntegers](class_math.html#a7c871f51dfc34ae986cd577e732183ae)
:::

::: ttdeci
int AddTwoIntegers(int a, int b)
:::

::: ttdoc
Adds two Integers.
:::

::: ttdef
**Definition** [FPS.cs:47](_f_p_s_8cs_source.html#l00047)
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
-   [FPS.cs](_f_p_s_8cs.html){.el}
-   Generated by [![doxygen](doxygen.svg){.footer width="104"
    height="31"}](https://www.doxygen.org/index.html) 1.9.8
:::
