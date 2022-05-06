## Welcome to Windows COM Objects DataBase

This is a simple website that contains a database of COM Objects from different windows builds. 
This database was generated using James Forshaw's oledotnetview tool which I encourage to to check out and use for messing around with COM. 

If you have any requests or suggesstions for additions to this DB or additional features for convience of search, open an issue in the repo. 

### Current Dataset
This repo contains a COM database for the following windows build for both x86 and x64 COM obejcts 
- CASE_Windows10_1909
- CASE_Windows10_20H2
- CASE_Windows11_21H2
- CASE_WindowsServer2016
- CASE_WindowsServer2019

Inside each folder of each build you'll find multiple csv file that contains various information regarding a COM object, soem data will over lap and some will be only in a certain csv, i'l leave the exploration to you. 
However if you're just getting started i recommend startign with **comClass.csv**. 

**These are the various CSVs available**
- comAppId.csv
- comCategory.json
- comClass.csv
- comClassInServices.csv
- comInterfaces.csv
- comProgId.csv
- comRuntimeClass.csv
- comRuntimeServer.csv
- comTypeLib.csv

### Analyzing with Pandas
You can very easily import the csv or json into a DataFrame and work with it immidietly.

```python
import pandas as pd

# skiprows, skips the first row of the csv, in these csv it is required, otherwise the dataframe will not load currectly
comClassDataframe = pd.read_csv("comClass.csv", skiprows=1)
```

### How it Looks
![Uploading image.png…]()

