# SignboardLayout

> **SignboardLayout** is a benchmark dataset designed to advance **scene text layout analysis** by providing **fine-grained semantic annotations and text grouping**. Unlike traditional scene text datasets, which focus only on detection and recognition, our dataset enables structured text extraction in **real-world signboard environments**.  

## News & Updates  
-  [x] **[14/03/2025] Paper Submitted** – Our dataset has been submitted for review. Stay tuned for updates. 
-  [ ] **Dataset Update** – Added new annotations and refined existing labels to improve quality.  
-  [ ] **New Benchmark Results** – Updated model performance benchmarks on the dataset.  

We will continue to update this section as new developments occur.

## Key Features  

- 📸 **2,025 signboard images** collected from diverse locations and business types.  
- 🏷️ **44,271 annotated text instances** with **semantic labels, text groups, and line indices**.  
- 🌍 **Multilingual support**: Covers **English, Vietnamese, and Chinese** with mixed orientations.  
- 🔠 **Comprehensive annotation schema**:  
  - **Semantic categorization** (e.g., business name, address, phone number).  
  - **Text grouping** (text instances conveying related information are grouped together to maintain logical structure and contextual relationships). 
  - **Line indexing** (each text instance within a group is assigned a line index to distinguish different lines and preserve the hierarchical structure of multi-line text).
- 🗂️ **Two annotation formats**:  
  - **COCO format** (compatible with object detection and OCR pipelines).  
  - **Hierarchical format** (inspired by HierText, with additional group labels).  

## Dataset Access  

Since the dataset is too large to be stored directly in this repository, you can download it from the following sources:

📥 **[Download Dataset (Google Drive)](YOUR_GOOGLE_DRIVE_LINK_HERE)**  
📥 **[Download Dataset (Hugging Face)](YOUR_HUGGING_FACE_LINK_HERE)** 


## Dataset Structure  

After downloading, you will have the following files:  
```
SignboardLayout/
│── images/ # Signboard images
│── annotations/ # Annotation files
│ │── coco_annotations.json   # Annotations in COCO format
│ │── Hier_annotations.json   # Annotations in Hierarchical format
│── samples/ # Example images
│── README.md # Dataset details and usage guide
│── LICENSE # Dataset license
│── scripts/ # Helper scripts for processing annotations
```

## 🔧 Installation & Usage  

### 1️⃣ Load COCO Annotations  
```python
import json

# Load COCO-format annotations
with open("annotations/coco_annotations.json", "r") as f:
    coco_data = json.load(f)

# Print the first annotation
print(coco_data["annotations"][0])
```

### 2️⃣ Load Hierarchical Annotations
```python
import json

# Load hierarchical annotations
with open("annotations/Hier_annotations.json", "r") as f:
    hier_data = json.load(f)

# Print the first annotation
print(hier_data[0])
```

### 3️⃣ Visualize Annotations
```python
import cv2
import matplotlib.pyplot as plt

img_path = "images/sample1.jpg"

# Load and display image
image = cv2.imread(img_path)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title("Sample Signboard Annotation")
plt.show()
```

## Potential Applications  
- **Scene Text Detection and Recognition** 
- **Scene Text Layout Analysis**
- **Multilingual OCR Enhancement**  
- **Structured Information Extraction** 
- **Document Understanding & Parsing** 

---

## Citation  
If you use this dataset, please cite our paper:  
```bibtex
@article{YourPaper2025,
  author    = {},
  title     = {},
  journal   = {},
  year      = {},
}
```

## Contributions & Contact  
We welcome contributions! Feel free to submit issues or pull requests.  
For inquiries, contact **giangttc2003@gmail.com** or **22520004@gm.uit.edu.vn** 📩  

## License  
This dataset is released under the **CC BY 4.0 License**.  
You are free to use, modify, and distribute it with proper attribution.  
