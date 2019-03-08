# Volume Smear

Volume Smear is like a directional blur for volumes (3D or 2D). The blur direction can be supplied as a single vector, or with a custom vector volume field. For doing simple directional blurs along the X, Y, or Z axis, Houdini's built in Volume Blur is much faster, but this is useful for more complex situations.

It's also possible to use custom filter kernels supplied as additional input vector volumes. This will weight the blur samples by the x axis of the volume, allowing you to have custom intensity falloffs or colour shifting.

Surface SDF field generated from a particle system, smeared along simulation velocity vectors:

![Smeared particle surface](https://github.com/mattebb/hda/raw/master/examples/images/volume_smear_particles.jpg)


A 2D colour vector volume smeared by a directional noise field, using a colour spectrum ramp as a custom filter kernel.

![Custom filter (spectrum ramp)](https://github.com/mattebb/hda/raw/master/examples/images/volume_smear_spectrum.gif)

A 3D colour vector volume (mandril texture) smeared with a refractive crystal effect, using a specctrum ramp as a custom filter kernel

![Custom filter (spectrum ramp)](https://github.com/mattebb/hda/raw/master/examples/images/volume_smear_mandril.gif)
