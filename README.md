# DataCite Repository

Python3 scripts to help researchers submit valid XML documents to DataCite to create DOIs and their metadata.  

## dataCiteExcelToXML.py
This script creates well-formed XML documents for importation into [DataCite](https://datacite.org/index.html) from an Excel workbook.

The script first combines metadata in the Excel sheets into an easily-readable CSV using the Python [pandas library](https://pandas.pydata.org/pandas-docs/stable/index.html) and the [xlrd package](https://pypi.org/project/xlrd/). The script will prompt you for the filename of the Excel document and what you'd like the CSV file to be named.

The script then creates one or many XML documents from the CSV based on the request number  field, using the [lxml](https://lxml.de/index.html) package and [CSV module](https://docs.python.org/3/library/csv.html#module-csv). Each unique request number creates a corresponding XML document. The XML documents are formed to adhere to the [DataCite Metadata Schema 4.2](https://schema.datacite.org/) and are named based on request number.

#### Documents needed:
* Completed Excel workbook based on [this template](https://github.com/mjanowiecki/datacite/blob/master/metadataExamples.xlsx)

#### Documents created:
* One CSV document with all data from completed Excel workbook
* One or many XML documents
* Log file with terminal & error messages
