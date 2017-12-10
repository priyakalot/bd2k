## README

This is the beginning of a project to analyze time expressions in case reports from PubMed. The main analysis can be found in time-expressions-analysis.ipynb.

### running-SUTime
I used SUTime (https://nlp.stanford.edu/software/sutime.html) to collect time expressions ("daily","2 days later") from case reports. Specifically, I used a Python wrapper for SUTime (https://github.com/FraBle/python-sutime). 

### time_expressions_part_a.txt and time_expressions_part_b.txt
Outputs from running-SUTime. JSON objects of time phrases in each case report fed into SUTime.

### time-expressions-analysis.ipynb
Analysis of time expressions caught by SUTime on a total of 200 case reports
