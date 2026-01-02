# 📊 Text-to-Excel Converter & Analyzer

> A Python-based utility deployed on Streamlit that seamlessly converts text data into Excel format while providing instant statistical insights.

![Python](https://img.shields.io/badge/Python-3.x-blue)
![Framework](https://img.shields.io/badge/Framework-Streamlit-red)
![Library](https://img.shields.io/badge/Library-Pandas-150458)
![Status](https://img.shields.io/badge/Status-Active-brightgreen)

## 🖥️ Interface Preview
![Main Interface](assets/interface.png)

### 🎥 [Click Here to Watch the Demo Video](https://drive.google.com/file/d/1GWxymqDNsD63AOm0zNCJGaEqQlXKVdva/view?usp=sharing)

## 📖 Table of Contents
- [Overview](#-overview)
- [Key Features](#-key-features)
- [Tech Stack](#-tech-stack)
- [Installation & Setup](#-installation--setup)
- [Usage Guide](#-usage-guide)
- [Example Scenario](#-example-scenario)
- [Dependencies](#-dependencies)
- [Contributing](#-contributing)

## 📖 Overview
This tool is designed to simplify data formatting tasks. It allows users to upload raw text files (CSV-like or delimited), extract specific data fields, and convert them into downloadable Excel (`.xlsx`) files. Beyond simple conversion, the application automatically calculates and displays **row-wise averages** for numeric data, filtering out non-numeric identifiers automatically.

## ✨ Key Features

* **📂 Easy File Upload:** Drag and drop support for `.txt` or `.csv` formatted text files.
* **⚙️ Custom Data Selection:** Interactively select which data fields/columns to process.
* **📈 Smart Analysis:** Automatically calculates **row-wise averages**, ignoring non-numeric columns (like IDs or Names).
* **📥 One-Click Export:** Download the processed data immediately as a formatted Excel file.
* **⚡ Real-time Interface:** Built on Streamlit for a responsive, web-based experience.

## 🛠️ Tech Stack

* **Language:** Python 3.x
* **Frontend:** Streamlit
* **Data Processing:** Pandas
* **Excel Engine:** OpenPyXL

## 🚀 Installation & Setup

Follow these steps to run the application locally.

### 1. Prerequisites
Ensure you have Python 3 installed.
```bash
python --version
```

### 2. Install Dependencies
Install the required libraries using pip:
```bash
pip install pandas openpyxl streamlit
```

### 3. Run the Application
Launch the Streamlit interface:
```bash
streamlit run app.py
```
*The app should automatically open in your default web browser at `http://localhost:8501`.*

## 📖 Usage Guide

1.  **Upload:** Click the "Browse files" button to upload your text file.
2.  **Preview:** The app will show a preview of the raw data.
3.  **Process:** The app automatically converts the text to a structured DataFrame.
4.  **Analyze:** View the calculated averages displayed on the dashboard.
5.  **Download:** Click the **"Download Excel"** button to save the file to your machine.

## 💡 Example Scenario

Imagine you upload a file containing student scores with the following content:

**Input (Text File):**
```csv
Student_ID, Math, Science, History
101, 80, 90, 85
102, 70, 75, 80
```

**Processing Logic:**
The app identifies `Student_ID` as non-numeric/identifier (or excludes it based on logic) and calculates the average of the numeric fields (`Math`, `Science`, `History`).

**Output (App Display & Excel):**

| Student_ID | Math | Science | History | **Average Score** |
| :--- | :--- | :--- | :--- | :--- |
| 101 | 80 | 90 | 85 | **85.0** |
| 102 | 70 | 75 | 80 | **75.0** |

## 📦 Dependencies
* `streamlit`: For the web interface.
* `pandas`: For data manipulation and averaging.
* `openpyxl`: For writing `.xlsx` files.

## 🤝 Contributing
Feel free to fork this project and submit pull requests for custom delimiters or advanced statistical features!
