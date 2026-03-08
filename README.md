# Image Compression with Singular Value Decomposition (SVD)

Machine Learning practical assignment exploring image compression and reconstruction using Singular Value Decomposition (SVD).

The project demonstrates how images can be represented as matrices and compressed by keeping only a subset of their singular values. By reconstructing the image using different subsets of singular values, it is possible to analyse how much visual information is preserved.

---

# Project Structure

```
svd-image-compression/
│
├── svd_image_compression.ipynb
└── README.md
```

---

# Project Overview

The goal of this project is to apply **Singular Value Decomposition (SVD)** to compress grayscale images and analyse how image quality changes when different singular values are used during reconstruction.

Images can be represented as matrices where each element corresponds to the intensity of a pixel. SVD decomposes this matrix into three matrices that capture the underlying structure of the image.

By keeping only a subset of singular values, it is possible to approximate the original image with fewer parameters, effectively achieving compression.

The workflow includes:

1. Loading and preprocessing an image
2. Converting the image to grayscale if necessary
3. Representing the image as a numerical matrix
4. Performing Singular Value Decomposition
5. Reconstructing the image using different subsets of singular values
6. Comparing the reconstructed images with the original

---

# Singular Value Decomposition

For a matrix **A**, SVD decomposes it into three matrices:

```
A = U Σ Vᵀ
```

Where:

- **U** contains the left singular vectors
- **Σ** is a diagonal matrix containing singular values
- **Vᵀ** contains the right singular vectors

The singular values represent the importance of each component in reconstructing the original matrix.

---

# Image Compression Strategy

The compression process consists of reconstructing the image using only a subset of singular values.

Several reconstruction strategies are explored:

### Top k singular values

The image is reconstructed using the **largest singular values**, which usually contain most of the important information.

Smaller values of **k** produce stronger compression but also greater loss of visual quality.

---

### Middle k singular values

The reconstruction uses **singular values from the middle of the spectrum**.

This experiment shows how much information is contained in intermediate components.

---

### Smallest k singular values

The reconstruction uses only the **smallest singular values**.

These components typically contain very little useful information, resulting in poor image reconstruction.

---

# Visualisation

The project displays:

- the **original image**
- reconstructed images using **different values of k**
- reconstructions using **different subsets of singular values**

This allows visual comparison of how image quality degrades as fewer important components are used.

---

# Observations

The experiments demonstrate that:

- The **largest singular values contain most of the visual information** of the image.
- Using only a small number of top singular values can still produce a recognisable reconstruction.
- Middle and smallest singular values contain significantly less useful information.

This illustrates why SVD is effective for **dimensionality reduction and data compression**.

---

# Technologies Used

- Python  
- NumPy  
- Matplotlib  
- Pillow / image processing tools  
- Jupyter Notebook  

---

# Running the Project

Install dependencies:

```
pip install numpy matplotlib pillow
```

Launch Jupyter Notebook:

```
jupyter notebook
```

Open and run:

```
svd_image_compression.ipynb
```

---

# Concepts Demonstrated

- Linear Algebra in Machine Learning
- Singular Value Decomposition
- Image Compression
- Matrix Factorisation
- Dimensionality Reduction
