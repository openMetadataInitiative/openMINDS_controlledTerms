<a href="https://github.com/HumanBrainProject/openMINDS_controlledTerms/blob/v1/img/openMINDS_terms_logo.png">
    <img src="https://github.com/HumanBrainProject/openMINDS_controlledTerms/blob/v1/img/light_openMINDS-terms-logo.png" alt="openMINDS controlledTerms logo" title="openMINDS controlledTerms" align="right" height="70" />
</a>

# openMINDS_controlledTerms

The openMINDS_controlledTerms repository is part of the **open** **M**etadata **I**nitiative for **N**euroscience **D**ata **S**tructures (openMINDS). It contains the schema-templates as well as corresponding terminologies (as JSON-LDs) for all terms that are defined and maintained centrally in this repository. Where applicable, the defined terms are connected to a matching ontological term. Schemas of openMINDS_core as well as openMINDS_SANDS reference to these controlled terms.

The **openMINDS_controlledTerms** repository is part of the **open** **M**etadata **I**nitiative for **N**euroscience **D**ata Structures (**openMINDS**). It contains schemas for the consistent registration of well-defined terms as well as a corresponding library of terminologies with controlled instances (including links to ontological terms where applicable). The openMINDS_controlledTerms instances are used within the EBRAINS Knowledge Graph to increase data integration and foster relations to other metadata initiatives.

The major versions are developed and maintained in different version-branches. **Each version can be accessed by checking out the corresponding version-branch.** You are currently on **version-branch v1**. Note: the default branch is always the latest version-branch in use within the EBRAINS Knowledge Graph. 

For application and technical details please go to the [central openMINDS repository](https://github.com/HumanBrainProject/openMINDS) or the [openMINDS Collab](https://wiki.ebrains.eu/bin/view/Collabs/openminds/).

## schemas
In the **schemas** directory, all openMINDS_controlledTerms schemas (v1) are defined in the openMINDS syntax (`*.schema.tpl.json`). Details about the openMINDS syntax can be found [here](https://wiki.ebrains.eu/bin/view/Collabs/openminds/Documentation/Implementation%20details/#HTheopenMINDSsyntax). To ensure a central access point for all openMINDS schemas across all versions and metadata models, each change in the schemas will lead to a new build of the central openMINDS repository.

## instances
In the **instances** directory, it is possible to store **controlled instances** (as JSONLDs) for all openMINDS_controlledTerms schemas (v1), except `TermSuggestion`. The subdirectory of **instances** should resemble the **schemas** directory with the schema type as an additional subdirectory. As mentioned above, the controlled instances are used within the EBRAINS Knowledge Graph to increase data integration and to foster relations with other metadata initiatives. Within the EBRAINS Knowledge Graph, a `TermSuggestion` can be used to suggest new controlled instances as potential keywords or study targets. 

**How to request new instances?** Requests for adding new controlled instances can be made by getting in touch with the openMINDS development team (through the issue tracker or the support email: coming soon). The team will attend to a request as soon as possible. Note that instances should be well defined to be useful for the community. They should at least provide a one sentence definition, and, where applicable, a reference to a matching ontology term.

**How to correctly define an openMINDS instance?** openMINDS instances are written as JSON-LDs. A correctly instantiated openMINDS JSON-LD should always contain the following technical attributes, and at least the required properties of the respective schema type they are validated against:

```json
{
  "@context": {
    "@vocab": "https://openminds.ebrains.eu/vocab/"
  },
  "@id": "https://openminds.ebrains.eu/instances/OPENMINDS_SCHEMA_NAME/HUMAN_READABLE_INSTANCE_ID",
  "@type": "OPENMINDS_SCHEMA_TYPE",
  "PROPERTY_NAME": "METADATA_VALUE"
}
```

The values written in capital letters need to be replaced accordingly. Here a full example of an instance for an openMINDS_controlledTerms schema type (cf. `/instances/species/homoSapiens.jsonld`):

```json
{
  "@context": {
    "@vocab": "https://openminds.ebrains.eu/vocab/"
  },
  "@id": "https://openminds.ebrains.eu/instances/species/homoSapiens",
  "@type": "https://openminds.ebrains.eu/controlledTerms/Species",
  "definition": "The species *Homo sapiens* (humans) belongs to the family of *hominidae* (great apes).",
  "description": null,
  "interlexIdentifier": "http://uri.interlex.org/base/ilx_0105114",
  "knowledgeSpaceLink": "https://knowledge-space.org/wiki/NCBITaxon:9606#human",
  "name": "Homo sapiens",
  "preferredOntologyIdentifier": "http://purl.obolibrary.org/obo/NCBITaxon_9606",
  "synonym": [
    "Homo sapien",
    "human",
    "man"
  ] 
}
```
Note that properties that are defined as optional in an openMINDS schema can either be provided with a `null` value in the JSON-LD or left out completely.
 
## tests
In the **tests** directory you can find JSON-LDs designed to test the validation behaviour of each schema. The subdirectory of **tests** should resemble the **schemas** directory with the schema type as an additional subdirectory. Each JSON-LD follows the naming convention `{schema_name}-{custom_test_name}.jsonld`. For test cases supposed to fail the validation, the suffix **`-nok`** should be attached (`{schema_name}-{custom_test_name}-nok.jsonld`). The tests are validated every time a change is introduced and therefore are ensuring the correct behavior of the schemas.

## How to contribute
Please check our [contribution document](./CONTRIBUTING.md).

## License
This work is licensed under the MIT License.

**Logo:** The openMINDS logo was created by U. Schlegel, based on an original sketch by C. Hagen Blixhavn and feedback by L. Zehl.

