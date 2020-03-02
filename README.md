# Single cell quantification
Module for single-cell data extraction given a segmentation mask(s) and multi-channel h5 image(s). The CSV structure is aligned with histoCAT output.

**CommandSingleCellExtraction.py**:

* mask_dir: Path to directory where masks are stored (Ex: ./segmentation)

* z_stacks: Path to image(s) for quantification.  (Ex: ./registration/*.h5)

* output: Path to output directory. (Ex: ./feature_extraction)

* channel_names: csv file containing the channel names for the z-stack (Ex: ./my_channels.csv)

* suffix: Series of suffixes applied to the oringal images upon exporting from ilastik/noise removal. Assumes that you only added suffixes to your original images upon quantification (Ex: orignal = my_image.hdf5 -> ilastik -> my_image_probabilities.tif -> segmentation -> my_image_probabilities_mask.tif)

# Run script
python CommandSingleCellExtraction.py --mask_dir ./segmentation  --z_stacks ./registration/Exemplar_001.h5  --output ./feature_extraction --channel_names ./my_channels.csv --suffix _Probabilities_mask

# Developer
Joshua Hess (https://github.com/JoshuaHess12)

Denis Schapiro (https://github.com/DenisSch)
