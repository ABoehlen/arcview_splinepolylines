# arcview_splinepolylines
Splinepolylines is an Avenue extension used in ArcView GIS that uses a basic combination of densifying the polyline and implementing the Bezier's spline method on the polyline.

## Purpose
![Splinepolylines Dialog](https://github.com/ABoehlen/arcview_splinepolylines/blob/main/splinepolylines_dialog.png)

Splinepolylines creates simulated spline curves as graphic elements from selected polyline features. The line width and colour can be defined. The lines can be scaled according to the theme's reference scale, if desired.

It's possible to convert the resulting graphic elements to a new shapefile. The defined symbology is retained.

This tool uses a basic combination of densifying the polyline and implementing the Bezier's spline method on the polyline. This script needs a view and the target theme active.

A combination of the following two parameters will produce different results depending on the nature and scale of the Polyline.

* densityfactor 0.000 to 1.000 only
* iterations 1 to 100 works best

## Background
ESRI's ArcView GIS is a rather old (1995 – 2002), but for many purposes still useful GIS application. Due to its age it's very fast on modern hardware and has full support for the still widely used vector data format _Shape_ (SHP).

Avenue is ArcView's built-in object oriented scripting language. "By using Avenue, you can customize the program and further extend its power", describes Amir H. Razavi the language's purpose in his 1999 book \[1\].

## System requirements
An ArcView GIS 3.x installation is required.

## Installation
Download the repository into your desired directory:

```
cd <directory>
git clone https://github.com/ABoehlen/arcview_splinepolylines
```

* Copy splinepolylines.avx into the ext32 directory of your ArcView installation.
* Open ArcView GIS with a new empty project or with an existing one.
* Choose File –> Extensions
* Turn on the Extension Splinepolylines and close the Extension dialog again.
* In the View documents open an existing view or create a new one.
* In the button list of the View document GUI click on the new button "Spline polylines". The tool dialog should open.

## License

This project is licensed under the MIT License - see the LICENSE file for details

***

## Literature
\[1\] Razavi, Amir H.: ArcView GIS Developer's Guide, 1999
