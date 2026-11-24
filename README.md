# COU07506 Digital Signal Processing Labs

This repository contains the practical laboratory work for **COU 07506: Digital
Signal Processing** at the Dar es Salaam Institute of Technology. The project
is organized by teaching week and uses Jupyter notebooks to demonstrate core
discrete-time signal and system concepts with Python.

## Learning progression

The labs build from basic signal generation to sampling and finally to
systems, convolution, correlation, and difference equations:

| Week | Topic | Main activities |
| --- | --- | --- |
| [Week 1](Week-01/) | Elementary discrete-time signals and audio | Generate impulse, step, ramp, exponential, and periodic signals; load and analyze a voice recording |
| [Week 2](Week-02/) | Sampling, aliasing, and quantization | Demonstrate aliasing, compare downsampling and decimation, implement a uniform quantizer, measure SQNR, and quantize voice |
| [Week 3](Week-03/) | Convolution, correlation, and difference equations | Implement convolution manually, smooth noisy signals, test linearity and time invariance, estimate delays, and analyze discrete-time systems |

## Repository structure

```text
COU07506-DSP-Labs/
├── requirements.txt
├── Week-01/
│   ├── COU07506_Week01_240242462281.ipynb
│   └── my_voice.wav
├── Week-02/
│   └── COU07506_Week02_240242462281.ipynb
└── Week-03/
    └── COU07506_Week03_240242463081.ipynb
```

`my_voice.wav` is the audio input used by the Week 1 and Week 2 audio
experiments. Keep it at the shown location so the relative paths in the
notebooks resolve correctly.

## Requirements

- Python 3
- Jupyter Notebook or JupyterLab
- Packages listed in [`requirements.txt`](requirements.txt), including:
  - NumPy
  - SciPy
  - Matplotlib
  - IPython and Jupyter components

## Installation

From the project root, create and activate a virtual environment, then install
the pinned dependencies:

```powershell
py -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install -r requirements.txt
```

If PowerShell script execution is restricted, activate the environment from a
Command Prompt instead:

```bat
.venv\Scripts\activate.bat
```

## Running the labs

Start Jupyter from the project root:

```powershell
jupyter notebook
```

Open a notebook from its corresponding week folder and run the cells from top
to bottom. Running cells sequentially is recommended because later sections
reuse signals, functions, and variables created earlier.

## Lab highlights

### Week 1

- Generates elementary sequences using NumPy.
- Visualizes discrete-time signals with Matplotlib.
- Compares periodic signals and evaluates signal values.
- Loads, plays, and inspects `my_voice.wav`.
- Includes analysis and pre-lab questions about DSP devices and signals.

### Week 2

- Uses the Nyquist criterion to explain aliasing.
- Samples a sinusoid at multiple sampling rates.
- Compares naive audio downsampling with proper decimation.
- Implements a configurable uniform quantizer.
- Verifies the approximate 6 dB SQNR improvement per additional bit.
- Tests voice quantization at 4, 8, and 12 bits.

### Week 3

- Implements linear convolution using nested loops and compares it with
  `numpy.convolve`.
- Applies convolution as a moving-average smoother for noisy data.
- Tests linearity and time invariance experimentally.
- Uses cross-correlation to estimate a hidden signal delay and examines the
  effect of noise.
- Computes impulse and step responses from difference equations using
  `scipy.signal.lfilter`.

## Notes

- The notebooks are educational lab records and include explanatory markdown,
  calculations, plots, and experimental observations.
- Audio playback may require a working notebook audio backend and speakers or
  headphones.
- Re-running a notebook may replace or refresh displayed outputs; save the
  notebook if updated outputs need to be retained.

