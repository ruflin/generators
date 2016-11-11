# Kibana templates extractor

Kibana stores its data in an elasticsearch index. Dashboards, index-pattern, search and visualization are all stored as JSON with encoded JSON strings inside. Exporting and versioning these files is kind of clunky as all data is one line. Trying to figure out what exactly changed can be hard.

These `kibana_extract.py` script takes the exported kibana json files, extract the nested json strings to json itself and store them in a separate document. The top level json document is formatted as json and indented.

The `kibana_consturct.py` script does the opposite and takes all the documents and constructs again a valid Kibana json file with the nested documents inside based on the `j2` templates.
