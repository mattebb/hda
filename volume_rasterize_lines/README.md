# Volume Rasterize Lines

Volume Rasterize Lines can be used to create volume representations of curves with variable thickness. In most cases this can be approximated more efficiently by heavily resampling input curves and using Volume Rasterize Particles but in cases where that's not appropriate, this can work too. There's also a bit more control over the feathering off of density away from the curve spine.

Example hip file: https://github.com/mattebb/hda/raw/master/examples/volume_rasterize_lines.hiplc

<img src="https://github.com/mattebb/hda/raw/master/examples/images/volume_rasterize_lines_curve.jpg" width="280"><img src="https://github.com/mattebb/hda/raw/master/examples/images/volume_rasterize_lines_vol.jpg" width="280"><img src="https://github.com/mattebb/hda/raw/master/examples/images/volume_rasterize_lines_slice.jpg" width="280">

It works by creating an implicit distance field of each line segment of a resampled curve, and feathering density in from the zero distance boundary. While a bit more complicated, it's faster than using xyzdist()/primuv().
