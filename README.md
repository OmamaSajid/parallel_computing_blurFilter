# Parallel Image Blurring using MPI (Python)

This project implements a **parallel image blur filter** using **MPI (Message Passing Interface)** in Python.  
The input image is divided into overlapping chunks, processed in parallel by multiple MPI processes, and then combined to produce the final blurred image.

The project also compares **serial vs parallel execution time** to demonstrate the performance benefits of MPI.


## ✨ Features
- Parallel image processing using **mpi4py**
- Supports multiple blur filters:
  - Gaussian Blur
  - Median Blur
  - Box Blur
- Uses overlapping boundaries for smooth edges
- Saves final MPI and serial outputs
- Compares serial and parallel execution times
- Generates result and timing visualizations

---

## 🛠️ Technologies Used
- Python  
- MPI (`mpi4py`)  
- Pillow (PIL)  
- NumPy  
- Matplotlib  

---

## 📂 Project Structure

main.py  

images/ (contains):  
contains chunk images from each MPI process
mpi_blurred_image.png  
serial_blurred_image.png  
README.md  

---

## 🚀 How to Run the Project

### 1️⃣ Install Dependencies
```bash
pip install mpi4py pillow numpy matplotlib

### 2️⃣ Run Using MPI
mpirun -np 4 python main.py
### 3️⃣ Inputs Required
Image filename (with extension)

Blur type: gaussian, median, or box

Blur radius (positive integer)

🖼️ Results and Visualization
Sample Input Image
 ![Image Alt](image_url).
