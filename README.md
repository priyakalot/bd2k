# bd2k
I wrote the code in this repository as part of a data science research internship at the NIH BD2K (Big Data to Knowledge) Center of Excellence for Biomedical Computing at UCLA during Spring 2017.

My main focus was on developing a user-friendly method for reading in article entries from PubMed in the MEDLINE format, and using such a method to retrieve data to study occurrences of and between MeSH terms in cardiovascular-related case reports. 

## getData
The function "getData" allows users to input a file name, and returns a data frame with each article's PMID, MeSH terms, date of publication, and journal ID. A few notes:

* The basic logic of the function is that it first only reads in the variable names to check which parts of each article entry should eventually be read in. This was done in order to cut down on reading in large amounts of unneeded data, and increase efficiency of the function. The function then goes back through the file extracting the information of the selected variables and enters the information into a data frame.

* MeSH terms for each article are entered into the resulting data frame in a list. In other words, the column with MeSH terms contains a list entry for each record that contains all the MeSH terms contained in the record.

* The function assumes there is a blank line at the start of the text document, as this is what text files of MEDLINE formatted articles from PubMed look like.

* The function assumes that every entry begins with a PMID.
