# Table-Reading-Understanding-and-Extraction

Tables and forms are a very common way to organize information in structured documents. Indeed, the physical organization of a table or a form gives a lot of information concerning the logical meaning of the content. The requirement of detection and identification of tables from document images is crucial as tables contain important information, and also most of the layout analysis methods fail in the presence of tables in the document image. To build a solution that can detect tables and its layout in a given documents, then make sense of the information they present. Tables present in documents are often used to compactly communicate important information in rows and columns. To automatically extract this information by digitization of paper documents, the tabular structures need to be identified and the layout and inter-relationship between the table elements need to be reserved for subsequent analysis.

# Methodology
The whole process from taking the input to table extraction can be broken down in to following simpler steps: 
#### 1. Pre-processing 
• Image scaling and Skew correction • Binarizing • Identification and dilation of ruling lines • Storing and replacing the ruling lines with foreground pixels • Identification of connected components and labelling • Statistics such as mean/median of character height/gap etc. • Noise reduction
#### 2. Formation of text blocks (coalesce different components/pixels/characters into one text block)
• Identify whether or not the connected components are in the same line • Finding consecutive components of each of the connected components
#### 3. Table detection
Identifying possible candidate text lines which can form a part of the table
#### 4. Table extraction
• Identification of rows and columns in the table, row and column header and corresponding contents \
• Each of the cell blocks is tagged by its appropriate block labels of headers (rows/columns) and then a dictionary of block labels and corresponding strings extracted using Tesseract OCR is formulated
# Main Frameworks/Tools used 
• Numpy \
• PIL \
• Scipy \
• cv2 \
• glob \
• pytesseract (Tesseract OCR engine) \
• pdf2image \

# Presentation
https://agabhi017.github.io/Table-Reading-Understanding-and-Extraction/ \
(Alternatively, please look for 'Presentation.pdf' in the main repository if the page takes longer to load)

#### The solution was presented at Axis Bank AI Hackathon and SYND-iNNOVATE (Syndicate Bank Hackathon)

# Demo
https://www.youtube.com/watch?v=btkYKrPptbE

The solution was presented at Axis Bank AI Hackathon and SYND-iNNOVATE
