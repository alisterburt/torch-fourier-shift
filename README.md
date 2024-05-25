# torch-phase-shift

[![License](https://img.shields.io/pypi/l/torch-phase-shift.svg?color=green)](https://github.com/alisterburt/torch-phase-shift/raw/main/LICENSE)
[![PyPI](https://img.shields.io/pypi/v/torch-phase-shift.svg?color=green)](https://pypi.org/project/torch-phase-shift)
[![Python Version](https://img.shields.io/pypi/pyversions/torch-phase-shift.svg?color=green)](https://python.org)
[![CI](https://github.com/alisterburt/torch-phase-shift/actions/workflows/ci.yml/badge.svg)](https://github.com/alisterburt/torch-phase-shift/actions/workflows/ci.yml)
[![codecov](https://codecov.io/gh/alisterburt/torch-phase-shift/branch/main/graph/badge.svg)](https://codecov.io/gh/alisterburt/torch-phase-shift)

*torch-fourier-shift* is a package for shifting 2D and 3D images with subpixel precision 
by applying phase shifts to Fourier transforms in PyTorch.

<figure markdown>
  ![A very simple example](./assets/shift_2d_image.png){ width="500" }
  <figcaption>Shifting a 2D image with torch-fourier-shift</figcaption>
</figure>


```python
import torch
from torch_fourier_shift import fourier_shift_image_2d

# create a dummy image
my_image = torch.tensor(
    [[0, 0, 0, 0, 0, 0],
     [0, 1, 0, 0, 0, 0],
     [0, 0, 0, 0, 0, 0],
     [0, 0, 0, 0, 0, 0],
     [0, 0, 0, 0, 0, 0],
     [0, 0, 0, 0, 0, 0]]
)

# shift the image by 1 pixel in dim 0, 2 pixels in dim 1
shifted_image = fourier_shift_image_2d(image=my_image, shifts=torch.tensor([1, 2]))
```

## Installation

*torch-fourier-shift* is available on PyPI.

```shell
pip install torch-fourier-shift
```

## Usage

Please check the the docs at [teamtomo.org/torch-fourier-shift](https://teamtomo.org/torch-fourier-shift/)



