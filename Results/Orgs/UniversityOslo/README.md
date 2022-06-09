# University of Oslo Results

## What Contributed

### Threat Actor Context Ontology
The University of Oslo presented the [Threat Actor Context Ontology](https://github.com/oasis-open/tac-ontology) of the [OASIS Threat Actor Context Technical Committee (TAC TC)](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=tac) in support of cybersecurity automation and, in particular, the sense-making and decision-making functions of cyberspace defense as they are described in the [IACD framework](https://www.iacdautomate.org/). 

The core model of the TAC ontology is based on the [STIX 2.1 standard](https://docs.oasis-open.org/cti/stix/v2.1/stix-v2.1.pdf) and further augments it with other representations that describe components from the domain of Cyber Threat Intelligence (CTI). For example, we presented the [Threat Agent Library](https://www.researchgate.net/publication/324091298_Threat_Agent_Library_Helps_Identify_Information_Security_Risks) (developed by Tim Casey and Intel Corporation in 2007) that describes a threat actor type typology. We extended the ontology by encoding the TAL typology in Web Ontology Language (OWL). We demonstrated the reasoning capability of the ontology by automatically inferring the types of a set of adversaries and their activities in near real-time (e.g., cybercriminals or nation-state-sponsored).

The following video provides an introduction to the TAC ontology and how it consumes STIX data to provide us with searchable, shareable, and interoperable knowledge graphs of CTI as linked open data.

TAC Ontology Video on Youtube: https://www.youtube.com/watch?v=p5cF6ZmNaNI.

We further discussed how the TAC ontology could integrate with other open-source solutions (STIX shifter and Kestrel threat hunting language) and utilize open standards (OpenC2, CACAO, SBOM, VEX, CSAF) to address different cybersecurity automation use cases.

### CACAO Security Playbooks
As an ad-hoc contribution, we briefed about the [CACAO](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=cacao) security playbooks "standard" and presented use cases on how CACAO can orchestrate and automate cyberspace defense, also by utilizing STIX and TAXII, OpenC2, Kestrel, and the TAC ontology. An emphasis was given in demonstrating how CACAO can utilize OpenC2 for command and control of cyber defense systems and components. Finally, we discussed and demonstrated how we can share (and couple with CTI) CACAO security playbooks using STIX 2.1. To achieve that we designed a STIX 2.1 property extension for the Course of Action object type. The STIX 2.1 "Extension" we demonstrated is available on [GitHub](https://github.com/fovea-research/stix2.1-coa-playbook-extension). We provided for further reading a [technical report](https://arxiv.org/pdf/2203.04136.pdf) that explains the STIX 2.1 extension we presented.

## Use Cases and Take Aways
The participants showed high interest in the inference capabilities of the Threat Actor Context ontology to derive new understandings pertinent to CTI and support human intelligence analysis and decision making. 

Another well-received aspect is the availability of a plethora of open source and closed source software that can consume the ontology and be used as knowledge management solutions.



# Jump to
## Return to Contributing Companies/Agencies/Universities
[return to Contributing Companies/Agencies/Universities](../../Orgs)

## Return to Results
[return to Results](../../../Results)

## Return to Agenda
[return to Agenda](../../../Agenda)

## Return to Home
[return to Home](../../../index.md)
