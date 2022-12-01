Possibility in time for another repo would be established for interworking requirements and conformance specifications. E.g.

## Requirements
1. CASP compliant interfaces meet one of the following specifications for sharing threat indicators:
   + STIX 2.1
   + for sharing indicators of behavior, CASP compliant interfaces meet one of the following specifications:
      * IoB
   + for sharing information about threat actors, CASP compliant interfaces meet one of the following specifications:
      * TAC
1. CASP compliant interfaces meet one of the following specifications for sharing playbooks
   + CACAO
1. CASP compliant interfaces meet one of the following specifications for threat hunting
   + kestrel
1. CASP compliant interfaces use one of the following command languages for command & control:
   + OpenC2 over MQTT
   + OpenC2 over HTTPS
1. If security posture is assessed, CASP compliant systems meet one of the following specifications:
   + PACE
1. To aid in business decision making, CASP compliant systems WILL supply data to business decision making systems meeting one of the following specifications:
   + VSMI
1. CASP compliant systems WILL create complete Software Bill of Materials (SBOM) according to one of the following specifications:
   + For licensing use cases, SBOMs SHOULD be in SPDX format (per ISO/IEC 5692:2021) but MAY be in CycloneDX format as long as all necessary information is included for that usecase.
   + For cybersecurity use cases, SBOMs SHOULD be in CycloneDX format but MAY be in SPDX format as long as all necessary information is included for that usecase.
   + For software architecture use cases, SBOMs SHOULD be in one of the following formats:
      * CycloneDX
      * SPDX
1. CASP compliant systems WILL create Vulnerability Exploitability eXchange (VEX) documents for known vulnerabilities affecting the system and MAY create VEX documents for vulnerabilities not-affecting the system.
   + VEX documents SHOULD be in CSAF format using the VEX profile but MAY be in CycloneDx format as long as all necessary VEX information is included.


## Conformance
Create conformance profiles for
each logical set of requirements (eg PACE, CTI, VSM, OpenC2)
and create conformance requirements for each as part of CASP-compliant system.
