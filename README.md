# FSU_ISC4221C_Fall23_Lab5

# Programming Assignment: Image Manipulation

You can create one or several python files with your answers. But you must provide a self contained report where you explain what you did.


## Topics:
- Basic understanding of Python programming
- Familiarity with libraries such as OpenCV or PIL for image processing
- Knowledge of image formats, histograms, and image filters

## Tools:
- Python 3.x
- PIL or ImageIO (Talk to the professor if you want to use other library like OpenCV)
- NumPy
- Matplotlib (for plotting histograms and images)


## Question 1: Image Formats Conversion (10 pts)

Write a Python program that converts an image from one format to another (e.g., from JPG to PNG and vice versa).

**Requirements:**
- **Inputs:** Path to the source image, Output file format ('JPG' or 'PNG')
- **Output:** Path where the converted image will be saved
- **Supported formats:** JPG, PNG


## Question 2: Image Histogram Plotting (15 pts)

Write a function that takes an image and plots its histogram. 

**Mathematical Model:**
$H(i) = \text{Frequency of intensity level } i \text{ in the image}$

Where $H(i)$ is the height of the histogram at intensity $i$.

**Requirements:**
- Should work on grayscale and color images
- If it's a color image, plot histograms for each channel (R, G, B)
- In your report show the results of your histograms for the images `rainbow.png`, `rainbow2.png` and
for `cave.png`


## Question 3: Histogram Stretching (15 pts)

Implement histogram stretching to enhance the contrast of an image.

**Mathematical Model:**
$I_{\text{out}} = \frac{(I_{\text{in}} - \text{min})}{(\text{max} - \text{min})} \times (L-1)$
Where $I_{\text{in}}$ and $I_{\text{out}}$ are the input and output intensities, $\text{min}$ and $\text{max}$ are the minimum and maximum intensities in the input image, and $L$ is the number of intensity levels.

**Requirements:**
- **Input:** Grayscale image
- **Output:** Grayscale image with enhanced contrast

In your report show your results for the image `cave_badhist.png`.

## Question 4: Image Filtering (20 pts)

Implement the Sobel filter, mean filter, and median filter, and apply them to an input image.

**Mathematical Models:**

- **Sobel filter**: 

$G_x = \begin{pmatrix} -1 & 0 & 1 \\ -2 & 0 & 2 \\ -1 & 0 & 1 \end{pmatrix} * I$,
$G_y = \begin{pmatrix} -1 & -2 & -1 \\ 0 & 0 & 0 \\ 1 & 2 & 1 \end{pmatrix} * I$

- **Mean filter**: \\ 

$I_{\text{out}} = \frac{1}{9} \sum_{i,j \in \text{kernel}} I_{\text{in}}(i,j)$ 

![matrix](imgs/CodeCogsEqn.pgn)


$G_y = \begin{pmatrix}  \frac{1}{9} &  \frac{1}{9} & \frac{1}{9} \\ \frac{1}{9} &  \frac{1}{9} & \frac{1}{9} \\ \frac{1}{9} &  \frac{1}{9} & \frac{1}{9} \end{pmatrix} * I$

- **Median filter**: \\

$I_{\text{out}} = \text{median}(I_{\text{in}}(i,j) \text{ for } i,j \in \text{3x3 kernel})$

**Requirements:**
- **Input:** Grayscale image
- **Output:** Filtered image
- Implement each filter as a separate function

Test your filters with: 
- Sobel filter: `books.png`
- Mean and median filter: `noise.png`