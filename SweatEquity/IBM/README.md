# IBM Sweat Equity

## Projects Description

### stix-shifter (OCA)
STIX-shifter is an open-source python library that queries security products and data stores using STIX patterning and presents the results as STIX cyber observable objects.  The project contains several connectors such as Splunk, QRadar, and Crowdstrike Falcon. 

STIX-shifter uses connectors as follows:
STIX patterns are translated into the target data source's native query language.
Translated queries are sent via the target data source's APIs.
Search results are fetched via the target data source's APIs.
The fetched results are translated into STIX observed-data SDOs.

It allows for federated search against supported data sources: One STIX pattern can query multiple security products and return the results in a unified STIX format. The STIX objects can then be ingested by other projects (ie. Kestrel).

### Kestrel (OCA)
[Kestrel](https://github.com/opencybersecurityalliance/kestrel-lang) is a threat hunting language aiming to make cyber threat hunting _fast_ by providing a layer of abstraction to build reusable, composable, and shareable hunt-flow.

Kestrel key concepts: [entity-based reasoning](https://kestrel.readthedocs.io/en/latest/language.html#entity-based-reasoning) and [composable hunt-flow](https://kestrel.readthedocs.io/en/latest/language.html#composable-hunt-flow)

You can try Kestrel in a [cloud sandbox](https://mybinder.org/v2/gh/opencybersecurityalliance/kestrel-huntbook/HEAD?filepath=tutorial)

Download and share your Kestrel huntbook in the [kestrel-huntbook](https://github.com/opencybersecurityalliance/kestrel-huntbook) repo.

Download and share your Kestrel analytics in the [kestrel-analytics](https://github.com/opencybersecurityalliance/kestrel-analytics) repo.

Join OCA slack workspace to discuss Kestrel and your hunt
OCA workspace: https://open-cybersecurity.slack.com/
Invitation: https://docs.google.com/forms/d/1vEAqg9SKBF3UMtmbJJ9qqLarrXN5zeVG3_obedA3DKs/viewform?edit_requested=true

### OpenC2
We have implemented two actuators as part of DARPA's Cyber Hunting at Scale (CHASE) project along with their Actuator profiles
Kestrel Actuator:  Allows Kestrel huntbooks to be executed through OpenC2 investigate command. Results of the hunt are returned as part of OpenC2 response messages.
Ansible Actuator:  Connects Ansible playbooks to OpenC2 actions/targets. The actuator maps action and target pairs to available Ansible playbooks. We will also discuss the creation of new custom OpenC2 Container target that we needed to implement for our use case. 

## Use Case
The use case will be shown from shallow to deep in a 3-step procedure:

Danny will show how to use the STIX-shifter command-line utility to do federated search, and explain how connectors are used to search against data sources using STIX patterning.

Then Xiaokui will show how to use federated search (stix-shifter) in cyber threat hunting across multiple data sources. The hunt is written and executed as a Kestrel hunt book for reuse and sharing.

An APT in a hybrid cloud: an attacker penetrates into an enterprise network through a phishing email. After probing the privileges of the victim, the attacker injects vulnerabilities into the source code of a product of the company. The attack propagates from the enterprise's network to its cloud where the product is deployed. During the execution of the product, the attacker is able to exploit the service due to the implanted vulnerability, and access confidential data at another cloud from the service. Finally, the attacker exfiltrates the confidential data out through a stealthy Twitter channel.

Xiaokui will demo how to start hunt with TTP pattern matching, which directly tackles the top of the Pyramid of Pain. Also will be shown are intro- and inter-host provenance tracking, vulnerable dependency discovery, TI enrichment, and visualization analytic hunt steps.

Xiaokui will explain how to write a Kestrel analytics to retrieve SBOM for a piece of software, and how to implement the vulnerable dependency discovery analytic step shown in the demo.

Next Mike will build on Xiaokui's demonstration by automating the response procedure using OpenC2. Kestrel will be invoked as part of an investigation step via the OpenC2 Kestrel actuator, automatically executing the huntbook Xiaokui showed when an exploited process is alerted. Results from the investigation will augment the decision making process in which the outcome may be to perform a mitigation response via the OpenC2 Ansible actuator.


## Return to Sweat Equity
[return to Sweat Equity](../../SweatEquity)

## Return to Agenda
[return to Agenda](../../Agenda)

## Return to Home
[return to Home](../../index.md)
