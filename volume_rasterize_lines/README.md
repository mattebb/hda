# Volume Rasterize Lines

Volume Rasterize Lines can be used to create volume representations of curves with variable thickness. In most cases this can be approximated more efficiently by heavily resampling input curves and using Volume Rasterize Particles but in cases where that's not appropriate, this can work too. There's also a bit more control over the feathering off of density away from the curve spine

![Original Curve](https://github.com/mattebb/hda/raw/master/examples/images/volume_rasterize_lines_curve.jpg)

It works by creating an implicit distance field of each linear segment of  