<a href="https://github.com/HumanBrainProject/openMINDS_controlledTerms/blob/v1/img/openMINDS_terms_logo.png">
    <img src="https://github.com/HumanBrainProject/openMINDS_controlledTerms/blob/v1/img/openMINDS_terms_logo.png" alt="openMINDS controlledTerms logo" title="openMINDS controlledTerms" align="right" height="70" />
</a>

# openMINDS_controlledTerms

The openMINDS_controlledTerms repository is part of the **open** **M**etadata **I**nitiative for **N**euroscience **D**ata **S**tructures (openMINDS). It contains the schema-templates as well as corresponding terminologies (as JSON-LDs) for all terms that are defined and maintained centrally in this repository. Where applicable, the defined terms are connected to a matching ontological term. Schemas of openMINDS_core as well as openMINDS_SANDS reference to these controlled terms.

The major versions are developed and maintained in different version-branches. The default branch is always the latest version-branch. **Each version can be accessed by checking out the corresponding version-branch.** This README describes the version-branch v1. 

For more information on openMINDS in general, please go to the main repository: https://github.com/HumanBrainProject/openMINDS

## schemas
The controlledTerms v1 schemas are defined as JSON-schema inspired templates with only a few customized technical properties (prefixed with `"_"`). These simplified schema-templates are easy to read and can be robustly translated to other, well known target formats (e.g., HTML, JSON-schema, etc.). 

Except for the schema-template-property (`"_type"`), the schema-template is identical across all controlled terms (cf. the "abstract" schema-template used for all controlled terms:
[controlledTerm.schema.tpl.json](https://raw.githubusercontent.com/HumanBrainProject/openMINDS_controlledTerms/master/v1.0/controlledTerm.schema.tpl.json)).

The schema-template-property `"_type"` is unique for each terminology it controlles and extends the generic controlledTerm.schema.tpl.json (cf., e.g., `"_type": "https://openminds.ebrains.eu/controlledTerms/BiologicalSex"` in [biologicalSex.schema.tpl.json](https://raw.githubusercontent.com/HumanBrainProject/openMINDS_controlledTerms/master/v1.0/biologicalSex.schema.tpl.json)). This differentiation facilitates the identification of conceptually related terms (cf. **terminologies**).

## terminologies
The controlled terminologies are stored as JSON-LDs, conceptually grouped 
according to the corresponding schema-type. For simplicity the name of the 
term defined in each JSON-LD is reused in the filename and identifier (cf. 
[female.jsonld](https://raw.githubusercontent.com/HumanBrainProject/openMINDS_controlledTerms/master/v1.0-terminologies/biologicalSex/female.jsonld)).

## How to contribute
Please check our [contribution document](./CONTRIBUTING.md).

## License
This work is licensed under the MIT License.

**Logo:** The openMINDS logo was created by U. Schlegel, based on an original sketch by C. Hagen Blixhavn and feedback by L. Zehl.
