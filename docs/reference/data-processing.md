# Data processing

As a cyber threat intelligence platform, OpenCTI offers functionalities that enable users to move quickly from raw data to operational intelligence by building up high-quality, structured information.

To do so, the platform provides a number of essential capabilities, such as automated data deduplication, merging of similar entities while preserving relationship integrity, the ability to modulate the confidence levels on your intelligence, and the presence of inference rules to automate the creation of logical relationships among your data.

The purpose of this page is to list the features of the platform that contribute to the intelligibility and quality of intelligence.

## Deduplication

The first essential data intelligence mechanism in OpenCTI is the [deduplication](../usage/deduplication.md) of information and relations.

This advanced functionality not only enables you to check whether a piece of data, information or a relationship is not a duplicate of an existing element, but will also, under certain conditions, enrich the element already present.

If the new duplicated entity has new content, the pre-existing entity can be enriched with the new information from the duplicate.

It works as follows (see details in the [dedicated page](../usage/deduplication.md)):

- For entities: based on the entity's properties based on a specific ID generated by the "ID Contributing Properties" platform (properties listed on the dedicated page).
- For relationships: based on type, source, target, start time, and stop time.
- For observables: a specific ID is also generated by the platform, this time based on the specifications of the STIX model.

The ability to update and enrich is determined by the confidence level and quality level of the entities and relationships (see diagram on page [deduplication](https://docs.opencti.io/latest/usage/deduplication/?h=deduplic)).

## Merging

OpenCTI's [merging](../administration/merging.md) function is one of the platform's crucial data intelligence elements.

From the Data > Entities tab, this feature lets you merge up to 4 entities of the same type. A parent entity is selected and assigned up to three child entities.

The benefit of this feature is to centralize a number of similar elements from different sources without losing data or degrading the quality of the information. During merging, the platform will create relationships to anchor all the data to the consolidated entity.

This enrichment function consolidates the data and avoids duplication, but above all initiates a structured intelligence process while preserving the integrity of pre-existing relationships as presented [here](../usage/merging.md#data-streamlining-section).

## Confidence level and data segregation

Another key element of OpenCTI's data intelligence is its ability to apply confidence levels and to segregate the data present in the platform.

The [confidence level](../usage/reliability-confidence.md#confidence-level-section) is directly linked to users and [Role Based Access Control](../administration/users.md). It is applied to a user directly or indirectly via the confidence level of the group to which the user belongs. This element is fundamental as it defines the levels of data manipulation to which the user (real or connector) is entitled.

The correct application of confidence levels is all the more important as it will determine the confidence level of the data manipulated by a user. It is therefore a decisive mechanism, since it underpins the confidence you have in the content of your instance.

While it is important to apply a level of trust to your users or groups, it is also important to define a way of categorizing and protecting your data.

[Data segregation](../administration/segregation.md) makes it possible to apply marking definitions and therefore establish a standardized framework for classifying data.

These marking definitions, like the classic Traffic Light Protocols (TLP) implemented by default in the platform, will determine whether a user can access a specific data set. The marking will be applied at the group level to which the user belongs, which will determine the data to which the user has access and therefore the data that the user can potentially handle.

## Inference rules

In OpenCTI, data intelligence is not just about the ability to segregate, qualify or enrich data. OpenCTI's [inference rules](../administration/reasoning.md) enable you to mobilize the data on your platform effectively and operationally.

These predefined rules enable the user to speed up cyber threat management. For example, inferences can be used to automatically identify incidents based on a sighting, to create sightings on observables based on new observed data, to propagate relationships based on an observable, etc.

In all, the platform includes some twenty high-performance inference rules that considerably speed up the analysis and response to threats (see the full list [here](../administration/reasoning.md)).

These rules are based on a logical interpretation of the data, resulting in a pre-analysis of the information by creating relationships that will enrich the intelligence in the platform. There are three main benefits: efficiency, completeness and accuracy. These user benefits can be found [here](../usage/inferences.md).

Note: If these rules are present in the platform, they are not activated by default.

Once activated, they scan all the data in your platform in the background to identify all the existing relationships that meet the conditions of the rules. Then, the rules operate continuously to create relationships. If you deactivate a rule, all the objects and relationships it has created will be deleted.

These actions can only be carried out by an administrator of the instance.
