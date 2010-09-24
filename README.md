Scope
=====

FactoryTiles aims to be a complete but minimal graphicsset for RoboRally®.
Complete means that all possible situations can be displayed with these graphics.
Minimal means that there are no graphics not needed to display the original game.

If you want RoboRally®, include FactoryTiles. If you want zombies, fork FactoryTiles.
This also means, your graphicsengine needs to support semi-transparency and rotation.

Paradigms
=========

* The viewpoint is exactly from above.
* The viewpoint has a finite distance.
* The default direction is north to south.

Buildnotes
==========

The default rendersize is 64 x 64 pixels per tile and current renderings are part ot the distribution.
Other resolutions can be generated by appending them to the make command, if you need other sizes for debugging or production.
For example, use following to generate images for 32x32, 64x64 and 128x128 tilessize.
    $ make .32 .64 .128

Dependencies
------------

* `make` - dependency-driven creation
* `GNU` - basic folder and file operations
* `Inkscape` - renders the SVGs into PNGs
* `markdown` - renders README.md into README.html (optional)

Tilemodel
=========

Each tile on the playing field has one floor, eventually some properties and up to two robots on it.

Floors
------

* abyss - infinitely deep nothing or the brink to it
* belt - conveyor or express belts
* repair - repairzone
* turntable - turns robots

Properties
----------

* checkpoint - marks the route
* laser - damages robots occassionally (rotate as needed)
* laser emitter - emits laser (embedded into walls)
* press - destructs robots occassionally (embedded into walls)
* slide - moves robots occassionally
* wall - keeps robots from crossing it (binary naming is for a reason)

Robots
------

* The eight original Robots

Renderorder
===========

The order from background do foreground is as follows:
floor, checkpoint, slide, laser, wall, laser emitter, robot, press

Status
======

<table>
    <thead>
        <tr>
            <td>Component</td> <td>Status</td> <td>Size</td>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>make framework</td> <td><b>done</b></td> <td></td>
        </tr>
        <tr>
            <td>robot</td> <td>todo</td> <td>8 graphics</td>
        </tr>
        <tr>
            <td>floor/abyss</td> <td><b>done</b></td> <td>20 graphics</td>
        </tr>
        <tr>
            <td>floor/belt</td> <td><b>done</b></td> <td>14 graphics</td>
        </tr>
        <tr>
            <td>floor/repair</td> <td>todo</td> <td>2 graphics</td>
        </tr>
        <tr>
            <td>floor/turntable</td> <td>todo</td> <td>2 graphics</td>
        </tr>
        <tr>
            <td>module</td> <td>todo</td> <td>9 graphics</td>
        </tr>
        <tr>
            <td>property/checkpoint</td> <td>todo</td> <td>6 graphics</td>
        </tr>
        <tr>
            <td>property/laser</td> <td>todo</td> <td>10 graphics</td>
        </tr>
        <tr>
            <td>property/laser emitter</td> <td>todo</td> <td>3 graphics</td>
        </tr>
        <tr>
            <td>property/press</td> <td>todo</td> <td>3 graphics</td>
        </tr>
        <tr>
            <td>property/slide</td> <td>todo</td> <td>5 graphics</td>
        </tr>
        <tr>
            <td>property/wall</td> <td><i>partially</i></td> <td>11/15 graphics</td>
        </tr>
    </tbody>
    <tfoot>
        <tr>
            <td>overall</td> <td>46 %</td> <td>45/97 graphics</td>
        </tr>
    <tfoot>
</table>

Time needed to build: 55 seconds.
