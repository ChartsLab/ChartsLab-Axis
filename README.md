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


<a name="Axis" href="#axis">#</a> ChartsLab.<b>Axis</b>(<i>ctx **Context**</i>)

Constructs a new axis generator object for the given with ready for drawing in the given canvas context with defaults
 [Tick number](#TickNumber) is equals to 10, [Inner tick number](#InnerTickNumber) equals to 3, [Tick label padding](#TickLabelPadding) equals to 25, [Outer tick size](#OuterTickSize) equals to 5, [Inner tick size](#InnerTickSize) equals to 15, [Axis width](#AxisWidth) equals to 2, [Tick width](#TickWidth) equals to 2, and auto  [TickFormat](#TickFormat)
 
 ![ChartsLab-Axis](/Images/AxisTwo.JPG)
 
<a name="Position" href="#position">#</a> Axis.<b>Position</b>(<i>[StartPoint **Array**], [EndPoint **Array**]</i>)
 
 Position Take 2 Array each contain 2 value for start and end coordinates for this axis, you can control the position of start you axis it validate it and raise an error for problems see raised errors [ErrorHandler](https://github.com/ChartsLab/) for more details.
 
<a name="Side" href="#side">#</a> Axis.<b>Side</b>(<i>side **String**</i>)

  Side take string and let you choose the side of you axis or oriantation, it validate the string to a given values (TOP, BOTTOM, LEFT, RIGHT) (comming soon Enums) but for now you must write it capital letters.
 
<a name="AxisLabel" href="#axisLabel">#</a> Axis.<b>Label</b>(<i>text **String**</i>)
  
  This function let you choose the label of your axis. The position of the label in the center and the orintation and rotation are dynamically allocated based on [Side](#side), [Position](#position).
 
<a name="AxisWidth" href="#axisWidth">#</a> Axis.<b>AxisWidth</b>(<i>size **Integer**</i>)
  
  This function allows you to choose the line width for you axis to be drawen with (the axis is a line at the end). **Note**: the axis width is not correlated to tick in any way.
  
  
<a name="AxisScale" href="#axisScale">#</a> Axis.<b>Scale</b>(<i>scale **Scale**</i>)

  Scale is the mapping function that maps each tick to certain position along the Axis based on it's value and the scale type, see [Scale](https://github.com/ChartsLab/ChartsLab-Scale/) for more details, this function simpilify for you to find the position and this is the only required class need for axis plotting.

<a name="TickWidth" href="#TickWidth">#</a> Axis.<b>TickWdith</b>(<i>width **Number**</i>)

  Like AxisWidth function you can also control the tick line width that used in drawing, **note**: the tick width is different the [tickPadding](#TickPadding) and [tickSize](#OuterTickSize).

<a name="TickPadding" href="#TickPadding">#</a> Axis.<b>TickPadding</b>(<i>padding **Number**</i>)

<a name="TickNumber" href="#TickNumber">#</a> Axis.<b>TickNumber</b>(<i>tickNumber **Number**</i>)

<a name="InnerTickNumber" href="#InnerTickNumber">#</a> Axis.<b>InnerTickNumber</b>(<i>innerTickNumber **Number**</i>)

<a name="OuterTickSize" href="#OuterTickSize">#</a> Axis.<b>OuterTickSize</b>(<i>size **Number**</i>)

<a name="InnerTickSize" href="#InnerTickSize">#</a> Axis.<b>InnerTickSize</b>(<i>size **Number**</i>)

<a name="DashedTick" href="#DashedTick">#</a> Axis.<b>DashedTick</b>(<i>flag **Boolean**</i>)


