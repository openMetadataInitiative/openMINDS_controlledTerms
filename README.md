# openMINDS_controlledTerms

The openMINDS_controlledTerms repository is part of the open Metadata 
Initiative for Neuroscience Data Structures (openMINDS). It contains the 
schema templates as well as the corresponding terminologies (JSON-LDs) for all 
terms that are defined and maintained via the EBRAINS Curation service 
(EBRAINS terminology) and / or related ontologies.

For more information on openMINDS please go to the main repository:  
https://github.com/HumanBrainProject/openMINDS

## v1.0 (schema-templates)
Except for the schema-type (`_type`), the schema-template is identical across 
all controlled terms (cf. 
[controlledTerm.schema.tpl.json](https://raw.githubusercontent.com/HumanBrainProject/openMINDS_controlledTerms/master/v1.0/controlledTerm.schema.tpl.json)).

The schema-type is unique for each terminology it controlles and extends the 
generic controlledTerm.schema.tpl.json (cf., e.g., 
[biologicalSex.schema.tpl.json](https://raw.githubusercontent.com/HumanBrainProject/openMINDS_controlledTerms/master/v1.0/biologicalSex.schema.tpl.json)). 
This differentiation facilitates the identification of conceptually related 
terms.

## v1.0-terminologies
The controlled terminologies are stored as JSON-LDs, conceptually grouped 
according to the corresponding schema-type. For simplicity the name of the 
term defined in each JSON-LD is used as filename and as identifier (cf. 
[female.jsonld](https://raw.githubusercontent.com/HumanBrainProject/openMINDS_controlledTerms/master/v1.0-terminologies/biologicalSex/female.jsonld)).
