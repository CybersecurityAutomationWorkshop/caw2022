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
* OpenC2 message validation tools
* Non-OpenC2 interface specifications (PACE PAR)
* Posture attribute repository (PAR) proof of concept

### 1.1 OpenC2 Actuator Profiles

### 1.2 OpenC2 message validation tools

### 1.3 Non-OpenC2 interface specifications (PACE PAR)

### 1.4 Posture Attribute Repository proof of concept
DoD will develop and make available to CAW participants a PAR proof of concept
implemented on Amazon Web Services using a [GraphQL interface](https://aws.amazon.com/appsync/).
CAW participants will be able to query a set of dummy components (IT assets) and a set of random
but syntactically valid example SBOMs associated with those components.
PAR content will be managed exclusively by the Posture Attribute Collection and
Posture Attribute Evaluation systems; all user access is query-only.

![GraphQL](images/AWS-GraphQL-s.png)

**PAR Structure**

Every entry in the PAR has an ID, which must be globally unique and in the form of an
Internationalized Resource Identifier ([IRI](https://datatracker.ietf.org/doc/html/rfc3987)).
Initially the PAR will include two entry types: devices and SBOMs.
* A device is a physical or virtual processing element owned or managed by an organization.
A device entry includes asset identifying and configuration information
including the SBOM(s) applicable to that device.
* A Software Bill of Materials ([SBOM](https://ntia.gov/SBOM))
is a nested inventory for software, a list of ingredients that make up software components.
An SBOM entry includes the SBOM unique identifier, the seven
[SBOM minimum elements](https://www.ntia.doc.gov/files/ntia/publications/sbom_minimum_elements_report.pdf),
and the SBOM document in one of several types and data formats.

## 2. Which interfaces in which usecases

[return to Home](../../index.md)
