# biosensequality
**A Data Quality Report Generator for the NSSP BioSense Platform**

The purpose of this package is to make it easy to produce automated data quality reports for the National Syndromic Surveillance Program’s (NSSP) BioSense Platform. Data from this platform are emergency department records. Functions in this package will track null fields and invalid field entries, returning counts and percentages for each of these checks at both the facility and state-wide level. Functions in this package will also generate timeliness reports: How long was the average lag between a time when a patient visited the emergency department and when the NSSP received the first record for that visit?

If you want to use this package to both pull data and generate reports, it requires a connection to a database named “BioSense_Platform” with a username that is prepended with “BIOSENSE\”, using the RODBC package. This is the same log-in information that we use here at Kansas Department of Health and Environment (KDHE) Syndromic Surveillance to log-in to Adminer and RStudio Server. If you do not want to connect with RODBC or have the data stored locally, you can also use functions here that will skip the pulling data aspect and just focus on generating reports. You must make sure that the variables are named exactly the same as they were when you pulled them from processed tables in the database.

This package can be installed using the `devtools` package. If you do not have this package installed, you can install it with:

`install.packages("devtools")`

After this, you can install the `biosensequality` package using the `install_github` function from `devtools`:

`devtools::install_github("Mengjiao0714/biosensequality")`

**Getting Started**

Take a look at the introductory vignette (http://rpubs.com/markhw/bioqual-vignette) for an introduction on how to use the function; also check out the explainer (http://rpubs.com/markhw/bioqual-interpret) on how to interpret the results.

