# German Federal Office for Information Security (BSI) Sweat Equity

## Tools

Several Open Source Tools have been made available on GitHub to ease the use of CSAF. Please find a list below:

### Secvisogram

[Secvisogram](https://github.com/secvisogram/secvisogram/) is an [online editor](https://secvisogram.github.io) for creating CSAF documents. It can also check whether a given CSAF document is valid and display a human-readable preview. It is written in JavaScript and therefore client-based. You can run your own version of it and modify the [HTML template for the preview](https://github.com/secvisogram/secvisogram/blob/main/PREVIEW-TEMPLATING.md) to your needs. [Source Code](https://github.com/secvisogram/secvisogram/) is available under MIT.

### CSAF Distribution

The repo [CSAF Distribution](https://github.com/csaf-poc/csaf_distribution) contains several tools around the distribution, discovery and retrieval of CSAF documents. It contributes to the understanding of [Section 7](https://docs.oasis-open.org/csaf/csaf/v2.0/csaf-v2.0.html#7-distributing-csaf-documents) in the CSAF standard. Even though it is officially still "work in progress" it can already be used. Guidance on the build, setup and usage of the Go applications is provided in the repo. [Source Code](https://github.com/csaf-poc/csaf_distribution) is available under MIT.

#### [CSAF Provider(https://github.com/csaf-poc/csaf_distribution#csaf_provider)

is an implementation of the role [CSAF trusted provider](https://docs.oasis-open.org/csaf/csaf/v2.0/csaf-v2.0.html#723-role-csaf-trusted-provider), also offering a simple HTTPS based management service. It is more or less a static site generator.

#### [CSAF Uploader(https://github.com/csaf-poc/csaf_distribution#csaf_uploader)

is a command line tool that uploads CSAF documents to the [csaf_provider](#csaf_provider).

#### [CSAF Aggregator(https://github.com/csaf-poc/csaf_distribution#csaf_aggregator)

is an implementation of the role [CSAF Aggregator](https://docs.oasis-open.org/csaf/csaf/v2.0/csaf-v2.0.html#725-role-csaf-aggregator).

#### [CSAF Checker(https://github.com/csaf-poc/csaf_distribution#csaf_checker)

is a tool for testing a [CSAF trusted provider](https://docs.oasis-open.org/csaf/csaf/v2.0/csaf-v2.0.html#723-role-csaf-trusted-provider) according to [Section 7 of the CSAF standard](https://docs.oasis-open.org/csaf/csaf/v2.0/csaf-v2.0.html#7-distributing-csaf-documents).

### CSAF validator library

[csaf-validator-lib](https://github.com/secvisogram/csaf-validator-lib) is Node.js implementation of a [CSAF full validator](https://docs.oasis-open.org/csaf/csaf/v2.0/csaf-v2.0.html#9116-conformance-clause-16-csaf-full-validator) and therefore validates whether a given CSAF document is valid and passes all tests. As it is currently still work in progress only the functionality of a [CSAF basic validator](https://docs.oasis-open.org/csaf/csaf/v2.0/csaf-v2.0.html#9114-conformance-clause-14-csaf-basic-validator) is completely implemented. Nevertheless, other tests have been added or are in the process of being added. [Source Code](https://github.com/secvisogram/csaf-validator-lib) is available under MIT.

### CSAF validator service

[CSAF Validator Service](https://github.com/secvisogram/csaf-validator-service) is a service to validate documents against the [CSAF standard](https://docs.oasis-open.org/csaf/csaf/v2.0/csaf-v2.0.html). It uses the [csaf-validator-lib](#csaf-validator-library) under the hood which is included as a `git subtree` module. [Source Code](https://github.com/secvisogram/csaf-validator-service) is available under MIT.

### CSAF CMS backend (aka Secvisogram Backend)

[CSAF CMS Backend] is a backend providing part of the [CSAF content management system](https://docs.oasis-open.org/csaf/csaf/v2.0/csaf-v2.0.html#916-conformance-clause-6-csaf-content-management-system) support to authors of CSAF documents. It is still work in progress. An integration with [Secvisogram](#secvisogram) is planned but it can also be used with other frontend systems as it is completely REST-based. See the [documentation](https://github.com/secvisogram/csaf-cms-backend/blob/main/documents/architecture-decisions.md) for more details. [Source Code](https://github.com/secvisogram/csaf-cms-backend) is available under MIT.

## Files

### Security Advisories

A list of real security advisories written in CSAF is available at the [OASIS TC repository](https://github.com/oasis-tcs/csaf/tree/master/csaf_2.0/examples/csaf). This also includes one from BSI.

### VEX

A list of generic VEX documents written in CSAF is available at the [OASIS TC repository](https://github.com/oasis-tcs/csaf/tree/master/csaf_2.0/examples/csaf/csaf_vex). [One for Secvisogram](https://github.com/oasis-tcs/csaf/tree/master/csaf_2.0/examples/csaf/csaf_vex/sec-vex-2022-0001.json) is available in the repo as well.

## Return to Sweat Equity
[return to Sweat Equity](../../SweatEquity)

## Return to Agenda
[return to Agenda](../../Agenda)

## Return to Home
[return to Home](../../index.md)
