# openMINDS_controlledTerms

The openMINDS_controlledTerms repository is part of the open Metadata 
Initiative for Neuroscience Data Structures (openMINDS). It contains the 
schema-templates as well as the corresponding terminologies (JSON-LDs) for all 
terms that are defined and maintained via the EBRAINS Curation service and / or 
related ontologies.

For more information on openMINDS in general and the processing pipelines for the schema-templates please go to the main repository: https://github.com/HumanBrainProject/openMINDS

## v1.0 (schema-templates)
The controlledTerms v1.0 schemas are JSON-schema inspired schema-templates with a few custom template-properties (prefixed with `"_"`) which allow us to simplify their readability and increase their reusability.

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

## How to contribute
When contributing to this repository, please first discuss the change you wish to make via issue before making a change. 

For providing feedback or for change requests to specific schema-templates or terminologies please name the corresponding file name in the issue title and describe your concern / request in a comment.

You can also contribute directly by making a Pull Request (PR). Please name at least one member of the openMINDS development team to review your PR. To facilitate the review process describe shortly the purpose of your PR and what is affected by it. If your PR is accepted it will be merged by the assigned reviewer.

## License
This work is licensed under the MIT License.
