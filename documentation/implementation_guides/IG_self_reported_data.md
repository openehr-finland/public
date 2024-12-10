# The well-being information reported by the citizen/patient/customer himself (MUST)

## Status

**DEV**

## Version history

| Version | Date | Update | Responsible
| --- | --- | --- | --- |
| 0.0.1 | 22.10.2024 | initial version | Henri Huttunen |
| 0.0.2 | 23.10.2024 | Added examples | Riikka Lahtela |

## Terminology

| Term/Concept | Description | Source |
| --- | --- | --- |
|  |  |  |
|  |  |  |

## Introduction

This implementation guide describes how the marking of well-being data reported by citizen/patient/customer themselves in openEHR data models should be implemented in Finland.

### Background

In Finland, well-being information refers to information reported by the customer himself, such as his own entries and notes, self-monitoring results and measurements, results of risk tests and virtual health checks or well-being checks, and other information produced by personal well-being applications. The well-being information can also include a self-care plan or a self-care plan.

Marking well-being information self-generated by a customer is particularly important, because in light of current legislation, social and healthcare service providers must be able to understand that the processed information is well-being information self-generated by the customer. The customer consent must be obtained for the utilization of welfare information in the provision of services. If well-being information is stored in the service provider's register, the information about the information source must be preserved or validated and recorded by a professional, in which case it becomes customer information.

### Related work

### Participants

- Riikka Lahtela / Istekki
- Heidi Koikkalainen / FreshEHR
- Henri Huttunen / UNA

## Implementation overview

The entry of well-being information reported by the customer is recommended to be done in archetypes at two different levels. This ensures flexibility and that the data source remains usable in different use cases.
1. The data models use the "Self-reported data" archetype as a basis
![kuva](https://github.com/user-attachments/assets/5e66a3c7-191b-491b-8ee1-50a371df60d9)

2. The source of the information is described by the attributes from the reference model (RM) at the archetype level as produced by the citizen himself<br/>
   2.1. ENTRY.provider: the ENTRY.provider attribute of the Entry class is used to define the information producer as a citizen. The attribute is not mandatory, because often the information producer is stored otherwise, e.g. composer or the other_participations attribute is used<br/>
   2.2. COMPOSITION.composer: in COMPOSITION.composer, the value of PARTY_PROXY is marked as self

Attention: the folder option offered by openEHR is not recommended for entering data produced by the citizen himself.

![kuva](https://github.com/user-attachments/assets/b2b14149-21b7-4b58-9f72-c0b4e155ed1a)

### Models and examples

In the following example, a template named Communication has been created in Archetype Designer. The COMPOSITION archetype of Self-reported data is used as a container archetype for the template. Thus, it does not contain anything, so either SECTION or ENTRY archetype(s) has to be added as content based on slot rules. Related to the topic of communication, the ENTRY archetype of Communication Capability and within it the CLUSTER archetype of Language, have been added in this example.
![kuva](https://github.com/openehr-finland/documentation/blob/main/implementation_guides/pics/Self_Example_Communication.png)

In addition, the value “self” is filled in Rm Attributes:
1) Self-reported data: COMPOSITION.composer > menu: Rm Attributes > field: composer (PARTY_PROXY)
![kuva](https://github.com/openehr-finland/documentation/blob/main/implementation_guides/pics/Self_Composer.png)

2) Communication Capability: ENTRY.provider > menu: Rm Attributes composer > field: provider (PARTY_PROXY)
![kuva](https://github.com/openehr-finland/documentation/blob/main/implementation_guides/pics/Self_Provider.png)

Technical version of the example: https://github.com/openehr-finland/openehr-finland/blob/b019cc8497d231c20e6e093b39914f37ebe1e196/local/Communication.t.json

### Detailed descriptions

#### The self-reported data archetype

The purpose of a self-reported data archetype is ”A container for information provided by an individual, to support clear separation of patient generated from clinician-generated health data”. 

The data source may vary from data recorded by patient’s own initiative (i.e. wellbeing data) to patient reported outcome measurements (PROM)/patient reported experience measurements (PREM) and patient recorded data of treatment at home. The data is either generated by the patient or by the device. 

The self-reported data archetype is used as a generic container that can include many contexts. In the template, the content of the self-reported data archetype can be compiled with any SECTION and ENTRY archetypes intended for the clinical purpose.

## Attachments
 