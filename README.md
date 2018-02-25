# Evolcon Widget Library
This is a widget library developed by Evolcon (well... duh...). Right now, it contains 3 KPI objects, but we will update it frequently adding more and more visualizations (or at least, that's the plan).

## Table of Contents
* [Getting Started](#getting-started)
* [Demo App](#demo-app)
* [QlikFreak KPI](#qlikfreak-kpi)
* [Evolcon KPI](#evolcon-kpi)
* [Super Relevant KPI](#super-relevant-kpi)
* [History](#history)
* [Authors](#authors)
* [License](#license)

## Getting Started

#### Qlik Sense Desktop
1. Download the package and unzip it.
2. Copy the new folder to this location: C:/Users/?????/Documents/Qlik/Sense/Extensions/.

#### Qlik Sense Server
Although widget libraries can be imported from both QMC and Dev Hub, the uniqueness check of a widget is only performed when importing from Dev Hub. Therefore, we strongly recommended you import all widget libraries from Dev Hub.
1. Download the ZIP file.
2. Open the Qlik Dev Hub. On the start page, click **+** and select **Import widget library**.
3. Locate the ZIP file containing the widget library to import and then click **Open**.

## Demo App
Don't forget to check the demo app included in this package. It contains multiple examples of all the widgets in the library. Even though there are some good pointers in this guide, it's easier to understand how to configure the objects by looking at real applications. If you want to have this module available in your hub, just copy the QVF in this location: C:/Users/?????/Documents/Qlik/Sense/Apps/

## QlikFreak KPI
Simple KPI with an image on the left.
<p align="center"><img src="https://qlikfreak.files.wordpress.com/2018/02/35_1001.png"></p>
This widget only receives one expression and it has 4 blocks:

* **Image**: Link to the image file (JPG, PNG, SVG, etc).
* **Title:** First line. Usually displays the KPI name, but it can be hidden.
* **KPI:** Big number in the middle (your expression).
* **Comment:** Third line. Useful for comments of comparisons. Can be hidden as well.

### Notes

* The image address doesn't need quotes or equals sign. Just paste the link.
* When you define the width of the image, the height is calculated automatically.
* **Right Padding** refers to the distance (pixels) between the image and the numbers.
* All the labels can be static (just type in whatever you want) or dynamic (using Qlik expressions) 
```
='Amount (USD): ' & money(sum(Sales))
```
* You can use RGB, HEX or [CSS colors](https://www.w3schools.com/cssref/css_colors.asp). If the color is static, you can type it directly in the box:
```
rgb(100, 50, 10)
turquoise
#FFF000
```
If you want to use an expression, you can do something like this:
```
=if(sum(Sales) > 1000, rgb(255, 50, 10), 
 if(sum(Sales) > 500, 'turquoise', '#FFF000'))

```
## Evolcon KPI
KPI + labels + symbols + lines. Yeah, that's a lot.
<p align="center"><img src="https://qlikfreak.files.wordpress.com/2018/02/35_1011.png"></p>
This widget only receives one expression and it has 6 parts (see the diagram below):

* **Title**: First line. Usually displays the KPI name.
* **Upper Line**: Line between the title and the KPI (the blue one).
* **Symbol**: A label with independent color and size. Shares the same line with the KPI.
* **KPI**: Your KPI. Shares the same line with the Symbol.
* **Lower Line**: Line between the KPI and the comment (the orange one).
* **Comment**: Last line. Useful for comments or comparisons.
<p align="center"><img src="https://qlikfreak.files.wordpress.com/2018/02/35_102.png"></p>

### Notes

* The alignment (left - center - right) applies to all the objects inside this widget.
* The labels, lines and symbol can be hidden.
* All the labels can be static (just type in whatever you want) or dynamic (using Qlik expressions) 
```
='Amount (USD): ' & money(sum(Sales))
```
* You can use RGB, HEX or [CSS colors](https://www.w3schools.com/cssref/css_colors.asp). If the color is static, you can type it directly in the box:
```
rgb(100, 50, 10)
turquoise
#FFF000
```
If you want to use an expression, you can do something like this:
```
=if(sum(Sales) > 1000, rgb(255, 50, 10), 
 if(sum(Sales) > 500, 'turquoise', '#FFF000'))

```
* You can adjust the space between and after both lines (pixels)
* The **Symbol > Suggestions** section has no impact on the widget. it just contains common symbols that you can easily copy and paste.
* If you increase the line width and make the color dynamic, you can create a weird/cool visual cue.

## Super Relevant KPI
Simple KPI... Actually, it was just an experiment... It's not thaaaat useful, but it looks cool.
<p align="center"><img src="https://qlikfreak.files.wordpress.com/2018/02/35_103.png"></p>
Nothing to explain here. Just add your expression and that's it.

## History
* Feb 25, 2018: Initial release. New widgets: QlikFreak KPI, Evolcon KPI, Super Relevant KPI.

## Authors
* **Evolcon** [Visit Website](http://evolcon.com/)
* **Julian Villafuerte:** [QlikFreak](https://qlikfreak.wordpress.com/)  -  [Twitter](https://twitter.com/qlikfreak)

## License
Copyright © 2018, Julian Villafuerte. Released under the MIT license.

If you create something cool based on this library, be sure to share it with us in [Twitter](https://twitter.com/intent/tweet?text=%40qlikfreak%20%40evolcon)! 
