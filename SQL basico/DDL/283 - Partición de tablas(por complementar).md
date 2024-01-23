---
aliases:
  - Partición de tablas
---
# ¿Que es una [[283 - Partición de tablas(por complementar)|Partición de tablas]]?

>[!warning] Problema
>Cuando las bases de datos cerceen, las consultas se hacen mas **lentas** incluso cuando establecimos bien los indices. 


> Distribuimos las entidades entre varias entidades físicas

## Dos tipos de partición

Partición vertical: Es cuando dividimos la tabla aunque ya este normalizada

Partición horizontal
Dividir las filas en tablas. por ejemplo dividirla por cada año

## Código

>[!example] Tenemos que crear una tabla particionada
>```SQL
> CREATE TABLE sales (
>	timestamp Date NOT NULL
>)
> PARTITION BY RANGE (timestamp); 


>[!example] Crear particiones
> ```SQL
>  CREATE TABLE sales_2019_q1 PARTITION OF sales
>	FOR VALUES FROM ('2019-01-01') TO ('2019-03-31')
> -- Asi por todos lo trimestres del año
> CREATE INDEX ON sales('timestamp')
> -- se recomienda agregar un indice a la columna que uso para particionar

## Pros y contras 

**Pros:**
- Optimiza los indices para que los que se usan mucho quepa en la memoria
- Tambien puedo mover las particiones que rara vez se accede a un medio mas lento.
- [[261 - OLAP|OLAP]] y [[262 - OLTP|OLTP]] se benefician

**Contras**
- Crear una tabla y copear los datos
- No siempre le podemos poner las mismas [[3 - Constraints|Constraints]] por ejemplo una [[2 - Primary Key|Primary Key]]

**Particiones en varias maquinas y se le llama fragmentación**

![[Pasted image 20231201122126.png]]
