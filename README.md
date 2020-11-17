# openMINDS_controlledTerms

The openMINDS_controlledTerms repository is part of the open Metadata 
Initiative for Neuroscience Data Structures (openMINDS). It contains the 
schema-templates as well as the corresponding terminologies (JSON-LDs) for all 
terms that are defined and maintained via the EBRAINS Curation service and / or 
related ontologies.

For more information on openMINDS in general and the processing pipelines for the schema-templates please go to the main repository:  
https://github.com/HumanBrainProject/openMINDS

## v1.0 (schema-templates)
The controlledTerms schemas are JSON-schema inspired schema-templates with a few custom template-properties (prefixed with `"_"`) which allow us to simplify their readability and increase their reusability.

Except for the schema-template-property (`"_type"`), the schema-template is identical across 
all controlled terms (cf. the "abstract" schema-template used for all controlled terms:
[controlledTerm.schema.tpl.json](https://raw.githubusercontent.com/HumanBrainProject/openMINDS_controlledTerms/master/v1.0/controlledTerm.schema.tpl.json)).

The schema-template-property `"_type"` is unique for each terminology it controlles and extends the 
generic controlledTerm.schema.tpl.json (cf., e.g., `"_type": "https://openminds.ebrains.eu/controlledTerms/BiologicalSex"` in
[biologicalSex.schema.tpl.json](https://raw.githubusercontent.com/HumanBrainProject/openMINDS_controlledTerms/master/v1.0/biologicalSex.schema.tpl.json)). 
This differentiation facilitates the identification of conceptually related 
terms (cf. v1.0-terminologies).

## v1.0-terminologies
The controlled terminologies are stored as JSON-LDs, conceptually grouped 
according to the corresponding schema-type. For simplicity the name of the 
term defined in each JSON-LD is reused in the filename and identifier (cf. 
[female.jsonld](https://raw.githubusercontent.com/HumanBrainProject/openMINDS_controlledTerms/master/v1.0-terminologies/biologicalSex/female.jsonld)).

## License
This work is licensed under the MIT License.
