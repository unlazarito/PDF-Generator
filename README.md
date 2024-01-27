# README

## PDF Generator from CSV using Python

This Python script utilizes the `fpdf` library to generate a PDF document based on data from a CSV file. The generated PDF contains multiple pages, each representing a different topic along with a specified number of pages.

### Requirements
- Python 3.x
- Install the `fpdf` library using:
  ```bash
  pip install fpdf
  ```

### Usage
1. Ensure you have a CSV file named `topics.csv` with the following columns:
    - `Topic`: The title of the topic.
    - `Pages`: The number of pages for each topic.

2. Run the script using:
    ```bash
    python script_name.py
    ```

3. The script will read the CSV file, generate a PDF (`pdf-template.pdf`), and populate it with topics and pages.

### Script Explanation

1. **Import Libraries**
   - The script uses the `fpdf` library for PDF generation and `pandas` for reading the CSV file.

2. **Initialize PDF Object**
   - An `FPDF` object is created with specified orientation, unit, and format.

3. **Read CSV Data**
   - The script reads data from the `topics.csv` file into a pandas DataFrame (`df`).

4. **Iterate Over DataFrame**
   - For each row in the DataFrame, a new page is added to the PDF.
   - Topic title is added to the page along with a horizontal line.
   - Footer is set with the same topic title.

5. **Generate Multiple Pages for Each Topic**
   - If a topic has more than one page, additional pages are generated with the same topic title in the footer.

6. **Output PDF**
   - The generated PDF is saved as `pdf-template.pdf`.

### Note
- Ensure that the CSV file is correctly formatted with the required columns.
- Check the output PDF (`pdf-template.pdf`) for the finalized document.
