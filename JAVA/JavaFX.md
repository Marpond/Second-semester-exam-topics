## Scene graph
In JavaFX, applications were coded using a Scene Graph. It holds all the application primitives that are termed as nodes, such as:
1. Geometrical objects
2. UI controls
3. Containers
4. Media elements

Hierarchical order of the nodes
![](Pasted%20image%2020220620233338.png)
- **Root node**
Does not contain any parents
- **Branch node**
Nodes with children
- **Leaf node**
Nodes without children

## Transformation
1. **Rotation**
In rotation, we rotate the object at a particular angle **θ (theta)** from its origin.
2. **Scaling**
To change the size of an object, scaling transformation is used.
3. **Translation**
Moves an object to a different position on the screen.
4. **Shearing**
A transformation that slants the shape of an object is called the Shear Transformation.

## Chart
JavaFX Provides support for various **Pie Charts** and **XY Charts**. The charts that are represented on an XY–plane include 
1. **AreaChart
2. **BarChart
3. **BubbleChart
4. **LineChart
5. **ScatterChart
6. **StackedAreaChart
7. **StackedBarChart

**Creating a Chart**
To create a chart, you need to −
1. Define the axis of the chart
2. Instantiate the respective class
3. Prepare and pass data to the chart

## UI controls
Core visual elements, user interacts with these.

## 2D shapes
XY
- Rectangle
- Circle
- Line
- Ellipse

## 3D shapes
XYZ
- Cylinder
- Box
- Sphere

## Binding


## Animation
Transition
```java
translateTransition.setDuration(Duration.millis(1000)); 

translateTransition.setNode(circle); 

translateTransition.setByX(300); 

translateTransition.setCycleCount(50); 

translateTransition.setAutoReverse(false); 

translateTransition.play();
```
Timeline
```java
Timeline timeline = new Timeline(new Keyframe(Duration.millis), e -> {

});
```
Animation timer