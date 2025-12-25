
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

## 🛠️ Technologies Used
- Python  
- MPI (`mpi4py`)  
- Pillow (PIL)  
- NumPy  
- Matplotlib  

## 📂 Project Structure
```
project/
├── main.py
├── images/
│   ├── chunk_images/           # Contains chunk images from each MPI process
│   ├── mpi_blurred_image.png
│   └── serial_blurred_image.png
├── results/
│   ├── comparison_plot.png
│   └── timing_results.txt
└── README.md
```

## 🚀 How to Run the Project

### 1️⃣ Install Dependencies
```bash
pip install mpi4py pillow numpy matplotlib
```

### 2️⃣ Run Using MPI
```bash
mpirun -np 4 python main.py
```

### 3️⃣ Inputs Required
When prompted, provide:
- Image filename (with extension, e.g., `input.jpg`)
- Blur type: `gaussian`, `median`, or `box`
- Blur radius (positive integer, e.g., `3`)

## 📊 Results and Visualization

### Sample Input Image
![Sample Input](image/origanl.jpeg)

*Note: If the image above doesn't display, you can view it directly [here](https://github.com/OmamaSajid/parallel_computing_blurFilter/blob/main/image/origanl.jpeg)*

### Expected Outputs:
1. **Serial Blurred Image** - Processed using single-core execution
2. **Parallel Blurred Image** - Processed using MPI parallel processing
3. **Performance Comparison Plot** - Visual comparison of execution times
4. **Timing Results** - Text file with detailed execution time data

## 📈 Performance Comparison
The project automatically generates:
- Execution time comparison between serial and parallel implementations
- Speedup calculation: `Speedup = Serial Time / Parallel Time`
- Visualization of timing results using matplotlib

## 🔧 Customization
You can modify the following parameters in the code:
- Number of MPI processes (change `-np` value)
- Blur radius intensity
- Input image path
- Output directory structure

## 🤝 Contributing
Feel free to fork this repository and submit pull requests for:
- Additional blur filters
- Performance optimizations
- Code improvements
- Documentation enhancements

## 📄 License
This project is open-source and available under the MIT License.

## 👥 Author
**Omama Sajid**  
GitHub: [OmamaSajid](https://github.com/OmamaSajid)

---

*Last Updated: December 2024*
```

**Key fixes applied:**
1. Properly formatted headings with consistent markdown syntax
2. Fixed the code block formatting with proper triple backticks
3. Corrected the image URL formatting
4. Added alternative text and direct link for the image
5. Improved project structure visualization with tree format
6. Added missing sections (License, Author, Contributing)
7. Fixed typos and improved readability
8. Added proper section organization with emoji icons for visual clarity
