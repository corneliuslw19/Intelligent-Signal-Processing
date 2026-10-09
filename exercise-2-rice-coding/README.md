# Lossless Audio Compression Using Rice Coding

## Overview
This project implements a lossless audio compression and decompression system in Python 
using Differential Pulse Code Modulation (DPCM), ZigZag mapping, and Rice coding.
The implementation processes WAV audio files and evaluates compression efficiency using two Rice parameters, K=2 and K=4.
The project demonstrates fundamental lossless compression techniques, parameter comparison, and 
verification of reconstructed audio data.

## Features
- Reads uncompressed WAV audio files.
- Applies first-order Differential Pulse Code Modulation (DPCM) to calculate prediction residuals.
- Uses ZigZag mapping to convert signed residuals into non-negative integers.
- Implements Rice encoding and decoding using K=2 and K=4.
- Saves compressed audio data in a custom `.ex2` file format.
- Reconstructs the original audio signal through inverse ZigZag mapping and inverse DPCM.
- Verifies lossless reconstruction using `numpy.array_equal()`.

## Technologies Used
- Python
- NumPy
- SciPy
- Jupyter Notebook

## Project Structure
```text
Exercise-2/
├── README.md
├── requirements.txt
├── rice_coding.ipynb
├── audio/              # User-provided WAV files (not included)
└── results/            # Generated compressed and reconstructed files
```

The original coursework audio files and generated audio outputs are excluded from the public repository.

## How It Works
1. **Audio Loading:** Reads WAV audio samples from the input directory.
2. **DPCM:** Calculates the difference between consecutive audio samples to obtain prediction residuals.
3. **ZigZag Mapping:** Converts signed residuals into non-negative integers.
4. **Rice Encoding:** Compresses the mapped values using Rice parameters K=2 and K=4.
5. **File Generation:** Saves the encoded data in a custom `.ex2` format.
6. **Decoding:** Reverses Rice coding and ZigZag mapping to recover the residuals.
7. **Audio Reconstruction:** Uses inverse DPCM to reconstruct the original audio samples.
8. **Verification:** Compares reconstructed samples with the originals using `numpy.array_equal()`.

## Installation
Install the required Python libraries:

```bash
pip install numpy scipy notebook
```

Alternatively, if a `requirements.txt` file is provided:

```bash
pip install -r requirements.txt
```

## Running the Project
1. Download or clone the repository.
2. Obtain two compatible, uncompressed PCM WAV audio files that you have permission to use.
3. Create an `audio/` directory inside `Exercise-2/` if it does not already exist.
4. Place the WAV files inside `audio/`.
5. Rename the files to `Sound1.wav` and `Sound2.wav`, or update the `SOUND_FILES` list in `rice_coding.ipynb` to match your filenames.
6. Open `rice_coding.ipynb` in VS Code or Jupyter Notebook, with `Exercise-2/` as the working directory.
7. Run the notebook cells in order.

The notebook generates compressed `.ex2` files and reconstructed WAV files inside the `results/` directory.

**Note:** Different audio samples may produce significantly different compression results. 
The compression statistics below were obtained using the original coursework audio files.

## Compression Results
The original experiment evaluated two audio samples using K=2 and K=4.
| Audio File | K=4 | K=2 |
|---|---|---|
| Sound1.wav | 14.43% compression | 142.48% expansion |
| Sound2.wav | 5,534.01% expansion | 22,339.16% expansion |

For Sound1, K=4 achieved positive compression, while K=2 increased the file size.

For Sound2, both parameters produced substantial file expansion, demonstrating that 
fixed-parameter Rice coding is not equally effective for all audio signals.

The decoded audio samples were verified against the originals using `numpy.array_equal()`, confirming 
lossless reconstruction in the original experiments.

## Dataset Availability
The original WAV audio samples were provided for university coursework and are not redistributed in this public repository.

Users who wish to reproduce the implementation should provide their own appropriately licensed PCM WAV audio files. 
The results may differ depending on the characteristics of the supplied audio.

The generated compressed `.ex2` files and reconstructed WAV files from the original experiments are also excluded.

## Limitations
- Rice coding efficiency depends on the distribution of prediction residuals.
- Fixed Rice parameters may produce significant file expansion for certain audio signals.
- The implementation is designed for compatible WAV audio inputs rather than arbitrary audio formats.
- Different audio samples may require different Rice parameters for better compression efficiency.

Potential improvements include adaptive Rice parameter selection and more advanced prediction techniques.

## Conclusion
This project demonstrates the implementation of a lossless audio compression and decompression 
workflow using DPCM, ZigZag mapping, and Rice coding.
The experiments highlight the importance of parameter selection and input data 
characteristics in compression performance, while sample-level verification confirms the correctness of the reconstruction process.