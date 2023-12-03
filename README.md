# PDF Merger using PyPDF2

This script demonstrates how to merge multiple PDF files into a single PDF using PyPDF2 library in Python.

## Requirements

- Python 3.x
- PyPDF2 library

  You can install PyPDF2 using pip:

    ```bash
        pip install PyPDF2


## Usage
1. Place the script in the directory where your PDF files are located.
2. Run the script using Python:
    ```bash
      python pdf_merger.py

The script will merge all the PDF files in the current directory into a single PDF file named combined.pdf.

### Code Explanation
The Python script uses PyPDF2 library to merge PDF files:

    
      import PyPDF2
      import sys
      import os
      
      merger = PyPDF2.PdfMerger()
      
      for file in os.listdir(os.curdir):
          if file.endswith(".pdf"):
              merger.append(file)
      
      merger.write("combined.pdf")

The  **PdfMerger object** from PyPDF2 library is used to merge multiple PDF files. It iterates through the files in the current directory and appends all files with a **.pdf** extension to the merger. Finally, it writes the merged PDF to a file named combined **.pdf**

Feel free to modify the script or adapt it according to your specific requirements.

For more information about PyPDF2 library and its functionalities, refer to the [PyPDF2 documentation](https://pypi.org/project/PyPDF2/).
