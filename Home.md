
```button
name Nuevo registro
type command
action QuickAdd: Bibliografias
```

# Resumen_extractos

```dataview
TABLE without id 
  file.link AS "Title",
  Author AS "Author",
  Category AS "Category",
  Type, 
  Status

FROM "Bibliografia"
where Type = "Book" or "Document" or "Video" and  !contains(file.name, "000")  and !contains(Type, "Quote") and !contains(Type, "Image") and !contains(Type, "Annotation") and !contains(Type, "Extract") and !contains(file.name, "Library") and !contains(file.name, "Bibliografia") 
SORT Status asc
```

