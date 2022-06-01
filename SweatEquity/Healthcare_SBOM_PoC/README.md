# Healthcare SBOM PoC Sweat Equity

The Healthcare SBOM PoC consists of Health Delivery Organizations (HDOs),
Medical Device Manufacturers (MDMs), government officials
from several countries, and interested security professionals.
A proof of concept (PoC) has been running for several years.
Phase 1 proved the value of providing SBOMs.
Phase 2 expanded the number of participants
(8 HDO’s consuming SBOMs from 7 MDM’s)
and began exploring VEXs as well.
Phase 3 is just beginning.

The sweat equity that is being provided includes example
SBOMs, VEXs, Use Cases and even a How-to Guide.
Diagrams show how the PoC follows the general “PACE” workflow.
Unfortunately due to the conditions of the PoC NDA,
actual systems and artifacts can not be demonstrated –
just discussed in general terms.

Representing the Healthcare SBOM PoC will be Ed Heierman of Abbott,
Ed created the sweat equity material, but it represents the work of many
contributors.

## How-To Guide
The Healthcare PoC created a How-To Guide for SBOM Generation that contains [SBOM Examples.](https://www.ntia.gov/files/ntia/publications/howto_guide_for_sbom_generation_v1.pdf)

Topics include:
1. Collecting SBOM Content
2. Generation Guidance
- Software Identity
- Unique Identifier
- SBOM Completeness
- SBOM Document Identity
- SBOM Content for Included Components
3. SPDX Format
4. SWID Format
5. System of Systems Example

## SBOM Flow
The PACE flow for SBOM generation
![image](https://user-images.githubusercontent.com/106685105/171497964-8785cfd8-84f7-4616-87fc-4dae747c2115.png)

## VEX Use Cases
The Healthcare PoC identified the following use cases for VEX:
1. Vulnerability in a Component That is Not Included in the Medical Device
- The vulnerability status is “Not Affected”
2. Vulnerability in a Component that Does Not Impact the Medical 
- The vulnerability status is “Not Affected”
3. Vulnerability in a Component that Does Impact the Medical Device
- The vulnerability status is “Affected”
4. The Vulnerability in a Component is Under Investigation
- The vulnerability status is “Unknown”
5. Medical Device Pre-procurement
- The HDO evaluates the VEX content prior to purchasing the medical device.
  
## VEX Content
The Healthcare POC identified the following VEX Content.
### VEX Document Identity
### Product Details
- Primary Component from SBOM
- Software Identity of the Primary Component
   + Supplier Name
   + Component Name
   + Version String
   + Unique Identity (from Supplier)
### Vulnerability Detail
- Included Component from SBOM
-	Software Identity of the Included Component
   + Supplier Name
   + Component Name
   + Version String
   + Unique Identity (from Supplier)
-	Included Component Unique Identifier (CPE)
-	Identifier of the Vulnerability (CVE)
   + CVSS Risk Score
### Vulnerability Statement
-	Vulnerability Status
   + Impact coded value (Not Affected, Affected, Fixed, Under Investigation)
   + Impact statement
   + Textual description (Port disabled, etc.)
-	Resulting Risk Score
   + CVSS 3.0 Rubric for Medical Devices
-	Consumer Action
   + Textual description
   + Statements such as:Patch now, Patch later, Remove from the network, etc.

## SBOM Example
##Document Header
SPDXVersion: SPDX-2.2
DataLicense: CC0-1.0
SPDXID: SPDXRef-DOCUMENT
DocumentName:  ACME-INFUSION-1.0-SBOM-DRAFTv2021-06-07T165013
DocumentNamespace:  http://www.hospitalproducts.acme
Creator: Organization:  ACME-Hospital-Division()
Created: 2021-07-31T16:50:13Z
CreatorComment:  <text>Draft SCME INFUSION PoC II SBOM document in SPDX format. Unofficial content for demonstration purposes only.</text>



##Packages

PackageName: INFUSION
SPDXID: SPDXRef-INFUSION-1.0
ExternalRef: PACKAGE-MANAGER purl pkg:supplier/ACME/INFUSION@1.0
PackageVersion: 1.0
PackageSupplier: Organization: ACME
Relationship: SPDXRef-DOCUMENT DESCRIBES SPDXRef-INFUSION-1.0
Relationship: SPDXRef-INFUSION-1.0 CONTAINS NOASSERTION
PackageDownloadLocation: NOASSERTION
FilesAnalyzed: false
PackageLicenseConcluded: NOASSERTION
PackageLicenseDeclared: NOASSERTION
PackageCopyrightText: NOASSERTION




PackageName: Windows Embedded Standard 7
SPDXID: SPDXRef-Windows-Embedded-Standard-7-6.1.7601
ExternalRef: PACKAGE-MANAGER purl pkg:supplier/Microsoft/Windows-Embedded-Standard-7@6.1.7601
PackageVersion: 6.1.7601
PackageSupplier: Organization: Microsoft
Relationship: SPDXRef-INFUSION-1.0 CONTAINS SPDXRef-Windows-Embedded-Standard-7-6.1.7601
Relationship: SPDXRef-Windows-Embedded-Standard-7-6.1.7601 CONTAINS NOASSERTION
PackageDownloadLocation: NOASSERTION
FilesAnalyzed: false
PackageLicenseConcluded: NOASSERTION
PackageLicenseDeclared: NOASSERTION
PackageCopyrightText: NOASSERTION




PackageName: Windows Embedded Standard 7 with SP1 patches
SPDXID: SPDXRef-Windows-Embedded-Standard-7-with-SP1-patches-3.0
ExternalRef: PACKAGE-MANAGER purl pkg:supplier/Microsoft/Windows-Embedded-Standard-7-with-SP1-patches@3.0
ExternalRef: SECURITY cpe23Type cpe:2.3:o:microsoft:windows_7:-:sp1:*:*:*:*:*:*
PackageVersion: 3.0
PackageSupplier: Organization: Microsoft
Relationship: SPDXRef-INFUSION-1.0 CONTAINS SPDXRef-Windows-Embedded-Standard-7-with-SP1-patches-3.0
Relationship: SPDXRef-Windows-Embedded-Standard-7-with-SP1-patches-3.0 CONTAINS NONE
PackageChecksum: SHA1: d6a770ba38583ed4bb4525bd96e50461655d2759
PackageDownloadLocation: NOASSERTION
FilesAnalyzed: false
PackageLicenseConcluded: NOASSERTION
PackageLicenseDeclared: NOASSERTION
PackageCopyrightText: NOASSERTION
ExternalDocumentRef: DocumentRef-Win-Embd-7SP1-SBOM http://www.hospitalproducts.acme/ACME-IVD-Analyzer-1.5-SBOM-v20201007  SHA1: d6a770ba38583ed4bb4525bd96e50461655d2759
Relationship:  SPDXRef-Windows-Embedded-Standard-7-with-SP1-patches-3.0 CONTAINS DocumentRef-Win-Embd-7SP1-SBOM:SPDXRef-Windows-Embedded-Standard-7-with-SP1-patches-3.0




PackageName: SQL 2005 Express
SPDXID: SPDXRef-SQL-2005-Express-9.00.5000.00SP4
ExternalRef: PACKAGE-MANAGER purl pkg:supplier/Microsoft/SQL-2005-Express@9.00.5000.00SP4
PackageVersion: 9.00.5000.00SP4
PackageSupplier: Organization: Microsoft
Relationship: SPDXRef-INFUSION-1.0 CONTAINS SPDXRef-SQL-2005-Express-9.00.5000.00SP4
Relationship: SPDXRef-SQL-2005-Express-9.00.5000.00SP4 CONTAINS NOASSERTION
PackageDownloadLocation: NOASSERTION
FilesAnalyzed: false
PackageLicenseConcluded: NOASSERTION
PackageLicenseDeclared: NOASSERTION
PackageCopyrightText: NOASSERTION




PackageName: .Net Frame Work
SPDXID: SPDXRef-.Net-Frame-Work-V2.1.21022.8SP2
ExternalRef: PACKAGE-MANAGER purl pkg:supplier/Microsoft/.Net-Frame-Work@V2.1.21022.8SP2
PackageVersion: V2.1.21022.8SP2
PackageSupplier: Organization: Microsoft
Relationship: SPDXRef-INFUSION-1.0 CONTAINS SPDXRef-.Net-Frame-Work-V2.1.21022.8SP2
Relationship: SPDXRef-.Net-Frame-Work-V2.1.21022.8SP2 CONTAINS NOASSERTION
PackageDownloadLocation: NOASSERTION
FilesAnalyzed: false
PackageLicenseConcluded: NOASSERTION
PackageLicenseDeclared: NOASSERTION
PackageCopyrightText: NOASSERTION




PackageName: Bobs Browser
SPDXID: SPDXRef-Bobs-Browser-1
ExternalRef: PACKAGE-MANAGER purl pkg:supplier/Bob/Bobs-Browser@1
PackageVersion: 1
PackageSupplier: Organization: Bob
Relationship: SPDXRef-INFUSION-1.0 CONTAINS SPDXRef-Bobs-Browser-1
Relationship: SPDXRef-Bobs-Browser-1 CONTAINS NONE
PackageChecksum: SHA1: d6a770ba38583ed4bb4525bd96e50461655d2759
PackageDownloadLocation: NOASSERTION
FilesAnalyzed: false
PackageLicenseConcluded: NOASSERTION
PackageLicenseDeclared: NOASSERTION
PackageCopyrightText: NOASSERTION

## VEX Example
{
  "document": {
    "csaf_version": "2.0",
    "publisher": {
      "category": "user",
      "name": "ACME-Hospital-Division",
      "contact_details": "Fred Flinstone, fredflinstone@acme.com",
      "namespace": "http://www.hospitalproducts.acme"
    },
    "title": "ACME-INFUSION-1.0-VEX-DRAFT Use Case complete",
    "tracking": {
      "current_release_date": "2021-04-27T18:01:00.000Z",
      "id": "ACME_INFUSION_1_0_VEX_1_0_0",
      "initial_release_date": "2021-04-27T18:01:00.000Z",
      "revision_history": [
        {
          "date": "2021-04-27T18:01:00.000Z",
          "number": "1.0.0",
          "summary": "Initial version. Unofficial content for demonstration purposes only."
        }
      ],
      "status": "draft",
      "version": "1.0.0-beta",
      "generator": {
        "engine": {
          "name": "Secvisogram",
          "version": "1.9.0"
        },
        "date": "2021-12-13T16:25:51.786Z"
      }
    },
    "category": "vex",
    "notes": [
      {
        "category": "other",
        "text": "Draft ACME INFUSION PoC II VEX document. Unofficial content for demonstration purposes only.",
        "title": "Author Comment"
      }
    ]
  },
  "product_tree": {
    "branches": [
      {
        "name": "ACME",
        "category": "vendor",
        "branches": [
          {
            "name": "INFUSION",
            "category": "product_name",
            "branches": [
              {
                "name": "1.0",
                "category": "product_version",
                "product": {
                  "product_id": "SPDXRef-INFUSION-1.0",
                  "name": "ACME INFUSION 1.0",
                  "product_identification_helper": {
                    "purl": "pkg:supplier/ACME/INFUSION@1.0"
                  }
                }
              }
            ]
          }
        ]
      },
      {
        "name": "Microsoft",
        "category": "vendor",
        "branches": [
          {
            "name": "Windows",
            "category": "product_family",
            "branches": [
              {
                "name": "Embedded Standard 7",
                "category": "product_name",
                "branches": [
                  {
                    "name": "1",
                    "category": "service_pack",
                    "product": {
                      "product_id": "SPDXRef-Windows-Embedded-Standard-7-with-SP1-patches-3.0",
                      "name": "Microsoft Windows Embedded Standard 7 SP1",
                      "product_identification_helper": {
                        "purl": "pkg:supplier/Microsoft/Windows-Embedded-Standard-7-with-SP1-patches@3.0",
                        "cpe": "cpe:2.3:o:microsoft:windows_7:sp1:*:*:*:*:*:*:*"
                      }
                    }
                  }
                ]
              }
            ]
          }
        ]
      },
      {
        "name": "Bob",
        "category": "vendor",
        "branches": [
          {
            "name": "Bobs Browser",
            "category": "product_name",
            "branches": [
              {
                "name": "v12.1",
                "category": "product_version",
                "product": {
                  "product_id": "SPDXRef-Bobs-Browser-1",
                  "name": "Bob Bobs Browser v12.1",
                  "product_identification_helper": {
                    "cpe": "cpe:/a:Bob:BobsBrowser:v12.1",
                    "purl": "pkg:supplier/Bob/Bobs-Browser@12.1"
                  }
                }
              }
            ]
          }
        ]
      },
      {
        "name": "Apache",
        "category": "vendor",
        "branches": [
          {
            "name": "Log4j",
            "category": "product_name",
            "branches": [
              {
                "name": "2.0",
                "category": "product_version",
                "product": {
                  "product_id": "CSAFPID-0004",
                  "name": "Apache Log4j 2.0",
                  "product_identification_helper": {
                    "cpe": "cpe:2.3:a:apache:log4j:2.0:-:*:*:*:*:*:*",
                    "purl": "pkg:supplier/apache/log4j@2.0"
                  }
                }
              }
            ]
          }
        ]
      }
    ]
  },
  "vulnerabilities": [
    {
      "cve": "CVE-2017-0144",
      "scores": [
        {
          "products": [
            "SPDXRef-Windows-Embedded-Standard-7-with-SP1-patches-3.0"
          ],
          "cvss_v3": {
            "version": "3.0",
            "vectorString": "CVSS:3.0/AV:N/AC:H/PR:N/UI:N/S:U/C:H/I:H/A:H",
            "baseScore": 8.1,
            "baseSeverity": "HIGH",
            "attackVector": "NETWORK",
            "attackComplexity": "HIGH",
            "privilegesRequired": "NONE",
            "userInteraction": "NONE",
            "scope": "UNCHANGED",
            "confidentialityImpact": "HIGH",
            "integrityImpact": "HIGH",
            "availabilityImpact": "HIGH"
          }
        },
        {
          "products": [
            "SPDXRef-INFUSION-1.0"
          ],
          "cvss_v3": {
            "version": "3.0",
            "vectorString": "CVSS:3.0/AV:N/AC:H/PR:N/UI:N/S:U/C:H/I:H/A:H/MAV:P/MAC:H/MPR:H/MUI:N/MS:U/MC:N/MI:N/MA:H",
            "baseScore": 8.1,
            "baseSeverity": "HIGH",
            "attackVector": "NETWORK",
            "attackComplexity": "HIGH",
            "privilegesRequired": "NONE",
            "userInteraction": "NONE",
            "scope": "UNCHANGED",
            "confidentialityImpact": "HIGH",
            "integrityImpact": "HIGH",
            "availabilityImpact": "HIGH",
            "modifiedAttackVector": "PHYSICAL",
            "modifiedAttackComplexity": "HIGH",
            "modifiedPrivilegesRequired": "HIGH",
            "modifiedUserInteraction": "NONE",
            "modifiedScope": "UNCHANGED",
            "modifiedConfidentialityImpact": "NONE",
            "modifiedIntegrityImpact": "NONE",
            "modifiedAvailabilityImpact": "HIGH"
          }
        }
      ],
      "product_status": {
        "known_affected": [
          "SPDXRef-Windows-Embedded-Standard-7-with-SP1-patches-3.0"
        ],
        "known_not_affected": [
          "SPDXRef-INFUSION-1.0"
        ]
      },
      "threats": [
        {
          "details": "The SMB service is disabled. \n\t\t\t\tThe medical device restricts access to the O/S to field service personnel. \n\t\t\t\tThe medical devices is segmented from the hospital network through the use of an instrument firewall.\n\t\t\t\tThe medical device only allows the installation/executation of known/trusted components.",
          "category": "impact",
          "product_ids": [
            "SPDXRef-INFUSION-1.0"
          ]
        }
      ],
      "remediations": [
        {
          "details": "A future instrument update will contain the patch for KB4012215 that fixes the vulnerability in Windows 7 SP1.",
          "category": "none_available",
          "product_ids": [
            "SPDXRef-INFUSION-1.0"
          ]
        }
      ],
      "notes": [
        {
          "category": "summary",
          "text": "Vulnerability in a Component that Does Not Impact the Medical Device",
          "title": "Use Case 2"
        }
      ]
    },
    {
      "cve": "CVE-2021-1000000",
      "product_status": {
        "known_affected": [
          "SPDXRef-Bobs-Browser-1"
        ],
        "under_investigation": [
          "SPDXRef-INFUSION-1.0"
        ]
      },
      "scores": [
        {
          "products": [
            "SPDXRef-Bobs-Browser-1"
          ],
          "cvss_v3": {
            "version": "3.1",
            "vectorString": "CVSS:3.1/AV:N/AC:L/PR:L/UI:N/S:C/C:H/I:H/A:H",
            "baseScore": 9.9,
            "baseSeverity": "CRITICAL",
            "attackVector": "NETWORK",
            "attackComplexity": "LOW",
            "privilegesRequired": "LOW",
            "userInteraction": "NONE",
            "scope": "CHANGED",
            "confidentialityImpact": "HIGH",
            "integrityImpact": "HIGH",
            "availabilityImpact": "HIGH"
          }
        }
      ],
      "notes": [
        {
          "category": "summary",
          "text": "The Vulnerability in a Component is Under Investigation",
          "title": "Use Case 4"
        }
      ]
    },
    {
      "cve": "CVE-2021-44228",
      "scores": [
        {
          "products": [
            "CSAFPID-0004"
          ],
          "cvss_v3": {
            "version": "3.0",
            "vectorString": "CVSS:3.0/AV:N/AC:L/PR:N/UI:N/S:C/C:H/I:H/A:H",
            "baseScore": 10,
            "baseSeverity": "CRITICAL",
            "attackVector": "NETWORK",
            "attackComplexity": "LOW",
            "privilegesRequired": "NONE",
            "userInteraction": "NONE",
            "scope": "CHANGED",
            "confidentialityImpact": "HIGH",
            "integrityImpact": "HIGH",
            "availabilityImpact": "HIGH"
          }
        },
        {
          "products": [
            "SPDXRef-INFUSION-1.0"
          ],
          "cvss_v3": {
            "version": "3.0",
            "vectorString": "CVSS:3.0/AV:N/AC:L/PR:N/UI:N/S:C/C:N/I:N/A:N/MAV:P/MAC:H/MPR:H/MUI:N/MS:U/MC:N/MI:N/MA:H",
            "baseScore": 0,
            "baseSeverity": "NONE",
            "attackVector": "NETWORK",
            "attackComplexity": "LOW",
            "privilegesRequired": "NONE",
            "userInteraction": "NONE",
            "scope": "CHANGED",
            "confidentialityImpact": "NONE",
            "integrityImpact": "NONE",
            "availabilityImpact": "NONE"
         }
        }
      ],
      "product_status": {
        "known_affected": [
          "CSAFPID-0004"
        ],
        "known_not_affected": [
          "SPDXRef-INFUSION-1.0"
        ]
      },
      "threats": [
        {
          "details": "Apache log4j is not used.",
          "category": "impact",
          "product_ids": [
            "SPDXRef-INFUSION-1.0"
          ]
        }
      ],
      "notes": [
        {
          "category": "summary",
          "text": "Vulnerability in a Component that is Not Included in the Medical Device",
          "title": "Use Case 1"
        }
      ]
    }
  ]
}


## Return to Sweat Equity
[return to Sweat Equity](../../SweatEquity)

## Return to Agenda
[return to Agenda](../../Agenda)

## Return to Home
[return to Home](../../index.md)
