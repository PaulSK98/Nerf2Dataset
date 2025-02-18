# Automating 3D Dataset Generation with Neural Radiance Fields

[![Conference: ROBOVIS 2025](https://img.shields.io/badge/Conference-ROBOVIS%202025-blue.svg)](https://robovis.org)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Dataset](https://img.shields.io/badge/Data-Download-orange)](link_to_dataset)
[![Paper](https://img.shields.io/badge/Paper-PDF-red)](link_to_paper)
![Teaser Image](figures/Teaser.png)

Authors: **Paul Schulz** (OVGU Magdeburg)   **Thorsten Hempel** (OVGU Magdeburg)   **Ayoub Al-Hamadi** (OVGU Magdeburg)  

##  Key Contributions

✅ **End-to-end automated dataset generation pipeline for monocular 3D Detection/6D Pose Estimation**  
✅ **Combines textured mesh creation via Neural Rendering and SoTA synthetic datset generation to create datasets for arbitrary complex objects**  
✅ **Capable of training performant 6D pose estimation models**  
✅ **Requires minimal resources and manual intervention**  

---
## 📌 Pipeline Overview
![Pipeline Image](figures/Pipeline.png)

### 1️⃣ **Object Capturing**
- Capturing 2D images of the target object using a **rotating plate** and a **static camera**  
- Using **Structure from Motion (SfM)** for camera pose estimation 
- Applying **foreground extraction** for object segmentation  

### 2️⃣ **Model Generation**
- Training a **Radiance Field** to create **meshes**  
- Refining meshes for high fidelity through **vertex and face optimization**  
- Mapping of  **diffuse texture** to generate **textured mesh** 

### 3️⃣ **Synthetic Dataset Generation**
- Creating **3D scenes** with virtual cameras, lighting, and background variations  
- Performing **automated annotation** (bounding boxes, segmentation, etc.)  
- Generating diverse datasets for **robust training of pose estimation models** 


---

## 🎯 Results

<table>
  <tr>
    <td>
      <img src="figures/Elephant.jpg" onmouseover="this.src='figures/Elephant.gif';" onmouseout="this.src='figures/Elephant.jpg';" width="300">
    </td>
    <td>
      <img src="figures/Remote.jpg" onmouseover="this.src='figures/Remote.gif';" onmouseout="this.src='figures/Remote.jpg';" width="300">
    </td>
    <td>
      <img src="figures/Multimeter.jpg" onmouseover="this.src='figures/Multimeter.gif';" onmouseout="this.src='figures/Multimeter.jpg';" width="300">
    </td>
  </tr>
</table>



---

## 🚀 Getting Started

### 🔧 Installation

```bash
git clone https://github.com/PaulSK98/Nerf2Dataset.git
cd Nerf2Dataset
pip install -r requirements.txt

