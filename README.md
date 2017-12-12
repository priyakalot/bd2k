# Time Expressions Annotations and Analysis

This is the beginning of a project to analyze time expressions in case reports from PubMed. The main analysis can be found in time-expressions-analysis.ipynb.

### running-SUTime
I used SUTime (https://nlp.stanford.edu/software/sutime.html) to collect time expressions ("daily","2 days later") from case reports. Specifically, I used a Python wrapper for SUTime (https://github.com/FraBle/python-sutime). 

SUTime and FraBle give examples of how to run SUTime on one document. To run SUTime on multiple documents, use running-SUTime. Have all documents saved as .txt files in one folder, and replace the the file paths in the code to point to your own folder with documents. Your output will then be a dictionary of JSON objects. An example of one JSON object with an annotation is below--
```json
{
  "end": 437, 
  "start": 428,
  "text": "12 months",
  "type": "DURATION",
  "value": "P12M"
}
```
### time_expressions_part_a.txt and time_expressions_part_b.txt
Outputs from running-SUTime. JSON objects of time phrases in each case report fed into SUTime.

### time-expressions-analysis.ipynb
Analysis of time expressions caught by SUTime on a total of 200 case reports
