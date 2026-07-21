# Ledger – CSV Reconciliation Tool

A browser-based CSV/XLSX reconciliation tool for comparing two datasets and identifying missing records, duplicate keys, and cell-level differences.

> **No server required.** All processing happens locally in your browser.

## Features

* 📄 Supports CSV, XLS, and XLSX files
* 🔍 Automatic column/header mapping
* 🔑 Single or composite primary key selection
* 📊 Summary reconciliation dashboard
* ✅ Row matching between Source and Target files
* 🔄 Smart value comparison

  * Numeric values (`1000` = `1,000`)
  * Multiple date formats
  * NULL / blank equivalence
  * Boolean normalization (`Yes/No`, `True/False`)
  * List comparison
* ⚠ Detects:

  * Missing rows in Target
  * Missing rows in Source
  * Duplicate keys
  * Cell-level differences
* 📥 Export reports

  * Summary
  * Differences
  * Missing Rows
  * Full Comparison
  * Individual column mismatch reports
* 🌙 Light/Dark theme
* 🚀 Runs completely offline after loading

---

## Demo

If deployed using GitHub Pages:

```
https://<your-username>.github.io/<repository-name>/
```

---

## Project Structure

```
.
├── index.html          # Main application
├── README.md
└── assets/             # (Optional) screenshots, icons, sample files
```

---

## How It Works

### 1. Upload Files

Upload the **Source** and **Target** CSV/XLSX files.

### 2. Worksheet Selection

If Excel files contain multiple worksheets, choose the sheets to compare.

### 3. Header Mapping

The application automatically matches columns using:

* Exact match
* Case-insensitive match
* Normalized header match
* Smart matching

You can manually adjust mappings if needed.

### 4. Select Primary Key

Choose one or more columns that uniquely identify each record.

Composite keys are fully supported.

### 5. Compare Data

The application:

* Matches rows
* Detects duplicates
* Finds missing records
* Compares every mapped column

### 6. Review Results

Interactive reports include:

* Mismatched columns
* Missing rows
* Duplicate keys
* Summary statistics

### 7. Export Reports

Download comparison results as CSV or Excel.

---

## Smart Comparisons

The tool automatically treats these values as equal:

| Source                              | Target                            |
| ----------------------------------- | --------------------------------- |
| `1000`                              | `1,000`                           |
| `TRUE`                              | `Yes`                             |
| `FALSE`                             | `No`                              |
| `NULL`                              | *(blank)*                         |
| `2024-05-01`                        | `01/05/2024`                      |
| `"Advisor Confirmed(Professional)"` | `Advisor Confirmed(Professional)` |

---

## Technologies

* HTML5
* CSS3
* Vanilla JavaScript
* Papa Parse
* SheetJS (xlsx)

No backend framework is required.

---

## Running Locally

Clone the repository:

```bash
git clone [https://github.com/cjvprasad/csv-reconciliation.git]
```

Open:

```
index.html
```

or use a local web server:

```bash
python -m http.server
```

Then visit:

```
http://localhost:8000
```

---

## GitHub Pages Deployment

1. Push the project to GitHub.
2. Open **Settings**.
3. Navigate to **Pages**.
4. Select:

```
Source:
Deploy from a branch
```

5. Choose:

```
Branch: main
Folder: / (root)
```

6. Save.

Your site will be available at:

```
https://cjvprasad.github.io/csv-reconciliation/
```

---

## Browser Support

* Chrome ✅
* Microsoft Edge ✅
* Firefox ✅
* Safari ✅

---

## Privacy

All processing happens entirely in the browser.

* No data is uploaded.
* No server-side processing.
* No external database.
* Files remain on your device.

--- browser-native data reconciliation tool for comparing CSV and Excel datasets efficiently.
