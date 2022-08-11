# Quality Management Procedures



Managing data quality is an important component of the data lifecycle. Data quality management is the prevention and correction of data defects or issues within a dataset that reduce our ability to apply data towards our science-based conservation efforts. There are two distinct components of data quality management that are often lumped together: quality assurance and quality control.&#x20;

* **Quality Assurance (QA)** – Implementing processes that prevent data defects from occurring. For example, writing a detailed protocol for a long-term survey so the methodology is maintained as new staff come on board. Quality assurance begins before the data are collected and includes processes and procedures used to prevent errors while collecting or entering the data.
* **Quality Control (QC)** – Detecting and repairing defects once you have the data. For example, noticing a negative value in a count field may indicate a data-entry error, which might be fixed by reviewing a field data sheet. Quality control should occur as soon as possible after collecting the data and before submitting, archiving, or sharing data.

While this topic is listed in this handbook under the "Acquire" section, it is important to note that quality management can be applied at any stage in the data management lifecycle.

### Quality Assurance

The following are examples of quality assurance measures that can be incorporated into your project workflow:

* Creating Standard Operating Procedures
* Staff training and testing
* Incorporating data standards
* Creating standard data sheets for field data collection
* Creating defined value lists (data domains) for computer data entry
* Designating missing value codes
* Identifying required fields

### Quality Control

The following are examples of quality control that can be incorporated into your workflow:

* Check for outliers and anomalous values or gaps.
* Review the file content and descriptors to ensure that there are no missing data values for key parameters.
* Sort the records by key parameters to highlight discrepancies.
* Check the validity of measured or derived values and scan for impossible values (e.g., a pH of 74).
* Check the time frame and the temporal units. Generate time series plots to detect anomalous values or data gaps.
* Review statistical summaries (e.g., mean, median, minimum values, maximum values, etc.).
* If geolocation is a parameter, use scatter plots or GIS software to map each location to check for errors in coordinates. For GIS image and vector files, ensure the projection parameters have been accurately stated.
* Additional information such as data type, scale, corner coordinates, missing data value, size of an image, and the number of bands should be checked for accuracy.
* Remove any unnecessary parameters or columns used in processing that are uninformative.
