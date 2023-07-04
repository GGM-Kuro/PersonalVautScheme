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
    position: 1
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
  bike:
    input: number
    accessorKey: bike
    key: bike
    id: bike
    label: bike
    position: 4
    skipPersist: false
    isHidden: false
    sortIndex: -1
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
  mood:
    input: select
    accessorKey: mood
    key: mood
    id: mood
    label: mood
    position: 2
    skipPersist: false
    isHidden: false
    sortIndex: -1
    options:
      - { label: "😣", value: "😣", color: "hsl(0,74%,82%)"}
      - { label: "😒", value: "😒", color: "hsl(0,0%,58%)"}
      - { label: "😁", value: "😁", color: "hsl(121,100%,76%)"}
      - { label: "<% tp.system.suggester(['😁','😣','😒'], ['😁','😣','😒']) %>", value: "<% tp.system.suggester(['😁','😣','😒'], ['😁','😣','😒']) %>", color: "hsl(358, 95%, 90%)"}
      - { label: "<% await tp.system.suggester(['😁','😣','😒'], ['😁','😣','😒']) %>", value: "<% await tp.system.suggester(['😁','😣','😒'], ['😁','😣','😒']) %>", color: "hsl(117, 95%, 90%)"}
      - { label: "<% await tp.system.suggester(['😁','😣','😒'], ['😁','😣','😒']); %>", value: "<% await tp.system.suggester(['😁','😣','😒'], ['😁','😣','😒']); %>", color: "hsl(107, 95%, 90%)"}
      - { label: "<% await tp.system.suggester(['😁','😣','😒'], ['😁','😣','😒'],true,'how was the day?') %>", value: "<% await tp.system.suggester(['😁','😣','😒'], ['😁','😣','😒'],true,'how was the day?') %>", color: "hsl(233, 95%, 90%)"}
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
      option_source: manual
  practice:
    input: select
    accessorKey: practice
    key: practice
    id: practice
    label: practice
    position: 100
    skipPersist: false
    isHidden: false
    sortIndex: -1
    options:
      - { label: "❌", value: "❌", color: "hsl(84, 95%, 90%)"}
      - { label: "✅", value: "✅", color: "hsl(10, 95%, 90%)"}
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
  englishClass:
    input: select
    accessorKey: englishClass
    key: englishClass
    id: englishClass
    label: englishClass
    position: 100
    skipPersist: false
    isHidden: false
    sortIndex: -1
    options:
      - { label: "❌", value: "❌", color: "hsl(176, 95%, 90%)"}
      - { label: "✅", value: "✅", color: "hsl(10, 95%, 90%)"}
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
  pagination_size: 10
  font_size: 16
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