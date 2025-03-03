# rgbmaker  [![astropy](http://img.shields.io/badge/powered%20by-AstroPy-orange.svg?style=flat)](http://www.astropy.org/)   [![PyPI - Python Version](https://img.shields.io/pypi/v/rgbmaker.svg)](https://pypi.org/project/rgbmaker/) [![PyPI - Python Version](https://img.shields.io/pypi/pyversions/rgbmaker)](https://pypi.org/project/rgbmaker/) [![Documentation Status](https://readthedocs.org/projects/rgbmaker/badge/?version=latest)](https://rgbmaker.readthedocs.io/en/latest/?badge=latest) ![PyPI - Downloads](https://img.shields.io/pypi/dm/rgbmaker)
A python package which communicates to different astronomical services and fetches fits and numerical data.

# Developement
```bash
$ pip install -e .[dev]
```

# Installation:
```bash
$ pip install rgbmaker
```

# Usage
```bash
$ rgbmaker -h
usage: rgbmaker [-h] [-p POSITION] [-r RADIUS] [-i IMAGESOPT] [-n NAME] [-a ARCHIVES] [-k KIND] [-s SPIDX_FILE]
                [-px PIXELS] [-A ANNOT]

A python package which communicates to different 
astronomical services and fetches fits and numerical data.

optional arguments:
  -h, --help            show this help message and exit
  -p POSITION, --position POSITION
                        (Required) The object name or the coordinates of the object in the FK5 (J2000) system. Ex: "14 09 48.86
                        -03 02 32.6", M87, NGC1243, without quotes.
  -r RADIUS, --radius RADIUS
                        (Required) (default = 0.12) (float) The size of the image in degrees, this size will be used for the field
                        of view in the resultant image. For reference, in the night sky, the moon is about 0.52 degrees across.
  -i IMAGESOPT, --imagesopt IMAGESOPT
                        (default=2)(string)(values=1,2,3) IOU ROR Optical (option = 1) Composite Contours on DSS2R (option = 2)
  -n NAME, --name NAME  (Optional) (default=Anonymous) (string) Your name will be displayed on the image enabling mentors,
                        professors, fellow students to be able to recognize your work. Credit is important!
  -a ARCHIVES, --archives ARCHIVES
                        (default=1)(string) This option currently offers access to the NVAS image archive. Selecting this option
                        will return the top 5 results from NVAS (if exists). These can be downloaded as .imfits files
  -k KIND, --kind KIND  (default='base64') choose from base64, plot, png, jpg to show base64 of resultant image, plot on output,
                        save png/jpg files
  -s SPIDX_FILE, --spidx_file SPIDX_FILE
                        (Default=None) enter path to spidx.fits file that contains spectral index data.
  -px PIXELS, --pixels PIXELS
                        (default=480) change pixel value for the final resulatant image.
  -A ANNOT, --annot ANNOT
                        (default=True) remove any annotation by setting this to False.
  -S FLUX_LIST, --flux_list FLUX_LIST
                        (Optional) (Default=None) Takes input as list for spectral index calculation.
  -S_e FLUX_ERROR, --flux_error FLUX_ERROR
                        (Optional) (Default=None) Takes input as list for spectral index calculation.
  -freq FREQ_LIST, --freq_list FREQ_LIST
                        (Optional) (Default=None) Takes input as list for spectral index calculation.
```

```py
$ python3.8

> from rgbmaker.fetch import query
> result = query(name='Avi', position='3C 33.1', radius=0.12, kind='jpg')
> print(result)
```
# Demo


[![asciicast](https://asciinema.org/a/uvMgrVQBJwUCmR3C22J7qxBMA.svg)](https://asciinema.org/a/uvMgrVQBJwUCmR3C22J7qxBMA)

