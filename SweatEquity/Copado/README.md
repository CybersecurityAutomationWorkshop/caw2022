# Copado Sweat Equity

VSM has multiple uses within an organization. They can happen as individual lines of effort or they can occur in concert to provide maximum impact. This choice will depend on an organization's business goals. 

The sample use cases are:

 - Auditability of VSM feeds into security operations (SOC UC)
 - Output of signatures into SBOM build out (SBOM UC)
 - Management layer allowing for aggregation, enrichment, analysis, and action (Methodology UC)


1. SOC UC

Given the current state of the cybersecurity industry, it is becoming increasingly apparent that one ‘system of record’ in an enterprise is not sufficient, especially for post-incident analysis and forensics. A well implemented value stream mapping will bring together disparate information from across verticals in an enterprise to create a lattice of assurance that will make it less likely that an adversary can tamper with data to hide their tracks. This will create an environment of auditability that leads to enhanced forensics capabilities. In more advanced applications, value stream mapping could have an impact on areas such as enhanced behavioral detection and automated response.

This use case will focus on gathering data and analysis. Important considerations for each steep step are outlined below.

Gathering & Collecting Data

All types of data should be collected, and where possible, using existing systems and
infrastructure. Having multiple ‘systems of record’ allows for greater forensic auditability. Leveraging multiple components of  existing infrastructure -- as opposed to centralizing all data collection -- has many benefits. The added resiliency of distributed data sources and the increased fidelity and breadth of information collected will enhance the overall situational awareness.

Events could be one or multiple observables and include: logging systems or log output from specific systems, access control systems events, debugging logs, system and server monitoring tools, intrusion detection and prevention events, software bill of materials analysis, and CI/CD pipeline events. Other relevant data can be collected by incorporating event gathering at every stage of the system development life cycle.

VSM focuses on human interaction in the software development process. It seeks to understand and capture the context of the build systems, underlying code, and the design and stories representing the initial software itself.

Leveraging existing systems that already collects events across specific domains, such as a production logging server, or a physical security system tracking ingress and egress from an office, and interfacing those systems in such a way that events can be correlated provides a powerful tool for improving and maintaining systems.

Individual events should be time-stamped and digitally signed. This allows the source of the event to be identified and the time the event occured to be recorded, and the entire event to be tamper-resistant. Any change to the contents of the event will invalidate the cryptographic signature or hash. Ultimately, these events could be stored in an immutable ledger. This provides an easy mechanism to audit various aspects of a process, procedure, or system as every event is recorded.

The process of identifying and collecting observables at various stages of the SDLC goes a long way towards helping to improve the security posture of an organization. In addition to providing robust post-incident forensic capabilities, areas that need attention can be identified and addressed. This creates a feedback loop that makes both defense and post-incident analysis more effective.

Analysis

Knowing context and the operating parameters of a system can allow for great insight into its operation. Everything from overall system performance, to predictive models for identifying when a fault is imminent, can be discovered through data analysis when given enough inputs of relevance. The result of the analysis is assurance and auditability. Organizations will have the ability to validate what occurred, and when, provides the ability to easily audit a system. An immutable ledger allows events to be stored in such a way that each corresponding event is cryptographically tied to all the events that occured before it. Changing any event invalidates all subsequent events in the chain. This, combined with cryptographically signed events, is a very
powerful mechanism for tracking system state both in realtime and historically.



2. SBOM UC

The forensic capabilities created with implementing VSM could leverage the Software Bill of Materials (SBOM) and other software supply chain requirements. Using the SBOM as a distributed ledger record of the originating VSM from the organization can give 3rd parties greater trust in the organization software build process. 

SBOM will illuminate and track component parts of software. By integrating the output hash of VSM into the SBOM standard as a record of the chain of evidence of software development creates an immutable record of the entire process which can later be forensically examined. If the record on file does not match the cryptographically verified record from the software developer/creator, evidence of a problem exists that can be more closely examined for attribution and potential impact. Copado acknowledges that further development and research is required to create an industry-standard way of signing data to be certain of its provenance but early signs show promise in this area.



3. Methodology UC

Value stream mapping at its root is a management and quality methodology built out of the lean manufacturing methodology originated by Deming  to assist an organization creating more consistent and better output of its manufacturing processes. Modern software development tools and data systems will be the input to value stream management which is the overall framework for executing the strategy uncovered in the mapping process. When done correctly, this process identifies and remediates inefficiencies, delays, and bottlenecks to transform an organization’s business practices. This practice is cross-functional and pulls in many parts of an organization to combine areas where responsibility, authority, budget, and more all come together. Value stream mapping is being adopted at an increasingly greater rate by organizations as it has positive impacts on business functions and finances. Gartner estimated that by 2023, 70% of all organizations will use Value Stream Management. Copado’s approach to layer in cybersecurity applicability will expand on the positive impacts.

Value stream mapping tools gather event data from each segment and process in the SDLC. The more accurate and specific the event data, the better the tool will be able to help organizations calculate value and identify blockers in their development process.

A well executed value stream mapping program in software can increase transparency, establish the identity of an information source, and provide for robust forensic analysis. Value stream management concepts focus holistically on the business, bringing in stakeholders across verticals into the security process. As demonstrated by the graphic below, several components across an enterprise can be pulled into a value stream mapping program to maximize impact. Currently, the software development and delivery process is greatly diffused and involves multiple languages, tools, and teams. This creates delays and potentially inhibits the identity of information sources. Value stream management creates connections between all events in a given environment. It maps the linear movements between data, manual processes and handoffs, and operational aspects of a system to provide a deeper understanding of that environment.

## Return to Home
[return to Home](../../index.md)
