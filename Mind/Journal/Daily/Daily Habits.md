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
      - { label: "❌", value: "❌", color: "hsl(0,95%,84%)"}
      - { label: "✅", value: "✅", color: "hsl(119,100%,80%)"}
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
  english:
    input: select
    accessorKey: english
    key: english
    id: englishClass
    label: english
    position: 100
    skipPersist: false
    isHidden: false
    sortIndex: -1
    options:
      - { label: "❌", value: "❌", color: "hsl(15,94%,86%)"}
      - { label: "✅", value: "✅", color: "hsl(124,100%,85%)"}
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
  breackfast:
    input: select
    accessorKey: breackfast
    key: breackfast
    id: breackfast
    label: breackfast
    position: 100
    skipPersist: false
    isHidden: false
    sortIndex: -1
    options:
      - { label: "❌", value: "❌", color: "hsl(326, 95%, 90%)"}
      - { label: "✅", value: "✅", color: "hsl(127,100%,84%)"}
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
  train:
    input: select
    accessorKey: train
    key: train
    id: train
    label: train
    position: 100
    skipPersist: false
    isHidden: false
    sortIndex: -1
    options:
      - { label: "❌", value: "❌", color: "hsl(21, 95%, 90%)"}
      - { label: "✅", value: "✅", color: "hsl(119,100%,83%)"}
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
  read:
    input: number
    accessorKey: read
    key: read
    id: read
    label: read
    position: 100
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
  study:
    input: select
    accessorKey: study
    key: study
    id: study
    label: study
    position: 100
    skipPersist: false
    isHidden: false
    sortIndex: -1
    options:
      - { label: "✅", value: "✅", color: "hsl(124,100%,83%)"}
      - { label: "❌", value: "❌", color: "hsl(0,96%,90%)"}
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
  activity:
    input: select
    accessorKey: activity
    key: activity
    id: activity
    label: activity
    position: 100
    skipPersist: false
    isHidden: false
    sortIndex: -1
    options:
      - { label: "❌", value: "❌", color: "hsl(0,100%,88%)"}
      - { label: "✅", value: "✅", color: "hsl(141, 95%, 90%)"}
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