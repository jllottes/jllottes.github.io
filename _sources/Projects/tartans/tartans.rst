
Tartans
=======

.. rubric:: due: Saturday, April 8, 11:59PM


Tartan is a traditional Scottish fabric pattern consisting of
intersecting horizontal and vertical stripes in various colors.
Tartans are a part of the Scottish highland dress.

 .. figure:: Campbell_of_Breadalbane.png
    :width: 350px
    :align: center

    *A lithograph of a member of the Scottish Highland clan of Campbell dressed
    in the Campbell tartan.*

The `Scottish Register of Tartans <https://www.tartanregister.gov.uk/index>`_
lists thousands of tartan designs that were created for use by various clans,
localities, organizations etc.

Making a tartan
---------------

Vertical and horizontal stripes of a tartan have the same pattern:

 .. image:: warp_weft.png
       :width: 300px
       :align: center

In order to combine these pictures into an image of a tartan we can use
a checkerboard that alternates between showing vertical and horizontal stripes.
In the image below vertical stripes were given slightly darker colors to show
this pattern more clearly:

 .. image:: campbell_sample1.png
       :width: 250px
       :align: center

The resulting image will look as follows:

 .. image:: campbell_sample2.png
       :width: 250px
       :align: center

A more realistic image of a tartan can be obtained by modifying the way in which
vertical and horizontal stripes are combined. Instead of using the checkerboard
pattern, each column of pixels shows two pixels of vertical stripes, then
two pixels of horizontal stripes and so on. In each subsequent column this pattern
gets shifted down by one pixel:

 .. image:: campbell_sample3.png
       :width: 250px
       :align: center

This method was used to produce the following picture:

 .. image:: campbell_sample4.png
       :width: 250px
       :align: center



Recipe for a tartan
-------------------

To specify the design of a tartan it suffices to give widths and colors
of its vertical stripes. Since horizontal stripes have the same pattern as the
vertical ones, there is no need to describe them separately. For example, the pattern
of stripes of the Campbell tartan can be described as follows:

B14 K6 B6 K6 B6 K32 OG32 K6 OG32 K32 B32 K6 B6 K6 B32 K32 OG32 K6 OG32 K32 B6 K6 B6 K6 B28

The letter codes B, K, OG indicate different stripe colors, and the number following
each letter code is the width of the stripe. In the production of
tartan fabrics this number gives the number of threads in the stripe. In computer
generated images of tartans we can take it to be the width of the stripe in pixels or some
other units. The pattern will repeat to fill an image of an arbitrary size.

To complete the description of a tartan one needs to specify what color each letter
code stands for. This can be done e.g. by giving RGB coordinates of each color:

B : [52, 80, 100],   K : [16, 16, 16],   OG : [92, 100, 40]


Project
-------

The table below lists several tartan patterns. Find the tartan assigned
to you and write Python code that produces an image of this tartan. Dimensions of
the image must be 500x500 threads, with pattern repeating as many times as needed
to fill the whole image.


**Note.**  This is a programming project. Your project report does not need to
include narrative, beyond comments explaining how your code works. The project will
be graded according to the following rubrics:

* Reproduction of the assigned tartan: 70%
* Report organization and code documentation: 30%


+---------------------------+------------------------------------------------------------------------+
| Tartan                    | Description                                                            |
+===========================+========================================================================+
| .. image:: frankadl.png   | | **Adler, Noah**                                                      |
|    :width:  150px         | | R4 K2 R56 K48 R2 K12 R2 K48 R56 K2 R4                                |
|                           |                                                                        |
|                           | | R : [200, 0, 0]                                                      |
|                           | | K : [16, 16, 16]                                                     |
+---------------------------+------------------------------------------------------------------------+
| .. image:: calebaye.png   | | **Ayers, Caleb**                                                     |
|    :width:  150px         | | B2 K8 B8 G18 K4 G18 B8 K8 B2                                         |
|                           |                                                                        |
|                           | | B : [44, 44, 128]                                                    |
|                           | | K : [16, 16, 16]                                                     |
|                           | | G : [0, 104, 24]                                                     |
+---------------------------+------------------------------------------------------------------------+
| .. image:: sacapozz.png   | | **Capozzi, Skyler**                                                  |
|    :width:  150px         | | T4 W44 T40 LT6 T6 LT6 T6 LT48 T6 LT6 T6 LT6 T40 W44 T4               |
|                           |                                                                        |
|                           | | T : [96, 64, 0]                                                      |
|                           | | W : [224, 224, 224]                                                  |
|                           | | LT : [160, 136, 88]                                                  |
+---------------------------+------------------------------------------------------------------------+
| .. image:: nacaussi.png   | | **Caussin, Natalie**                                                 |
|    :width:  150px         | | N2 T4 N30 T4 W20 LT30 T4 LT4 T4 LT30 W20 T4 N30 T4 N2                |
|                           |                                                                        |
|                           | | W : [224, 224, 224]                                                  |
|                           | | T : [96, 64, 0]                                                      |
|                           | | LT : [160, 136, 88]                                                  |
|                           | | N : [136, 136, 136]                                                  |
+---------------------------+------------------------------------------------------------------------+
| .. image:: pjcorbel.png   | | **Corbelli, Pierce**                                                 |
|    :width:  150px         | | WY5 DY64 AK64 DY10 AK64 DY64 WY5                                     |
|                           |                                                                        |
|                           | | WY : [224, 224, 224]                                                 |
|                           | | AK : [28, 28, 28]                                                    |
|                           | | DY : [232, 192, 0]                                                   |
+---------------------------+------------------------------------------------------------------------+
| .. image:: tjdrozdo.png   | | **Drozdowski, Tyler**                                                |
|    :width:  150px         | | C128 B36 C4 B6 C4 B6 C28 L16 C4 L8 C4 L8 C4 L16 C28 B6 C4 B6 C4 B36  |
|                           |                                                                        |
|                           | | L : [40, 136, 196]                                                   |
|                           | | B : [32, 32, 96]                                                     |
|                           | | C : [160, 0, 72]                                                     |
+---------------------------+------------------------------------------------------------------------+
| .. image:: hehr.png       | | **Hehr, Keith**                                                      |
|    :width:  150px         | | XR8 A6 DY52 DB8 DY4 DB10 XR6 DB18 DY10 DB18 XR6 DB10 DY4 DB8 DY52 A6 |
|                           |                                                                        |
|                           | | DY : [232, 192, 0]                                                   |
|                           | | XR : [200, 0, 0]                                                     |
|                           | | DB : [32, 32, 96]                                                    |
|                           | | A : [92, 140, 168]                                                   |
+---------------------------+------------------------------------------------------------------------+
| .. image:: amhemmer.png   | | **Hemmerling, Ashley**                                               |
|    :width:  150px         | | K5 R60 K28 Y2 K28 R10 K28 Y2 K28 R60 K5                              |
|                           |                                                                        |
|                           | | R : [220, 0, 0]                                                      |
|                           | | Y : [232, 192, 0]                                                    |
|                           | | K : [16, 16, 16]                                                     |
+---------------------------+------------------------------------------------------------------------+
| .. image:: bmhill3.png    | | **Hill, Breanna**                                                    |
|    :width:  150px         | | K8 W8 K64 W64 K8 W64 K64 W8 K8                                       |
|                           |                                                                        |
|                           | | W : [224, 224, 224]                                                  |
|                           | | K : [16, 16, 16]                                                     |
+---------------------------+------------------------------------------------------------------------+
| .. image:: hopejohn.png   | | **Johnson, Hope**                                                    |
|    :width:  150px         | | YT44 DR6 YT6 DR6 YT6 DR6 YT6 DR6 YT44 FSB3 YT3 G3 YT3 LN3            |
|                           |                                                                        |
|                           | | DR : [136, 0, 0]                                                     |
|                           | | LN : [192, 192, 192]                                                 |
|                           | | YT : [216, 176, 0]                                                   |
|                           | | FSB : [36, 116, 232]                                                 |
|                           | | G : [0, 104, 24]                                                     |
+---------------------------+------------------------------------------------------------------------+
| .. image:: wasifkha.png   | | **Khan, Wasif**                                                      |
|    :width:  150px         | | K2 R54 G8 R4 G8 R8 G18 W2 G18 R16 G18 W2 G18 R8 G8 R4 G8 R54 K2      |
|                           |                                                                        |
|                           | | G : [0, 104, 24]                                                     |
|                           | | R : [220, 0, 0]                                                      |
|                           | | W : [224, 224, 224]                                                  |
|                           | | K : [16, 16, 16]                                                     |
+---------------------------+------------------------------------------------------------------------+
| .. image:: wli3539.png    | | **Li, Wei**                                                          |
|    :width:  150px         | | R6 K6 LSB14 RY52 K52 WW10 K52 RY52 LSB14 K6                          |
|                           |                                                                        |
|                           | | WW : [252, 252, 252]                                                 |
|                           | | K : [0, 0, 0]                                                        |
|                           | | LSB : [152, 200, 232]                                                |
|                           | | RY : [188, 140, 0]                                                   |
|                           | | R : [200, 0, 0]                                                      |
+---------------------------+------------------------------------------------------------------------+
| .. image:: mnlopez.png    | | **Lopez, Matthew**                                                   |
|    :width:  150px         | | K6 R2 K60 R56 K2 R2 W6 R2 K2 R56 K60 R2 K6                           |
|                           |                                                                        |
|                           | | K : [16, 16, 16]                                                     |
|                           | | W : [224, 224, 224]                                                  |
|                           | | R : [220, 0, 0]                                                      |
+---------------------------+------------------------------------------------------------------------+
| .. image:: huixinlu.png   | | **Luo, Huixin**                                                      |
|    :width:  150px         | | O3 Y24 O24 WW6 Y4 FG52 O6 Y2 O6 FG52 Y4 WW6 O24 Y24 O3               |
|                           |                                                                        |
|                           | | WW : [248, 248, 248]                                                 |
|                           | | FG : [168, 148, 72]                                                  |
|                           | | O : [248, 132, 16]                                                   |
|                           | | Y : [232, 192, 0]                                                    |
+---------------------------+------------------------------------------------------------------------+
| .. image:: jasonmig.png   | | **Mighty, Jason**                                                    |
|    :width:  150px         | | R4 B24 R8 G24 R48 W8 R48 G24 R8 B24 R4                               |
|                           |                                                                        |
|                           | | G : [0, 104, 24]                                                     |
|                           | | B : [44, 44, 128]                                                    |
|                           | | R : [220, 0, 0]                                                      |
|                           | | W : [224, 224, 224]                                                  |
+---------------------------+------------------------------------------------------------------------+
| .. image:: amm245.png     | | **Miller, Alexandria**                                               |
|    :width:  150px         | | B10 R4 B20 R32 W4 R32 B20 R4 B10                                     |
|                           |                                                                        |
|                           | | B : [44, 44, 128]                                                    |
|                           | | R : [220, 0, 0]                                                      |
|                           | | W : [184, 184, 184]                                                  |
+---------------------------+------------------------------------------------------------------------+
| .. image:: jrmills2.png   | | **Mills, Jack**                                                      |
|    :width:  150px         | | D50 B4 R50 G20 R8 D50 R4 G4 R50 G4 R4 G4 R50 G4 R4 D50 R8 G20 R50 B4 |
|                           |                                                                        |
|                           | | B : [44, 44, 128]                                                    |
|                           | | R : [200, 0, 0]                                                      |
|                           | | D : [32, 32, 96]                                                     |
|                           | | G : [0, 104, 24]                                                     |
+---------------------------+------------------------------------------------------------------------+
| .. image:: jamurall.png   | | **Muralles, Jonathan**                                               |
|    :width:  150px         | | DR3 R6 LN46 R6 DR6 R46 K4 R6 K4 R46 DR6 R6 LN46 R6 DR3               |
|                           |                                                                        |
|                           | | K : [16, 16, 16]                                                     |
|                           | | LN : [192, 192, 192]                                                 |
|                           | | R : [200, 0, 0]                                                      |
|                           | | DR : [136, 0, 0]                                                     |
+---------------------------+------------------------------------------------------------------------+
| .. image:: dallasmu.png   | | **Murawski, Dallas**                                                 |
|    :width:  150px         | | K3 W32 K32 DN4 K4 DN4 K4 DN44 K4 DN4 K4 DN4 K32 W32 K3               |
|                           |                                                                        |
|                           | | DN : [92, 92, 92]                                                    |
|                           | | W : [224, 224, 224]                                                  |
|                           | | K : [16, 16, 16]                                                     |
+---------------------------+------------------------------------------------------------------------+
| .. image:: tjryan5.png    | | **Ryan, Tim**                                                        |
|    :width:  150px         | | B4 LB8 B20 LB20 W4 LB20 B10 LB20 W4 LB20 B20 LB8 B4                  |
|                           |                                                                        |
|                           | | LB : [40, 136, 196]                                                  |
|                           | | B : [44, 44, 128]                                                    |
|                           | | W : [224, 224, 224]                                                  |
+---------------------------+------------------------------------------------------------------------+
| .. image:: giacomos.png   | | **Scilla, Giacomo**                                                  |
|    :width:  150px         | | K6 Y4 K42 Y4 K12 Y48 K4 Y12 K4 Y48 K12 Y4 K42 Y4 K6                  |
|                           |                                                                        |
|                           | | Y : [232, 192, 0]                                                    |
|                           | | K : [16, 16, 16]                                                     |
+---------------------------+------------------------------------------------------------------------+
| .. image:: etsmith3.png   | | **Smith, Eric**                                                      |
|    :width:  150px         | | K16 Y4 K32 Y48 R4 Y48 K32 Y4 K16                                     |
|                           |                                                                        |
|                           | | K : [16, 16, 16]                                                     |
|                           | | Y : [216, 176, 0]                                                    |
|                           | | R : [200, 0, 0]                                                      |
+---------------------------+------------------------------------------------------------------------+
| .. image:: tssmith8.png   | | **Smith, Taylor**                                                    |
|    :width:  150px         | | A2 K24 A24 B8 R48 A8 R48 B8 A24 K24 A2                               |
|                           |                                                                        |
|                           | | A : [60, 130, 175]                                                   |
|                           | | B : [44, 64, 132]                                                    |
|                           | | R : [220, 0, 0]                                                      |
|                           | | K : [16, 16, 16]                                                     |
+---------------------------+------------------------------------------------------------------------+
| .. image:: tstrade.png    | | **Strade, Thomas**                                                   |
|    :width:  150px         | | DG56 W8 DB12 LG28 DG8 LG28 DB12 W8 DG56 A8                           |
|                           |                                                                        |
|                           | | W : [224, 224, 224]                                                  |
|                           | | DB : [32, 32, 96]                                                    |
|                           | | A : [92, 140, 168]                                                   |
|                           | | LG : [152, 180, 128]                                                 |
|                           | | DG : [0, 56, 32]                                                     |
+---------------------------+------------------------------------------------------------------------+
| .. image:: vnwalker.png   | | **Walker, Veronica**                                                 |
|    :width:  150px         | | Y2 DG48 DB14 DR52 DB14 DR52 DB14 DG48 Y2                             |
|                           |                                                                        |
|                           | | DB : [32, 32, 96]                                                    |
|                           | | Y : [232, 192, 0]                                                    |
|                           | | DG : [0, 56, 32]                                                     |
|                           | | DR : [136, 0, 0]                                                     |
+---------------------------+------------------------------------------------------------------------+
| .. image:: mvwarsaw.png   | | **Warsaw, Mike**                                                     |
|    :width:  150px         | | DR4 DB12 G30 BL18 DB60 BL18 G12 MY4 G12 BL18 DB60 BL18 G30 DB12      |
|                           |                                                                        |
|                           | | G : [20, 100, 0]                                                     |
|                           | | MY : [200, 140, 0]                                                   |
|                           | | BL : [20, 116, 180]                                                  |
|                           | | DB : [0, 0, 80]                                                      |
|                           | | DR : [140, 0, 0]                                                     |
+---------------------------+------------------------------------------------------------------------+
| .. image:: jiexing.png    | | **Xing, Jie**                                                        |
|    :width:  150px         | | RB8 MY4 RB24 DR4 RB8 DR8 K8 G24 A4 G8 A4 G24 K8 DR8 RB8 DR4 RB24 MY4 |
|                           |                                                                        |
|                           | | A : [92, 140, 168]                                                   |
|                           | | MY : [208, 152, 0]                                                   |
|                           | | DR : [136, 0, 0]                                                     |
|                           | | G : [0, 104, 24]                                                     |
|                           | | RB : [28, 0, 112]                                                    |
|                           | | K : [16, 16, 16]                                                     |
+---------------------------+------------------------------------------------------------------------+
| .. image:: zhuoweix.png   | | **Xu, Zhuowei**                                                      |
|    :width:  150px         | | B3 K4 T32 O50 B12 O50 T32 K4 B3                                      |
|                           |                                                                        |
|                           | | B : [44, 44, 128]                                                    |
|                           | | K : [16, 16, 16]                                                     |
|                           | | T : [96, 64, 0]                                                      |
|                           | | O : [216, 124, 0]                                                    |
+---------------------------+------------------------------------------------------------------------+
| .. image:: gaozhou.png    | | **Zhou, Gao**                                                        |
|    :width:  150px         | | R4 G4 R4 K10 NB44 W4 NB44 K10 R4 G4 R4                               |
|                           |                                                                        |
|                           | | G : [0, 104, 24]                                                     |
|                           | | NB : [0, 60, 100]                                                    |
|                           | | R : [200, 0, 0]                                                      |
|                           | | W : [224, 224, 224]                                                  |
|                           | | K : [16, 16, 16]                                                     |
+---------------------------+------------------------------------------------------------------------+
| .. image:: kaixinzo.png   | | **Zou, Kaixin**                                                      |
|    :width:  150px         | | G4 R64 B18 R12 B4 R6 B4 R24 WW6 R24 B4 R6 B4 R12 B18 R64 G4          |
|                           |                                                                        |
|                           | | WW : [252, 252, 252]                                                 |
|                           | | B : [44, 44, 128]                                                    |
|                           | | G : [0, 104, 24]                                                     |
|                           | | R : [200, 0, 0]                                                      |
+---------------------------+------------------------------------------------------------------------+
