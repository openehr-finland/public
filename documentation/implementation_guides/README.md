# OpenEHR Finland implementation guides
Under this section, openEHR Finland publishes all the implementation guides that are ready or under review.

> **STATUS:** TRIAL

## Intro to implementation guides

The models in openEHR, both the reference model (RM) and most archetypes, are supposed to be used globally and usually have functions that cover different national needs if you use the models wisely. However, in order to fit the laws and working methods of an individual country, you may need to agree on HOW the models should be used to meet the national requirements. This should be done in a common way so that different suppliers and caregivers do the same and thus more smoothly can reuse applications, reuse software modules and exchange data.

## Status of implementation guides

Each version of an implementation guide has a status to indicate how mature it is as follows:

- TRIAL - Is in open auditing or commenting. Can be used in production, but changes may occur.
- STABLE - Verified by openEHR Finland and is considered “in use”, no further changes are added. If there is a need for changes, a new version is created.

## Version management

Version management should follow semantic versioning when the implementation guide gets the Trial status. The version to be set then is 1.0.0.

## Directive

In each implementation guide there are directives on how to do and they should be interpreted as follows:

- MUST (MUST)
-- This is an absolute requirement, no exceptions
- MUST NOT (NOT)
-- This is absolutely forbidden, no exceptions
- SHOULD (SHOULD)
-- This should be followed, exceptions are allowed for a justified reason

## Create implementation guides

Implementation guides must follow a uniform structure, which is defined in the [template]([https://github.com/openehr-finland/documentation/blob/main/implementation_guides/IG_template.md](https://github.com/openehr-finland/public/blob/main/documentation/implementation_guides/IG_template.md)) of the implementation guide.

Attachments that should be part of the published implementation guide are last placed in the guide while working materials linked to the development of a new implementation guide should be added as subpages to the implementation guide itself. This is to make it clear what is part of the guide itself (regardless of status) and what is other related material.

## Management of associated models

Models (archetypes and templates) created with the development of an implementation guide should be handled in accordance with seperate guides (TBD). Therefore, the work will take place in separate projects at first. When the work is to be sent for review, a release containing the models should be included. When the work is considered ready and ready to be published (in accordance with the rules specified in the chapter hereinafter referred to as “Review and publication process”).

## Translation

All implementation guides are written in English to make them more accessible. Finnish translations of the implementation guides can be added as subpages to the English versions.

## Review and publication process

When the implementation guide is considered ready for review, a request for comments and official approval process must be implemented as described on page [https://github.com/openehr-finland/public/documentation/](https://github.com/openehr-finland/public/blob/main/documentation/README.md).

Once the implementation guide is considered to be fully revised and completed, it should be presented to openEHR Finland as an organization by bringing it up at an administrative meeting. There, the guide must be approved as final before its official publication. This also applies to when the guide should go from TRIAL to STABLE status.

The implementation guide is then published on the GitHub page and its status is changed to STABLE. The news of the publication will be disseminated via openEHR Finland's mailing list and communicated also to other relevant stakeholders.
