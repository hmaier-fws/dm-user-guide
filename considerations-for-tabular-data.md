# Considerations for Tabular Data

Much of the Region’s data is contained in spreadsheets or databases (i.e., tabular data, most commonly MS Excel or MS Access files). Spatial data also has attributes in table format.  Below are some best practices when dealing with this type of data.&#x20;

### Creating tidy data

A copy of your tabular data should always be kept in a tidy format. Tidy data is a way of structuring tabular datasets in a consistent and easily analyzed format. In a tidy dataset:

* Each column is a variable
* Each row is an observation
* Each cell is a value

Common errors that make data "messy" include putting multiple values in one column, using formatting to convey information, putting multiple datasets on one worksheet, adding summary fields or tables, and mixing data, analysis, and presentation. See Hadley Wickham's 2014 article "[Tidy Data](https://vita.had.co.nz/papers/tidy-data.pdf)" for an in-depth discussion on this way of structuring datasets.

{% hint style="info" %}
Ideally, you should structure your data collection methods and/or data entry methods to produce tidy data from the get-go, rather than having to do tidying later on.
{% endhint %}

### Other tabular dataset best practices

When working in a database (i.e. a Microsoft Access file), the tidy dataset might be the only version of the data you have. However, when working within a single workbook (i.e. a single Excel file), work can be broken out into multiple worksheets that contain derivatives of the data, such as tables, pivot tables, summaries, and figures. The following best practices apply to spreadsheets with multiple worksheets.

One sheet in the file should provide a brief description of each other sheet in the file, like a table of contents. Each row of this sheet represents one sheet of the file. The first column should contain the sheet name, while the second column should contain the sheet description.&#x20;

One sheet in the file should contain a tidy, machine-readable version of the data. In addition to the basic tidy data principles described above, the tidy version of the data should also follow the following principles in order to be considered machine-readable.

* Variable names should use only letters, numbers, dashes (-), and underscores (\_). Do not use spaces or any other characters. The variable name should include the unit where this is relevant (e.g., length\_cm and weight\_g).
* Avoid formatting information in this sheet (e.g., comma in the thousands place, font settings, border lines, colors, etc). If the formatting is there to convey some information; instead, add a new variable to record that information. For example, instead of highlighting a cell to indicate a possible error, add another column and assign an error code to the observation (e.g. 1=sensor failure, 2=lost data sheet).
* For the purposes of tidy data, blank cells indicate that the data point is missing; some use -9999 to indicate missing data. “0” in a cell means that the data point was collected and it was “0”. The treatment of missing data should **always** be recorded in the data dictionary (described below).
* In addition to being part of the workbook, the tidy data sheet should also be saved in an open format (e.g. text, CSV, TSV) using the same name as the Excel file (e.g. fish\_data.xlsx and fish\_data.csv)
* Establish the unit of analysis and ensure that is maintained throughout the dataset (e.g. in a bird banding dataset, the unit of analysis is likely an individual bird).
* Add unique identifiers to records to enable data quality management. See the [Unique Identifiers](broken-reference) section for more information.

One sheet in the file should provide a brief description of each variable in the tidy data. Each row of this sheet represents one variable. This is termed the **data dictionary** and will be part of the metadata record for the tidy data. An example and a template for the data dictionary is available [here](https://doimspp.sharepoint.com/:x:/s/AlaskaDataStewardship/EV4M7\_juM5FOgGm9r\_hWiOABsJDdLPaPQG0Bmm4sja5fsQ?e=wznkFo).&#x20;

Other sheets in the file can contain summaries of the data (pivot tables), graphical representations of the data (figures), or derived quantities from the data (formulae, macros, etc). Avoid including metadata on these sheets.&#x20;

Save the original workbook in the most recent format supported by the application. For example, save Excel files in .xlsx format rather than .xls format. Though Excel is acceptable for working copies of data, the end goal is to provide the tidy data and any processing scripts and/or derived data in an open source, machine-readable format.

### Examples

#### Tidy Data

![Tidy data example](<.gitbook/assets/image (8).png>)

Why is the above data considered tidy?

* Each column contains one variable
* Each row contains one observation
* Each cell contains one value

#### "Messy" Data

![Mess data example](<.gitbook/assets/image (4).png>)

Why is this data untidy/not machine readable?

* There are three different tables on one sheet
* One row is NOT one observation
* One column is NOT one variable &#x20;
  * Some of the values have indications of additional information
* Totals and percentages are calculated in the sheet
* Some of the rows have indications of formatting embedded

