---
Author: DataCAMP
Category: ETL
Type: Apunte
Status: Terminado
relación: "[[Extraccion de datos]]"
---
```python
# Import pandas
import pandas as pd
# Assign spreadsheet filename: file
file = 'battledeath.xlsx'
# Load spreadsheet: xls
xls = pd.ExcelFile(file)
# Print sheet names Son las hojas de excel
print(xls.sheet_names)# vemos las hojas de excel

# Load a sheet into a DataFrame by name: df1

df1 = xls.parse('2004')# extraer los datos de la hoja de calculo
# Print the head of the DataFrame df1
print(df1.head())
# Load a sheet into a DataFrame by index: df2
df2 = xls.parse(0) # ver el index de la hoja de calculo
# Print the head of the DataFrame df2
print(df2.head())
```

# tiene los mismos parametros que [[Importación de archivos CSV]]
`df1 = xls.parse(0, skiprows=[0], names=['Country','AAM due to War (2002)'])`

# con pandas

```python
# Import package

import pandas as pd

url = "https://assets.datacamp.com/course/importing_data_into_r/latitude.xls"

xls = pd.read_excel(url,sheet_name=None)

print(xls)
print(xls['1700'])

