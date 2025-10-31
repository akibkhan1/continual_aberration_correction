# continual_aberration_correction

Download the DIV2K dataset using these links

> https://data.vision.ee.ethz.ch/cvl/DIV2K/DIV2K_train_HR.zip

> https://data.vision.ee.ethz.ch/cvl/DIV2K/DIV2K_valid_HR.zip

The DIV2K High-Resolution (HR) dataset is a collection of high-quality natural images designed primarily for image super-resolution research. It contains:

Training set: 800 high-resolution images (DIV2K_train_HR), each with a resolution around 2K (≈2040×1080). These images cover a wide variety of real-world scenes: urban, rural, indoor, and natural.

Validation set: 100 high-resolution images (DIV2K_valid_HR), drawn from the same distribution as the training images, used for quantitative and qualitative evaluation.

All images are stored in PNG format without compression artifacts to preserve visual fidelity.

Download the PSFs for different lens from this link

> https://edmond.mpdl.mpg.de/file.xhtml?fileId=101784&version=1.0

PSF Data Description: The zip file contains MATLAB files, one for each lens and aperture setting. Each MATLAB file contains a cell-array C, the array has the size (N,4), N being the number of measured PSF-patches for the given lens/aperture combination. N is on the order of 4000. The 4 entries are: 1: x-position, 2: y-position, 3: index of the exposure time, 4: 111x111x3 RGB patch of a PSF. The x/y-positions are the the pixels of the Canon 5DSR sensor.

Run `get_blurred_dataset.py` to generate blurred dataset for a particular lens system.
