# rekall: spatiotemporal query language

[![Build Status](https://travis-ci.com/scanner-research/rekall.svg?branch=master)](https://travis-ci.com/scanner-research/rekall)
[![Documentation Status](https://readthedocs.org/projects/rekallpy/badge/?version=latest)](https://rekallpy.readthedocs.io/en/latest/?badge=latest)

Rekall is a spatiotemporal query language. It operates over sets of intervals
and allows for combining and filtering on temporal and spatial predicates.

Rekall has a main [Python API](https://github.com/scanner-research/rekall/tree/master/rekallpy)
for all the core interval processing operations. Rekall also has a
[Javascript API](https://github.com/scanner-research/rekall/tree/master/rekalljs)
which we use for the [vgrid](https://github.com/scanner-research/vgrid) video
metadata visualization widget.

## Getting Started
* Quickly [set up](#setup) your environment
* Try out the [tutorials](tutorials/)
* Check out the [documentation](https://rekallpy.readthedocs.io/en/latest/?badge=latest)
* View the [developer guide](#developer-guidelines)

## Sample Usage
Put something here...

## Setup
[1] Install anaconda:  
Instructions here: https://www.anaconda.com/download/

[2] Clone the repository:
```
git clone https://github.com/scanner-research/rekall.git
cd rekall
```

[3] Create virtual environment:
```
conda stuff
source stuff
```
This creates a virtual environment and installs `rekall`, `vgrid`, and
`vgrid_jupyter` (our video visualization libraries). In particular, we install
`python3`, `pip`, and `npm` in the environment, and `ffmpeg` for `vgrid`'s
video visualization. 

[4] Run unit tests:
```
cd rekallpy
python -m unittest discover test
```
If the tests run successfully, you should see 50+ dots followed by
"Ran XX tests in XXs." and "OK".

Check out the [tutorials](tutorials/) to get familiar with the Rekall API!

Or, to use Rekall in another project/environment (Python3 required):

```
pip install rekallpy
npm install --save @wcrichto/rekall
```

## Developer Guidelines
If you are interested in contributing to Rekall (and we welcome contribution
via pull requests!), follow the [setup](#setup) guidelines above, and then
install `rekallpy` and `rekalljs` from source:

UNININSTALL AND LINK NEW PACKAGES

If you are making changes to `rekalljs`, you will also need to install `vgrid`
and `vgrid_jupyter` from source:

UNINSTALL AND LINK NEW PACKAGES

### Python API

#### Through pip

```
pip3 install rekallpy
```

#### From source

```
git clone https://github.com/scanner-research/rekall
cd rekall/rekallpy
pip3 install -e .
```

### Javascript API

You must have [npm](https://www.npmjs.com/get-npm) already installed.

#### Through npm

```
npm install --save @wcrichto/rekall
```

#### From source

```
git clone https://github.com/scanner-research/rekall
cd rekall/rekalljs
npm install
npm run prepublishOnly
npm link
```
