
# Image Segmentation and Analysis Project

This project involves segmenting grayscale images to identify and analyze distinct phases or features. The project is divided into two tasks:

---

## **Task 1: Segment Image into 4 Phases**
### **Objective**
Segment the provided image into the following phases:
1. **Dark (Air):** Regions with low intensity values (background air/voids).
2. **Hollow/Void (Air Encircled by Bright Solid):** Circular or void areas surrounded by solid.
3. **Hollowed-Solid:** Bright solid regions containing small voids.
4. **Non-Hollow Solid:** Fully solid bright regions with no voids.

### **Steps:**
1. Load the image and preprocess it by applying Gaussian blur to reduce noise.
2. Apply global thresholding to segment different intensity-based phases.
3. Use morphological operations to refine the segmentation.
4. Label connected components for classification into the specified phases.
5. Calculate the area fraction of each phase:
   - Percentage of the total image area occupied by each phase.
6. Visualize and analyze the segmentation results.

### **Output:**
- Segmented images for each phase.
- A report detailing the area fraction of each phase.

---

## **Task 2: Analyze Circular and Non-Circular Particles**
### **Objective**
Segment the image into:
1. **Air (Background):** Dark regions (voids).
2. **Circular Particles:** Bright circular regions based on a circularity threshold.
3. **Non-Circular Particles:** Bright irregular regions.

### **Steps:**
1. Load the image and preprocess it by applying Gaussian blur to reduce noise.
2. Use thresholding to separate particles from the background.
3. Remove border particles and refine the shapes using morphological operations.
4. Label connected components and analyze their properties (e.g., area, perimeter, centroid).
5. Classify particles based on circularity (calculated as `4 * π * (area / perimeter²)`).
6. Calculate the following metrics:
   - Number of circular particles.
   - Average diameter and standard deviation of circular particles.
   - Area ratios of circular and non-circular particles.
7. Visualize the segmented masks for circular and non-circular particles.

### **Output:**
- Visualizations for segmented circular and non-circular particles.
- Metrics:
  - Number of circular particles.
  - Average diameter and its standard deviation.
  - Area ratio of circular vs. non-circular particles.

---

## **Setup and Requirements**
### **Dependencies**
Install the required libraries:
- Python 3.x
- OpenCV
- NumPy
- Matplotlib
- Scikit-Image
- SciPy

Install the dependencies using:
```bash
pip install opencv-python-headless numpy matplotlib scikit-image scipy
```



## **Example Metrics**
### Task 1 (Phases):
- **Dark (Air):** 30.4% of total area.
- **Hollow/Void:** 15.7% of total area.
- **Hollowed-Solid:** 20.1% of total area.
- **Non-Hollow Solid:** 33.8% of total area.

### Task 2 (Particles):
- **Number of Circular Particles:** 62.
- **Average Diameter of Circular Particles:** 6.29 pixels.
- **Standard Deviation of Diameters:** 4.18 pixels.
- **Area Ratio of Circular Particles:** 2.86%.
- **Area Ratio of Non-Circular Particles:** 29.85%.

---

