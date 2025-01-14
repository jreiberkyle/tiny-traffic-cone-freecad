# Tiny Traffic Cone

A snap-together, 1/10 scale model of a traffic cone made in FreeCAD v1.

The printed cone is approximately 71mm tall, 25mm x 25mm wide, and weighs 4g.

The cone reference model is the 28" traffic cone with 6" and 4" reflective bands.

Spec source: https://www.cabletiesandmore.com/jbc-safety-white-traffic-cones

With variations between printers and filaments, the fit parameters may need to be customized. To
customize fit, see the FreeCAD file 'parameters' sheet for fit dimensions:
- 'fit' - cone/band fit
- 'base fit' - cone/base fit
- 'slide fit' - base outer / slide inner fit

<img src=".github/images/cones_sm.jpeg" width="400"/>

## Status

As of version 1.0.0, the Cone and Bands part of the design is satisfactory and are not expected
to change. Design effort will shift to varieties of bases. Currently, there is a stacking base
that is excellent for forming a stack of cones (which stick together if pressed, try it!). There
are dreams of making a magnetic base and a weighted base.

The FreeCAD file is the work of someone who is new to the software, so probably rough quality. Many
of the parameters can be changed using the 'parameters' sheet in the file.

## Context

The traffic cone is a powerful symbol. It represents boundaries, safety, and caution.
In the chaotic fullness of life, may we all have access to these protections.
In the porousness of that which transcends the bounds of life, may we all be concious
and intentional about the ways we percieve and actualize separation.

The values that go into this design are:
1. Excellence in design
1. Minimize waste
1. Face a challenge

The goals of this design are:
1. Scaled model that complies to regulations
1. Sized to hold in the hand
1. Minimal filament usage
1. Break into components to allow iterating on parts with minimal time/filament waste for testing
1. Combine parts in a way that allows separating them again
1. Use FreeCAD to learn the software

## Outcomes

Parts of the design that I love are:
1. It utilizes vase mode (or mock vase mode) to make a strong print with a single wall. 
1. The bands snap onto the cone with a satisfying click. 
1. When stacked, the cones 'grab onto' each other when pressed together. This appears to be 
caused by the layer lines 'locking' together.
1. The slide base holds everything together quite well after sliding together. It has withstood much handling.

Findings:
- The cone base needs to be about 4 layers of solid infill to make a robust joint with the cone.
- To achieve a similar snap on the upper and lower bands, the length of the tabs along the polar angle has
to be smaller in the lower band - this is due to the radius being larger for the lower band.
There is an equation for this, I just used intuition after testing with the same polar angle.
- Using vase mode (or mock vase mode) creates some complexity in printing but allows 
for easier modeling - there is no need to model the inner part of the cone (which is complex!) or bands.


## Print Instructions

All models are printed using the following settings:
* 0.2 mm layer height
* 0.4 mm nozzle
* 0.45 mm width

### Bands

Load 'tiny-traffic-cone-BottomBand.step' and 'tiny-traffic-cone-TopBand.step' into the slicer.
Add as many instances as desired.

Enable vase mode. Set bottom solid layers to 0.
Enable 'Complete individual objects' and confirm the sequence of object print works with the
printer configuration (e.g. ensure objects in front are printed first).

These settings are included in 'tiny-traffic-cone-bands.3mf'.

### Cone

Load 'tiny-traffic-cone-Cone.step' into the slicer.

#### Regular Mode

Mock vase mode with the following settings:
* number of perimeters: 1
* top and bottom solid layers: 0
* infill: 0%.

Add a modifier slab that is 0.8 mm tall and wider/deeper than cone bottom (~35mm).
Position the modifier so that it covers the base of the cone.
In the modifier, override bottom layers to 4.

Add as many instances as desired.

These settings are included in 'tiny-traffic-cone-Cone.3mf'.

#### Vase Mode (untested with latest model) - One model at a time

Enable vase mode. Set bottom solid layers to 4.

These settings are included in 'tiny-traffic-cone-Cone-vasemode.3mf'.

### Base

Load 'tiny-traffic-cone-SlideBaseInner-Stacking.step' and 'tiny-traffic-cone-SlideBaseOuter.step' into the slicer.

Align SlideBaseOuter so that the flat plane is on the bottom, touching the build surface.
Align SlideBaseInner so that the larger plane is on the bottom, touching the build surface.

Set seam position to Random.

These settings are included in 'tiny-traffic-cone-base.3mf'.

## Construction Instructions

Orient the slide base outer part so that the octagonal indent is up. Drop the cone in tip first so that it rests in the octagonal
groove of the base and extends downward. Orient the slide base inner part so that the largest surface is facing the outer part. It
should slide in without much effort.

Use some force to snap the bands onto the cone.
