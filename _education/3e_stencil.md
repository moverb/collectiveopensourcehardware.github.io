---
title: "![icon_stencil](/media_files/steps_stencil.png) <br /> Step 2 - Creating a Stencil"
permalink: /education/reproduction_stencil/
---

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:5;border-color:#416960;border-width:2px; border-style:solid;}
.tg td{font-family:Arial, sans-serif;font-size:16px;padding:2px 10px;border-style:solid;border-width:0px;overflow:hidden;word-break:normal;border-color:#bbb;color:#594F4F;}
.tg .tg-rmb8{font-weight:bold;vertical-align:top; text-align:right;}
.tg .tg-rmb9{vertical-align:top}
.tg .tg-yw4l{font-weight:bold;vertical-align:top; text-align:right;}
.tg .tg-yw42{vertical-align:top}
</style>

<table class="tg">
  <tr>
    <td class="tg-yw4l">Material</td>
    <td class="tg-yw42">Coated paper (eg. glossy magazine, Mylar or other)</td>
  </tr>
  <tr>
    <td class="tg-rmb8">Tools</td>
    <td class="tg-rmb9">Laser cutter, KiCAD</td>
  </tr>
  <tr>
    <td class="tg-yw4l">Needed Skills<br></td>
    <td class="tg-yw42">Basic PC knowledge, handling of laser cutter</td>
  </tr>
  <tr>
    <td class="tg-rmb8">Time</td>
    <td class="tg-rmb9">circa 60 minutes</td>
  </tr>
</table>

<video width="555" height="400" align="center" controls>
  <source src="/media_files/videos/Stencil.mp4" type="video/mp4">
    Your browser does not support the video tag.
</video>

## Starting with Production

The following steps you should do in a fablab where you find the materials and tools like a lasercutter.

Before fitting all the small electronic parts on to the PCB we need to apply solder first. In this tutorial you learn how to create a reusable stencil which is used later to spread solder on to the whole board.

Instead of applying solder manually to every solder joint we use a laser cutter to create a stencil which can be reused if you want to prepare more than one PCB. You fix the stencil on the board so you can see all the solder junctions but nothing else - afterwards you spread solder on the board which is explained in the [next tutorial](/education/reproduction_smt_soldering/).

![fitting the stencil onto the PCB](/media_files/stencil_fit.jpg)

## Preparing the laser cutter

A laser cutter uses a focused high power laser to cut materials or engrave surfaces. Similar to a 3D printer or a CNC machine the laser beam is moved along two axes by a motion controller. There are software tools that generate motion commands from different file formats, in our case we use the open source software [VisiCut](http://hci.rwth-aachen.de/visicut-download) to use the laser cutter *Epilog Zing*.

![Epilog Zing laser cutter](/media_files/epilog_zing.jpg) ![Epilog Zing laser cutter with materials](/media_files/laser_cutter_with_materials.jpg)

The most important parameters to determine for engraving the surface or cutting through the material are:
- the power of the laser beam
- the speed of the beam

Tht depth of the cut in the material rises with the power of the beam and the stopping time. If the parameters are not correct, the beam won't cut through the material or even burn the material. Also note that different materials need different parameters to achieve the desired cut or engrave. Tests showed that coated paper from glossy magazines or a material called *Mylar* are a good choice for laser cutting of the stencil. To find the right parameters for laser cutters you need to perform some test cuts with different power and speed settings. Use the [laser cutter template](/media_files/lasercut_test.svg) to conduct some tests by varying speed and power with a piece of material of your choice. A test scenario could look like this:

1. 10% power, 100% speed
2. 5% power, 100% speed
3. 4% power, 100% speed
4. 4% power, 50% speed

![laser cutting test with different parameters](/media_files/reproduction_3e_test_cuts.png)

In this example the parameter set of test no. 2 was used to laser cut the stencil. In test no. 1 the fine bridges on the left side of the test cut are connected due to too much power. Tests no. 3 and 4 show that the power was not high enough to cut through some spots of the material.

### KiCAD SVG export

The stencil can be created by exporting an image in SVG file format from the KiCAD board file. The process is analog to exporting a gerber file explained [in the PCB production tutorial](pcb_production.md).

<!--
`Hier noch Klick-Video und/oder Beschreibung für SVG export!`
-->

The new file is a vectorized graphic in SVG file format. You can open and modify the file if needed with image processing tools like [Gimp](https://www.gimp.org) or [Inkscape](https) Use the parameter settings obtained from the test cuts and create your stencil. Small spots where the laser didn't cut through the material can be repaired using a knife.

<!--![Finished stencil](/media_files/stencil_finished.jpg)-->
