# MCR-Data-Extractor
A Python-based tool for automating data extraction from Mortgage Call Reports (MCR) and converting them into structured CSV files.

# Project Description
A Python-based tool for automating data extraction from Mortgage Call Reports (MCR) and converting them into structured CSV files. It is specifically designed to process various sections of MCR PDF reports, including Credit Lines, Servicing data, and Financial Condition (FC) information. By parsing PDF text content and applying regular expression matching, this tool efficiently transforms unstructured or semi-structured PDF data into analysis-ready CSV files.

# Supported Report Version
This tool is developed and tested primarily for RMLA-General V5 and RMLA-FC V5 versions of Mortgage Call Reports. While it may work with other versions, optimal performance and accuracy are guaranteed for V5 reports.

# Key Features
PDF File Scanning and Classification:
Automatically identifies and classifies General and FC type PDF reports.

Credit Line Data Extraction:
Precisely extracts credit line information from General type PDFs, including Record ID, Name of Provider, Credit Limit, and Remaining Credit Available at Period End.

Servicing Data Extraction:
Extracts servicing-related data from General type PDFs, such as UPB, Loan Count, and Average Loan Size, and supports the extraction of free-text notes (NOTE).

Financial Condition (FC) Data Extraction:
Extracts detailed financial data from FC type PDFs, supporting matching based on predefined field lists and handling various note information within FC reports (e.g., FCNOTE, A230J Explanation).

CSV Format Output:
Outputs extracted data into separate CSV files for easy subsequent data analysis and processing.

Error Handling and Skipping Mechanism:
Identifies and skips PDF files with encoding issues or unreadable content, enhancing processing robustness.

# Technical Stack
Python 3.x
pdfplumber: For extracting text content from PDFs. 
pandas: For data processing and CSV file generation.
re: For regular expression matching, enabling precise data extraction.

# Limitations
PDF Encoding Issues:
Some PDF files may have encoding issues, preventing correct data reading and extraction. Such files will be skipped and logged.

Format Dependency:
Data extraction is highly dependent on the layout and structure of the PDF reports. Significant changes in report format may require adjustments to regular expressions and extraction logic.

Performance:
Processing a large number of PDF files may take a considerable amount of time.

# Contribution
Contributions to this project are welcome! If you have any suggestions for improvement or find bugs, please submit an Issue or Pull Request.

Author: Ryandong621
Date: February 5, 2026
