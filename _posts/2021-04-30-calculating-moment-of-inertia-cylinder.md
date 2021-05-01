---
layout: post
title: Calculating the Moment of Inertia of a Cylinder
tags: [moment of inertia]
---

The moment of inertia of a shape about an axis of rotation is equals to the integral of the density \\( \rho \\) times the squared distance of each point \\( \mathbf{p} \\) from the axis over the entire volume of the shape. Let \\( \mathbf{r} \\) be the vector connecting \\( \mathbf{p} \\) to its closest point on the axis of rotation, then

$$ \iiint \rho (x,y,z) \, \| \mathbf{r} (x,y,z) \|^2 \, \mathrm{d}V $$

Consider a cylinder of radius \\( R \\) and length \\( L \\) with its main axis (i.e. axis of rotational symmetry) aligned with the \\( x \\) axis on a right-hand coordinate system where \\( y \\) points up.

![Cylinder](/assets/img/Cylinder.svg)

The density \\( \rho \\) is assumed to be constant.

A point on the volume of this cylinder in the three-dimensional Euclidean space can be described in cylindrical coordinates:

$$ \mathbf{p}(r,\theta,\ell) = (p_x, p_y, p_z) = (\ell,r \sin \theta, r \cos \theta) $$

The squared length of the vector connecting \\( \mathbf{p} \\) to its closest point on the axis of rotation \\( x \\) is

$$ \| \mathbf{r} \|^2 = p_y^2 + p_z^2 $$

Thus, the moment of inertia along the \\( x \\) axis is:

$$ I_{xx} = \rho \int _{-{\frac {L}{2}}}^{\frac {L}{2}} \int _{0}^{2\pi} \int _{0}^{R} \left( p_y^2 + p_z^2 \right) \, r \, \mathrm{d}r \, \mathrm{d}\theta \, \mathrm{d}\ell $$

Note the use of \\( r \, \mathrm{d}r \, \mathrm{d}\theta \\) for the integral in polar coordinates. Missing \\( r \\) here is a common mistake. Developing the integral further, we get

$$ \rho \int _{-{\frac {L}{2}}}^{\frac {L}{2}} \int _{0}^{2\pi} \int _{0}^{R} \left( r^2 \cos^2 \! \theta + r^2 \sin^2 \! \theta \right) \, r \, \mathrm{d}r \, \mathrm{d}\theta \, \mathrm{d}\ell $$

$$ \rho \int _{-{\frac {L}{2}}}^{\frac {L}{2}} \int _{0}^{2\pi} \int _{0}^{R} r^2 \left(\cos^2 \! \theta + \sin^2 \! \theta \right) \, r \, \mathrm{d}r \, \mathrm{d}\theta \, \mathrm{d}\ell $$

It's well known that

$$ \cos^2 \! \theta + \sin^2 \! \theta = 1 $$

thus

$$ \rho \int _{-{\frac {L}{2}}}^{\frac {L}{2}} \int _{0}^{2\pi} \int _{0}^{R} r^3 \, \mathrm{d}r \, \mathrm{d}\theta \, \mathrm{d}\ell $$

$$ \rho \int _{-{\frac {L}{2}}}^{\frac {L}{2}} \int _{0}^{2\pi} \left. \frac {r^4}{4} \right|_{0}^{R}  \, \mathrm{d}\theta \, \mathrm{d}\ell $$

$$ \rho \int _{-{\frac {L}{2}}}^{\frac {L}{2}} \int _{0}^{2\pi} \frac {R^4}{4}  \, \mathrm{d}\theta \, \mathrm{d}\ell $$

$$ \rho \int _{-{\frac {L}{2}}}^{\frac {L}{2}} \left. \frac {\theta R^4}{4} \right|_{0}^{2\pi} \, \mathrm{d}\ell $$

$$ \rho \int _{-{\frac {L}{2}}}^{\frac {L}{2}} \frac {2 \pi R^4}{4} \, \mathrm{d}\ell $$

$$ \rho \left. \frac {\pi R^4 \ell}{2} \right|_{-{\frac {L}{2}}}^{\frac {L}{2}} $$

$$  \rho \, \frac {\pi R^4}{2} \left( \frac {L}{2} - \left(-{\frac {L}{2}}\right) \right) $$

$$  \rho \, \frac {\pi R^4}{2} \left( \frac {L}{2} + {\frac {L}{2}} \right) $$

$$ \rho \, \frac {\pi R^4 L}{2} $$

The volume of the cylinder is the area of its base \\( \pi R^2 \\) times its length \\( L \\)

$$ V = \pi R^2 L $$

then

$$ \rho \, \pi R^2 L \frac {R^2}{2} $$

$$ \rho \, V \frac {R^2}{2} $$

The mass of the cylinder is

$$ M = \rho V $$

Finally

$$ I_{xx} = \frac {M R^2}{2} $$

The moment of inertia along the other two principal axes \\( I_{yy} \\) and \\( I_{zz} \\) are equal due to symmetry. Lets calculate \\( I_{zz} \\).

$$ I_{zz} = \rho \int _{-\frac {L}{2}}^{\frac{L}{2}} \int _{0}^{2\pi} \int _{0}^{R} \left( p_x^2 + p_y^2 \right) \, r \, \mathrm{d}r \, \mathrm{d}\theta \, \mathrm{d}\ell $$

$$ \rho \int _{-\frac {L}{2}}^{\frac{L}{2}} \int _{0}^{2\pi} \int _{0}^{R} \left( \ell^2 + r^2 \sin^2 \! \theta \right) \, r \, \mathrm{d}r \, \mathrm{d}\theta \, \mathrm{d}\ell $$

$$ \rho \int _{-\frac {L}{2}}^{\frac{L}{2}} \int _{0}^{2\pi} \int _{0}^{R} \ell^2 r + r^3 \sin^2 \! \theta \, \mathrm{d}r \, \mathrm{d}\theta \, \mathrm{d}\ell $$

$$ \rho \int _{-\frac {L}{2}}^{\frac{L}{2}} \int _{0}^{2\pi} \left. \frac {\ell^2 r^2}{2} + \frac{r^4}{4} \sin^2 \! \theta \, \right|_{0}^{R} \, \mathrm{d}\theta \, \mathrm{d}\ell $$

$$ \rho \int _{-\frac {L}{2}}^{\frac{L}{2}} \int _{0}^{2\pi} \frac{\ell^2 R^2}{2} + \frac{R^4}{4} \sin^2 \! \theta \, \mathrm{d}\theta \, \mathrm{d}\ell $$

The integral of \\( \sin^2 \\! \theta \\) is (from [Wikipedia](https://en.wikipedia.org/wiki/List_of_integrals_of_trigonometric_functions#Integrands_involving_only_sine))

$$ \int \sin^2 \! \theta \, \mathrm{d}\theta = \frac{\theta}{2} - \frac{1}{4} \sin 2 \theta $$

thus

$$ \rho \int _{-\frac {L}{2}}^{\frac{L}{2}} \left. \frac{\ell^2 R^2 \theta}{2} + \frac{R^4}{4} \left( \frac{\theta}{2} - \frac{1}{4} \sin 2 \theta \right) \right|_{0}^{2\pi} \, \mathrm{d}\ell $$

$$ \rho \int _{-\frac {L}{2}}^{\frac{L}{2}} \frac{2 \pi R^2 \ell^2}{2} + \frac{R^4}{4} \left( \frac{2 \pi}{2} - \frac{1}{4} \sin 4 \pi \right) \, \mathrm{d}\ell $$

Given that \\( \sin 4 \pi = 0 \\), we continue like so

$$ \rho \int _{-\frac {L}{2}}^{\frac{L}{2}} \pi R^2 \ell^2 + \frac{\pi R^4}{4} \, \mathrm{d}\ell $$

$$ \rho \left( \left. \frac{\pi R^2 \ell^3}{3} + \frac{\pi R^4 \ell}{4} \right|_{-\frac {L}{2}}^{\frac{L}{2}} \right) $$

$$ \rho \left( \frac{\pi R^2}{3} \left( \left( \frac{L}{2} \right)^3 - \left( -\frac{L}{2} \right)^3 \right) + \frac{\pi R^4}{4} \left(\frac{L}{2} - \left( -\frac{L}{2} \right) \right) \right) $$

$$ \rho \left( \frac{\pi R^2}{3} \left( \frac{L^3}{8} - \left( -\frac{L^3}{8} \right) \right) + \frac{\pi R^4}{4} \left(\frac{L}{2} + \frac{L}{2} \right) \right) $$

$$ \rho \left( \frac{\pi R^2}{3} \left( \frac{L^3}{8} + \frac{L^3}{8} \right) + \frac{\pi R^4 L}{4} \right) $$

$$ \rho \left( \frac{\pi R^2}{3} \frac{L^3}{4} + \frac{\pi R^4 L}{4} \right) $$

$$ \rho \left( \frac{\pi R^2 L^3}{12} + \frac{\pi R^4 L}{4} \right) $$

$$ \rho \frac{\pi R^2 L^3 + 3 \pi R^4 L}{12} $$

$$ \rho \pi R^2 L \frac{L^2 + 3 R^2}{12} $$

Finally, using our knowledge about the cylinder volume and mass from above

$$ I_{zz} = I_{yy} = \frac{M}{12} \left( L^2 + 3 R^2 \right) $$

And we're done. I hope it was clear.
