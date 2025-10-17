# 🧩 Matchkey Generator

This project reads an input file named **orders.csv**, generates a standardized **matchkey** for each row based on the address fields, and saves two output files:

1. **orders_with_matchkey.csv** → includes all original columns plus a new column `matchkey`  
2. **orders_with_hashed_matchkey_sha256.csv** → same dataset, but the `matchkey` column is replaced with its SHA-256 hash

---

## ⚙️ Setup Instructions

### 1️⃣ Create and activate a virtual environment
It is strongly recommended to use a virtual environment to keep dependencies isolated. This repo was developed using python 3.12.x

**macOS / Linux**
```bash
python3 -m venv venv
source venv/bin/activate
```

**Windows (PowerShell)**
```bash
python -m venv venv
venv\Scripts\activate
```

---

### 2️⃣ Install dependencies
After activating your virtual environment, install the required packages:

```bash
pip install -r requirements.txt
```

---

### 3️⃣ Run the notebook
1. Place your **orders.csv** file in the same folder as `matchkey_generator_sha256.ipynb`.  
2. Open and run the notebook.  
3. The following files will be generated automatically:
   - `orders_with_matchkey.csv`
   - `orders_with_hashed_matchkey_sha256.csv`

---

## 🧠 Important Notes
- The **only required columns** are:
  - `line1`
  - `line2`
  - `postal_code`
- All other columns will remain untouched.
- The script does **not** modify or remove any data — it only adds or replaces the `matchkey` column as described above.

---

## 📁 Example
A placeholder file named **orders.csv** is included in this folder to illustrate the expected structure.  
You can replace it with your own exported data — as long as the required columns (`line1`, `line2`, and `postal_code`) are present, everything will work automatically.
