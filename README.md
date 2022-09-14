# How-to-create-a-directional-compass-with-the-WinUI-radial-gauge
This repository contains sample for how to create a directional compass with the WinUI radial gauge

This article describes how to create the directional compass using the Syncfusion WinUi Radial Gauge control.

Step 1: Create the RadialGauge control by referring to this getting started link. Set the StartAngle and EndAngle of RadialAxis as 320 to heading the North value as 0 and get the full circular axis.

XAML
```
<gauge:SfRadialGauge>
    <gauge:SfRadialGauge.Axes>
        <gauge:RadialAxis StartAngle="320"
                          EndAngle="320">
        </gauge:RadialAxis>
    </gauge:SfRadialGauge.Axes>
</gauge:SfRadialGauge>
```

Step 2: Set the Minimum and Maximum of the radial axis as 0 and 360 respectively, and the Interval as 30 to display eight direction values in the radial axis.

XAML
```
<gauge:SfRadialGauge>
    <gauge:SfRadialGauge.Axes>
        <gauge:RadialAxis Minimum="0"
                          Maximum="360"
                          Interval="30">
        </gauge:RadialAxis>
    </gauge:SfRadialGauge.Axes>
</gauge:SfRadialGauge>
```

Step 3: To customize the major and minor ticks, you can use the MajorTickLength, MinorTickLength, TickLengthUnit and MinorTicksPerInterval as shown in the following code sample.

XAML
```
<gauge:RadialAxis MajorTickLength="0.16"
                  MinorTickLength="0.16"
                  TickLengthUnit="Factor"
                  MinorTicksPerInterval="10">
</gauge:RadialAxis>
```

Step 4: Add two Needle Pointers to divide the gauge into four parts : north, east, south and west.

XAML
```
<gauge:RadialAxis.Pointers>
    <gauge:NeedlePointer Value="310"
                         NeedleLengthUnit="Factor"
                         NeedleLength="0.7"
                         NeedleStartWidth="1"
                         NeedleEndWidth="1"
                         NeedleFill="#FFC4C4C4"
                         KnobRadius="0"
                         TailLengthUnit="Factor"
                         TailLength="0.7"
                         TailWidth="1"
                         TailFill="#FFC4C4C4">
    </gauge:NeedlePointer>
</gauge:RadialAxis.Pointers> 
```

Step 5: To denote the directions, you can use Annotations as shown in the following code sample.

XAML
```
<gauge:RadialAxis.Annotations>
    <gauge:GaugeAnnotation DirectionValue="230"
                           PositionFactor="0.5">
        <gauge:GaugeAnnotation.Content>
            <Label Text="W"
                   FontAttributes="Bold"
                   FontSize="18"
                   TextColor="Black" />
        </gauge:GaugeAnnotation.Content>
    </gauge:GaugeAnnotation>
    <gauge:GaugeAnnotation DirectionValue="310">
    </gauge:GaugeAnnotation>
    <gauge:GaugeAnnotation DirectionValue="129">
    </gauge:GaugeAnnotation>
    <gauge:GaugeAnnotation DirectionValue="50">
    </gauge:GaugeAnnotation>
</gauge:RadialAxis.Annotations>
```

Step 6: Add a Shape Pointer to indicate the direction as follows.

XAML
```
<gauge:RadialAxis.Pointers>
    <gauge:ShapePointer Value="90"
                        ShapeType="Triangle" />
</gauge:RadialAxis.Pointers>
```

Output

 ![Direction compass](https://www.syncfusion.com/uploads/user/kb/winui/winui-2848/winui-2848_img1.png)

View the sample in GitHub.

See also

How to create an application using the WINUI Radial Gauge?

How to customize Axis?

How to customize Axis Label?

How to customize Axis Label using Label Prepared Event?

How to customize Ticks?

How to customize Needle Pointer?

How to position and customize annotations?


