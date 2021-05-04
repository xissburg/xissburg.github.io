---
layout: post
title: Calculating the Centroid of a Hemisphere
tags: [centroid, center of mass]
---

Consider a hemisphere of radius \( R \) with its bottom face centered at the origin, laying on the \( xz \)-plane, where the \( y \) axis points up.

![Hemisphere](/assets/img/Hemisphere.svg)

Let \( \mathbf{C} = (C_x, C_y, C_z) \) be its centroid. The \(x\) and \(z\) coordinates of the centroid are obviously zero due to symmetry. The vertical \(y\) coordinate can be calculated as the average vertical position \( p_y \) of all points contained in the volume of the hemisphere, i.e. the sum of all \( p_y \) divided by the volume.

$$ C_y = \frac{1}{V} \iiint \limits _{H} p_y \, \mathrm{d}V $$

The volume of a sphere of radius \( R \) is well known to be

$$ V_s = \frac{4}{3} \pi R^3 $$

The volume of the hemisphere is thus half of that

$$ V = \frac{2}{3} \pi R^3 $$

A point on the volume of this hemisphere in the three-dimensional Euclidean space can be described in spherical coordinates:

$$ \mathbf{p}(r,\varphi,\theta) = (p_x, p_y, p_z) = (r \cos  \theta \sin \varphi, r \cos \varphi, r \sin \theta \sin \varphi) $$

where \( \varphi \) is the angle between the vector \( \mathbf{p} \) and the \( y \) axis and \( \theta \) the angle between the projection of \( \mathbf{p} \) in the \( xz \)-plane and the \( x \) axis. Then, the triple integral in spherical coordinates can be written as

$$ C_y = \frac{1}{V} \int _{0}^{2 \pi} \int _{0}^{\frac{\pi}{2}} \int _{0}^{R} p_y \, r^2 \sin \varphi \,  \mathrm{d}r \, \mathrm{d} \varphi \, \mathrm{d} \theta $$

Note the \( r^2 \sin \varphi \) term due to the integral being done in spherical coordinates, which is an extra term needed to account for the curvature of the infinitesimal pieces being integrated. This great article at [Khan Academy](https://www.khanacademy.org/math/multivariable-calculus/integrating-multivariable-functions/x786f2022:polar-spherical-cylindrical-coordinates/a/triple-integrals-in-spherical-coordinates) explains that sort of integral in detail. Substituting \( p_y = r \cos \varphi \) and developing the integral further, we get

$$ C_y = \frac{1}{V} \int _{0}^{2 \pi} \int _{0}^{\frac{\pi}{2}} \int _{0}^{R} r^3 \cos \varphi \sin \varphi \,  \mathrm{d}r \, \mathrm{d} \varphi \, \mathrm{d} \theta $$

$$ \frac{1}{V} \int _{0}^{2 \pi} \int _{0}^{\frac{\pi}{2}} \left. \frac{r^4}{4} \cos \varphi \sin \varphi \, \right|_{0}^{R} \, \mathrm{d} \varphi \, \mathrm{d} \theta $$

$$ \frac{1}{V} \int _{0}^{2 \pi} \int _{0}^{\frac{\pi}{2}} \frac{R^4}{4} \cos \varphi \sin \varphi \, \mathrm{d} \varphi \, \mathrm{d} \theta $$

The integral of \( \cos \varphi \sin \varphi \) is (from [Wikipedia](https://en.wikipedia.org/wiki/List_of_integrals_of_trigonometric_functions#Integrands_involving_both_sine_and_cosine))

$$ \int \cos \varphi \sin \varphi \, \mathrm{d}\varphi = \frac{1}{2} \sin^2 \varphi $$

thus

$$ C_y = \frac{1}{V} \int _{0}^{2 \pi} \left. \frac{R^4}{4} \frac{1}{2} \sin^2 \varphi \, \right|_{0}^{\frac{\pi}{2}} \, \mathrm{d} \theta $$

$$ \frac{1}{V} \int _{0}^{2 \pi} \frac{R^4}{8} \left( \sin^2 \frac{\pi}{2} - \sin^2 0 \right) \, \mathrm{d} \theta $$

$$ \frac{1}{V} \int _{0}^{2 \pi} \frac{R^4}{8} \, \mathrm{d} \theta $$

$$ \frac{1}{V} \left( \left. \frac{\theta R^4}{8} \, \right|_{0}^{2 \pi} \right)$$

$$ \frac{1}{V} \frac{2 \pi R^4}{8} $$

$$ \frac{3}{2 \pi R^3} \frac{2 \pi R^4}{8} $$

$$ \frac{3}{8} R $$

That is, the vertical position of the centroid is 3/8-ths of the radius.
