---
Author: DataCAMP
Category: ETL
Type: Apunte
Status: Terminado
relación: "[[Extraccion de datos]]"
---
Es un programa muy usado para hacer estadística sobre economía y epidemial.

```python
import pandas as pd
from sas7bdat import SAS7BDAT
with SAS7BDAT(file) as file:
	df_sas = file.to_data_frame()

```

# archivos Stata

`pd.read_stata('file)`