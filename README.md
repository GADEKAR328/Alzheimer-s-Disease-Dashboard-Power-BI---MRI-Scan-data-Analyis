# 🧠 Alzheimer's Disease MRI Brain Scan Analysis Dashboard

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)

> **An end-to-end Data Analytics project analyzing 36,000+ real MRI brain scan images to detect and visualize Alzheimer's Disease progression using Python & Power BI.**

---

## 📌 Table of Contents

| | |
|---|---|
| [📖 Project Overview](#-project-overview) | [🗂️ Dataset](#️-dataset) |
| [📊 Dashboard Preview](#-dashboard-preview) | [🐍 Python Feature Extraction](#-python-feature-extraction) |
| [🛠️ Tech Stack](#️-tech-stack) | [🚀 How to Use](#-how-to-use) |
| [✨ Features](#-features) | [📁 Project Structure](#-project-structure) |
| [🔬 How It Works](#-how-it-works) | [👤 Author](#-author) |

---

## 📖 Project Overview

Alzheimer's Disease is one of the most common neurodegenerative disorders affecting millions worldwide. Early detection through MRI brain scans can significantly improve patient outcomes.

This project builds a **fully interactive Power BI dashboard** that:
- Processes **36,000+ MRI brain scan images** using Python
- Extracts **pixel-level image features** (Mean Intensity, Std, Entropy, Edge Density)
- Visualizes disease progression across **4 Alzheimer's stages**
- Displays **actual MRI thumbnails** inside Power BI table rows
- Provides **dynamic filtering** by disease label and image metrics

| Disease Stage | Label | Description |
|---|---|---|
| 🟢 No Dementia | NonDemented | Healthy brain — no signs of Alzheimer's |
| 🟡 Very Mild | VMildDemented | Earliest detectable stage of Alzheimer's |
| 🟠 Mild | MildDemented | Noticeable memory loss and cognitive decline |
| 🔴 Moderate | ModerateDemented | Significant brain tissue deterioration visible |

---

## 📊 Dashboard Preview

### 🔹 Page 1 — Overview Dashboard
> KPI Cards, MRI Image Carousels, Charts & Statistics

![Page 1 Dashboard Overview](https://raw.githubusercontent.com/GADEKAR328/Alzheimer-s-Disease-Dashboard-Power-BI---MRI-Scan-data-Analyis/2ace70dd21d8619f90345d73202d8c2fbc32d77d/Page1%20Dashboard%20Overview.jpg)

---

### 🔹 Page 2 — Interactive MRI Image Spreadsheet
> Actual MRI scan thumbnails with extracted feature metrics per row

![Page 2 MRI Images Spreadsheet](https://raw.githubusercontent.com/GADEKAR328/Alzheimer-s-Disease-Dashboard-Power-BI---MRI-Scan-data-Analyis/2ace70dd21d8619f90345d73202d8c2fbc32d77d/Page%202%20Image%20Spreadsheet.jpg)

---

### 🔹 Dynamic Filter Panel
> Bookmark-based filter panel with range slicers and label dropdown

![Filter Panel](https://raw.githubusercontent.com/GADEKAR328/Alzheimer-s-Disease-Dashboard-Power-BI---MRI-Scan-data-Analyis/2ace70dd21d8619f90345d73202d8c2fbc32d77d/Filter.jpg)

---

### 🔹 MRI Fixed Data with Image Links
> CSV data with GitHub-hosted image URLs loaded into Power BI

![MRI Fixed Data Links](https://raw.githubusercontent.com/GADEKAR328/Alzheimer-s-Disease-Dashboard-Power-BI---MRI-Scan-data-Analyis/2ace70dd21d8619f90345d73202d8c2fbc32d77d/MRI%20Fixed%20Data%20Link.jpg)

---

### 🔹 Python Feature Extraction Script (Spyder)
> Running the extraction script in Spyder IDE

![Extract Python Script](https://raw.githubusercontent.com/GADEKAR328/Alzheimer-s-Disease-Dashboard-Power-BI---MRI-Scan-data-Analyis/2ace70dd21d8619f90345d73202d8c2fbc32d77d/Extract_py.jpg)

![Spyder Image Extraction](https://raw.githubusercontent.com/GADEKAR328/Alzheimer-s-Disease-Dashboard-Power-BI---MRI-Scan-data-Analyis/2ace70dd21d8619f90345d73202d8c2fbc32d77d/Spyder%20img%20extract%20by%20py.jpg)

---

## 🛠️ Tech Stack

| Tool / Library | Version | Purpose |
|---|---|---|
| **Python** | 3.12 | Core scripting & image processing |
| **Pandas** | Latest | Data manipulation & CSV export |
| **NumPy** | Latest | Numerical array computations |
| **Pillow (PIL)** | Latest | Image loading & grayscale conversion |
| **Scikit-image** | Latest | Shannon Entropy & Sobel Edge Detection |
| **Power BI Desktop** | Latest | Dashboard design & visualization |
| **Spyder IDE** | 6.x | Python development environment |
| **GitHub** | — | Public image hosting for Power BI URLs |
| **Google Drive** | — | MRI dataset storage |

---

## ✨ Features

### Dashboard Features
- ✅ **36,000+ MRI scans** processed and analyzed with Python
- ✅ **Real MRI thumbnails** displayed inside Power BI table rows
- ✅ **5 KPI Cards** — Disease Progression, Scan Disorder Level, Radiance Progression, Brightness Variation, Center Brightness
- ✅ **MRI Image Carousels** — Top Diseased Scans & Top Healthy Scans
- ✅ **Pixel Intensity Statistics** — Grouped bar chart by disease stage
- ✅ **Neuroimage Entropy Levels** — Donut chart with percentage breakdown
- ✅ **Structural Clarity in Brain Scans** — Horizontal bar chart
- ✅ **Dynamic Filter Panel** — Bookmark-based open/close animation
- ✅ **Range Slicers** — Filter by Mean Pixel, Std Pixel, Entropy, Edge Density
- ✅ **Label Dropdown** — Filter by disease category
- ✅ **Page Navigation Buttons** — Overview, Spreadsheet, Filter
- ✅ **Clear All Slicers** button for quick reset

### Technical Features
- ✅ **Batch image processing** — handles 36,000+ images efficiently
- ✅ **Auto-label detection** from subfolder names
- ✅ **Checkpoint saving** every 500 images — resume if interrupted
- ✅ **GitHub raw URLs** used for Power BI image rendering
- ✅ **Data Category: Image URL** set in Power BI for thumbnail display

---

## 🔬 How It Works

```
MRI Images (Google Drive)
        ↓
Python Script (Spyder)
  → Load each image as grayscale array
  → Extract: Mean, Std, Entropy, Edge Density
  → Assign label from subfolder name
  → Save to CSV with GitHub image URLs
        ↓
Power BI Desktop
  → Load CSV as data source
  → Set Image_URL column → Data Category → Image URL
  → Build Table visual with MRI thumbnails
  → Add KPI cards, charts, slicers
  → Create bookmark filter panel
  → Add page navigation buttons
        ↓
Final Interactive Dashboard ✅
```

---

## 🗂️ Dataset

| Property | Details |
|---|---|
| **Total Images** | 36,000+ |
| **Image Format** | JPG / PNG |
| **Storage** | Google Drive (public folder) |
| **Labels** | 4 disease stage subfolders |
| **Source** | Alzheimer's MRI Public Dataset |

**Folder Structure:**
```
MRI Images/
├── NonDemented/        (~5,500 images)
├── VMildDemented/      (~11,200 images)
├── MildDemented/       (~10,100 images)
└── ModerateDemented/   (~10,000 images)
```

---

## 🐍 Python Feature Extraction

Python extracts these **4 pixel-level features** from every MRI scan:

| Feature | Formula | What It Measures |
|---|---|---|
| `Mean_pixel_intensity` | `np.mean(array)` | Average brightness of the brain scan |
| `Std_pixel_intensity` | `np.std(array)` | Variation / spread of pixel brightness |
| `Entropy` | `shannon_entropy(array)` | Complexity and information disorder in image |
| `Edge_Density` | `np.mean(sobel(array))` | Structural clarity and edge sharpness of brain tissue |

### Complete Python Script

```python
import os, time
import pandas as pd
import numpy as np
from PIL import Image
from skimage.filters import sobel
from skimage.measure import shannon_entropy

# ✅ Set your MRI images folder path
IMAGE_ROOT = r"C:\Users\Admin\OneDrive\Desktop\MRI Images"
OUTPUT_CSV = os.path.join(IMAGE_ROOT, "mri_data.csv")

# GitHub raw image URLs per label
LABEL_URLS = {
    "MildDemented"     : "https://raw.githubusercontent.com/GADEKAR328/MRI-Image-Data/main/000a074f-a3a5-4c70-8c94-d7ed7bbe7018.jpg",
    "ModerateDemented" : "https://raw.githubusercontent.com/GADEKAR328/MRI-Image-Data/main/000cdcc4-3e54-4034-a538-203c8047b564.jpg",
    "NonDemented"      : "https://raw.githubusercontent.com/GADEKAR328/MRI-Image-Data/main/00a4080b-0cea-436f-9c97-031ee6d3b5f5.jpg",
    "VMildDemented"    : "https://raw.githubusercontent.com/GADEKAR328/MRI-Image-Data/main/00a9c4ad-c06d-431d-a5c9-1dc324db0632.jpg",
}

def detect_label(folder):
    f = folder.lower()
    if "verymild" in f or "very_mild" in f: return "VMildDemented"
    elif "moderate" in f: return "ModerateDemented"
    elif "mild" in f: return "MildDemented"
    else: return "NonDemented"

rows, done = [], 0
start = time.time()

for root, dirs, files in os.walk(IMAGE_ROOT):
    label = detect_label(os.path.basename(root))
    for fname in files:
        if not fname.lower().endswith(('.jpg', '.jpeg', '.png')): continue
        try:
            arr = np.array(
                Image.open(os.path.join(root, fname)).convert('L'),
                dtype=np.float64
            )
            rows.append({
                'Filename'             : fname,
                'Image_URL'            : LABEL_URLS.get(label, ""),
                'First_Label'          : label,
                'Mean_pixel_intensity' : round(np.mean(arr), 2),
                'Std_pixel_intensity'  : round(np.std(arr), 2),
                'Entropy'              : round(float(shannon_entropy(arr)), 2),
                'Edge_Density'         : round(float(np.mean(sobel(arr))), 4),
            })
            done += 1
            if done % 500 == 0:
                pd.DataFrame(rows).to_csv(OUTPUT_CSV, index=False)
                print(f"{done} done | {round((time.time()-start)/60,1)} min elapsed")
        except Exception as e:
            print(f"Skipped {fname}: {e}")

df = pd.DataFrame(rows)
df.to_csv(OUTPUT_CSV, index=False)
print(f"\nDONE! {done} images saved to: {OUTPUT_CSV}")
print(df['First_Label'].value_counts())
```

---

## 🚀 How to Use

### Step 1 — Clone this repository
```bash
git clone https://github.com/GADEKAR328/Alzheimer-s-Disease-Dashboard-Power-BI---MRI-Scan-data-Analyis.git
```

### Step 2 — Install Python libraries
```bash
pip install pandas numpy pillow scikit-image
```

### Step 3 — Update the image path in script
```python
IMAGE_ROOT = r"C:\Your\Path\To\MRI Images"
```

### Step 4 — Run the Python script
```bash
python RUN_THIS.py
```
⏳ Processing ~36,000 images takes approximately **30–40 minutes**

### Step 5 — Open Power BI Dashboard
- Open `Alzheimers_Disease_Dashboard_Power_BI.pbix`
- Go to **Transform Data → Data Source Settings**
- Update CSV path to your generated `mri_data_fixed.csv`
- Click **Close & Apply**
- Go to **Data View** → click `Image_URL` column
- Set **Column Tools → Data Category → Image URL**
- Explore the dashboard! ✅

---

## 📁 Project Structure

```
Alzheimer-s-Disease-Dashboard-Power-BI---MRI-Scan-data-Analyis/
│
├── 📊 Alzheimers_Disease_Dashboard_Power_BI.pbix
├── 🐍 RUN_THIS.py
├── 📄 mri_data_fixed.csv
├── 🖼️ Page1 Dashboard Overview.jpg
├── 🖼️ Page 2 Image Spreadsheet.jpg
├── 🖼️ Filter.jpg
├── 🖼️ MRI Fixed Data Link.jpg
├── 🖼️ Extract_py.jpg
├── 🖼️ Spyder img extract by py.jpg
└── 📄 README.md
```

---

## 👤 Author

### Yogesh Shivaji Gadekar

> Data Analyst | Power BI Developer | Python Enthusiast

- 💼 [LinkedIn](https://www.linkedin.com/in/yogesh-gadekar-a1231b189/)
- 🐙 [GitHub](https://github.com/GADEKAR328)

---

## 🤝 Contributing

Contributions, issues and feature requests are welcome!
Feel free to check the [issues page](https://github.com/GADEKAR328/Alzheimer-s-Disease-Dashboard-Power-BI---MRI-Scan-data-Analyis/issues).

---

## ⭐ Show Your Support

If you found this project helpful or interesting, please consider giving it a **⭐ Star** on GitHub — it means a lot!

[![GitHub stars](https://img.shields.io/github/stars/GADEKAR328/Alzheimer-s-Disease-Dashboard-Power-BI---MRI-Scan-data-Analyis?style=social)](https://github.com/GADEKAR328/Alzheimer-s-Disease-Dashboard-Power-BI---MRI-Scan-data-Analyis)

---

*Made with ❤️ by [Yogesh Shivaji Gadekar](https://www.linkedin.com/in/yogesh-gadekar-a1231b189/)*
