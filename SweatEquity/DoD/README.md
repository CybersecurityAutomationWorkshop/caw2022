# DoD Sweat Equity

DoD is a cochair and has members of the OpenC2 Technical Committee,
has individual participants in the Security Posture Attribute
Collection and Evaluation
([PACE](https://github.com/opencybersecurityalliance/PACE/tree/main/docs/Arch))
OASIS Open Project,
and sponsors HII to participate in both OpenC2 and PACE.

## 1. Software/Application/Device Contributions
DoD's contributions to the CAW include development of:
* OpenC2 actuator profiles (both PACE and non-PACE related)
* Profile creation and message validation tools
* Posture Attribute Repository (PAR) proof of concept

### 1.1 OpenC2 Actuator Profiles

### 1.2 Profile Creation and Message Validation Tools
The OpenC2 [JADN Software](https://github.com/oasis-open/openc2-jadn-software) repo contains:
* Template to use when creating new actuator profiles
* Template to use when developing OpenC2 producer and consumer device schemas
* Software to translate schemas between multiple formats
* Software to validate profile and device schemas
* Software to resolve external references to produce a self-contained device schema
* Example actuator profile and device schemas (SLPF, PAC, SBOM, ER)
* Example OpenC2 commands and responses
* Software to validate commands and responses against a device schema

This software can be used both when creating new actuator profiles and when
developing and testing OpenC2 implementations prior to interoperability testing.

![Schema Tools](https://raw.githubusercontent.com/oasis-tcs/openc2-usecases/main/Actuator-Profile-Schemas/images/ap-process.jpg)

### 1.3 Posture Attribute Repository Proof of Concept
Decision-making components will be able to retrieve PACE information from a
Posture Attribute Repository.

![PAR](https://raw.githubusercontent.com/opencybersecurityalliance/PACE/main/docs/Arch/par_01.png)

Although a specific PAR API has not yet been determined, DoD will develop and make available a PAR proof of concept
implemented on Amazon Web Services using a [GraphQL](https://aws.amazon.com/appsync/) interface*.
CAW participants will be able to query a set of dummy components (IT assets) and a set of random
but syntactically valid example SBOMs associated with those components.
PAR content will be managed exclusively by the Posture Attribute Collection and
Posture Attribute Evaluation systems; all user access is query-only.

`*` [This article](https://www.onegraph.com/blog/post/2/how-onegraph-onboards-users-who-are-new-to-graphql)
provides some background on GraphQL capabilities and our rationale for using it as a PAR API.

![GraphQL](images/AWS-GraphQL-s.png)

**PAR Structure**

Initially the PAR will include two types: Device and SBOM.
* A Device is a physical or virtual processing element owned or managed by an organization.
A device entry includes asset identifying and configuration information
including the SBOM(s) applicable to that device.
* A Software Bill of Materials ([SBOM](https://ntia.gov/SBOM))
is a nested inventory for software, a list of ingredients that make up software components.
An SBOM entry includes the SBOM unique identifier, NTIA's seven
[SBOM minimum elements](https://www.ntia.doc.gov/files/ntia/publications/sbom_minimum_elements_report.pdf),
and the SBOM document in one of several types and data formats.

**Accessing the PAR**

The [CAW PAR proof of concept](https://job35fyyhbf3lppotkyvrtnjn4.appsync-api.us-east-1.amazonaws.com/graphql)
is a GraphQL endpoint (not web page) that implements the
[PAR API](https://raw.githubusercontent.com/oasis-open/openc2-jadn-software/master/Schemas/par-api.jidl),
populated with a set of example devices and SBOMs.  See this [tutorial](PAR/PAR.md) to explore using the PAR.

## 2. Which interfaces in which usecases

[return to Home](../../index.md)
