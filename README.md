# HISTORICAL-BUDGET-ANALYSIS

DATA COLLECTION:

The Data was collected from the https://www.indiabudget.gov.in/  site. The data achieved, was in the form of pdfs. The data comprised of the Annual Financial Budget Speeches from the years 1947-2021. 

DATA EXTRACTION:

The data was extracted from the Table - “General Statement of Revenue and Expenditure” under the section - “Budget of the Central Government”. The table comprised of the Revenue and the Expenditure heads with their respective Budget Estimate of the previous year, Revised Estimate of the previous year, and the Budget Estimate of the particular year. The pdf files had to be extracted to a csv/excel file to make analysis possible. There are various methods to extract data from pdfs: 

a)	Copying and Pasting data: copy the selected data and paste in the csv file.

b)	Manual Data Entry: Enter each information you want to put in the csv file.

c)	PDF converters: Available as software or web based online solutions. E.g.: Adobe, PDFtoExcel, etc.

d)	PDF Extraction tools: The tables in pdfs contain various texts, values, images. The tools extract the table data and converts to csv format. E.g., Nanonets

At first, the pdfs were extracted using python. The tools that were used for the process were:

a)	Response-Python Requests: Since this project require to scan through 70 years pdf files, downloading so many files were not feasible hence extracting data from urls itself was considered. So, the requests.Response() Object consists of the server's response to the HTTP request. The module gives you the liberty to send HTTP requests using Python which in turn returns a response.

b)	Urllib: It is a package that gathers many modules to work with urls.

c)	Pdftotext: Since the tables could not be extracted from the files as the files were scanned documents due to which the tables could not be identified in the documents. It is a Pdf text extraction method. The library extracts the pdf and converts it into a readable text format. The main idea was to extract the important figures from the extracted text.

d)	Pdfminer: It is also another text extraction tool.

e)	PyPdf2: A library that is built as a PDF toolkit. It enables the programmer to extract, split, merge, crop, encrypt/decrypt the pdf files.

f)	Tabula-py: This is a python wrapper that reads tables from pdf and converts into a pandas dataframe or a csv, tsv, json file.

However, all the above methods failed to succeed as every method gave a gibberish output as the data is fetched from 1940s period, because of the typewriter font used during that time the text/values could not be identified by the ‘Tesseract’ library.

DATA ANALYSIS:

For analysis, the data in pdfs were converted to data in csv format manually. The Revenue and Expenditure csv files were loaded using a dataframe. To visualize the data, the libraries such as numpy, pandas, matplotlib and plotly were imported. 

The data was then transposed and indexed so that the data is visualized appropriately according to my requirement. The transposed data was then loaded and hence visualized in the form of stacked bar chart. Each department in the revenue and the expenditure data were allotted a different color to give a clear representation of data. 

RESULTS:

There was a lot of missing data as the data was collected from the year 1947 to 2021, because of which the heads such as the Defence services, Social and Economic services, Transport and Communication, Agriculture and Allied services, Taxes of Union territories initiated after about 10 years of Independence. The missing values are also due to the government pdfs not displaying the complete data for a few years and due to missing government files of some years from the official site.

The most evident rise in the Revenue department has been of Corporation tax as its amount depends on the net income companies get while using their business activity, normally during one business year hence as the company income rises, the Corporation tax also rises every year.

The other heads in Revenue Budget that has faced hikes are: Administration Services(Dark Blue) Income Tax Union Excise and so on.

In the Expenditure department, there has been significant growth in the Agriculture and Allied Services department. The revenue expenditure budget estimate on Agriculture and associated administrations in India added up to a estimate of 4.1 trillion Indian rupees in monetary year 2018 which was a clear development contrasted with financial year 2009 as Agriculture has been the foundation of the Indian economy, giving large job offers for the population.

The other heads in Expenditure budget that has faced hikes are: Science and Technology, Transport and Communication, Economic Services etc.
