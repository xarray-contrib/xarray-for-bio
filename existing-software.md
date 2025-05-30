# Software using Xarray

```{note}
Do you know of something that should be included here? Please open an Issue or Pull Request on [Github](https://github.com/xarray-contrib/xarray-for-bio/issues) to add it!
```



- [sgkit](https://sgkit-dev.github.io/sgkit/latest/index.html)
- [spatial-data](https://spatialdata.scverse.org/en/latest/index.html) and the packages that build uses `Xarray`
    - Internally it uses the [multi-scale-spatialimage](https://github.com/spatial-image/multiscale-spatial-image?tab=readme-ov-file#multiscale-spatial-image) library to convert [OME-NGFF](https://ngff.openmicroscopy.org/) formatted data into `Xarray.DataTree`s of `Dataset`s
- [Napari](https://napari.org/stable/) supports displaying Xarray. See [Example](https://napari.org/dev/gallery/xarray-latlon-timeseries.html)


