# Tiny Traffic Cone

A snap-together, 1/10 scale model of a traffic cone made in FreeCAD v1.

The cone model is 28" cone with 6" and 4" reflective bands.

Spec source: https://www.cabletiesandmore.com/jbc-safety-white-traffic-cones

See FreeCAD file 'parameters' sheet for fit dimensions:
- 'fit' - cone/band fit
- 'base fit' - cone/base fit
- 'slide fit' - base outer / slide inner fit

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
