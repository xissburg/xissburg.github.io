A capsule can be decomposed into a cylinder and two hemispheres, where each hemisphere sits on a cylinder cap. The moment of inertia of a capsule can be calculated as a composition of the [moment of inertia of a cylinder](https://xissburg.github.io/2021-04-30-calculating-moment-of-inertia-cylinder) and the [moment of inertia of a hemisphere](https://xissburg.github.io/2022-09-30-calculating-moment-of-inertia-hemisphere).

Consider a capsule of radius \( R \) and cylindrical length \( L \) centered at the origin with its main axis (i.e. axis of rotational symmetry) aligned with the \( x \) axis on a right-hand coordinate system where \( y \) points up. The total length of the capsule is \( L + 2R \) and its mass is \( M \).

The volume of the cylindrical portion is

$$ V_{cyl} = \pi R^2 L $$

The volume of a hemisphere is

$$ V_{hemi} = \frac{2 \pi R^3}{3} $$

The volume of the capsule is the sum

$$ V = V_{cyl} + 2 V_{hemi} $$

Thus, the mass of the cylindrical portion is

$$ M_{cyl} = \frac{V_{cyl}}{V} M $$

and the mass of a hemisphere is

$$ M_{hemi} = \frac{V_{hemi}}{V} M $$

The moment of inertia of the cylindrical portion along the \( x \) axis is:

$$ I_{cyl \, xx} = \frac {M_{cyl} R^2}{2} $$

The moment of inertia of one of the hemispheres along the \( x \) axis is:

$$ I_{hemi \, xx} = \frac{2}{5} M_{hemi} R^2 $$

Thus, the moment of inertia of the capsule along the \( x \) axis is the sum:

$$ I_{xx} = I_{cyl \, xx} + 2 I_{hemi \, xx} = \frac {M_{cyl} R^2}{2} + \frac{4}{5} M_{hemi} R^2 = \frac{\left( 5 M_{cyl} + 8 M_{hemi} \right) R^2}{10} $$

The moment of inertia of a cylinder along the \( z \) or \( y \) axis is

$$ I_{cyl \, yy} = I_{cyl \, zz} = \frac{M_{cyl}}{12} \left( L^2 + 3 R^2 \right) $$

The moment of inertia of a hemisphere along the \( z \) or \( y \) axis is

$$ I_{hemi \, yy} = I_{hemi \, zz} = \frac{2}{5} M_{hemi} R^2 $$

The moment of inertia of the capsule along the \( y \) and \(z\) axes are the same due to symmetry. Let's calculate \( I_{zz} \) using the parallel axis theorem to add the moment of inertia of the hemispheres whose center of mass is at a distance of \( L/2 + 3R/8 \) from the origin.

$$ I_{zz} = I_{cyl \, zz} + 2 \left( I_{hemi \, zz} + M_{hemi} \left( \frac{L}{2} + \frac{3}{8} R \right)^2 \right) $$

$$ = I_{cyl \, zz} + 2 I_{hemi \, zz} + M_{hemi}  \frac{(4L + 3R)^2}{32} $$

Likewise

$$ I_{yy} = I_{cyl \, yy} + 2 I_{hemi \, yy} + M_{hemi}  \frac{(4L + 3R)^2}{32} $$
