##数学的方法
数据的最简单的形式的数据,如果数据联系起来最简单的方法是利用数学方法。不会做除法运算的简单的三角函数等,孩子开始复杂的计算式,数学方法是数值的关系和模式进行的非常方便的方法。

###算术运算符
Dynamo的一套组件,这些组件使用代数函数和两个数字输入值,导致一个输出值(+,-,X,/,等等)。这些在Dynamo中都可以找到。

| 图标 | 名称 |  语法  | 输入 | 输出 |
| -- | -- | -- | -- | -- | -- |-- |
| ![](../images/icons/add-Large.png) | Add | + | var[]...[], var[]...[] | var[]...[] |
| ![](../images/icons/sub-Large.png) | Subtract | - | var[]...[], var[]...[] | var[]...[] |
| ![](../images/icons/mul-Large.png) | Multiply | * | var[]...[], var[]...[] | var[]...[] |
| ![](../images/icons/div-Large.png) | Divide | / | var[]...[], var[]...[] | var[]...[] |

### 参数化公式
>此次演习中附属的样本,请下载文件(右单击[另存为])[Building Blocks of Programs - Math.dyn](datasets/4-2/Building Blocks of Programs - Math.dyn). 所有的样本文件的列表,请参照附录。

在运算符中, the next logical step is to combine operators and variables to form a more complex relationship through **公式**. Let's make a Formula that can be controlled by input parameters, like sliders.

![](images/4-2/4-2-5/01.png)
>1. **Number Sequence:** define a number sequence based on three inputs: *start, amount* and *step*.  This sequence represents the 't' in the parametric equation, so we want to use a list that's large enough to define a spiral.

The step above has created a list of numbers to define the parametric domain.  The golden spiral is defined as the equation:  ![](images/4-2/4-2-5/x.gif)=![](images/4-2/4-2-5/goldenSpiral.gif) and
![](images/4-2/4-2-5/y.gif)=![](images/4-2/4-2-5/goldenSpiral2.gif). The group of Nodes below represent this equation in visual programming form.

![](images/4-2/4-2-5/02.png)
> When stepping through the group of Nodes, try to pay attention to the parallel between the visual program and written equation.
1. **Number Slider:** Add two number sliders to the canvas.  These sliders will represent the *a* and the *b* variables of the parametric equation.  These represent a constant which is flexible, or parameters which we can adjust towards a desired outcome.
2. ** * :** The multiplication Node is represented by an asterisk.  We'll use this repeatedly to connect multiplying variables
3. **Math.RadiansToDegrees:** The '*t*' values need to be translated to degrees for their evaluation in the trigonometric functions.  Remember, Dynamo defaults to degrees for evaluating these functions.
4. **Math.Pow:** as a function of the '*t*' and the number '*e*' this creates the Fibonacci sequence.
5. **Math.Cos and Math.Sin:**  These two trigonmetric functions will differentiate the x-coordinate and the y-coordinate, respectively, of each parametric point.
6.  **Watch: **We now see that our output is two lists, these will be the *x* and *y* coordinates of the points used to generate the spiral.

###From Formula to Geometry
Now, the bulk of Nodes from the previous step will work fine, but it is a lot of work.  To create a more efficient workflow, have a look at **Code Blocks** (section 3.3.2.3) to define a string of Dynamo expressions into one node.  In this next series of steps, we'll look at using the parametric equation to draw the Fibonacci spiral.
![](images/4-2/4-2-5/03.png)
> 1. **Point.ByCoordinates:** Connect the upper multiplication node into the '*x*' input and the lower into the '*y*' input. We now see a parametric spiral of points on the screen.

![](images/4-2/4-2-5/03aaa.png)
> 1. **Polycurve.ByPoints:** Connect Point.ByCoordinates from the previous step into *points*.  We can leave *connectLastToFirst* without an input because we aren't making a closed curve.  This creates a spiral which passes through each point defined in the previous step.

We've now completed the Fibonacci Spiral!  Let's take this further into two separate exercises from here, which we'll call the Nautilus and the Sunflower.  These are abstractions of natural systems, but the two different applications of the Fibonacci spiral will be well represented.

###From Spiral to Nautilus

![](images/4-2/4-2-5/03.png)
> 1. As a jumping-off point, let's start with the same step from the previous exercise: creating a spiral array of points with the **Point.ByCoordinates** Node.

![](images/4-2/4-2-5/03aa.png)
> 1. **Polycurve.ByPoints:** Again, this is the Node from the pervious exercise, which we'll use as a reference.
2. **Circle.ByCenterPointRadius:** We'll use a circle Node here with the same inputs as the previous step.  The radius value defaults to *1.0*, so we see an immediate output of circles. It becomes immediately legible how the points diverge further from the origin.

![](images/4-2/4-2-5/03a.png)
> 1. **Circle.ByCenterPointRadius:** To create a more dynamic array of circles, we plug the original number sequence (the '*t*' sequence) into the radius value.
2. **Number Sequence:** This is the original array of '*t*'.  By plugging this into the radius value, the circle centers are still diverging further from the origin, but the radius of the circles is increasing, creating a funky Fibonacci circle graph.  Bonus points if you make it 3D!

###From Nautilus to Phyllotaxis Pattern
Now that we've made a circular Nautilus shell, let's jump into parametric grids.  We're going to use a basic rotate on the Fibonacci Spiral to create a Fibonacci grid, and the result is modeled after the [growth of sunflower seeds.](http://ms.unimelb.edu.au/~segerman/papers/sunflower_spiral_fibonacci_metric.pdf)

![](images/4-2/4-2-5/03.png)
> 1. Again, as a jumping-off point, let's start with the same step from the previous exercise: creating a spiral array of points with the **Point.ByCoordinates** Node.

![](images/4-2/4-2-5/04.png)
> 1. **Geometry.Rotate:** There are several Geometry.Rotate options; be certain you've chosen the Node with *geometry*,*basePlane*, and *degrees* as its inputs.  Connect **Point.ByCoordinates** into the geometry input.
2. **Plane.XY:** Connect to the *basePlane* input. We will rotate around the origin, which is the same location as the base of the spiral.
3. **Number Range:** For our degree input, we want to create multiple rotations. We can do this quickly with a Number Range component.  Connect this into the *degrees* input.
4. **Number:** And to define the range of numbers, add three number nodes to the canvas in vertical order. From top to bottom, assign values of *0.0,360.0,* and *120.0* respectively.  These are driving the rotation of the spiral.  Notice the output results from the **Number Range** node after connecting the three number nodes to the Node.

Our output is beginning to resemble a whirlpool.  Let's adjust some of the **Number Range** parameters and see how the results change:
![](images/4-2/4-2-5/05.png)
> 1. Change the step size of the **Number Range** node from *120.0* to *36.0*.  Notice that this is creating more rotations and is therefore giving us a denser grid.

![](images/4-2/4-2-5/06.png)
> 1. Change the step size of the **Number Range** node from *36.0* to *3.6*.  This now gives us a much denser grid, and the directionality of the spiral is unclear.  Ladies and gentlemen, we've created a sunflower.

