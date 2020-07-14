#  How does perimeter change when a shape is stretched?

In graphics editing programs, the stretching tool is one of the most basic, fundamental, and intuitive tools available to you. It's also a fairly natural geometric operation. It plays nice with area measurements in that if you stretch a shape so that it lengthens by X%, the area also grows by X%.

But what does stretching do to a shape's perimeter? It turns out that for an arbitrary 2D shape, we can only provide upper and lower bounds for how the perimeter will change.

In this post, I've generalized the conventional "stretching tool" by allowing stretches in any direction, not just horizontally or vertically. Try to get a sense of how this works with the interactive below. Click and drag in the interactive to stretch. For simplicity, I used a square here, but you could replace the square with your desired 2D shape.

<center><iframe src="https://editor.p5js.org/pyrbgle/embed/EWH_vHUdM" style="width:600px;height:600px;border:none;"></iframe></center>

## It depends on the shape

So, how does the perimeter change when you stretch a shape? For one thing, it depends on what shape you start with.

Assuming some arbitrary stretching direction, we expect certain shapes to have their perimeters grow more than other shapes. For example, the perimeters of circles when you stretch them are more likely to grow more than the perimeters of squares.

## For an arbitrary shape

What if we have no information about what shape we start with? What can we say about how perimeter will grow when we stretch it? It turns out that regardless of stretching direction, the following statement will always be true.

**If you stretch a shape in one direction by a certain amount, the perimeter will grow by less than that amount.**

Why is this? Here's a kind of explanation by example. Imagine stretching a shape horizontally so it's twice as long, and then stretching it vertically so it's twice as tall. We end up with an exact copy of the shape we started out with, but one that's doubled in size. Therefore, the perimeter will have also doubled. Now imagine we just do the first part of that operation: stretching the shape horizontally so it's twice as long. The perimeter of this stretched shape will be smaller the perimeter of our doubled copy, which means the perimeter will have less than doubled.

## For multiple stretches

For multiple stretches, there is a similar result. It turns out that after you stretch a shape multiple times in multiple directions, like in the interactive above, there will always be a singe direction that stretches the most and a direction that stretches the least. These directions turn out to be perpendicular. You can see these directions as the axes of the ellipse that encircles the shape. The directions are called the **singular vectors** and their lengths are called the **singular values**. “Singular” here basically means "single", "lone", "one only". There is a "single" largest vector and a "single" smallest vector.

**It will always be the case that perimeter grows by more than the smallest singular value and by less than the largest singular value.**

The reason is simple. If every direction was stretched by the largest singular value, the shape would grow uniformly by that amount and so the perimeter growth would equal this value. But some directions are stretched less, so the perimeter is less. The same reasoning explains why the smallest singular value is a lower bound for perimeter growth.

Now for a given starting shape, the exact amount of perimeter growth can vary within these bounds. In other words, it’s possible to stretch a shape in multiple ways and end up with the same singular values, but get different perimeter growths. Therefore, the singular values provide the tightest possible bounds on perimeter growth assuming some arbitrary starting shape.