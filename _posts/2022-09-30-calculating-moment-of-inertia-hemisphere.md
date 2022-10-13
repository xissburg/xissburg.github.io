---
layout: post
title: Calculating the Moment of Inertia of a Hemisphere
tags: [moment of inertia, hemisphere]
---

The moment of inertia of a shape about an axis of rotation is equals to the integral of the density \\( \rho \\) times the squared distance of each point \\( \mathbf{p} \\) from the axis over the entire volume of the shape. Let \\( \mathbf{r} \\) be the vector connecting \\( \mathbf{p} \\) to its closest point on the axis of rotation, then

$$ \iiint \rho (x,y,z) \, \| \mathbf{r} (x,y,z) \|^2 \, \mathrm{d}V $$

Consider a hemisphere of radius \\( R \\) with its bottom face centered at the origin, laying on the \\( xz \\)-plane, where the \\( y \\) axis points up.

![Hemisphere](/assets/img/Hemisphere.svg)

The density \\( \rho \\) is assumed to be constant.

A point on the volume of a hemisphere in the three-dimensional Euclidean space can be described in spherical coordinates:

$$ \mathbf{p}(r,\varphi,\theta) = (p_x, p_y, p_z) = (r \cos \! \theta \sin \! \varphi, r \cos \! \varphi, r \sin \! \theta \sin \! \varphi) $$

where \\( \varphi \\) is the angle between the vector \\( \mathbf{p} \\) and the \\( y \\) axis and \\( \theta \\) the angle between the projection of \\( \mathbf{p} \\) in the \\( xz \\)-plane and the \\( x \\) axis.

The moment of inertia along the \\( y \\) axis is the simplest to calculate. 

$$ I_{yy} = \rho \int _{0}^{2\pi} \int _{0}^{\frac{\pi}{2}} \int _{0}^{R} \left( p_x^2 + p_z^2 \right) \, r^2 \sin \! \varphi \, \mathrm{d}r \, \mathrm{d}\varphi \, \mathrm{d}\theta $$

Substituting \\( p_x \\) and \\( p_z \\) and developing further:

$$ \rho \int _{0}^{2\pi} \int _{0}^{\frac{\pi}{2}} \int _{0}^{R} \left( r^2 \cos^2 \! \theta \sin^2 \! \varphi + r^2 \sin^2 \! \theta \sin^2 \! \varphi \right) \, r^2 \sin \! \varphi \, \mathrm{d}r \, \mathrm{d}\varphi \, \mathrm{d}\theta $$

$$ \rho \int _{0}^{2\pi} \int _{0}^{\frac{\pi}{2}} \int _{0}^{R} r^2 \sin^2 \! \varphi \left( \cos^2 \! \theta + \sin^2 \! \theta \right) \, r^2 \sin \! \varphi \, \mathrm{d}r \, \mathrm{d}\varphi \, \mathrm{d}\theta $$

$$ \rho \int _{0}^{2\pi} \int _{0}^{\frac{\pi}{2}} \int _{0}^{R} r^4 \sin^3 \! \varphi \left( \cos^2 \! \theta + \sin^2 \! \theta \right) \, \mathrm{d}r \, \mathrm{d}\varphi \, \mathrm{d}\theta $$

Applying the identity \\( \cos^2 \! \theta + \sin^2 \! \theta = 1 \\)

$$ \rho \int _{0}^{2\pi} \int _{0}^{\frac{\pi}{2}} \int _{0}^{R} r^4 \sin^3 \! \varphi \, \mathrm{d}r \, \mathrm{d}\varphi \, \mathrm{d}\theta $$

$$ \rho \int _{0}^{2\pi} \int _{0}^{\frac{\pi}{2}} \left. \frac {r^5}{5} \sin^3 \! \varphi \right|_{0}^{R} \, \mathrm{d}\varphi \, \mathrm{d}\theta $$

$$ \rho \frac {R^5}{5} \int _{0}^{2\pi} \int _{0}^{\frac{\pi}{2}} \sin^3 \! \varphi \, \mathrm{d}\varphi \, \mathrm{d}\theta $$

The integral of \\( \sin^3 \! \varphi \\) is (from [Wikipedia](https://en.wikipedia.org/wiki/List_of_integrals_of_trigonometric_functions#Integrands_involving_only_sine))

$$ \int \sin^3 \! \varphi \, \mathrm{d}\varphi = \frac {\cos 3\varphi}{12} - \frac{3 \cos \varphi}{4} $$

Thus

$$ \rho \frac {R^5}{5} \int _{0}^{2\pi} \left. \frac {\cos 3\varphi}{12} - \frac{3 \cos \varphi}{4} \right|_{0}^{\frac{\pi}{2}} \, \mathrm{d}\varphi \, \mathrm{d}\theta $$

$$ \rho \frac {R^5}{5} \int _{0}^{2\pi} \left( \frac {\cos \frac{3\pi}{2}}{12} - \frac{3 \cos \frac{\pi}{2}}{4} \right) - \left( \frac {\cos 0}{12} - \frac{3 \cos 0}{4} \right) \, \mathrm{d}\theta $$

$$ \rho \frac {R^5}{5} \int _{0}^{2\pi} - \! \left( \frac {1}{12} - \frac{3}{4} \right) \, \mathrm{d}\theta $$

$$ \rho \frac {R^5}{5} \int _{0}^{2\pi} - \! \left( \frac {1}{12} - \frac{9}{12} \right) \, \mathrm{d}\theta $$

$$ \rho \frac {R^5}{5} \int _{0}^{2\pi} \frac {2}{3} \, \mathrm{d}\theta $$

$$ \rho \frac {R^5}{5} \left. \frac {2}{3} \theta \right|_{0}^{2\pi} $$

$$ \rho \frac {R^5}{5} \frac {2}{3} 2\pi $$

$$ \rho \frac {4\pi R^5}{15} $$

The volume of a sphere of radius \\( R \\) is well known to be

$$ V_s = \frac{4 \pi R^3}{3} $$

The volume of the hemisphere is thus half of that

$$ V = \frac{2 \pi R^3}{3} $$

Rearranging and substituting

$$ \rho \frac {4\pi R^5}{15} = \rho \frac{2 \pi R^3}{3} \frac{2 R^2}{5} $$

$$ \rho V \frac{2 R^2}{5} $$

$$ M \frac{2 R^2}{5} $$

Finally

$$ I_{yy} = \frac{2}{5} M R^2 $$

The moment of inertia along the \\( x \\) and the \\( z \\) are identical due to symmetry. Let's calculate \\( I_{zz0} \\) around the origin and then use the inverse of the [parallel axis theorem](https://en.m.wikipedia.org/wiki/Parallel_axis_theorem) to obtain \\( I_{zz} \\) about the center of mass.

$$ I_{zz0} = \rho \int _{0}^{2\pi} \int _{0}^{\frac{\pi}{2}} \int _{0}^{R} \left( p_x^2 + p_y^2 \right) \, r^2 \sin \! \varphi \, \mathrm{d}r \, \mathrm{d}\varphi \, \mathrm{d}\theta $$

$$ \rho \int _{0}^{2\pi} \int _{0}^{\frac{\pi}{2}} \int _{0}^{R} \left( r^2 \cos^2 \! \theta \sin^2 \! \varphi + r^2 \cos^2 \! \varphi \right) \, r^2 \sin \! \varphi \, \mathrm{d}r \, \mathrm{d}\varphi \, \mathrm{d}\theta $$

$$ \rho \int _{0}^{2\pi} \int _{0}^{\frac{\pi}{2}} \int _{0}^{R} r^4 \left( \cos^2 \! \theta \sin^3 \! \varphi + \cos^2 \! \varphi \sin \! \varphi \right) \, \mathrm{d}r \, \mathrm{d}\varphi \, \mathrm{d}\theta $$

$$ \rho \int _{0}^{2\pi} \int _{0}^{\frac{\pi}{2}} \left. \frac {r^5}{5} \left( \cos^2 \! \theta \sin^3 \! \varphi + \cos^2 \! \varphi \sin \! \varphi \right) \right|_{0}^{R} \, \mathrm{d}\varphi \, \mathrm{d}\theta $$

$$ \rho \frac {R^5}{5} \int _{0}^{2\pi} \int _{0}^{\frac{\pi}{2}} \cos^2 \! \theta \sin^3 \! \varphi + \cos^2 \! \varphi \sin \! \varphi \, \mathrm{d}\varphi \, \mathrm{d}\theta $$

The integral of \\( \cos^2 \! \varphi \sin \! \varphi \\) is (again from [Wikipedia](https://en.wikipedia.org/wiki/List_of_integrals_of_trigonometric_functions#Integrands_involving_only_sine))

$$ \int \cos^2 \! \varphi \sin \! \varphi \, \mathrm{d}\varphi = - \frac {\cos^3 \! \varphi}{3} \! $$

Thus

$$ \rho \frac {R^5}{5} \int _{0}^{2\pi} \left. \cos^2 \! \theta \left( \frac {\cos 3\varphi}{12} - \frac{3 \cos \varphi}{4} \right) - \frac {\cos^3 \! \varphi}{3} \! \right|_{0}^{\frac{\pi}{2}} \, \mathrm{d}\theta $$

$$ \rho \frac {R^5}{5} \int _{0}^{2\pi} \cos^2 \! \theta \left( \left( \frac {\cos \frac{3\pi}{2}}{12} - \frac{3 \cos \frac{\pi}{2}}{4} \right) - \left( \frac {\cos 0}{12} - \frac{3 \cos 0}{4} \right) \right) - \left( \frac {\cos^3 \frac{\pi}{2}}{3} - \frac {\cos^3 0}{3} \right) \, \mathrm{d}\theta $$

$$ \rho \frac {R^5}{5} \int _{0}^{2\pi} \cos^2 \! \theta \left( - \left( \frac {1}{12} - \frac{3}{4} \right) \right) - \left( - \frac {1}{3} \right) \, \mathrm{d}\theta $$

$$ \rho \frac {R^5}{5} \int _{0}^{2\pi} \cos^2 \! \theta \left( - \frac {1}{12} + \frac{9}{12} \right) + \frac {1}{3} \, \mathrm{d}\theta $$

$$ \rho \frac {R^5}{5} \int _{0}^{2\pi} \cos^2 \! \theta \frac{2}{3} + \frac {1}{3} \, \mathrm{d}\theta $$

$$ \rho \frac {R^5}{5} \left[ \left. \frac{2}{3} \left( \frac{\theta}{2} + \frac{1}{4} \sin 2\theta \right) + \frac {\theta}{3} \right|_{0}^{2\pi} \right] $$

$$ \rho \frac {R^5}{5} \left[ \left. \frac{1}{6} \sin 2\theta + \frac {2\theta}{3} \right|_{0}^{2\pi} \right] $$

$$ \rho \frac {R^5}{5} \left[ \left( \frac{1}{6} \sin 4\pi + \frac {4\pi}{3} \right) - \frac{1}{6} \sin 0 \right] $$

$$ \rho \frac {R^5}{5} \frac {4\pi}{3} $$

$$ \rho \frac {2 \pi R^3}{3} \frac {2 R^2}{5} $$

$$ \rho V \frac {2 R^2}{5} $$

Finally

$$ I_{zz0} = I_{xx0} = \frac {2}{5} M R^2 $$

Despite the more involved math, the result is identical to \\( I_{yy} \\). Thinking of it qualitatively as the sum of squared distances from the rotation axis across the entire volume, it starts to make sense why they're the same.

According to the parallel axis theorem:

$$ I_{zz0} = I_{zz} + Md^2 $$

The [centroid of a hemisphere](https://xissburg.github.com/2021-05-01-calculating-centroid-hemisphere) is 3/8-ths of the radius above the origin, thus:

$$ I_{zz} = I_{zz0} - Md^2 $$

$$ I_{zz} = \frac {2}{5} M R^2 - M \left( \frac{3}{8} R \right)^2 = \left( \frac {2}{5} - \frac{9}{64} \right) M R^2 = \frac{173}{320} M R^2 $$

With this formula, the moment of inertia of a capsule will be derived in the next article.
