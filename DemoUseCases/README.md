# Demo Use Cases
## 1. Intro and Background

This and subtending pages describe the use cases
that the Cybersecurity Automation Workshop
interoperation scenarios are a part of.

This page is has 4 sections:
- this intro and background section
- big picture scenarios
- mid-level Scenarios
- detailed interoperation demos

At the workshop, the intent is to get working
the detailed interoperation demos.
For example HII OIF Orchestration retrieving an SBOM
from sFractal BlinkMaHa over MQTT using OpenC2 command
{link above to actual scenario}.
The list of detailed interoperation demos is in the
last section of this document. The intent of big picture and mid-level
scenarios is to show how those demos fit into the larger
cybersecurity automation landscape.

### 1.1 IACD Framework
The demo use cases will follow a modular functional framework
from Integrated Adaptive Cyber Defense (IACD).
In particular, it will use the sensing, sense making,
decision making, and acting terminology and
functional architecture.
See [IACD](./iacd.md) for more info.


## 2. Big Picture Ideal Use Cases

These are realistic (aka complex) use cases
and hence there are many elements for a given use case.
Any given use case will have:
- situation (e.g. "Criminal hackers are currently in the system")
- industry (e.g. "healthcare")
- organization (e.g. "General Hospital")
- infrastructure systems (e.g. BestInClass intrusion detection system, Stixshifter, PACE PES/PCS/PAR, ...)
- attributes (e.g. asset type, triage scale, SBOMs, VEXs)
- parameters (e.g. asset type = respirator, triage = life threatening, SBOM = incomplete CycloneDx, ...)
- assets (both micro e.g. mri47 with particular attributes/parameters, and macro e.g. 234 "level 1" devices with SBOMs and VEXs)
- playbooks (e.g. CACAO playbook to handle a particular set of conditions)
- security policies (e.g. General Hospital may choose to do different actions on VEX product_status="not affected/component_not_present" than on "not affected/vulnerable_code_not_in_execute_path" whereas Podunk Rural Community Hospital may choose to lump several/all VEX flags together.

The demonstrable use interoperability will tend to be down in the weeds
(eg HII OIF Orchestrator sending a retrieve-SBOM OpenC2 command
over MQTT to sFractal BlinkyMaHa).
This section will attempt to define some big picture use cases which
those specific interoperability use cases fit into.

These big-picture scenarios are:
- Enterprise Security Posture
    + See [Enterprise Security Posture](./enterprise_posture.md()
    + In this example, the enterprise (a large company or a large government agency) has a very complex security posture based on many factors across many internal organizations located in many places. But for the purpose of an executive dashboard, the security posture is bucketed into one of four states.
- comply to connect
   + See [comply to connect](./comply2connect.md)
   + https://www.cybersecurityautomationworkshop.org/Results/UseCases/ComplyToConnect/
- create some business-as-usual scenario
- create some threat-intel-comes-in scenario
- create some non-crippling-attack scenario
- create some material-attack in-progress scenario

## 3. Mid-level Scenarios

- connectors from big-pic business-as-usual to details
    + need to create
- connectors from big-pic threat-intel-comes-in to details
    + need to create
- connectors from big-pic non-crippling-attack to details
    + need to create
- connectors from big-pic material-attack to details
    + need to create

## 4. Interoperability Demos

blah blah
- Specific use case called whatever
- demo 1 of whatever (eg between two systems of single participant)
- demo 2 of whatever (eg between participant1 and participant2)
-  ... demo N of whatever
-  Next use case of this other thing
- demo 1 of this other thing
 ...

## 5 Other stuff that needs to get entered
Mine the following to flesh out Sections 2,3,4 better:
- PACE collect SBOM use cases
    + https://github.com/opencybersecurityalliance/PACE/blob/main/docs/UseCases/collect_sbom_from_device.md
    + https://github.com/opencybersecurityalliance/PACE/blob/main/docs/UseCases/collect_sbom_from_url.md
    + https://github.com/opencybersecurityalliance/PACE/blob/main/docs/UseCases/collect_sbom_with_command.md
- PACE evaluate SBOM/VEX/NCD use cases
    +
- Using PACE posture results in other use cases
    + https://github.com/opencybersecurityalliance/PACE/blob/main/docs/UseCases/ips-pcs-pes-usecase.md
    + https://github.com/opencybersecurityalliance/PACE/blob/main/docs/UseCases/stix-pcs-pes-usecase.md
    + the 3 use cases in https://github.com/sparrell/PACE/blob/main/docs/UseCases/Pace_Sbom_Vex_Flags_Prioritization/README.md#not_affected-flags - note "flags" are now "status_justification" in SBOM docs so PACE page needs updating for correct terminology
- CSAF/VEX use cases
   + http://www.cybersecurityautomationworkshop.org/SweatEquity/BSI/
- Interop pics
   + https://github.com/oasis-tcs/openc2-usecases/blob/main/PlugFests/2021.06.22-BC-SBOM-PoC/ParticipantInfo/sFractal/workPlan.1.md

# Return to Home
[return to Home](../index.md)
