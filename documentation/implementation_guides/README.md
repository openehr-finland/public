# OpenEHR Finland implementation guides
Under this section, we publish all the implementation guides that we work with or developed within the framework of the openEHR Finland work.

## Intro to implementation guides

The models in openEHR, both the reference model (RM) and most archetypes, are supposed to be used globally and usually have functions that cover different national needs if you use the models wisely. However, in order to fit the laws and working methods of an individual country, you may need to agree on HOW the models should be used to meet the national requirements. This should be done in a common way so that different suppliers and caregivers do the same and thus more smoothly can reuse applications, reuse software modules and exchange data.

## Status of implementation guides

Each version of an implementation guide has a status to indicate how mature it is as follows:

- DEV - Under development, can be changed at any time
- TRIAL - Is audited via public open referral opportunity and is considered ready to be tested in production, changes may apply.
- STABLE - Verified by at least two independent parties in the production environment and is considered “in use”, no further changes are added. If there is a need for changes, a new version is created.

## Version management

Version management should follow semantic versioning when the implementation guide gets the Trial status. The version to be set then is 1.0.0.

## Directive

In each implementation guide there are directives on how to do and they should be interpreted as follows:

- MUST (MUST)
-- This is an absolute requirement, no exceptions
- MUST NOTE (NOT)
-- This is absolutely forbidden, no exceptions
- SHOULD (SHOULD)
-- This should be followed, exceptions are allowed for a justified reason

## Create implementation guides

Implementation guides must follow a uniform structure, which is defined in the [template](https://github.com/openehr-finland/documentation/blob/main/implementation_guides/IG_template.md) of the implementation guide.

Attachments that should be part of the published implementation guide are last placed in the guide while working materials linked to the development of a new implementation guide should be added as subpages to the implementation guide itself. This is to make it clear what is part of the guide itself (regardless of status) and what is other related material.

## Management of associated models

Models (Archetypes and templates) created with the development of an implementation guide should be handled in accordance with seperati quides (TBD). In conclusion, the work will take place in a separate projects at first. When the work is to be sent on referral, a release containing the models should be included. When the work is considered ready and ready to be published (in accordance with the rules specified in the chapter hereinafter referred to as “Review and publification process”), the models should be put in a separate folder and merged back to the master branch.

## Translation

All implementation guides are written in English to make it more accessible. The Finnish translation of the implementation guide can be added as a subpage to the English version.

## Review and publification process

When the implementation guide is considered ready to be reviewed, the request for comments and approval process must be implemented as described on page https://github.com/openehr-finland/documentation.

When the implementation guide is considered to be revised and completed, this should be lifted to openEHR Finland as an organization by taking this up at an administrative meeting. There, the guide must be approved as final before publication before the publication itself. This also applies to when the guide should go from Trial to Stable.

Publication is then on the Github page. Status is changed to the Trial. Then the news of publication will be spread via openEHR Finland's mailing list and contact other needed stakeholders about the publication.
