---

database-plugin: basic

---

```yaml:dbfolder
name: new database
description: new description
columns:
  __file__:
    key: __file__
    id: __file__
    input: markdown
    label: File
    accessorKey: __file__
    isMetadata: true
    skipPersist: false
    isDragDisabled: false
    csvCandidate: true
    position: 0
    isHidden: false
    sortIndex: -1
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: true
      task_hide_completed: true
      footer_type: none
      persist_changes: false
  Author:
    input: select
    accessorKey: Author
    key: Author
    id: Author
    label: Author
    position: 100
    skipPersist: false
    isHidden: false
    sortIndex: -1
    width: 169
    options:
      - { label: "Udemy", value: "Udemy", color: "hsl(27, 95%, 90%)"}
      - { label: "Coderhouse", value: "Coderhouse", color: "hsl(65, 95%, 90%)"}
      - { label: "You Tube", value: "You Tube", color: "hsl(32, 95%, 90%)"}
      - { label: "Platzi", value: "Platzi", color: "hsl(147, 95%, 90%)"}
      - { label: "Christian laurean", value: "Christian laurean", color: "hsl(57, 95%, 90%)"}
      - { label: "DataCAMP", value: "DataCAMP", color: "hsl(210, 95%, 90%)"}
      - { label: "codigofacilito", value: "codigofacilito", color: "hsl(229, 95%, 90%)"}
      - { label: "Book", value: "Book", color: "hsl(145, 95%, 90%)"}
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
  Category:
    input: select
    accessorKey: Category
    key: Category
    id: Category
    label: Category
    position: 100
    skipPersist: false
    isHidden: false
    sortIndex: -1
    width: 194
    options:
      - { label: "Bases de datos", value: "Bases de datos", color: "hsl(73, 95%, 90%)"}
      - { label: "Programación", value: "Programación", color: "hsl(134, 95%, 90%)"}
      - { label: "Entorno", value: "Entorno", color: "hsl(294, 95%, 90%)"}
      - { label: "SQL", value: "SQL", color: "hsl(265, 95%, 90%)"}
      - { label: "fundamentos de sotware", value: "fundamentos de sotware", color: "hsl(354, 95%, 90%)"}
      - { label: "Linux", value: "Linux", color: "hsl(213, 95%, 90%)"}
      - { label: "Fundamentos de Data", value: "Fundamentos de Data", color: "hsl(256, 95%, 90%)"}
      - { label: "arquitectura", value: "arquitectura", color: "hsl(143, 95%, 90%)"}
      - { label: "Modelado de datos", value: "Modelado de datos", color: "hsl(330, 95%, 90%)"}
      - { label: "concepto", value: "concepto", color: "hsl(207, 95%, 90%)"}
      - { label: "Data science", value: "Data science", color: "hsl(7, 95%, 90%)"}
      - { label: "Procesamiento de datos", value: "Procesamiento de datos", color: "hsl(23, 95%, 90%)"}
      - { label: "Matematicas", value: "Matematicas", color: "hsl(44, 95%, 90%)"}
      - { label: "ETL", value: "ETL", color: "hsl(163, 95%, 90%)"}
      - { label: "AI", value: "AI", color: "hsl(256, 95%, 90%)"}
      - { label: "Marca Personal", value: "Marca Personal", color: "hsl(325, 95%, 90%)"}
      - { label: "Limpieza de datos", value: "Limpieza de datos", color: "hsl(284, 95%, 90%)"}
      - { label: "Pipelines", value: "Pipelines", color: "hsl(79, 95%, 90%)"}
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
  Type:
    input: select
    accessorKey: Type
    key: Type
    id: Type
    label: Type
    position: 100
    skipPersist: false
    isHidden: false
    sortIndex: -1
    options:
      - { label: "Apunte", value: "Apunte", color: "hsl(205, 95%, 90%)"}
      - { label: "Curso", value: "Curso", color: "hsl(132, 95%, 90%)"}
      - { label: "Video", value: "Video", color: "hsl(181, 95%, 90%)"}
      - { label: "imagen", value: "imagen", color: "hsl(106, 95%, 90%)"}
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
config:
  remove_field_when_delete_column: false
  cell_size: normal
  sticky_first_column: false
  group_folder_column: 
  remove_empty_folders: false
  automatically_group_files: false
  hoist_files_with_empty_attributes: true
  show_metadata_created: false
  show_metadata_modified: false
  show_metadata_tasks: false
  show_metadata_inlinks: false
  show_metadata_outlinks: false
  show_metadata_tags: false
  source_data: current_folder
  source_form_result: 
  source_destination_path: /
  row_templates_folder: /
  current_row_template: 
  pagination_size: 200
  font_size: 19
  enable_js_formulas: false
  formula_folder_path: /
  inline_default: false
  inline_new_position: last_field
  date_format: yyyy-MM-dd
  datetime_format: "yyyy-MM-dd HH:mm:ss"
  metadata_date_format: "yyyy-MM-dd HH:mm:ss"
  enable_footer: false
  implementation: default
filters:
  enabled: false
  conditions:
```