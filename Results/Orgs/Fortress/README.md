# Fortress Results

## What Contributed
recap sweat equity here, can ref to sweat page

[Fortress Information Security](https://www.fortressinfosec.com/) was able to demo a few capabilities of our [PACE system](https://github.com/opencybersecurityalliance/PACE), using our [File Integrity Assurance (FIA)](https://www.fortressinfosec.com/file-integrity-assurance) tool, including:

1. [Collect SBOM with Command](https://github.com/opencybersecurityalliance/PACE/blob/main/docs/UseCases/collect_sbom_with_command.md) using FIA as a Posture Collection Service (PCS) to use an API to upload an SBOM
2. [Retrieve SBOMs](https://github.com/opencybersecurityalliance/PACE/blob/main/docs/UseCases/retrieve_sbom.md) using FIA as a Posture Attribute Repository (PAR) to retrieve an uploaded SBOM, then
3. Evaluate the SBOM's data using FIA as a Posture Evaluation Service (PES) and initiate an SBOM Analysis job, and retrieve an Analysis Report

    - We also demonstrated the functionality and output of a Fortress SBOM Analysis Report.

In addition, we learned about how other workshop attendees are using OpenC2 and STIX/TAXII feeds to facilitate sharing of threat information. On the fly, we wrote a custom integration to:
1. Upload an SBOM to a STIX/TAXII Feed (Likely an industry first)
2. Initiate a Fortress SBOM Analysis job when a new SBOM is detected
3. Publish the Analysis Report to the STIX/TAXII Feed
4. And finally, we demonstrated the SBOM Blockchain solution to share upload and share SBOM and other software supply supply chain attestations. Other attendees complimented the appearance and functionality of the blockchain system.  

## Use Cases
**Anchore**
- Anchore demonstrated Syft, their tool to build SBOMs from containers and repositories
- Their license appears to allow for commercial reuse, so I think we should explore using Syft if/when we can.

**IBM** 
- The engineers at IBM were very interested in how we published an SBOM and subsequent Analysis Report as a STIX object. We discussed the method, and agreed that a dedicated STIX Domain Object for SBOM would be nice.  
- They also demonstrated 'STIX-shifter', a library allowing software to connect to products that house data repositories by using STIX Patterning, and return results as STIX Observations.
- They demonstrated 'Kestrel', a threat hunting language used to make cyber threat hunting faster and more effective, to build reusable, composable, and shareable hunt-flows.

## Take aways
We need to understand and actively support integrations with existing and emerging standards, including OpenC2, PACE, CSAF, and STIX/TAXII.
- OpenC2 is a standardized, vendor-neutral language for the command and control of technologies that provide or support cyber defenses. The use of standardized interfaces and protocols enables interoperability of different tools. By supporting OpenC2, Fortress can build native integrations for our entire suite of offerings and capabilities, allowing clients to automatically pull in our data when needed. 
- Posture Attribute Collection and Evaluation (PACE) is a process which consists of understanding and connecting the data between a system's software load, composition of that software load, patch levels, vulnerability, and configuration state. While the project is still in the early stages, PACE will likely be used to help assist AVM-style visibility.  
- Common Security Advisory Framework (CSAF) is the definitive reference for the language which supports creation, update, and interoperable exchange of security advisories as structured information on products, vulnerabilities and the status of impact and remediation among interested parties. Fortress should consider supporting CSAF, beyond just VEX, as a core component for our solutions using vulnerabilities and products. Specifically, we can publish our FIA results in CSAF format, among many other use cases.
- Structured Threat Information Expression (STIX) is a language used to exchange cyber threat intelligence (CTI). It's been around for a while, but with the maturation of SBOM, it has become clear that the information SBOMs provide is crucial to CTI processes. We propose that the STIX standards should support SBOMs as a new, independent STIX Domain Object (SDO).
- Integrating Fortress solutions with corporate cybersecurity tools and protocols will further drive customer use-cases, allowing more customer buy in across different BUs. It also allows their security teams to access new sources of data, especially IR, Threat Hunters, and post-incident personnel.

# Jump to
## Return to Contributing Companies/Agencies/Universities
[return to Contributing Companies/Agencies/Universities](../../Orgs)

## Return to Results
[return to Results](../../../Results)

## Return to Agenda
[return to Agenda](../../../Agenda)

## Return to Home
[return to Home](../../../index.md)