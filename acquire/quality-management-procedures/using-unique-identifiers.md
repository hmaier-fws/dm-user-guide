# Using Unique Identifiers

It is a best practice to add unique identifiers to table records during or immediately after data entry. If you are working with a long-standing dataset, it is recommended to add unique identifiers before conducting any tidying procedures. This addition not only prevents errors, but allows you to cross-reference with previous versions of the dataset.&#x20;

Before you begin, verify the current dataset does not contain duplicate records. This is particularly important if unique identifiers are being applied for the first time to a long-standing dataset. For example, In a bird banding dataset, you may concatenate the species, band number and date variables into a new column and check for uniqueness using the [Conditional Formatting command in Excel](https://support.microsoft.com/en-us/office/filter-for-unique-values-or-remove-duplicate-values-ccf664b0-81d6-449b-bbe1-8daaec1e83c2).

Once record uniqueness is established, add a column of unique identifiers. This may be done by concatenating values from key variables in the dataset or creating universally unique identifiers. **Key variables** are existing variables in the dataset that, separately and/or in combination, uniquely identify the record. **Universally Unique Identifiers (UUIDs)** are a formula-generated 128-bit integer number used to identify resources. 128-bits is big enough and the generation algorithm is unique enough that if every human on Earth generated 600,000,000 UUIDs there would only be a 50% probability of a duplicate.

## Identifier Best Practices

* Name the identifier column something unique and "identifying". A few options are "identifierID", "recordID", or "occurenceID".
* Utilize numeric identifiers to increase efficiency of sorting and filtering records. Do not use spaces, special characters or accents in the identifiers, since they may be modified when the dataset is converted in different formats.
* Limit the number of characters used in identifiers or utilize separators to avoid truncation. Specifically, Microsoft Excel has a character limit of 15 for numeric values and any digits past the fifteenth place is changed to zero. However, this can be avoided by inserting separators in the identifier (i.e. UUIDs use dashes).&#x20;
* If you create identifiers with key variables, ensure the variables uniquely identify each observation. Variables that have missing, zero, or null values are not suitable as key variables. Further, consider whether it is possible for an identifier comprised of concatenated key variables to be duplicated. Example: In a bird banding dataset, species, band number, and date may be suitable as key variables in combination IF the previously stated conditions are met.

## Options for creating UUIDs

**Online UUID Generator**

Create a bulk number of UUIDs using one of many [**online UUID generators**](https://www.uuidgenerator.net/) and paste the requisite number  in the designated identifier column of the dataset.

**Excel**

Create a copy of the empty identifier column in the dataset. Paste the following into the first cell of the copied column:&#x20;

\=LOWER(CONCATENATE(DEC2HEX(RANDBETWEEN(0,4294967295),8),"-",DEC2HEX(RANDBETWEEN(0,65535),4),"-",DEC2HEX(RANDBETWEEN(16384,20479),4),"-",DEC2HEX(RANDBETWEEN(32768,49151),4),"-",DEC2HEX(RANDBETWEEN(0,65535),4),DEC2HEX(RANDBETWEEN(0,4294967295),8)))

Drag the cell with the formula to the bottom of the dataset. When each record has a UUID, highlight the column and copy /’paste special’ to the original identifier column and select ‘Values’ to make sure that only the values are pasted and not formulas. Delete the identifier column with formulas.

**R**

You can generate UUIDs in [**R**](https://www.r-project.org/about.html) using various package. One option is the function [`UUIDgenerate()` ](https://www.rdocumentation.org/packages/uuid/versions/1.0-4/topics/UUIDgenerate)from the [**uuid package**](https://cran.r-project.org/web/packages/uuid/index.html). The following code demonstrates how to add an identifier column with UUIDs to a example data frame. Paste and run the code in [RStudio ](https://www.rstudio.com/products/rstudio/#rstudio-desktop)to see how it works.

{% hint style="info" %}
FWS employees can install R and RStudio on a DOI Windows computer from FWS Apps-to-Go. Search "IFW-R" in the search bar and install the latest versions of the applications.
{% endhint %}

```r
# Install tibble and uuid packages
install.packages(c("tibble","uuid"))

# Create an example data frame
my.df <- data.frame(variable.A = c(1, 1, 1), variable.B = c(2, 2, 2), variable.C = c(3, 3, 3))

# Add an empty identifier column to the beginning of the data frame
my.df<- tibble::add_column(my.df, "identifierID" = NA, .before = 1)

# Generate UUIDs for the number of rows in the data frame
id <- uuid::UUIDgenerate(use.time = FALSE, n = nrow(my.df))
                         
# Add the UUIDs to the identifier column in the data frame
my.df$identifierID<-id

```

#### Python

in development
