# Word2Vec Implementation

This project implements Word2Vec models using different architectures (Skip-gram and CBOW) and training methods (Softmax and Negative Sampling).

## System Requirements

- Multiple CPU cores
- GPU support (L4 GPU used in development)
- Python 3.x

For detailed system specifications, please refer to the report file.

## Installation

Install the required dependencies:
```
!pip install -r requirements.txt --use-deprecated=legacy-resolver
```

**Note**: The `requirements.txt` file may include some additional libraries that aren't strictly necessary for this Word2Vec implementation. This project does not use any deep learning libraries (such as PyTorch) in the actual implementation, as per project requirements.

## Usage

Run the notebooks in the following order:

1. Data Preprocessing:
   ```
   jupyter notebook preprocessing_main.ipynb
   ```
   Run all cells in this notebook to preprocess the data.

2. Model Training:
   You can run any of the following notebooks in any order, but the recommended sequence is:

   a. Skip-gram with Softmax:
      ```
      jupyter notebook SkipGram_softmax.ipynb
      ```

   b. CBOW with Softmax:
      ```
      jupyter notebook CBOW_softmax.ipynb
      ```

   c. Skip-gram with Negative Sampling:
      ```
      jupyter notebook SkipGram_negativeSampling.ipynb
      ```

## Performance Optimizations

- **Multiprocessing**: The data preprocessing step utilizes multiprocessing to speed up the process.
- **GPU Acceleration**: The implementation uses CuPy instead of NumPy to leverage GPU power for faster computations.

## Implementation Note

This Word2Vec implementation is built from scratch without using any deep learning libraries. While the `requirements.txt` file may list additional libraries (such as PyTorch) that were used for testing or comparison purposes, the core implementation adheres to the project requirement of not using pre-built deep learning models or libraries.