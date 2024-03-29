> **Translation note:**
> This article was translated from German. The original German article can be found [here](3D-Design.md).

> Back to [basic learning modules overview](../../translations/EN_Readme.md)

# 3D design
## Contents

1. [Introduction](#introduction)
2. [CAD software](#cad-software)
   - [File formats for CAD models](#file-formats-for-cad-models)
   - [Examples of CAD software](#examples-of-cad-software)
     - [FreeCAD](#freecad)
     - [Autodesk Fusion 360](#autodesk-fusion-360)
3. [3D graphics and modeling programs](#3d-graphics-and-modeling-programs)
   - [Examples of 3D graphics and 3D modeling programs](#examples-of-3d-graphics-and-3d-modeling-programs)
     - [Blender](#blender)
     - [Tinkercad](#tinkercad) 

[License information](#license-information)

[Image references](#image-references)


## Introduction

There are various software that can be used to draw or model digital 3D models. These 3D models can then be used, for example, for 3D printing, laser cutting or CNC milling.

Depending on the application, there are programs with different focuses and functions. CAD software (CAD = Computer Aided Design) is generally used to model components for technical products. On the other hand, there are also 3D graphics programs that have a more artistic focus, e.g. for complex shaped figures that can be used for 3D printing, product design, but also e.g. for 3D animation films.

<p align="center">									
<img height="300" src="images/1_CAD_FreeCAD_Example.png">									
<img height="300" src="images/2_Blender_example.png">																	
</p>									
									
<p align="center">									
<a href="#s1">[1]</a> <i> Assembly in the software FreeCAD - </i>									
<a href="#s2">[2]</a> <i> 3D model in 3D modeling software Blender </i>																	
</p>									

Instead of creating your own 3D models, you can also download finished models from the Internet, edit them if necessary and then print them out with a 3D printer, for example (more on this in the [3D printing basic learning module](../2_1_3D_printing/EN_3D_printing.md)). There are a variety of websites from which you can obtain 3D models or upload your own creations and share them with others (more on this in the [basic learning module on downloading 3D models](../1_3_Using_3D_models_from_the_internet/EN_Using_3D_models_from_the_internet.md)).

Another way to create a 3D model is through 3D scanning. This allows objects, spare parts or even people to be scanned and displayed as a 3D model on the computer. With some post-processing, these models can also be 3D printed (more on this in the [basic learning module on 3D scanning](../1_2_3D_scanning/EN_3D_scanning.md)).

## CAD software

CAD software is usually used in the technical field, e.g. in mechanical engineering, in architecture or electrical engineering - in companies for product development, planning of buildings and similar areas. But CAD programs have also proven themselves for hobby applications, e.g. for designing objects for 3D printing or CNC milling.

If a model designed in CAD is to be manufactured using CNC machines (milling or turning), it must be processed in CAM software (CAM = Computer Aided Manufacturing) in order to define milling diameters, speeds, work processes, etc. (more on this in the [basic learning module for CNC milling](../2_3_CNC_milling/EN_CNC_milling.md)). Many CAD programs have an integrated CAM module, which is referred to as CAD/CAM software.

When creating a 3D model - in CAD one speaks of "modeling" or "designing" - one usually works with so-called geometric and generative modeling.

You usually start by drawing a 2D sketch consisting of points, lines, curves and geometric shapes such as circles or hexagons. With dimensions you can define the sketch elements exactly, e.g. specify the length of lines or circle diameters with millimeter precision. So-called dependencies can be used, for example, to specify that two lines should be parallel or of the same length. The next step is to "pad" this 2D sketch into a 3D object with a specified thickness or rotate it around an axis to create a revolution. Based on this object, further elements can be added, for example by further 2D sketches and padding/rotation, by subtracting parts (e.g. for holes, bores or pockets), by duplicating elements or rounding edges.

<p align="center">
[3] <img height="130" src="images/3_FreeCAD_PartDesign_Pad.png"> <br>
[4] <img height="130" src="images/4_FreeCAD_PartDesign_Revolution.png"> <br>
[5] <img height="130" src="images/5_FreeCAD_PartDesign_Pocket.png">
</p>

<p align="center">
<a href="#s3">[3]</a> <i> 3D padding from a 2D sketch - </i>
<a href="#s4">[4]</a> <i> 3D rotary body (revolution) from 2D sketch - </i>
<a href="#s5">[5]</a> <i> Pocket from 2D sketch </i>
</p>


<p align="center">
<img height="300" src="images/6_FreeCAD_Sketch.png">
<img height="300" src="images/7_FreeCAD_PartDesign_example.png">
</p>

<p align="center">
<a href="#s6">[6]</a> <i> 2D Sketch in FreeCAD - </i>
<a href="#s7">[7]</a> <i> A part created with geometric modeling in FreeCAD </i>
</p>


Many CAD programs also contain functions for creating technical drawings (or engineering drawings). The component is first modeled in 3D and then projected onto a 2D drawing from different perspectives. These views can be arranged on a sheet, provided with dimensions and other information, and printed out. This is helpful for parts that you don't want to make with digital manufacturing methods, but with conventional tools, e.g. cutting and drilling wooden planks or aluminum profiles.

<p align="center">
<img height="400" src="images/8_FreeCAD_Drawing_TechDraw.png">
</p>

<p align="center">
<a href="#s8">[8]</a> <i> Technical drawing (or engineering drawing) in FreeCAD </i>
</p>

Some CAD programs have “parametric design” capabilities. Components are not dimensioned with exact numerical values (e.g. 10 mm), but with parameters (e.g. with "length" or "diameter"). With a parametric model, many different variants of the component can then be generated, for example a screw does not have to be remodeled in every variant, but only once as a parametric model, whereby the parameters "length" and "diameter" are varied, for example, and each screw model is saved as a variant. Parameters can also be linked using formulas (e.g. "length = 2 x diameter + 10 mm").

There are many video tutorials for learning CAD modeling on video portals such as YouTube. Some fab labs also offer workshops. The basics for simple models can be learned relatively quickly, but it takes a lot of training and practice for more complex CAD projects and advanced functions.


### File formats for CAD models

Each software has its own file format for project files, e.g. files in the "FreeCAD" software have the file extension *.FCStd and files in "Autodesk Fusion 360" have the extension *.f3d.
In the CAD area, however, there are numerous different file formats that can be created and opened by different CAD programs.

The STEP file format (*.ste, *.step or *.stp) deserves special mention. STEP stands for "STandard for the Exchange of Product model data" and is standardized in a globally recognized ISO standard. STEP files are therefore well suited as an exchange format between different CAD programs. So if you want to share your CAD file with someone who uses another CAD software, exporting it in STEP format is often a good solution, even if not all information and editing functions are preserved, but at least the file can be used in the other software opened, viewed and analyzed.

If you plan to release your product as open-source hardware, it is advisable to use CAD software that is free and based on open-source software (e.g. FreeCAD or Blender, see below for more) so that as many people as possible are able to open the files, edit and contribute to the project as an improved version.

Another important file format is STL, especially for 3D printing. Virtually any popular CAD or 3D graphics software can export 3D models in STL format so that you can then 3D print them (more on this in the [3D Printing basic learning module](../2_1_3D_printing/EN_3D_printing.md)).


### Examples of CAD software

Here is a selection of some popular CAD programs, most of which can be used free of charge:

#### FreeCAD

As the name suggests, FreeCAD is a so-called "free and open-source software", i.e. the software is absolutely free of charge, including for commercial applications, and its source code is open. This makes FreeCAD a popular software solution in open-source communities, as it guarantees that projects created with FreeCAD can be opened and edited by anyone free of charge, even in the long term (as open-source hardware). In addition, FreeCAD can be modified by anyone or supplemented and improved by extensions (open-source software), which means that there are already numerous bug fixes, additional functions, workbenches and macros programmed by the user community.

FreeCAD contains many different program modules (so-called "workbenches") and functions for 3D modeling, 3D printing, CAM and CNC milling, laser cutting, motion simulation, architecture and much more. A particular strength of FreeCAD is also parametric design, whereby the "Spreadsheet" workbench can be used to create spreadsheets that can be used to control parameters of the CAD model. FreeCAD is not cloud-based, but runs purely locally on the computer (Windows, Mac or Linux).

**Download:** https://www.freecad.org/

**FreeCAD Wiki:** https://wiki.freecad.org/

<p align="center">
<img height="300" src="images/9_FreeCAD_UI.png">
<img height="300" src="images/10_FreeCAD_example.png">
</p>

<p align="center">
<a href="#s9">[9]</a> <i> FreeCAD user interface - </i>
<a href="#s10">[10]</a> <i> Assembly with sketches in FreeCAD </i>
</p>


#### Autodesk Fusion 360

Fusion 360 is a software suite developed by Autodesk for CAD, CAM and other technical applications. Basically, Fusion 360 is a paid program, but it can also be used free of charge under certain conditions and with limited functionality. When registering, you have to state that you will use the program for "personal use". This free "hobby license" must be renewed regularly. As soon as you want to use projects commercially, you are obliged to buy a license. In addition, not all functions are available under the free license. The conditions and functions for free use are subject to change, the latest information can be found on the [Fusion-360 website](https://www.autodesk.de/products/fusion-360/).

Fusion 360 is cloud-based, i.e. you need a connection to the internet and have to log in with your account details the first time you use it. Project files are stored online in an Autodesk cloud, but can also be downloaded locally (e.g. as an f3d file). If there is no internet connection, you can work offline for a while, the files will be synchronized the next time you connect to the internet. However, the first registration must be done online.

Due to its clear and understandable usability, Fusion 360 is considered a comparatively easy-to-learn CAD software, which makes it a widely used and popular program in maker communities.

**Registration and download for personal use:** https://www.autodesk.de/products/fusion-360/personal

<p align="center">
<img height="300" src="images/11_Autodesk_Fusion_360_example.png">
<img height="300" src="images/12_Autodesk_Fusion_360_example.png">
</p>

<p align="center">
<a href="#s11">[11]</a> <i> </i>
<a href="#s12">[12]</a> <i> Autodesk Fusion 360: User Interface</i>
</p>



## 3D graphics and modeling programs

In contrast to CAD programs, which are used more for technical product development, 3D graphics programs are aimed more at artistic or design-related applications, e.g. for creating figures, vases, jars or other complex shapes.

So-called sculpting tools are often used here, with which 3D objects can be precisely deformed, similar to pottery with clay. The millimeter-precise dimensioning and construction of rather angular parts, such as technical components in CAD programs, is less important than the freedom in the shape and design of the 3D object.

Other functions of 3D graphics programs are e.g. texturing, animation (for animated films or video games) and rendering, e.g. for staging an object or product in a certain environment and exposure in a so-called scene. Many 3D graphics programs can export the models as an STL file, with which they can be 3D printed.

<p align="center">
<img height="250" src="images/13_Blender_sculpting_example.png">
<img height="250" src="images/14_Blender_rendering_example.png">
</p>

<p align="center">
<a href="#s13">[13]</a> <i> Sculpting in the software Blender - </i>
<a href="#s14">[14]</a> <i> Rendering of cooking pots in Blender </i>
</p>



### Examples of 3D graphics and 3D modeling programs

Here is a selection of some popular 3D graphics and 3D modeling programs that are free to use:

#### Blender

Blender is a 3D graphics suite released as "Free and open-source software". The software suite includes functions for modeling, texturing and animation. Blender is a program that is very popular in the professional as well as in the hobby area, is considered to be particularly sophisticated open-source software and the basics are relatively easy to learn.

**Download:** https://www.blender.org/

<p align="center">
<img height="300" src="images/15_Blender_UI.png">
<img height="300" src="images/16_Blender_sculpting_example.png">
</p>

<p align="center">
<a href="#s15">[15]</a> <i> Blender user interface - </i>
<a href="#s16">[16]</a> <i> Sculpting in Blender </i>
</p>



#### Tinkercad

Tinkercad is a free, browser-based web app that can be used for 3D design, but also for electronics and programming. It is relatively easy to use and is primarily aimed at children, young people and use in school lessons. But Tinkercad is also interesting for adults who don't want to go through the trouble of learning a complex CAD or 3D graphic design program.

Although Tinkercad appears to have "CAD" in its name, calling Tinkercad a CAD program would be a bit inappropriate. Although Tinkercad is good for creating simple 3D models, the system quickly reaches its limits as soon as you want to develop more complex technical products or 3D figures. The software is more geared towards simple operation than functionality, which is why the modeling process differs fundamentally from common CAD programs. STL export for 3D printing is possible with Tinkercad.

Like Fusion 360, Tinkercad belongs to the Autodesk company and requires the registration of a (free) user account. However, no software needs to be downloaded or installed, the application runs directly in the browser.

**Registration and application:** https://www.tinkercad.com/

<p align="center">
<img height="250" src="images/17_Tinkercad_UI_Browser.png">
<img height="250" src="images/18_Tinkercad_example.png">
</p>

<p align="center">
<a href="#s17">[17]</a> <i> Tinkercad user interface (in browser) - </i>
<a href="#s18">[18]</a> <i> 3D design of a caliper in Tinkercad </i>
</p>

# License information

**Author:** Oskar Lidtke, https://github.com/orcular-org/

<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/88x31.png" /></a><br />Except where otherwise noted, this work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">Creative Commons Attribution-ShareAlike 4.0 International License (CC BY-SA 4.0)</a>.

See best practices for [attribution](https://wiki.creativecommons.org/wiki/Best_practices_for_attribution) and [marking your own work](https://wiki.creativecommons.org/wiki/Marking_your_work_with_a_CC_license) with a CC license.

For attribution and licenses of the images used, see the section below.


# Image references

<a name="s1"></a>
**[1]** Gsuter.png (cropped) - **Image license:** [CC BY 3.0](https://creativecommons.org/licenses/by/3.0/) - **Source:** https://wiki.freecad.org/File:Gsuter.png

<a name="s2"></a>
**[2]** 3D Viewport, a Blender 2.93.4.png (cropped) - **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - **Source:** https://commons.wikimedia.org/wiki/File:3D_Viewport,_a_Blender_2.93.4.png

<a name="s3"></a>
**[3]** PartDesign Pad example (adapted) - **Image license:** [CC BY 3.0](https://creativecommons.org/licenses/by/3.0/) - **Source:** https://wiki.freecad.org/File:PartDesign_Pad_example.svg

<a name="s4"></a>
**[4]** PartDesign Revolution example (adapted) - **Image license:** [CC BY 3.0](https://creativecommons.org/licenses/by/3.0/) - **Source:** https://wiki.freecad.org/File:PartDesign_Revolution_example.svg

<a name="s5"></a>
**[5]** PartDesign Pocket example (adapted) - **Image license:** [CC BY 3.0](https://creativecommons.org/licenses/by/3.0/) - **Source:** https://wiki.freecad.org/File:PartDesign_Pocket_example.svg

<a name="s6"></a>
**[6]** GGTuto1 4 - **Image license:** [CC BY 3.0](https://creativecommons.org/licenses/by/3.0/) - **Source:** https://wiki.freecad.org/File:GGTuto1_4.PNG

<a name="s7"></a>
**[7]** FreeCAD-20.1 (cropped) - **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - **Source:** https://commons.wikimedia.org/wiki/File:FreeCAD-20.1.png

<a name="s8"></a>
**[8]** TechDraw Workbench Example - **Image license:** [CC BY 3.0](https://creativecommons.org/licenses/by/3.0/) - **Source:** https://wiki.freecad.org/File:TechDraw_Workbench_Example.png

<a name="s9"></a>
**[9]** Asm3 1 relnotes 0.20 - **Image license:** [CC BY 3.0](https://creativecommons.org/licenses/by/3.0/) - **Source:** https://wiki.freecad.org/File:Asm3_1_relnotes_0.20.jpg

<a name="s10"></a>
**[10]** screenshot-07.jpg (cropped) - **Image license:** [CC BY 3.0](https://creativecommons.org/licenses/by/3.0/) - **Source:** https://www.freecad.org/ (home page) [License info for freecad.org](https://wiki.freecad.org/Licence)

<a name="s11"></a>
**[11]** CAM Fusion 360 - **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - **Source:** https://commons.wikimedia.org/wiki/File:CAM_Fusion_360.png

<a name="s12"></a>
**[12]** 3D Design by fusion 360 - **Image license:** [CC BY-SA 2.0](https://creativecommons.org/licenses/by-sa/2.0/) - **Source:** https://www.flickr.com/photos/kenming_wang/32276624594

<a name="s13"></a>
**[13]** sculpt01.jpg - **Image license:** [CC BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/) - **Source:** https://www.blender.org/features/sculpting/ (Attribution: Blender Foundation – www.blender.org - [License info for blender.org](https://www.blender.org/about/website/) )

<a name="s14"></a>
**[14]** Kochtöpfe erstellt und gerendert in Blender-Cycles - **Image license:** [CC BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/deed.de) - **Source:** https://de.wikipedia.org/wiki/Datei:Kocht%C3%B6pfe_in_Blender-Cycles_gerendert.png

<a name="s15"></a>
**[15]** Sculpting Mode Example - **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - **Source:** https://docs.blender.org/manual/en/latest/sculpt_paint/sculpting/introduction/general.html#id

<a name="s16"></a>
**[16]** sculpt-paint_sculpt_multires_example.png (cropped) - **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - **Source:** https://docs.blender.org/manual/en/latest/sculpt_paint/sculpting/introduction/adaptive.html#multiresolution

<a name="s17"></a>
**[17]** Practice 3 D printing - **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - **Source:** https://commons.wikimedia.org/wiki/File:Windmill_3_D_printing.png

<a name="s18"></a>
**[18]** Caliper, drawn with Tinkercad - **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - **Source:** https://en.wikipedia.org/wiki/File:Schuifmaat_bottom_mechaniek.png
