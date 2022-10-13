---
layout: post
title: Intersecting Line Against Cylinder
tags: [intersection, line, segment, cylinder]
---

Consider a cylinder with radius \\( r \\) and length \\( \ell \\) whose axis contains points \\( \mathbf{q}_0 \\) and \\( \mathbf{q}_1 \\). Let \\( \mathbf{L}(t) = \mathbf{p}_0 + t (\mathbf{p}_1 - \mathbf{p}_0) \\) be a line passing through points \\( \mathbf{p}_0 \\) and \\( \mathbf{p}_1 \\), and \\( \mathbf{c}_L = \mathbf{p}_0 + t_c (\mathbf{p}_1 - \mathbf{p}_0) \\) be the point in \\( \mathbf{L} \\) closest to the cylinder axis and \\( \mathbf{c}_c \\) the point in the cylinder axis closest to \\( \mathbf{L} \\). If the distance \\( f \\) between the closest points is smaller than the cylinder radius, a value \\( \delta \\) can be added to and subtracted from \\( t_c \\) to find the intersection points \\( \mathbf{i}_0 = \mathbf{L}(t_c - \delta) \\) and \\( \mathbf{i}_1 = \mathbf{L}(t_c + \delta) \\) on the surface of the cylinder.

![Cylinder line intersection](/assets/img/CylinderLineIntersection.svg)

The line and the vector orthogonal to the line and the cylinder axis (i.e. their cross product) define a plane which cuts the cylinder, defining an ellipse as their intersection. The length of the semi-minor axis of this ellipse is \\( r \\), and the length of the semi-major axis is \\( s \\), which is unknown.

The the value of \\( s \\) is inversely proportional to the sine of the angle between the cylinder axis and \\( \mathbf{L} \\). At 90 degrees, \\( s = r \\). As the angle decreases, \\( s \\) increases.

$$ r = s \sin \theta $$

$$ r^2 = s^2 \sin^2 \theta $$

$$ r^2 = s^2 (1 - \cos^2 \theta) $$

$$ s^2 = \frac{r^2 } {1 - \cos^2 \theta} $$

Let \\( \mathbf{d} = \mathbf{p}_1 - \mathbf{p}_0 \\) and \\( \mathbf{e} = \mathbf{q}_1 - \mathbf{q}_0 \\). Using the dot product:

$$ \mathbf{d} \cdot \mathbf{e} = \| \mathbf{d} \| \| \mathbf{e} \| \cos \theta $$

$$ \left( \mathbf{d} \cdot \mathbf{e} \right)^2 = (\mathbf{d} \cdot \mathbf{d}) \, (\mathbf{e} \cdot \mathbf{e}) \cos^2 \theta $$

$$ \cos^2 \theta = \frac{\left( \mathbf{d} \cdot \mathbf{e} \right)^2}{ (\mathbf{d} \cdot \mathbf{d}) \, (\mathbf{e} \cdot \mathbf{e})} $$

Continuing on the development of \\( s \\):

$$ s^2 = \frac{r^2} {1 - \frac{\left( \mathbf{d} \cdot \mathbf{e} \right)^2}{(\mathbf{d} \cdot \mathbf{d}) \, (\mathbf{e} \cdot \mathbf{e})}} $$

$$ s^2 = \frac{r^2 (\mathbf{d} \cdot \mathbf{d}) \, (\mathbf{e} \cdot \mathbf{e})} {(\mathbf{d} \cdot \mathbf{d}) \, (\mathbf{e} \cdot \mathbf{e}) - \left( \mathbf{d} \cdot \mathbf{e} \right)^2} $$

Our ellipse equation is

$$ \frac{g^2}{s^2} + \frac{f^2}{r^2} = 1 $$

where \\( f \\) is the distance between \\( \mathbf{L} \\) and the cylinder axis and \\( g \\) is how much the closest point on \\( \mathbf{L} \\) must be offset to lie on the surface of the cylinder. Solving for \\( g \\):

$$ g^2 = s^2 \left(1 - \frac{f^2}{r^2} \right) $$

$$ = \frac{r^2 (\mathbf{d} \cdot \mathbf{d}) \, (\mathbf{e} \cdot \mathbf{e})} {(\mathbf{d} \cdot \mathbf{d}) \, (\mathbf{e} \cdot \mathbf{e}) - \left( \mathbf{d} \cdot \mathbf{e} \right)^2} \frac{r^2 - f^2}{r^2} $$ 

$$ = \frac{(\mathbf{d} \cdot \mathbf{d}) \, (\mathbf{e} \cdot \mathbf{e}) (r^2 - f^2)} {(\mathbf{d} \cdot \mathbf{d}) \, (\mathbf{e} \cdot \mathbf{e}) - \left( \mathbf{d} \cdot \mathbf{e} \right)^2} $$

The value of \\( g \\) is a measure of length, while \\( \delta \\) is a fraction of the length of \\( \mathbf{d} \\). To obtain \\( \delta \\), \\( g \\) must be divided by the length of \\( \mathbf{d} \\).

$$ \delta = \frac{g}{\| \mathbf{d} \|}$$

$$ \delta^2 = \frac{g^2}{\mathbf{d} \cdot \mathbf{d}} $$

$$ \delta^2 = \frac{(\mathbf{d} \cdot \mathbf{d}) \, (\mathbf{e} \cdot \mathbf{e}) (r^2 - f^2)} {(\mathbf{d} \cdot \mathbf{d}) \, (\mathbf{e} \cdot \mathbf{e}) - \left( \mathbf{d} \cdot \mathbf{e} \right)^2} \frac{1}{(\mathbf{d} \cdot \mathbf{d})} $$

$$ \delta^2 = \frac{(\mathbf{e} \cdot \mathbf{e}) (r^2 - f^2)} {(\mathbf{d} \cdot \mathbf{d}) \, (\mathbf{e} \cdot \mathbf{e}) - \left( \mathbf{d} \cdot \mathbf{e} \right)^2} $$

Now the first and second intersection points \\( \mathbf{i}_0 \\) and \\( \mathbf{i}_1 \\) can be calculated using \\( \delta \\).
