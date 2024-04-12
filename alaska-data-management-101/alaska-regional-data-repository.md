---
description: aka RDR
---

# Alaska Regional Data Repository

The Alaska Regional Data Repository is a centralized server dedicated to the storage of regional projects, data assets, and products and metadata. T**he RDR is intended to be the regionally accessible, secure, authoritative storage location for project documents, records, data and metadata and as a single source for serving data and metadata to publicly accessible catalogs and other repositories.**

The regional repository is for the storage of _completed resources_ (this does not mean they can never be replaced or updated); it is not intended for active working files. The process of depositing files in the RDR was designed to implement a data management quality control process where: 1) a digital resource passes from the "data producer" to 2) the "data steward" (who reviews metadata quality) then on to 3) the "data custodian" (who moves the resource to an appropriate storage location). The program repositories are managed by the respective program data managers (i.e. Custodians).\
This process helps to ensure that all assets in the repository have metadata that meet a minimum regional metadata standard and the project directory does not become a disorganized collection files that is often present in shared file systems.

You can reach the Repository by typing  **\\\ifw7ro-file.fws.doi.net\datamgt** into the address bar in File Explorer on any computer that is on, or has access to, the internal network.  Telework computers will need to use a VPN service like Pulse Secure to access the location.

To insure that files placed in the Repository are protected from loss or corruption, access to files within the Repository are controlled through permissions. You, and everyone on the network, may read and copy anything in the Repository, but write and modify permissions are limited.&#x20;

## Obtaining your project archive folder in the RDR

To obtain an archive folder for your project, complete a [Data Management Plan (DMP)](broken-reference) and submit it to your data manager.  The DMP is a working communication document between the project team and your data manager.&#x20;

After submission of a DMP, you will be provided with the address to your project archive folder in the RDR.  It will look something like this:&#x20;

![Example RDR digital location](</assets/image (8).png>)

## Organization of the Regional Data Repository

The Regional Data Repository contains a folder for each program using the RDR (Fisheries and Ecological Services = FES, Migratory Bird Management = MBM, National Wildlife Refuge System = NWRS, Office of Subsistence Management = OSM, and Science Applications = SA.  Within each program folder is a folder for each project that will serve as an archive.

The project archive folder name takes the format: ProgramAcronym\_SequentialNumber\_ShortTitle, i.e. MBMwa\_011\_YKDeltaNestPlot would stand for the Migratory Bird Management Waterfowl Program, YK  Delta Nest Plot Survey, and it was the 11th archive record created for that program. &#x20;

Listed and described below is the basic folder structure of the RDR.  Top level folders (**BOLD**) are generally maintained for every project.  Projects vary and the use of sub-folders, naming, and organization are at the discretion of the project staff and your data manager.  &#x20;

* **changelog.txt**  ReadMe text file to record additions, subtractions and alterations to contents of the archive record.
* **admin** material related to general project administration; could be replicated each year for multiyear projects, i.e., admin2019, admin2020.  Contents of the admin folder are often important record related to the project implementation and may include:
  *    contracts final executed agreements
  * correspondence important information relating to the execution of the project including permits obtained for the project
  * purchasing significant or unique purchasing information that is deemed important to archive
  * training training materials developed for the project
  * travel significant or unique travel information that is deemed important to archive
* **code** computer processing code i.e. R or Python scripts
* **data** generated from the project, and can be sorted in sub-folders, if needed.  Otherwise, naming conventions noted below, should be used to identify the data type.
  * raw data is unprocessed data as initially recorded. File structure may vary by project and it is recommended to organize data by data type.  File names of raw data may reflect the format raw\_type\_of\_data\_x and repeated as needed.    &#x20; Raw data may consist of spreadsheets, databases, images, text notes, sounds, geo points or lines, etc.
  * final data is data that has passed all quality control checks and are typically the data products destined for public release and used for analysis and reporting.  The structure and file names should mirror that of the raw data suck as&#x20;    final\_type\_of\_data\_x and repeated as needed.    ****
  * analysis output are result files of computer code or model, or other processing step or other derived tables needed from analysis.  i.e. an observer matrix table, model output file,  etc.  These should follow similar file naming format such as output\_type\_x and repeated as needed.
* **documents** include materials generated by the project; these products may also be described in metadata.  Some documents are internal work products and may not be intended for public consumption.  The contents of the documents folder may include:
  * [data management plan](broken-reference) for the project
  * proposal documents prepared to solicit both internal or external funding
  * public relations materials such as project photographs, maps, graphics, drawings, etc.&#x20;
  * publications peer-reviewed, final manuscripts
  * reports white papers that are not peer-reviewed, but provide results or information from the project
  * talks recordings or presentation slides related to the project
  * posters stand-alone posters related to the project
  * protocols may be a sub-folder and may include investigation plans, methods and protocol documents that guide project procedures
    * form\_template may include data sheets, or templates for data entry, etc. that are important for understanding the project
* **incoming** serves as a holding location for materials that should be filed under one of the other subfolder locations after review
* **metadata** contains the mdEditor JSON file for the project, associated products, project contacts, and data dictionaries.  All files in the RDR should be accompanied by metadata.
* **source\_data** may or may not be part of the project.  It is designated to house data that is NOT generated by the project, but used during the course of the project. It is generally existing pubished or freely available data.  These items may be placed in a separate folder or within the data folder if appropriately named.  File naming may follow a designated format such as source\_type\_of\_data\_x.

![Graphical representation of possible RDR project archive folder structure.  Green folders are common across all projects and should be maintained if appropriate, blue sub-folders may or may not apply to a given project or may or may not be used.  Subsequent orange and dark blue boxes represent example naming conventions or file types](</assets/image (9).png>)

Updated August 2022
