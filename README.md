# Data-Parsing-Evaluation-and-Analysis-Of-Railway-Domain-Technical-Documents
**1. Introduction**

The railway sector generates a significant amount of technical documentation essential for maintenance, operations, safety protocols, and infrastructure management. Efficient parsing, evaluation, and analysis of these documents help extract valuable insights, automate data extraction processes, and improve decision-making.
This project focuses on developing a system to parse, evaluate, and analyze technical documents related to the railway domain by leveraging advanced PDF parsing techniques, feature engineering methods, and data visualization tools.

**2. Objectives**

•	To parse and extract meaningful data from railway domain technical PDF documents.
•	To evaluate and compare different PDF parsing libraries for optimal extraction.
•	To analyze the extracted data to identify key features, trends, and patterns.
•	To perform feature engineering to enhance data quality and usability.
•	To visualize the analyzed data effectively using Power BI for better insight and decision-making.

**3. Data Collection**

•	The primary data source consists of multiple technical documents in PDF format related to the railway domain, including manuals, reports, specifications and also RFP documents.

**4. Methodology**

**4.1 PDF Parsing Libraries Used**

To ensure comprehensive data extraction, multiple PDF parsing libraries were employed. The selection and evaluation of these libraries were based on their ability to accurately extract text, handle complex formatting, and preserve the document structure.

**Pdf Parsing Libraries Used:**

**1. PyPDF2** – Extracts text, metadata, and merges/splits PDFs.  
**2. pdfplumber** – Extracts text while preserving layout and table structures.  
**3. pdfminer.six** – Extracts text and metadata with precise control.  
**4. PDFQuery** – Uses XPath queries for structured text extraction.  
**Table Extraction **
**5.Camelot** – Extracts tables from PDFs (works best with PDFs following tabular structure).  
**6. pdfplumber** – Extracts tables along with text content.  
**7. Tabula-py** – Extracts tables using Java-based Tabula.  

**Optical Character Recognition (OCR) for Scanned PDFs**

**8. Tesseract OCR (pytesseract) **– Converts scanned images of text into machine-readable text.  

**9.pdf2image** – Converts PDF pages into images for OCR processing.  
**10. OCRmyPDF** – Enhances PDFs by adding a text layer using OCR. 
**Metadata and Annotations Extraction**
**11.PyMuPDF (fitz)** – Extracts metadata, text, images, and annotations.  
**12. pdfrw** – Reads and modifies PDF files, including metadata updates.  

**PDF Generation & Manipulation**

**13. ReportLab** – Generates PDFs dynamically (e.g., invoices, reports).  

**14. PyMuPDF (fitz) **– Modifies and creates PDFs efficiently.  

**15. pdfrw** – Reads, modifies, and writes PDF files. 
 
**Libraries Used In our project:**

**PyMuPDF**
**pdfplumber**
**Camelot**
**Tabula**
**ocrmypdf**
**reportlab**

**4.2 Classification Scenario for Libraries**

The libraries were classified and evaluated based on specific scenarios relevant to railway domain documents, such as:
•	Handling of tabular data extraction
•	Extraction of technical terminologies and structured lists
•	Performance on scanned vs. digitally generated PDFs
•	Accuracy in retaining formatting and annotations
![image](https://github.com/user-attachments/assets/45519819-bd21-4901-8b24-46e1a42aed00)
![image](https://github.com/user-attachments/assets/5a623def-afec-4f6a-a235-aa02f75f5ca0)

**4.3 Data Parsing and Cleaning**

•	The raw extracted data from PDFs was cleaned to remove noise such as headers, footers, and irrelevant metadata.
•	Techniques such as regular expressions and natural language processing were employed to standardize the text data.
•	Special attention was given to technical terminologies common in railway documents.

**4.4 Feature Engineering**

To derive meaningful insights from the extracted text, advanced feature engineering techniques were applied. The primary goal was to transform unstructured text data into structured, analyzable features that could support deeper evaluation and visualization.
Libraries and Tools Used for Feature Engineering:
Named Entity Extraction and Classification:
Using the spaCy natural language processing library, each row of text from the railway technical documents was processed to extract named entities such as dates, organizations, locations, and other important phrases.
However, not all entities are equally valuable for technical analysis. To further enhance the dataset, each extracted entity was classified as either technical or non-technical based on the presence of certain domain-relevant keywords.
The feature engineering process involved:
•	Named Entity Recognition (NER): The en_core_web_sm model from spaCy was used to extract entities from the text.
•	Keyword-Based Classification: A custom list of known technical keywords (e.g., Python, AI, Cloud Computing, SQL, etc.) was created. Entities were matched against this list to determine if they were technical in nature.
•	Labeling:
o	Entities containing technical keywords were grouped under a new column technical_entity.
o	All remaining entities were grouped under non_technical_entities.
This classification enabled a more targeted analysis of the content, allowing downstream tasks (e.g., visualizations in Power BI) to focus specifically on technical trends, frequently mentioned technologies, or non-technical topics such as organizations or geographic references.

**5. Data Analysis and Visualization**

The processed and feature-engineered data was imported into Power BI, a powerful business intelligence tool, to conduct in-depth analysis and create interactive visualizations. Power BI was used to:
•	Generate dashboards displaying key metrics and trends
•	Visualize the distribution of technical terms and components
•	Compare document with entity,unique_entity,technical and non-technical words.
•	Identify patterns and insights to support railway domain decision-making
![image](https://github.com/user-attachments/assets/89bd8519-5c81-46d2-b103-fae679006179)

**6. Conclusion**

This project demonstrated the importance of selecting suitable PDF parsing tools tailored for the railway domain. Feature engineering significantly improved the usability of the extracted data for further analysis. The integration of Power BI enabled effective visualization, providing actionable insights for stakeholders. The developed approach can be extended to other technical domains requiring detailed document parsing and analysis.






