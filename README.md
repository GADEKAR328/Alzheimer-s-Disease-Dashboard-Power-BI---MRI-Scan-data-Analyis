# 🧠 Alzheimer's Disease MRI Brain Scan Analysis Dashboard

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)

---

## 📌 Table of Contents

- [Project Overview](#project-overview)
- [Dashboard Preview](#dashboard-preview)
- [Tech Stack](#tech-stack)
- [Features](#features)
- [Dataset](#dataset)
- [Python Feature Extraction](#python-feature-extraction)
- [How to Use](#how-to-use)
- [Project Structure](#project-structure)
- [Author](#author)

---

## 📖 Project Overview

This project analyzes **36,000+ real MRI brain scan images** across **4 Alzheimer's disease stages** using Python for feature extraction and Power BI for interactive visualization.

| Disease Stage | Description |
|---|---|
| 🟢 NonDemented | No signs of Alzheimer's |
| 🟡 Very Mild Demented | Early stage Alzheimer's |
| 🟠 Mild Demented | Moderate Alzheimer's symptoms |
| 🔴 Moderate Demented | Advanced Alzheimer's disease |

---

## 📊 Dashboard Preview

### Page 1 — Overview Dashboard
![Overview Dashboard](screenshots/overview.png)

### Page 2 — Interactive Spreadsheet with MRI Thumbnails
![Spreadsheet](screenshots/spreadsheet.png)

### Filter Panel
![Filter Panel](screenshots/filter.png)

---

## 🛠️ Tech Stack

| Tool | Purpose |
|---|---|
| Python | MRI image feature extraction |
| Pandas | Data manipulation |
| NumPy | Numerical computations |
| Pillow (PIL) | Image processing |
| Scikit-image | Entropy & edge detection |
| Power BI Desktop | Dashboard & visualization |
| GitHub | Image hosting for Power BI |

---

## ✨ Features

- ✅ **36,000+ MRI scans** analyzed with Python
- ✅ **MRI thumbnails** displayed inside Power BI table
- ✅ **KPI Cards** — Disease Progression, Scan Disorder Level, Radiance Progression, Brightness Variation, Center Brightness
- ✅ **Interactive Filter Panel** with range slicers for all metrics
- ✅ **Page Navigation** buttons for smooth UX
- ✅ **Bookmark-based** open/close filter animation
- ✅ **Charts** — Bar chart, Donut chart, Horizontal bar chart
- ✅ **MRI Image Carousels** for Top Diseased & Top Healthy Scans

---

## 🗂️ Dataset

- **Source:** Alzheimer's MRI dataset with 4 labeled categories
- **Total Images:** 36,000+
- **Format:** JPG/PNG brain scan images
- **Categories:**
  - NonDemented
  - VeryMildDemented
  - MildDemented
  - ModerateDemented

---

## 🐍 Python Feature Extraction

Python extracts these features from every MRI scan image:

| Feature | Description |
|---|---|
| `Mean_pixel_intensity` | Average brightness of the brain scan |
| `Std_pixel_intensity` | Variation in pixel brightness |
| `Entropy` | Complexity and disorder in the image |
| `Edge_Density` | Structural clarity of brain tissue |

### Python Script

```python
import os, pandas as pd, numpy as np
from PIL import Image
from skimage.filters import sobel
from skimage.measure import shannon_entropy

IMAGE_ROOT = r"C:\Users\Admin\OneDrive\Desktop\MRI Images"

def detect_label(folder):
    f = folder.lower()
    if "verymild" in f: return "VMildDemented"
    elif "moderate" in f: return "ModerateDemented"
    elif "mild" in f: return "MildDemented"
    else: return "NonDemented"

rows = []
for root, dirs, files in os.walk(IMAGE_ROOT):
    label = detect_label(os.path.basename(root))
    for fname in files:
        if not fname.lower().endswith(('.jpg','.png')): continue
        arr = np.array(Image.open(os.path.join(root, fname)).convert('L'), dtype=np.float64)
        rows.append({
            'Filename'             : fname,
            'First_Label'          : label,
            'Mean_pixel_intensity' : round(np.mean(arr), 2),
            'Std_pixel_intensity'  : round(np.std(arr), 2),
            'Entropy'              : round(float(shannon_entropy(arr)), 2),
            'Edge_Density'         : round(float(np.mean(sobel(arr))), 4),
        })

pd.DataFrame(rows).to_csv('mri_data.csv', index=False)
print("Done!")
```

---

## 🚀 How to Use

### Step 1 — Clone this repository
```bash
git clone https://github.com/GADEKAR328/Alzheimers-Disease-Dashboard.git
```

### Step 2 — Install Python libraries
```bash
pip install pandas numpy pillow scikit-image
```

### Step 3 — Run Python script
```bash
python RUN_THIS.py
```

### Step 4 — Open Power BI
- Open `Alzheimers_Disease_Dashboard_Power_BI.pbix`
- Refresh data source to point to your generated CSV
- Explore the dashboard!

---

## 📁 Project Structure

```
Alzheimers-Disease-Dashboard/
│
├── 📊 Alzheimers_Disease_Dashboard_Power_BI.pbix
├── 🐍 RUN_THIS.py
├── 📄 mri_data_fixed.csv
├── 📁 screenshots/
│   ├── overview.png
│   ├── spreadsheet.png
│   └── filter.png
└── 📄 README.md
```

---

## 🎬 Video Demo

▶️ [Watch Project Demo on YouTube](https://youtu.be/PcG1_ONGnpI)

---

## 👤 Author

**Your Name**
- 💼 [LinkedIn](https://linkedin.com/in/yourprofile)
- 🐙 [GitHub](https://github.com/GADEKAR328)

---

## ⭐ If you found this project helpful, please give it a star!

![Star](https://img.shields.io/github/stars/GADEKAR328/Alzheimers-Disease-Dashboard?style=social)
