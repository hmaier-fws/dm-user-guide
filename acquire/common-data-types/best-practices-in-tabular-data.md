# Best Practices in Tabular Data

Much of the Region’s data is contained in spreadsheets (i.e., tabular data, most commonly MS Excel files). Multiple spreadsheets within the same file can contain data and derivatives of the data (tables, summaries, pivot tables, formulas, figures). Below are some best practices when dealing with this type of data.&#x20;

* One sheet in the file should contain a clean version of the data. Nothing else should be on this sheet. This is sometimes also referred to as **tidy data**. In tidy data:
  * The first row contains variable names and each column represents one variable. Variable names should use only letters, numbers, dashes, “-“, and underscores, “\_”. Do not use spaces or any other characters. The variable name should include the unit where this is relevant (e.g., length\_cm and weight\_g).
  * Each row after the first row should represent one observation.
  * Avoid formatting information in this sheet (e.g., comma in the thousands place, font settings, border lines, colors, etc). If the formatting is there to convey some information; instead, add a new variable to record that information. For example, instead of highlighting a cell to indicate a possible error, add another column and assign an error code to the observation (e.g. 1=sensor failure, 2=lost data sheet).
  * For the purposes of tidy data, blank cells indicate that the data point is missing; some use -9999 to indicate missing data. “0” in a cell means that the data point was collected and it was “0”. The treatment of missing data should **always** be recorded in the data dictionary (see below).
  * The tidy data sheet, in addition to being part of the workbook, should also be saved in an open format (e.g. Text  or CSV or TSV) using the same name as the Excel file (e.g., fish\_data.xlsx and fish\_data.csv) in the same archive folder as the Excel file.
* One sheet in the file should provide a brief description of each variable in the tidy data. Each row of this sheet represents one variable. This is termed the **data dictionary** and will be part of the metadata record for the tidy data. An example and a template for the data dictionary is available [here](https://doimspp.sharepoint.com/:x:/s/AlaskaDataStewardship/EV4M7\_juM5FOgGm9r\_hWiOABsJDdLPaPQG0Bmm4sja5fsQ?e=wznkFo).&#x20;
* Other sheets in the file can contain summaries of the data (pivot tables), graphical representations of the data (figures), or derived quantities from the data (formulae, macros, etc). Avoid including metadata on these sheets.
* One sheet in the file should provide a brief description of each sheet in the file (what does it contain, any relevant information about its use) like a table of contents. Each row of this sheet represents one sheet of the file. First column is the sheet name, the second column is the sheet description.
* Save the original workbook in the most recent format supported by the application. For example, save Excel files in .xlsx format rather than .xls format.

### Tidy Data

![Tidy Data Example](/assets/tidy.PNG)

### Untidy Data

![Untidy Data Example](/assets/untidy.PNG)

#### Why is this data untidy?

* There are three different tables on one sheet
  * &#x20;It is necessary for human intervention to tidy the spreadsheets up before they are machine-readable
* One row is NOT one observation
* One column is NOT one variable &#x20;
  * Some of the values have indications of additional information
* &#x20;Totals and percentages are calculated in the sheet
  *    Some of the rows have indications of formatting embedded

#### Resources to tidy your data

[How to merge and tidy data with Excel](http://www.ttdatavis.onthinktanks.org/how-tos/how-to-merge-and-tidy-data-with-excel)

[How to tidy data with Python](https://www.jeannicholashould.com/tidy-data-in-python.html)





\




