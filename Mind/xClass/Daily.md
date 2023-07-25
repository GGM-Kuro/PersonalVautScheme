---
limit: 100
mapWithTag: true
icon: clipboard-list
excludes: 
extends: 
version: 1
---

mood:: {"type":"Select","options":{"valuesList":{"1":"😁","2":"😣","3":"😒"},"sourceType":"ValuesList","valuesListNotePath":"","valuesFromDVQuery":""}}
train:: {"type":"Boolean","options":{{"valuesList":{"true":"✅","false":"❌"}}}
read:: {"type":"Number","options":{"step":"1","min":"0"}}
practice:: {"type":"Cycle","options":{"valuesList":{"1":"❌","2":"✅"},"sourceType":"ValuesList","valuesListNotePath":"","valuesFromDVQuery":""}}
english:: {"type":"Cycle","options":{"valuesList":{"1":"❌","2":"✅"},"sourceType":"ValuesList","valuesListNotePath":"","valuesFromDVQuery":""}}
activity:: {"type":"Cycle","options":{"valuesList":{"1":"❌","2":"✅"},"sourceType":"ValuesList","valuesListNotePath":"","valuesFromDVQuery":""}}
breackfast:: {"type":"Cycle","options":{"valuesList":{"1":"❌","2":"✅"},"sourceType":"ValuesList","valuesListNotePath":"","valuesFromDVQuery":""}}