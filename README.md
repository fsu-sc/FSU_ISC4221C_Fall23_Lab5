# FSU_ISC4221C_Fall23_Lab5
Lab to test image manipulation
# Programming Assignment: Image Manipulation

## Prerequisites:
- Basic understanding of Python programming
- Familiarity with libraries such as OpenCV or PIL for image processing
- Knowledge of image formats, histograms, and image filters

## Tools:
- Python 3.x
- OpenCV (or PIL)
- NumPy
- Matplotlib (for plotting histograms and images)

---

## Question 1: Image Formats Conversion (10 pts)

Write a Python program that converts an image from one format to another (e.g., from JPG to PNG and vice versa).

**Requirements:**
- **Inputs:** Path to the source image, Output file format ('JPG' or 'PNG')
- **Output:** Path where the converted image will be saved
- **Supported formats:** JPG, PNG

---

## Question 2: Image Histogram Plotting

Write a function that takes an image and plots its histogram. 

**Mathematical Model:**
$H(i) = \text{Frequency of intensity level } i \text{ in the image}$

Where $H(i)$ is the height of the histogram at intensity $i$.

**Requirements:**
- Should work on grayscale and color images
- If it's a color image, plot histograms for each channel (R, G, B)

---

## Question 3: Histogram Stretching

Implement histogram stretching to enhance the contrast of an image.

**Mathematical Model:**
$I_{\text{out}} = \frac{(I_{\text{in}} - \text{min})}{(\text{max} - \text{min})} \times (L-1)$
Where \(I_{\text{in}}\) and \(I_{\text{out}}\) are the input and output intensities, \(\text{min}\) and \(\text{max}\) are the minimum and maximum intensities in the input image, and \(L\) is the number of intensity levels.

**Requirements:**
- **Input:** Grayscale image
- **Output:** Grayscale image with enhanced contrast

---

## Question 4: Image Filtering

Implement the Sobel filter, mean filter, and median filter, and apply them to an input image.

**Mathematical Models:**

- **Sobel filter**: 
\[
G_x = \begin{pmatrix} -1 & 0 & 1 \\ -2 & 0 & 2 \\ -1 & 0 & 1 \end{pmatrix} * I,
\]
\[
G_y = \begin{pmatrix} -1 & -2 & -1 \\ 0 & 0 & 0 \\ 1 & 2 & 1 \end{pmatrix} * I
\]
- **Mean filter**: 
\[
I_{\text{out}} = \frac{1}{9} \sum_{i,j \in \text{kernel}} I_{\text{in}}(i,j)
\]
- **Median filter**: 
\[
I_{\text{out}} = \text{median}(I_{\text{in}}(i,j) \text{ for } i,j \in \text{kernel})
\]

**Requirements:**
- **Input:** Grayscale image
- **Output:** Filtered image
- Implement each filter as a separate function
```
---

Feel free to adapt this assignment as needed for your class.
