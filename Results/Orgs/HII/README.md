# HII Results

## What Contributed

HII enumerated our plans for the CAW on our [Sweat Equity page](../../../SweatEquity/HII/README.md).

At the CAW, HII presented a [Posture Attribute Collection and
Evaluation
(PACE)](https://github.com/opencybersecurityalliance/PACE) over
OpenC2 framework that served as the cornerstone of the PACE
interworking discussions at the event. Having the
[OIF-Orchestrator](https://github.com/oasis-open/openc2-oif-orchestrator)
serve as a bridge between threat hunting/decision maker
components such as
[Kestrel](https://github.com/opencybersecurityalliance/kestrel-lang)
and endpoint utilities such as [Fortress File Integrity Assurance
(FIA)](../../../SweatEquity/Fortress/README.md), [Anchore Syft &
Grype](../../../SweatEquity/Anchore/README.md), or our own
[Yuuki](https://github.com/oasis-open/openc2-yuuki) actuators
allowed us to better hear presentations of other attendees in
terms of their tools’ ability to directly interface with the PACE
framework and HII's implementation of it. While much of our role
in the proposed interworking was as the intermediary, having a
functional end-to-end PACE solution allowed us to demonstrate the
viability of the OIF-Orchestrator as an intermediate Posture
Colleciton Service (PCS) directly. This enabled more discussions
to credibly use a “hand-waving lycan”, since OIF could be shown
to interoperate with other technologies.

Additionally, we provided access to the HII Blinky-Board to
visually demonstrate OpenC2 commands and facilitate simple
interworking with an OpenC2 device.

## Use Cases

HII's PAC over OpenC2 demonstration is both a collection of tools
as well as an implementation of a PACE use case. The primary
focus of HII's protoptying efforts was the PACE ["Collect SBOM
From
Device"](https://github.com/opencybersecurityalliance/PACE/blob/main/docs/UseCases/collect_sbom_from_device.md)
use case, shown here:

![PACE-SBOM-From-Device](https://raw.githubusercontent.com/opencybersecurityalliance/PACE/main/docs/UseCases/Images/CollectSbomFromDevice.png)

HII's prototype implementation of this use case is illustrated
below; our design utilizes HII's OIF-Orchestrator and Yuuki
components that enable rapid prototyping of OpenC2 exchanges,
with enhancements made to the OIF-Orchestrator to enable it to
serve as an OpenC2 Consumer / Producer.

![HII PACE
Prototype](./images/Orchestrator-Consumer-at-CAW.drawio.png)

We also extended the use case to retrieve device operating system
version information, using the [osquery](https://osquery.io/)
open source tool and an HII-developed custom OpenC2 actuator
profile for database interactions to access osquery's table-based
interface.

With these components, we demonstrated two specific use cases and
laid the ground work for two others.

 - [ ✓ ] [Collect SBOM From
   Device](https://github.com/opencybersecurityalliance/PACE/blob/main/docs/UseCases/collect_sbom_from_device.md)
 - [ x ] [Collect SBOM from
   URL](https://github.com/opencybersecurityalliance/PACE/blob/main/docs/UseCases/collect_sbom_from_url.md)
 - [ x ] Store externally provided SBOM (i.e., [Collect SBOM with
   Command](https://github.com/opencybersecurityalliance/PACE/blob/main/docs/UseCases/collect_sbom_with_command.md))
 - [ ✓ ] Collect OS version from Device



## Take aways

We conducted a successful demonstration of use the [OpenC2
language](https://openc2.org) to implement Posture Attribute
Collection (PAC) as a stepping stone to a more complete PACE
implementation.

HII is excited for the opportunity to work as part of a large
framework of tools to demonstrate OpenC2’s value as an open
standard to combat cyber threats. Having seen continued interest
in the integration of OpenC2 and the OIF into a variety of other
technologies and frameworks presented at the CAW, we are excited
to continue our efforts to develop open standards for
cybersecurity automation through both OpenC2 and PACE. We look
forward to further chances to work and talk with many CAW
participants. 

Further interoperability can aid our development of OpenC2
Actuator Profiles that better support common cybersecurity
Actions and Targets, as well as interfacing our technologies such
as the OIF-Orchestrator with both upstream tools such as Kestrel
and downstream tools such as SYFT/GRYPE. We have identified a
number of organizations that we hope to work going forward to
demonstrate such interoperability.

Following an inquiry in the breakout session on threat-hunting,
it was determined that OpenC2 could be integrated with Kestrel
and there was outside interest in this. Similarly, OpenC2’s
position as an OASIS standard allows it to be integrated with
[CACAO](http://oasis-open.org/committees/tc_home.php?wg_abbrev=cacao)
playbooks.

HII looks forward to future opportunities to demonstrate OpenC2
interoperability on a larger scale.

# Jump to
## Return to Contributing Companies/Agencies/Universities
[return to Contributing Companies/Agencies/Universities](../../Orgs)

## Return to Results
[return to Results](../../../Results)

## Return to Agenda
[return to Agenda](../../../Agenda)

## Return to Home
[return to Home](../../../index.md)
