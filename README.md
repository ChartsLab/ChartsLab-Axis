# ChartsLab-Axis
The axis component renders human-readable reference marks for [Scale](https://github.com/HishamElamir/ChartsLab-Scale/). This alleviates one of the more tedious tasks in visualizing data.
The axis component also uses html5 canvas element for drawing so it keeps your code beautiful and clean.

## Installing
For now you can download the latest release. You can also load directly from [Site(NotFound)](https://github.com/HishamElamir/), either as standalone micro library or as part of ChartsLab release.
```html
<script src="chartsLab/Axis.js"></script>
<script>
var axis = new Axis(canvasContext);
</script>
```

## Requires
Axis component requires just [Scale](https://github.com/HishamElamir/ChartsLab-Scale/) for ticks optimizing.

## API Reference

Axis rendered at specific oriantation(Side) and position. To change the position of the axis with respect to the chart, just give position function a start position and end(finish) position points. And Side function is the oriantation of the axis ticks and lable, at the end just call draw for render the component at the canvas. For example:

```js
Axis
  .Position([50,50], [500,50])
  .Side("TOP")
  .Draw();
```
The micro library API gives you alot of functionality to manipulate the components type and style and values as easy as possible

![ChartsLab-Axis](/Images/AxisOne.JPG)


<a name="Axis" href="#axis">#</a> ChartsLab.<b>Axis</b>(<i>canvasContext</i>)

Constructs a new axis generator object for the given with ready for drawing in the given canvas context with defaults
 [Tick number](#TickNumber) is equals to 10, [Inner tick number](#InnerTickNumber) equals to 3, [Tick label padding](#TickLabelPadding) equals to 25, [Outer tick size](#OuterTickSize) equals to 5, [Inner tick size](#InnerTickSize) equals to 15, [Axis width](#AxisWidth) equals to 2, [Tick width](#TickWidth) equals to 2, and auto  [TickFormat](#TickFormat)
 
 ![ChartsLab-Axis](/Images/AxisTwo.JPG)
 
<a name="Position" href="#position">#</a> Axis.<b>Position</b>(<i>[StartPoint Array], [EndPoint Array]</i>)
 
<a name="Side" href="#side">#</a> Axis.<b>Side</b>(<i>side String</i>)
 
<a name="AxisLabel" href="#axisLabel">#</a> Axis.<b>Label</b>(<i>text String</i>)
 
<a name="AxisWidth" href="#axisWidth">#</a> Axis.<b>AxisWidth</b>(<i>size Number</i>)

<a name="AxisScale" href="#axisScale">#</a> Axis.<b>Scale</b>(<i>scale Function</i>)

<a name="TickWidth" href="#TickWidth">#</a> Axis.<b>TickWdith</b>(<i>width Number</i>)

<a name="TickPadding" href="#TickPadding">#</a> Axis.<b>TickPadding</b>(<i>padding Number</i>)

<a name="TickNumber" href="#TickNumber">#</a> Axis.<b>TickNumber</b>(<i>tickNumber Number</i>)

<a name="InnerTickNumber" href="#InnerTickNumber">#</a> Axis.<b>InnerTickNumber</b>(<i>innerTickNumber Number</i>)

<a name="OuterTickSize" href="#OuterTickSize">#</a> Axis.<b>OuterTickSize</b>(<i>size Number</i>)

<a name="InnerTickSize" href="#InnerTickSize">#</a> Axis.<b>InnerTickSize</b>(<i>size Number</i>)

<a name="DashedTick" href="#DashedTick">#</a> Axis.<b>DashedTick</b>(<i>flag Boolean</i>)


