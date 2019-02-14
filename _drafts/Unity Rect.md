---
textarea: ''
date: 2019-02-14 09:09:18 +0000

---
Unity Rect

官方表述：

> 
> A 2D Rectangle defined by X and Y position, width and height.
>
> Unity uses a number of 2D coordinate spaces, most of which define X as increasing to the right, and Y increasing upwards. The one exception is in the GUI and GUILayout classes, where Y increases downwards.
>
> The following examples are illustrated in GUI space, where (0,0) represents the top-left corner and Y increases downwards.
>
> Rectangles can be specified in two different ways. The first is with an x and y position and a width and height:
>
> The other way is with the X and Y coordinates of each of its edges. These are called xMin, xMax, yMin and yMax:
>
> Note that although x and y have the same values as xMin and yMin, they behave differently when you set them. Setting x or y changes the position of the rectangle, but preserves its size:
>
> Setting any of xMin, xMax, yMin and yMax will resize the rectangle, but preserve the position of the opposite edge: