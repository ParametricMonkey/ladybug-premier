## 3D Chart [![](../../images/icons/3D_Chart.png)]

![](../../images/components/3D_Chart.png)

Use this component to make a 3D chart in the Rhino scene of any climate data or hourly simulation data.

#### Inputs
* ##### _inputData [Required]
A list of input data to plot.
* ##### _basePoint_ [Default]
An optional point with which to locate the 3D chart in the Rhino Model.  The default is set to the Rhino origin at (0,0,0).
* ##### _xScale_ [Default]
The scale of the X axis of the graph. The default will plot the X axis with a length of 3650 Rhino model units (for 365 days of the year). Connect a list of values for multiple graphs.
* ##### _yScale_ [Default]
The scale of the Y axis of the graph. The default will plot the Y axis with a length of 240 Rhino model units (for 24 hours of the day). Connect a list of values for multiple graphs.
* ##### _zScale_ [Default]
The scale of the Z axis of the graph. The default will plot the Z axis with a number of Rhino model units corresponding to the input data values.  Set to 0 to see graphCurves appear on top of the mesh.  Connect a list of values for multiple graphs.
* ##### _yCount_ [Default]
The number of segments on your y-axis.  The default is set to 24 for 24 hours of the day. This variable is particularly useful for input data that is not for each hour of the year.
* ##### legendPar_ [Optional]
Optional legend parameters from the Ladybug Legend Parameters component.
* ##### condStatement_ [Optional]
An optional conditional statement, which will remove data from the chart that does not fit the conditions. The input must be a valid python conditional statement (e.g. a > 25).
* ##### bakeIt_ [Optional]
If set to True, the chart will be Baked into the Rhino scene as a colored mesh.  Text will be baked as Rhino text objects, which facilitates easy export to PDF or vector-editing programs.

#### Outputs
* ##### readMe!
...
* ##### graphMesh
A 3D plot of the input data as a colored mesh.  Multiple meshes will be output for several input data streams or graph scales.
* ##### graphCurves
A list of curves and text surfaces representing the time periods corresponding to the input data.  Note that if the time period of the input data is not clear, no curves or labels will be generated here.
* ##### legend
A legend of the chart. Connect this output to a grasshopper "Geo" component in order to preview the legend in the Rhino scene.g
* ##### legendBasePts
The legend base point, which can be used to move the legend in relation to the chart with the native rasshopper "Move" component.
* ##### title
The title text of the chart.  Hook this up to a native Grasshopper 'Geo' component to preview it separately from the other outputs.
* ##### titleBasePts
Points for placement of the title and axes labels of the chart, which can be used to move these text items in relation to the chart with the native Grasshopper "Move" component.
* ##### dataPts
Points representing the location of each piece of data on the chart.  Use this to label the points of the chart with text lables using a native grasshopper "Text Tag" component.
* ##### conditionalHOY
The input data for the hours of the year that pass the conditional statement.


[Check Hydra Example Files for 3D Chart](https://hydrashare.github.io/hydra/index.html?keywords=Ladybug_3D Chart)