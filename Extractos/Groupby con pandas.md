---
Author: Platzi
Category: Programación
Type: Apunte
Status: Terminado
relación: "[[Curso de Pandas]]"
---
```python

df_walmart.groupby(by=["department"],axis=0).mean() 
# la bolsita son el typo de departamento y las columnas que vamos a sacar la media es ventas por semana
df_walmart.groupby("department")["weekly_sales"].mean() 

```

### Podemos tener multiples agregaciones

```python
#Multiples estadisticas

df_walmart.groupby("department")["weekly_sales"].agg(["max","min"])
#podemos tener las que queramos.

# doble agrupacion
df_walmart.groupby(["department","type"]["weekly_sales"].agg(["max","min"]) 

# doble de todo
df_walmart.groupby(["department","type"])[["weekly_sales","temperature_c"]].agg(["max","min"])

df_sleep.groupby(by=["Occupation"])["Quality of Sleep"].mean().sort_values().index[0]
```

## usando numpy

```python
unemp_fuel_stats = sales.groupby("type")[["unemployment","fuel_price_usd_per_l"]].agg([np.min,np.max,np.mean,np.median])
```