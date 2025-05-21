

---

# 🛒 Shelf Product Detection using OpenCV

This project automatically detects **missing products** on a retail store shelf using **image processing with OpenCV** in Python. It visually marks missing product slots and provides a **row-wise summary** of item availability.

---

## 📸 How It Works

1. Loads a shelf image (`shop1.jpg`)
2. Divides the image into a grid based on expected product layout (rows & columns)
3. Analyzes each cell to determine if a product is present using **contour detection**

### 🔍 Visual Highlights:

* 🟥 **Red box** → Missing product
* 🟩 **Green box** → Detected product
* 🧮 Outputs total number of missing items **per row**

---

## ✅ Requirements

* Python 3.x
* OpenCV (`cv2`)
* NumPy
* Google Colab *(optional, for `cv2_imshow`)*

---

## 🚀 How to Run

1. Upload your shelf image and name it `shop1.jpg`
2. Run the script in any Python environment (e.g., Google Colab or local Jupyter Notebook)
3. The result will be displayed with annotated red and green boxes indicating product presence

---

## 🛠️ Configuration

You can modify the shelf layout grid in the script using these parameters:

```python
NUM_ROWS = 3        # Number of rows (shelves)
NUM_COLS = 5        # Number of columns (product slots per row)
CELL_WIDTH = 60     # Width of each slot
CELL_HEIGHT = 100   # Height of each slot
START_X = 50        # Starting x-coordinate of the grid
START_Y = 80        # Starting y-coordinate of the grid
ROW_SPACING = 130   # Vertical space between rows
COL_SPACING = 100   # Horizontal space between columns
```

---

## 📂 Sample Output

* Printed output shows:

  ```
  📦 Row 1 analysis:
  🧮 Missing items in Row 1: 2 / 5
  📦 Row 2 analysis:
  🧮 Missing items in Row 2: 1 / 5
  ```
* Annotated image shows:

  * ✅ Green boxes around detected items
  * ❌ Red boxes around empty slots

---

## 🧠 Future Ideas

* Integrate **YOLO** or other deep learning models for smarter product recognition
* Export missing product data to CSV or database
* Automatically detect shelf layout from image

---


