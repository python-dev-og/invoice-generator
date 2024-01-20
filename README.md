![Python 3.11](https://img.shields.io/badge/python-3.11-blue.svg)
![Pandas](https://img.shields.io/badge/pandas-%5E1.3-blue)
![FPDF](https://img.shields.io/badge/fpdf-%5E1.7-blue)

# Invoice PDF Generator

## Overview
This Python script automates the conversion of invoice data from Excel files into well-structured PDF documents. It processes multiple Excel files stored in the `invoices` directory and generates corresponding PDFs with detailed invoice information.

## Requirements
- Python 3.x
- Pandas: A fast, powerful, flexible, and easy-to-use open-source data analysis and manipulation library.
- FPDF: A Python library for creating PDF documents.
- glob: A module for Unix-style pathname pattern expansion.
- pathlib: An object-oriented filesystem path library.

## Installation
To install the required libraries, run:
```bash
pip install pandas fpdf
```

## Usage
1. Place all the Excel invoice files in the `invoices` directory. The files should be in `.xlsx` format.
2. Ensure each Excel file is named in the format `invoice_number-date.xlsx`.
3. Each Excel file should contain a sheet named "Sheet 1" with invoice data.
4. Run the script. PDFs will be generated in the `PDFs` directory with the same name as the Excel file.

## Script Workflow
1. **File Path Collection**: Collects all Excel file paths in the `invoices` folder.
2. **PDF Initialization**: Initializes a PDF document for each invoice.
3. **Invoice Data Extraction**: Extracts the invoice number and date from the filename.
4. **Dataframe Processing**: Reads the Excel file and processes the data.
5. **PDF Content Creation**: 
    - Adds invoice number and date.
    - Formats and inserts the table header and rows with product details.
    - Calculates and displays the total sum of the invoice.
    - Adds the company name and logo.
6. **PDF Generation**: Outputs the finalized PDF document.

## Notes
- Customize the script as per your invoice layout and data structure.
- Ensure the `logo.png` file is available in the script directory for the company logo.
- Modify the path and formatting according to your requirements.