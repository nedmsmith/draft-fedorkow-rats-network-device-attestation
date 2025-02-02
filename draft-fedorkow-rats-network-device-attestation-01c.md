---
stand_alone: true
ipr: trust200902
docname: draft-fedorkow-rats-network-device-attestation-latest
cat: info
pi:
  toc: 'yes'
  tocdepth: '4'
  symrefs: 'yes'
  sortrefs: 'yes'
  compact: 'yes'
  subcompact: 'no'
title: Network Device Attestation Workflow
abbrev: Network Device Attestation Workflow
area: Security
wg: RATS Working Group
kw: Internet-Draft
date: 2019-06
author:
- role: editor
  ins: G. F. Fedorkow
  name: Guy Fedorkow
  org: Juniper Networks, Inc.
  street: ''
  city: ''
  region: ''
  code: ''
  country: US
  phone: ''
  email: gfedorkow@juniper.net
- ins: J. Fitzgerald-McKay
  name: Jessica Fitzgerald-McKay
  org: National Security Agency
  street: ''
  city: ''
  region: ''
  code: ''
  country: US
  phone: ''
  email: jmfitz2@nsa.gov
ref: {}
informative:
  RFC8348: 
  RFC7049: 
  RFC8572: 
  I-D.birkholz-yang-basic-remote-attestation: 
  I-D.birkholz-rats-architecture: 
  I-D.birkholz-rats-reference-interaction-model: 
  I-D.birkholz-suit-coswid-manifest: 
  I-D.birkholz-yang-swid: 
  I-D.ietf-sacm-coswid: 
  TAP:
    title: 'DRAFT: TCG Trusted Attestation Protocol (TAP) Information Model for TPM
      Families 1.2 and 2.0 and DICE Family 1.0, Version 1.0, Revision 0.29'
    author:
    - org: Trusted Computing Group
    date: 2018-10
  NIST-SP-800-155:
    target: https://csrc.nist.gov/csrc/media/publications/sp/800-155/draft/documents/draft-sp800-155_dec2011.pdf
    title: BIOS Integrity Measurement Guidelines (Draft)
    author:
    - org: National Institute for Standards and Technology
    date: 2011-12
  SNMP-Attestation-MIB:
    title: 'DRAFT: SNMP MIB for TPM-Based Attestation, Specification Version 0.8,
      Revision 0.02'
    author:
    - org: Trusted Computing Group
    date: 2018-05
  Canonical-Event-Log:
    title: 'DRAFT Canonical Event Log Format Version: 1.0, Revision: .12'
    author:
    - org: Trusted Computing Group
    date: 2018-10
  PC-Client-BIOS-TPM-1.2:
    target: https://www.trustedcomputinggroup.org/wp-content/uploads/TCG_PCClientImplementation_1-21_1_00.pdf
    title: TCG PC Client Specific Implementation Specification for Conventional BIOS,
      Specification Version 1.21 Errata, Revision 1.00
    author:
    - org: Trusted Computing Group
    date: 2012-02
  EFI:
    target: https://trustedcomputinggroup.org/wp-content/uploads/EFI-Protocol-Specification-rev13-160330final.pdf
    title: TCG EFI Platform Specification for TPM Family 1.1 or 1.2, Specification
      Version 1.22, Revision 15
    author:
    - org: Trusted Computing Group
    date: 2014-01
  RIM:
    title: 'DRAFT: TCG Reference Integrity Manifest'
    author:
    - org: Trusted Computing Group
    date: 2019-06
  Platform-DevID-TPM-2.0:
    title: 'DRAFT: TPM Keys for Platform DevID for TPM2, Specification Version 0.7,
      Revision 0'
    author:
    - org: Trusted Computing Group
    date: 2018-10
  Platform-Certificates:
    title: 'DRAFT: TCG Platform Attribute Credential Profile, Specification Version
      1.0, Revision 15, 07 December 2017'
    author:
    - org: Trusted Computing Group
    date: 2017-12
  Platform-ID-TPM-1.2:
    target: https://trustedcomputinggroup.org/wp-content/uploads/TPM_Keys_for_Platform_Identity_v1_0_r3_Final.pdf
    title: TPM Keys for Platform Identity for TPM 1.2, Specification Version 1.0,
      Revision 3
    author:
    - org: Trusted Computing Group
    date: 2015-08
  Firmware-Profile:
    target: https://trustedcomputinggroup.org/pc-client-specific-platform-firmware-profile-specification/
    title: Trusted Computing Group, PC Client Specific Platform Firmware Profile Specification
      Family "2.0", Level 00 Revision 1.03 Version 51
    author:
    - org: Trusted Computing Group
    date: 2019-06
  IEEE-802-1AR:
    title: 802.1AR-2018 - IEEE Standard for Local and Metropolitan Area Networks -
      Secure Device Identity, IEEE Computer Society
    author:
    - ins: M. Seaman
      org: IEEE Computer Society
    date: 2018-08
  IMA:
    target: https://sourceforge.net/p/linux-ima/wiki/Home/
    title: Integrity Measurement Architecture
    author:
    - surname: dsafford
      org: ''
    - surname: kds_etu
      org: ''
    - surname: mzohar
      org: ''
    - surname: reinersailer
      org: ''
    - surname: serge_hallyn
      org: ''
    date: 2019-06
  Roots-of-Trust:
    target: https://trustedcomputinggroup.org/wp-content/uploads/TCG_Roots_of_Trust_Specification_v0p20_PUBLIC_REVIEW.pdf
    title: TCG Roots of Trust Specification
    author:
    - org: Trusted Computing Group
    date: 2018-10
  NetEq:
    target: https://trustedcomputinggroup.org/wp-content/uploads/TCG_Guidance_for_Securing_NetEq_1_0r29.pdf
    title: TCG Guidance for Securing Network Equipment
    author:
    - org: Trusted Computing Group
    date: 2018-01
  NIST-IR-8060:
    target: https://nvlpubs.nist.gov/nistpubs/ir/2016/NIST.IR.8060.pdf
    title: Guidelines for the Creation of Interoperable Software Identification (SWID)
      Tags
    author:
    - org: National Institute for Standards and Technology
    date: 2016-04
  SWID:
    target: https://www.iso.org/standard/65666.html
    title: 'Information Technology Software Asset Management Part 2: Software Identification
      Tag, ISO/IEC 19770-2'
    author:
    - org: The International Organization for Standardization/International Electrotechnical
        Commission
    date: 2015-10
  PC-Client-BIOS-TPM-2.0:
    target: https://trustedcomputinggroup.org/pc-client-specific-platform-firmware-profile-specification
    title: PC Client Specific Platform Firmware Profile Specification Family "2.0",
      Level 00 Revision 1.04
    author:
    - org: Trusted Computing Group
    date: 2019-06

--- abstract

This document describes a workflow for network device attestation.

--- middle

# Introduction

There are many components to consider in fielding a trusted computing device,
from operating systems to applications.  Part of that is a trusted supply
chain, where manufacturers can certify that the product they intended to
build is actually the one that was installed at a customer's site.

Attestation is defined here as the process of creating, conveying and appraising
assertions about Platform trustworthiness characteristics, including Roots
of Trust, supply chain trust, identity, platform provenance, shielded locations,
protected capabilities, software configuration, hardware configuration, platform
composition, compliance to test suites, functional and assurance evaluations,
etc.

The supply chain itself has many elements, from validating suppliers of electronic
components, to ensuring that shipping procedures protect against tampering
through many stages of distribution and warehousing.  One element that helps
maintain the integrity of the supply chain after manufacturing is Attestation.

Within the Trusted Computing Group context, attestation is the process by
which an independent Verifier can obtain cryptographic proof as to the identity
of the device in question, evidence of the integrity of software loaded on
that device when it started up, and then verify that what's there is what's
supposed to be there.  For networking equipment, a verifier capability can
be embedded in a Network Management Station (NMS), a posture collection server,
or other network analytics tool (such as a software asset management solution,
or a threat detection and mitigation tool, etc.). While informally referred
to as attestation, this document focuses on a subset defined here as Remote
Integrity Verification (RIV).  RIV takes a network equipment centric perspective
that includes a set of protocols and procedures for determining whether a
particular device was launched with untampered software, starting from Roots
of Trust.  While there are many ways to accomplish attestation, RIV sets
out a specific set of protocols and tools that work in environments commonly
found in Networking Equipment.  RIV does not cover other platform characteristics
that could be attested, although it does provide evidence of a secure infrastructure
to increase the level of trust in other platform characteristics attested
by other means.

This profile outlines the RIV problem, and then identifies components that
are necessary to get the complete attestation procedure working in a scalable
solution using commercial products.

This document focuses primarily on software integrity verification using
the Trusted Platform Module (TPM) as a root of trust.

Attestation information of course must be protected by means of cryptographic techniques to assure its validity.  
It's important to note that TCG technologies are available to use either symmetric key encryption with shared keys, or public key cryptography using private/public key pairs.  
The two techniques can each produce secure results, but do require different provisioning mechanisms.  
The RIV document currently focuses on asymmetric keying approaches only; future work might include techniques for attestation using symmetric keys.

## Requirements Language

{::boilerplate bcp14}

## Goals

As a part of a trusted supply chain, Attestation requires two interlocking services:

* Platform Identity, the mechanism providing trusted identity, can reassure network 
  managers that the specific devices they ordered from authorized manufacturers for 
  attachment to their network are those that were installed, and that they continue to 
  be present in their network. As part of the mechanism for Platform Identity, 
  cryptographic proof of the identity of the manufacturer is also provided.
* Software Measurement is the mechanism that reports the state of mutable components 
  on the device, and can assure network managers that they have known, untampered 
  software configured to run in their network.

The RIV attestation workflow outlined in this document is intended to meet
the following high-level goals:

* Provable Device Identity - The ability to identify a device using a cryptographic
  identifier is a critical prerequisite to software inventory attestation.

* Software Inventory - A key goal is to identify the software release installed
  on the device, and to provide evidence of its integrity.

* Verification - Verification of software and configuration of the device shows
  that the software that's supposed to be installed on  there actually has
  been launched, without unauthorized modification.

This document itself is non-normative; the document does not define protocols,
but rather identifies protocols that can be used together to achieve the
goals above, and in some cases, highlights gaps in existing protocols.

## Problem Description

RIV is a procedure that assures a network operator that the equipment on
their network can be reliably identified, and that untampered software of
a known version is installed on each endpoint. In this context, endpoint
might include the conventional connected devices like servers and laptops, but also
connected devices that make up the network equipment itself, such as routers, 
switches and firewalls.

RIV can be viewed as a link in a trusted supply chain, and includes three
major processes:

* Creation of Evidence is the process whereby an endpoint generates cryptographic
  proof (evidence) of claims about platform properties. In particular, the
  platform identity and its software configuration are of critical importance

  * Platform Identity refers to the mechanism assuring the
    attestation relying party (typically a network administrator)
    of the identity of devices that make up their network,
    and that their manufacturers are known.
  
  * Software used to boot a platform can be described as a chain
    of measurements, started by a Root of Trust for Measurement,
    that normally ends when the system software is loaded.
    A measurement signifies the identity, integrity and version of each
    software component registered with the TPM, so that the
    subsequent appraisal stage can determine if the software
    installed is authentic, up-to-date, and free of tampering. 

  Clearly the 
  second part of the problem, attesting the state of mutable components
  of a given device, is of little value without
  reliable identification of the device in question.  By the
  same token, unambiguous identity of a device is necessary,
  but is insufficient to assure the operator of the provenance
  of the device through the supply chain, or that the device is
  configured to behave properly.

* Conveyance of Evidence is the process of reliably transporting evidence from
  the point in a connected device where a measurement is stored to an 
  appraiser/verifier, e.g. a management station. The transport
  is typically carried out via a management network. The channel must provide
  integrity and authenticity, and, in some use cases, may also require confidentiality.

* Appraisal of Evidence is the process of verifying the evidence received by
  a verifier/appraiser from a device, and using verified evidence to inform
  decision making. In this context, verification means comparing the device
  measurements reported as evidence with the configuration expected by the
  system administrator. This step can work only when there is a way to express
  what should be there, often referred to as golden measurements, or Reference
  Integrity Measurements, representing the intended configured state of the 
  connected device.

An implementation of RIV requires three technologies

1. Identity: Platform identity can be based on IEEE 802.1AR Device Identity {{IEEE-802-1AR}},
   coupled with careful supply-chain management by the manufacturer.  The
   DevID certificate contains a statement by the manufacturer that establishes
   the provenance of the device as it left the factory.  Some applications with
   a more-complex post-manufacture supply chain (e.g. Value Added Resellers),
   or with privacy concerns, may want to use an alternate mechanism for platform
   authentication based on TCG Platform Certificates {{Platform-Certificates}}.  
   RIV currently relies on asymmetric keying for identity; alternate approaches 
   might use symmetric keys.

2. Platform Attestation provides evidence of configuration of software elements
   throughout the product lifecycle.  This form of attestation  can be implemented
   with TPM PCR, Quote and log mechanisms, which provide an authenticated mechanism
   to report what software actually starts up on the device each time it reboots.

3. Reference Integrity Measurements must be conveyed from the software authority
   (often the manufacturer for embedded systems) to the system in which verification
   will take place

Service Providers benefit from a trustworthy attestation mechanism that provides
assurance that their network comprises authentic equipment, and has loaded software
free of known vulnerabilities and unauthorized tampering.

## Solution Requirements

The RIV attestation solution must meet a number of requirements to make it simple
to deploy at scale.

1. Easy to Use - This solution should work "out of the box" as far as possible,
   that is, with the fewest possible steps needed at the end-user's site.  Eliminate
   complicated databases or provisioning steps that would have to be executed
   by the owner of a new device. Network equipment is often required to "self-configure",
   to reliably reach out without manual intervention to prove its identity and
   operating posture, then download its own configuration. See {{RFC8572}} for an
   example of Secure Zero Touch Provisioning.

2. Multi-Vendor - This solution should identify standards-based interfaces that
   allow attestation to work with attestation-capable devices and verifiers
   supplied by different vendors in one network.

3. Scalable - The solution must not depend on choke points that limit the number
   of endpoints that could be evaluated in one network domain.

4. Extensible - A network equipment attestation solution needs to expand over
   time as new features are added. The solution must allow new features to be
   added easily, providing for a smooth transition and allowing newer and older
   architectural components to continue to work together. Further, a network
   equipment attestation solution and the specifications referenced here must
   define safe extensibility mechanisms that enable innovation without breaking
   interoperability.

5. Efficient - A network equipment attestation solution should, to the greatest
   extent feasible, continuously monitor the health and posture status of network
   devices. Posture measurements should be updated in real-time as changes to
   device posture occur and should be published to remote integrity validators.
   Validation reports should also be shared with their relying parties (for
   example, network administrators, or network analytics that rely on these
   reports for posture assessment) as soon as they are available.

## Scope

This document includes a number of assumptions to limit the scope:

* This solution is for use in non-privacy-preserving applications (for example,
  networking, Industrial IoT), avoiding the need for a Privacy Certificate
  Authority for attestation keys

* This document applies primarily to "embedded" applications, where the device
  manufacturer ships the software image for the device.

* The approach outlined in this document assumes the use of TPM 1.2 or TPM 2.0.

### Out of Scope

* Run-Time Attestation: Run-time attestation of Linux or other multi-threaded
  operating system processes considerably expands the scope of the problem.
  Many researchers are working on that problem, but this document defers the
  run-time attestation problem.

* Multi-Vendor Embedded Systems: Additional coordination would be needed for
  devices that themselves comprise hardware and software from multiple vendors,
  integrated by the end user.

* Processor Sleep Modes: Network equipment typically does not "sleep", so
  sleep and hibernate modes are not considered.

* Virtualization and Containerization:  These technologies are increasingly
  used in Network equipment, but are not considered in this revision of the
  document.

### Why Remote Integrity Verification?

Remote Integrity Verification can go a long way to solving the "Lying Endpoint"
problem, in which malicious software on an endpoint may both subvert the
intended function, and also prevent the endpoint from reporting its compromised
status.  Man-in-the Middle attacks are also made more difficult through a
strong focus on device identity

Attestation data can be used for asset management, vulnerability and compliance
assessment, plus configuration management.

### Network Device Attestation Challenges

There have been demonstrations of attestation using TPMs for years, accompanied
by compelling security reasons for adopting attestation. Despite this, the
technology has not been widely adopted, in part, due to the difficulties
in deploying TPM-based attestation. Some of those difficulties are:

* Standardizing device identity. Creating and using unique device identifiers
  is difficult, especially in a privacy-sensitive environment.  But attestation
  is of limited value if the operator is unable to determine which devices
  pass attestation validation tests, and which fail. This problem is substantially
  simplified for infrastructure devices like network equipment, where identity
  can be explicitly coded using IEEE 802.1AR, but doing so relies on adoption
  of 802.1AR {{IEEE-802-1AR}} by manufacturers and hardware system integrators.

* Standardizing attestation representations and conveyance. Interoperable remote
  attestation has a fundamental dependence on vendors agreeing to a limited
  set of network protocols commonly used in existing network equipment  for 
  communicating attestation data. Network device
  vendors will be slow to adopt the changes necessary to implement remote
  attestation without a fully-realized plan for deployment.

* Interoperability. Networking equipment operates in a fundamentally multi-vendor
  environment, putting additional emphasis on the need for standardized procedures
  and protocols.

* Attestation evidence is complex. Operating systems used in larger embedded
  devices are often multi-threaded, so the order of completion for individual
  processes is non-deterministic.  While the hash of a specific component is
  stable, once extended into a PCR, the resulting values are dependent on the
  (non-deterministic) ordering of events, so there will never be a single known-good
  value for some PCRs.  Careful analysis of event logs can provide proof that
  the expected modules loaded, but it's much more complicated than simply comparing
  reported and expected digests, as collected in TPM Platform Configuration 
  Registers (PCRs).

* Software configurations can have seemingly infinite variability.  This problem
  is nearly intractable on PC and Server equipment, where end users have unending
  needs for customization and new applications.  However, embedded systems,
  like networking equipment, are often simpler, in that there are fewer variations
  and releases, with vendors typically offering fewer options for mixing and
  matching.

* Standards-based mechanisms to encode and distribute Reference Integrity 
  Measurements, (i.e., expected values) are still in development.

* Software updates can be complex.  Even the most organized network operator
  may have many different releases in their network at any given time, with
  the result that there's never a single digest or fingerprint that indicates
  the software is "correct"; digests formed by hashing software modules on
  a device can only show the correct combination of versions for a specific
  device at a specific time.

None of these issues are insurmountable, but together, they've made deployment
of attestation a major challenge.  The intent of this document is to outline
an attestation profile that's simple enough to deploy, while yielding enough
security to be useful.

### Why is OS Attestation Different?

Even in embedded systems, adding Attestation at the OS level (e.g. Linux
IMA, Integrity Measurement Architecture {{IMA}}) increases the number of objects to be attested by one or two orders of
magnitude, involves software that's updated and changed frequently, and introduces
processes that begin in unpredictable order.

TCG and others (including the Linux community) are working on methods and
procedures for attesting the operating system and application software, but
standardization is still in process.

# Solution Outline

## 2.1 RIV Software Configuration Attestation using TPM

RIV Attestation is a process for determining the identity of software running
on a specifically-identified device.  Remote Attestation is broken into two
phases, shown in Figure 1:

* During system startup, measurements (i.e., digests computed as fingerprints
  of files) are extended, or cryptographically folded, into the TPM.  Entries
  are also added to an informational log.  The measurement process generally
  follows the Chain of Trust model used in Measured Boot, where each stage
  of the system measures the next one, and extends its measurement into the TPM, 
  before launching it.

* Once the device is running and has operational network connectivity, a separate,
  trusted server (called a Verifier in this document) can interrogate the network
  device to retrieve the logs and a copy of the digests collected by hashing
  each software object, signed by an attestation private key known only to
  the TPM.

The result is that the Verifier can verify the device's identity by checking
the certificate containing the TPM's attestation public key, and can
validate the software that was launched by comparing digests in the log with
known-good values, and verifying their correctness by comparing with the
signed digests from the TPM.

It should be noted that attestation and identity are inextricably linked;
signed evidence that a particular version of software was loaded is of little
value without cryptographic proof of the identity of the device producing
the evidence.

~~~~
    +-------------------------------------------------------+
    | +--------+    +--------+   +--------+    +---------+  |
    | | BIOS   |--->| Loader |-->| Kernel |--->|Userland |  |
    | +--------+    +--------+   +--------+    +---------+  |
    |     |            |           |                        |
    |     |            |           |                        |
    |     +------------+-----------+-+                      |
    |                        Step 1  |                      |
    |                                V                      |
    |                            +--------+                 |
    |                            |  TPM   |                 |
    |                            +--------+                 |
    |   Router                       |                      |
    +--------------------------------|----------------------+
                                     |
                                     |  Step 2
                                     |    +-----------+
                                     +--->| Verifier  |
                                          +-----------+

    Reset---------------flow-of-time-during-boot--...------->
~~~~
{: #TCG-Attestation-Model title='TCG Attestation Model' artwork-align="left"}

In Step 1, measurements are "extended" into the TPM as processes start. In
Step 2, signed PCR digests are retrieved from the TPM for off-box analysis
after the system is operational.

## RIV Keying

TPM 1.2 and TPM 2.0 have a variety of rules separating the functions of identity
and attestation, allowing for use-cases where software configuration must
be attested, but privacy must be maintained.

To accommodate these rules, enforced inside the TPM, in an environment where 
device privacy is not
normally a requirement, the TCG Guidance for Securing Network Equipment
{{NetEq}} suggests using separate keys for Identity (i.e., DevID) and
Attestation (i.e., signing a quote of the contents of the PCRs), but
provisioning an Initial Attestation
Key (IAK) and x.509 certificate that parallels the IDevID, with the same
device ID information as the IDevID certificate (i.e., the same Subject Name
and Subject Alt Name, even though the key pairs are different).  This allows
a quote from the device, signed by the IAK, to be linked directly to the
device that provided it, by examining the corresponding IAK certificate.

Inclusion of an IAK by a vendor does not preclude a mechanism whereby an
Administrator can define Local Attestation Keys (LAKs) if desired.

## RIV Information Flow

RIV workflow for networking equipment is organized around a simple use-case,
where a network operator wishes to verify the integrity of software installed
in specific, fielded devices.  This use-case implies several components:

1. A Device (e.g. a router or other embedded device, also known as an Attester)
  somewhere and the network operator wants to examine its boot state.

2. A Verifier (which might be a network management station) somewhere separate
  from the Device that will retrieve the information and analyze it to pass
  judgement on the security posture of the device.

3. A Relying Party, which has access to the Verifier to request attestation
  and to act on results.

4. This document assumes that signed Reference Integrity Measurements (RIMs)
  (aka "golden measurements") can either be created by the device manufacturer
  and shipped along with the device as part of its software image, or alternatively,
  could be obtained a number of other ways (direct to the verifier from the
  manufacturer, from a third party, from the owner's observation of what's
  thought to be a "known good system", etc.).  Retrieving RIMs from the device
  itself allows attestation to be done in systems which may not have access
  to the public internet, or by other devices that are not management stations
  per-se (e.g., a peer device).  If reference measurements are obtained from
  multiple sources, the Verifier may need to evaluate the relative level of
  trust to be placed in each source in case of a discrepancy.

These components are illustrated in Figure 2.

A more-detailed taxonomy of terms is given in {{I-D.birkholz-rats-architecture}}

~~~~
+---------------+        +-------------+        +---------+--------+
|               |        | Attester    | Step 1 | Verifier|        |
| Asserter      |        | (Device     |<-------| (Network| Relying|
| (Device       |        | under       |------->| Mngmt   | Party  |
| Manufacturer  |        | attestation)| Step 2 | Station)|        |
| or other      |        |             |        |         |        |
| authority)    |        |             |        |         |        |
+---------------+        +-------------+        +---------+--------+
       |                                             /\
       |                  Step 0                      |
       -----------------------------------------------

~~~~
{: #RIV-Reference-Configuration title='RIV Reference Configuration for Network Equipment' artwork-align="left"}

In Step 0, The Asserter (the device manufacturer) provides a Software Image
accompanied by Reference Integrity Measurements (RIMs) to the Attester (the
device under attestation) signed by the asserter. In Step 1, the Verifier
(Network Management Station), on behalf of a Relying Party, requests Identity,
Measurement Values (and possibly RIMs) from the Attester. In Step 2, the
Attester responds to the request by providing a DevID, Quotes (measured values),
and optionally RIMs, signed by the Attester.

See Section 3.1.1 for more narrowly defined terms related to Attestation

## RIV Simplifying Assumptions

This document makes the following simplifying assumptions to reduce complexity:

* The product to be attested is shipped with an IEEE 802.1AR DevID and an Initial
  Attestation Key (IAK) with certificate.  The IAK cert contains the same identity
  information as the DevID (specifically, the same Subject Name and Subject
  Alt Name, signed by the manufacturer), but it's a type of key that can be
  used to sign a TPM Quote.  This convention is described in TCG Guidance for
  Securing Network Equipment {{NetEq}}. For network equipment, which is generally non-privacy-sensitive, shipping
  a device with both an IDevID and an IAK already provisioned substantially
  simplifies initial startup. Privacy-sensitive applications may use the TCG
  Platform Certificate and additional procedures to install identity credentials
  on the platform after manufacture.  (See Section 2.3.1 below for the Platform
  Certificate alternative)

* The product is equipped with a Root of Trust for Measurement, Root of Trust
  for Storage and Root of Trust for Reporting  that is capable of conforming
  to the TCG Trusted Attestation Protocol (TAP) Information Model {{TAP}}.

* The vendor will ship Reference Integrity Measurements (i.e., known-good measurements)
  in the form of signed CoSWID tags {{I-D.ietf-sacm-coswid}}, {{SWID}},
  as described in TCG Reference Integrity Measurement Manifest {{RIM}}.

### DevID Alternatives

Some situations may have privacy-sensitive requirements that preclude shipping
every device with an Initial Device ID installed.  In these cases, the IDevID
can be installed remotely using the TCG Platform Certificate {{Platform-Certificates}}.

Some administrators may want to install their own identity
credentials to certify device identity and attestation results.  IEEE 802.1AR
{{IEEE-802-1AR}} allows for both Initial Device Identity credentials, installed by the manufacturer, (analogous to a physical serial number plate),
or Local Device Identity credentials installed by the administrator of the
device (analogous to the physical Asset Tag used by many enterprises to identify their property).  TCG TPM 2.0 Keys documents {{Platform-DevID-TPM-2.0}} and
{{PC-Client-BIOS-TPM-2.0}} specifies parallel Initial and Local Attestation Keys (IAK and LAK), and
contains figures showing the relationship between IDevID, LDevID, IAK and
LAK keys.

Device administrators are free to use any number of criteria to judge authenticity
of a device before installing local identity keys, as part of an on-boarding
process.  The TCG TPM 2.0 Keys document {{Platform-DevID-TPM-2.0}} also outlines
procedures for creating Local Attestation Keys and Local Device
IDs (LDevIDs) rooted in the manufacturer's IDevID as a check to reduce the
chances that counterfeit devices are installed in the network.

Note that many networking devices are expected to self-configure (aka Zero
Touch Provisioning).  Current standardized zero-touch mechanisms such as
{{RFC8572}} assume that identity keys are already in place before network on-boarding
can start, and as such, are compatible with IDevID and IAK keys installed by the 
manufacturer, but not with LDevID and LAK keys, which would have to be installed 
by the administrator.


### Additional Attestation of Platform Characteristics

The Platform Attribute Credential {{Platform-Certificates}} can also be used to convey additional information about a platform from the
manufacturer or other entities in the supply chain.  While outside the scope
of RIV, the Platform Attribute Credential can deliver information such as
lists of serial numbers for components embedded in a device or security assertions
related to the platform, signed by the manufacturer, system integrator or
value-added-reseller.

### Root of Trust for Measurement

The measurements needed for attestation require that the device being attested
is equipped with a Root of Trust for Measurement, i.e., some trustworthy
mechanism that can compute the first measurement in the chain of trust required
to attest that each stage of system startup is verified, and a Root of Trust
for Reporting to report the results {{Roots-of-Trust}}.

While there are many complex aspects of a Root of Trust, two aspects that
are important in the case of attestation are:

* The first measurement computed by the Root of Trust for Measurement, and stored
  in the TPM's Root of Trust for Storage, is presumed to be correct.

* There must not be a way to reset the RTS without re-entering the RTM code.

The first measurement must be computed by code that is implicitly trusted; if that
first measurement can be subverted, none of the remaining measurements can
be trusted. (See {{NIST-SP-800-155}}

### Reference Integrity Measurements (RIMs)

Much of attestation focuses on collecting and transmitting 'evidence' in
the form of PCR measurements and attestation logs.  But the critical part
of the process is enabling the verifier to decide whether the measurements
are "the right ones" or not.

While it must be up to network administrators to decide what they want on
their networks, the software supplier should supply the Reference Integrity
Measurements, (aka Golden Measurements or "known good" hash digests) that
may be used by a verifier to determine if evidence shows known good, known
bad or unknown software configurations.

In general, there are two kinds of reference measurements:

1. Measurements of early system startup (e.g., BIOS, boot loader, OS kernel)
   are essentially single threaded, and executed exactly once, in a known sequence,
   before any results could be reported.  In this case, while the method for
   computing the hash and extending relevant PCRs may be complicated, the net
   result is that the software (more likely, firmware) vendor will have one
   known good PCR value that "should" be present in the PCR after the box has
   booted.  In this case, the signed reference measurement simply lists the
   expected hash for the given version.

2. Measurements taken later in operation of the system, once an OS has started
   (for example, Linux IMA[16.]), may be more complex, with unpredictable "final"
   PCR values.  In this case, the Verifier must have enough information to reconstruct
   the expected PCR values from logs and signed reference measurements from
   a trusted authority. 

In both cases, the expected values can be expressed as signed CoSWID tags,
but the SWID structure in the second case is somewhat more complex. An example
of how CoSWIDs could be incorporated into a reference manifest can be found
in the IETF Internet-Draft "A SUIT Manifest Extension for Concise Software
Identifiers" {{I-D.birkholz-suit-coswid-manifest}}.

The TCG has done exploratory work in defining formats for reference integrity
manifests under the working title TCG Reference Integrity Manifest {{RIM}}.

### Attestation Logs

Quotes from a TPM can provide evidence of the state of a device up to the time
the evidence was recorded, but to make sense of the quote in most cases an
event log of what software modules contributed which values to the quote
during startup must also be provided.  The log must contain enough information 
to demonstrate its integrity by allowing exact reconstruction of the digest 
conveyed in
the signed quote (e.g., PCR values).

TCG has defined several event log formats:

* Legacy BIOS event log (TCG PC Client Specific Implementation Specification
  for Conventional BIOS, Section 11.3{{PC-Client-BIOS-TPM-1.2}})

* UEFI BIOS event log (TCG EFI Platform Specification for TPM Family 1.1 or
  1.2, Section 7 {{EFI}})

* Canonical Event Log {{Canonical-Event-Log}}

It should be noted that a given device might use more than one event log
format (e.g., a UEFI log during initial boot, switching to Canonical Log
when the host OS launches).

The TCG SNMP Attestation MIB {{SNMP-Attestation-MIB}} will support any
record-oriented log format, including the three TCG-defined
formats, but it currently leaves figuring out which log(s) are in what format
up to the Verifier.

# Standards Components

## Reference Models

### IETF Reference Model for Challenge-Response Remote Attestation

Initial work at IETF defines remote attestation as follows:

The Reference Interaction Model for Challenge-Response-based Remote Attestation
is based on the standard roles defined in {{I-D.birkholz-rats-architecture}}:

  * Attester: The role that designates the subject of the remote attestation.
    A system entity that is the provider of evidence takes on the role of an
    Attester.

  * Verifier: The role that designates the system entity and that is the appraiser
    of evidence provided by the Attester. A system entity that is the consumer
    of evidence takes on the role of a Verifier.

The following diagram illustrates a common information flow between a Verifier
and an Attester, specified in {{I-D.birkholz-rats-reference-interaction-model}}:

~~~~
Attester                                                     Verifier
   |                                                               |
   | <------- requestAttestation(nonce, authSecID, claimSelection) |
   |                                                               |
collectAssertions(assertionsSelection)                             |
   | => assertions                                                 |
   |                                                               |
signAttestationEvidence(authSecID, assertions, nonce)              |
   | => signedAttestationEvidence                                  |
   |                                                               |
   | signedAttestationEvidence ----------------------------------> |
   |                                                               |
   | verifyAttestationEvidence(signedAttestationEvidence, refassertions)
   |                                          attestationResult <= |
   |                                                               |
~~~~
{: #IETF-Attestation-Information-Flow title='IETF Attestation Information Flow' artwork-align="left"}

The RIV approach outlined in this document aligns with the RATS reference
model.

## RIV Workflow

The overall flow for an attestation session is shown in Figure 4.  In this
diagram:

* Step 0, positioning of the signed reference measurements, may happen in two
  ways:

* Step 0A below shows a verifier obtaining reference measurements directly
  from a software configuration authority, whether it's the vendor or another
  authority chosen by the system administrator.  The reference measurements
  are signed by the Asserter (i.e., the software configuration authority).

* \- Or - Step 0B, the reference measurements, signed by the Asserter, may be
  distributed as part of software installation, long before the attestation
  session begins.  Software installation is usually vendor-dependent, so there
  are no standards involved in this step.  However, the verifier can use the
  same protocol to obtain the reference measurements from the device as it
  would have used with an external reference authority

* In Step 1, the Verifier initiates an attestation session by opening a TLS
  session, validated using the DevID to prove that the connection is attesting
  the right box.

* In Step 2, measured values are retrieved from the Attester's TPM using a
  YANG or SNMP interface that implements the TCG TAP model (e.g. YANG Module
  for Basic Challenge-Response-based Remote Attestation Procedures {{I-D.birkholz-yang-basic-remote-attestation}}).

* In Step 3, the Attester also delivers a copy of the signed reference measurements,
  using Software Inventory YANG module based on Software Identifiers {{I-D.birkholz-yang-swid}}.

~~~~
+---------------+        +-------------+        +---------+
|               |        |             | Step 1 |         |
|               |        | Attester    |<------>| Verifier|
| Asserter      |        | (Device     |<------>| (Network|
|(Configuration |------->| under       | Step 2 | Mngmt   |
| Authority)    | Step 0A| attestation)|        | Station)|
|               |        |             |------->|         |
+---------------+        +-------------+ Step 3 +---------+
        |                                           /|\
        |                                            |
        ----------------------------------------------
                        Step 0B

~~~~
{: #RIV-Protocol-and-Encoding-Summary title='RIV Protocol and Encoding Summary' artwork-align="left"}

Either CoSWID-encoded reference measurements are signed by a trusted authority
and retrieved directly prior to attestation (as shown in Step 0A), or CoSWID-encoded
reference measurements are signed by the device manufacturer, installed on
the device by a proprietary installer, and delivered during attestation (as
shown in Step 0B). In Step 1, the Verifier initiates a connection for attestation.
The Attester's identity is validated using DevID with TLS. In Step 2, a
nonce, quotes (measured values) and measurement log are conveyed via TAP
with a protocol-specific binding (e.g. SNMP). Logs are sent in the Canonical
Log Format In Step 3, CoSWID-encoded reference measurements are retrieved
from the Attester using the YANG ({{I-D.birkholz-yang-swid}}.
.

The following components are used:

1. TPM Keys are configured according to {{Platform-DevID-TPM-2.0}}, {{PC-Client-BIOS-TPM-1.2}}, or {{Platform-ID-TPM-1.2}}

2. Measurements of bootable modules are taken according to TCG PC Client {{PC-Client-BIOS-TPM-2.0}} and Linux IMA {{IMA}}

3. Device Identity is managed by IEEE 802.1AR certificates {{IEEE-802-1AR}}, with keys protected by TPMs.

4. Quotes are retrieved according to TCG TAP Information Model {{TAP}}

5. Reference Integrity Measurements are encoded as CoSWID tags, as defined in
  the TCG RIM document {{RIM}}, compatible with NIST IR 8060 {{NIST-IR-8060}} and the IETF CoSWID draft {{I-D.ietf-sacm-coswid}}.  Reference measurements are signed by the device manufacturer.

## Layering Model for Network Equipment Attester and Verifier

Retrieval of identity and attestation state uses one protocol stack, while
retrieval of Reference Measurements uses a different set of protocols.  Figure
5 shows the components involved.

~~~~
+-----------------------+              +-------------------------+
|                       |              |                         |
|       Attester        |<-------------|        Verifier         |
|       (Device)        |------------->|   (Management Station)  |
|                       |      |       |                         |
+-----------------------+      |       +-------------------------+
                               |
           -------------------- --------------------
           |                                        |
---------------------------------- ---------------------------------
|Reference Integrity Measurements| |         Attestation           |
---------------------------------- ---------------------------------

********************************************************************
*         IETF Attestation Reference Interaction Diagram           *
********************************************************************

    .......................         .......................
    . Reference Integrity .         .  TAP (PTS2.0) Info  .
    .     Measurement     .         . Model and Canonical .
    .      Manifest       .         .     Log Format      .
    .......................         .......................

    *************************  .............. **********************
    * YANG SWID Module      *  . TCG        . * YANG Attestation   *
    * I-D.birkholz-yang-swid*  . Attestation. * Module             *
    *                       *  . MIB        . * I-D.birkholz-yang- *
    *                       *  .            . * basic-remote-      *
    *                       *  .            . * attestation        *
    *************************  .............. **********************

    *************************  ************ ************************
    * XML, JSON, CBOR (etc) *  *    UDP   * * XML, JSON, CBOR (etc)*
    *************************  ************ ************************

    *************************               ************************
    *   RESTCONF/NETCONF    *               *   RESTCONF/NETCONF   *
    ************************               *************************

    *************************               ************************
    *       TLS, SSH        *               *       TLS, SSH       *
    *************************               ************************

~~~~
{: #RIV-Protocol-Stacks title='RIV Protocol Stacks' artwork-align="left"}

IETF documents are captured in boxes surrounded by asterisks. TCG documents
are shown in boxes surrounded by dots. The IETF Attestation Reference Interaction
Diagram, Reference Integrity Measurement Manifest, TAP Information Model
and Canonical Log Format, and both YANG modules are works in progress. Information
Model layers describe abstract data objects that can be requested, and the
corresponding response SNMP is still widely used, but the industry is transitioning
to YANG, so in some cases, both will be required. TLS Authentication with
TPM has been shown to work; SSH authentication using TPM-protected keys is
not as easily done \[as of 2019]

# Conclusion

TCG technologies can play an important part in the implementation of Remote
Integrity Verification.  Standards for many of the components needed for
implementation of RIV already exist:

* Platform identity can be based on IEEE 802.1AR Device identity, coupled with
  careful supply-chain management by the manufacturer.

* Complex supply chains can be certified using TCG Platform Certificates {{Platform-Certificates}}

* The TCG TAP mechanism can be used to retrieve attestation evidence.  Work
  is needed on a YANG model for this protocol.

* Reference Measurements must be conveyed from the software authority (e.g.,
  the manufacturer) to the system in which verification will take place.  IETF
  CoSWID work forms the basis for this, but new work is needed to create an
  information model and YANG implementation.

Gaps still exist for implementation in Network Equipment (as of May 2019):

* Coordination of YANG model development with the IETF is still needed

* Specifications for management of signed Reference Integrity Measurements
  must still be completed

# Appendix

## Implementation Notes

Table 1 summarizes many of the actions needed to complete an Attestation
system, with links to relevant documents.  While documents are controlled
by a number of standards organizations, the implied actions required for
implementation are all the responsibility of the manufacturer of the device,
unless otherwise noted.

~~~~
+------------------------------------------------------------------+
|             Component                           |  Controlling   |
|                                                 | Specification  |
--------------------------------------------------------------------
| Make a Secure execution environment             |   TCG RoT      |
|   o Attestation depends on a secure root of     |   UEFI.org     |
|     trust for measurement outside the TPM, as   |                |
|     well as roots for storage amd reporting     |                |
|     inside the TPM.                             |                |
|   o  Refer to TCG Root of Trust for Measurement.|                |
|   o  NIST SP 800-193 also provides guidelines   |                |
|      on Roots of Trust                          |                |
--------------------------------------------------------------------
| Get a TPM properly provisioned as described in  | TCG TPM DevID  |
|   TCG documents.                                | TCG Platform   |
|                                                 |   Certificate  |
--------------------------------------------------------------------
| Put a DevID or Platform Cert in the TPM         | TCG TPM DevID  |
|    o Install an Initial Attestation Key at the  | TCG Platform   |
|      same time so that Attestation can work out |   Certificate  |
|      of the box                                 |-----------------
|    o Equipment suppliers and owners may want to | IEEE 802.1AR   |
|      implement Local Device ID as well as       |                |
|      Initial Device ID                          |                |
--------------------------------------------------------------------
| Connect the TPM to the TLS stack                | Vendor TLS     |
|    o  Use the DevID in the TPM to authenticate  | stack (This    |
|       TAP connections, identifying the device   | action is      |
|                                                 | simply         |
|                                                 | configuring TLS|
|                                                 | to use the     |
|                                                 | DevID as its   |
|                                                 | trust anchor.) |
--------------------------------------------------------------------
| Make CoSWID tags for BIOS/LoaderLKernel objects | IETF CoSWID    |
|    o  Add reference measurements into SWID tags | ISO/IEC 19770-2|
|    o  Manufacturer should sign the SWID tags    | NIST IR 8060   |
|    o  This should be covered in a new TCG       | TagVault SWID  |
|       Reference Integrity Manifest document     |   Tag Signing  |
|       -  IWG should define the literal SWID     |   Guidance     |
|          format                                 |-----------------
|       -  IWG should evaluate whether IETF SUIT  | TCG RIM        |
|          is a suitable manifest when multiple   |                |
|          SWID tags are involved                 |                |
|       -  There could be a proof-of-concept      |                |
|          project to actually make sample SWID   |                |
|          tags (a gap might appear in the        |                |
|          process)                               |                |
--------------------------------------------------------------------
|  Package the SWID tags with a vendor software   | There is no    |
|  release                                        | need to specify|
|    o  A tag-generator plugin could help         | where the tags |
|      (i.e., a plugin for common development     | are stored in a|
|      environments.  NIST has something that     | vendor OS, as  |
|      plugs into Maven Build Environment)        | long as there  |
|                                                 | is a standards-|
|                                                 | based mechanism|
|                                                 | to retrieve    |
|                                                 | them.          |
|                                                 |-----------------
|                                                 | TCG RIM        |
--------------------------------------------------------------------
|  BIOS SWIDs might be hard to manage on an OS    |                |
|  disk-- maybe keep them in the BIOS flash?      | TCG RIM        |
|  o  Maybe a UEFI Var?  Would its name have to be|                |
|     specified by UEFI.org?                      |                |
|  o  How big is a BIOS SWID tag?  Do we need to  |                |
|     use a tag ID instead of an actual tag?      |                |
|  o  Note that the presence of Option ROMs turns |                |
|     the BIOS reference measurements into a      |                |
|     multi-vendor interoperability problem       |                |
--------------------------------------------------------------------
|  Use PC Client measurement definitions as a     | TCG PC Client  |
|  starting point to define the use of PCRs       | BIOS           |
|  (although Windows  OS is rare on Networking    |-----------------
|  Equipment)                                     | There have been|
|                                                 | proposals for  |
|                                                 | non-PC-Client  |
|                                                 | allocation of  |
|                                                 | PCRs, although |
|                                                 | no specific    |
|                                                 | document exists|
|                                                 | yet.           |
--------------------------------------------------------------------
|  Use TAP to retrieve measurements               |                |
|    o  Map TAP to SNMP                           | TCG SNMP MIB   |
|    o  Map to YANG                               | YANG Module for|
|    o  Complete Canonical Log Format             |   Basic        |
|                                                 |   Attestation  |
|                                                 | TCG Canonical  |
|                                                 |   Log Format   |
--------------------------------------------------------------------
| Posture Collection Server (as described in IETF |                |
|  SACMs ECP) would have to request the           |                |
|  attestation and analyze the result             |                |
| The Management application might be broken down |                |
|  to several more components:                    |                |
|    o  A Posture Manager Server                  |                |
|       which collects reports and stores them in |                |
|       a database                                |                |
|    o  One or more Analyzers that can look at the|                |
|       results and figure out what it means.     |                |
--------------------------------------------------------------------
~~~~
{: #Component-Status title='Component Status' artwork-align="left"}

## Comparison with TCG PTS / IETF NEA

Some components of an Attestation system have been implemented for end-user
machines such as PCs and laptops. Figure 7 shows the corresponding protocol
stacks.

~~~~
+-----------------------+              +-------------------------+
|                       |              |                         |
|       Attester        |<-------------|        Verifier         |
|       (Device)        |------------->|   (Management Station)  |
|                       |      |       |                         |
+-----------------------+      |       +-------------------------+
                               |
           -------------------- --------------------
           |                                        |
---------------------------------- ---------------------------------
|Reference Integrity Measurements| |         Attestation           |
---------------------------------- ---------------------------------

--------------------------------------------------------------------
|         IETF Attestation Reference Interaction Diagram           |
-------------------------------------------------------------------

    .......................         --------------------------------
    . No Existing         .         |  TAPS (PTS2.0) Info Model and|
    . Reference Integrity .         |  Canonical Log Format        |
    . Measurement Manifest.         |                              |
    . Protocols Exist     .         --------------------------------
    .                     .
    .                     .        ---------------------- ----------
    .                     .        | YANG Attestation   | |IETF NEA|
    .                     .        | Module             | | Msg and|
    .                     .        | I-D.birkholz-yang- | | Attrib.|
    .                     .        | basic-remote-      | | for PA-|
    .                     .        | attestation        | | TNC    |
    .                     .        ---------------------- ----------
    .                     .        ---------------------- ----------
    .                     .        | XML, JSON, CBOR    | | PT-TLS |
    .                     .        ---------------------- | (for   |
    .                     .        ---------------------- |endpoint|
    .                     .        | NETCONF, RESTCONF, | |mcahines|
    .                     .        | COAP               | |        |
    .......................        ---------------------- ----------
    ----------------------------------------------------------------
    |                       TLS, SSH                               |
    ----------------------------------------------------------------
~~~~
{: #Attestation-for-End-User-Computers title='Attestation for End User Computers' artwork-align="left"}

# IANA Considerations {#IANA}

This memo includes no request to IANA.

# Security Considerations {#Security}

Attestation results from the RIV procedure are subject to a number of attacks:

* Keys may be compromised
* A counterfeit device may attempt to impersonate (spoof) a known authentic device
* Man-in-the-middle attacks may be used by a counterfeit device to attempt to deliver responses that originate in an actual authentic device
*Replay attacks may be attempted by a compromised device

Trustworthiness of RIV attestation depends strongly on the validity of keys used for identity and attestation reports.  RIV takes full advantage of TPM capabilities to ensure that results can be trusted.

Two sets of keys are relevant to RIV attestation

* A DevID key is used to certify the identity of the device in which the TPM is installed.
* An Attestation Key (AK) key signs attestation reports, (called 'quotes' in TCG documents), used to provide evidence for integrity of the software on the device.

TPM practices require that these keys be different, as a way of ensuring that a general-purpose signing key cannot be used to spoof an attestation quote.

In each case, the private half of the key is known only to the TPM, and cannot be 
retrieved externally, even by a trusted party.  To ensure that's the case, 
private/public key-pairs are usually generated inside the TPM, where they're never 
exposed, and cannot be extracted.  Although TPM 2.0 has mechanisms 
to "inject" externally-generated keys, those keys are marked as such, so the 
device owner can exercise judgement in deciding if they're trustworthy.

Keeping keys safe is just part attestation security; knowing which keys are bound 
to the device in question is just as important.

While there are many ways to manage keys in a TPM (See TPM2Keys doc), RIV includes 
support for "zero touch" provisioning (also known as zero-touch onboarding) of fielded 
devices [e.g. KentW's sZTP], where keys which have predictable trust properties are
provisioned by the device vendor.

Device identity in RIV is based on IEEE 802.1AR DevID. This specification provides several elements

* A DevID requires a unique key pair for each device, accompanied by an x.509 certificate
* The private portion of the DevID key is to be stored in the device, in a manner that provides confidentiality (Section 6.2.5 [IEEE802.1AR])

The x.509 certificate contains several components

* The public part of the unique DevID key assigned to that device 
* An identifying string that's unique to the manufacturer of the device.  This is normally the serial number of the unit, which might also be printed on label on the device.
* The certificate must be signed by a key traceable to the manufacturer's root key.

With these elements, the device's manufacturer and serial number can be identified by analyzing the DevID certificate, and the device can prove it's the legitimate holder of the cert by signing a nonce with its private key in response to a challenge.

RIV uses the DevID to validate a TLS connection to the device as the attestation session begins.  Security of this process derives from TLS security, with the DevID providing proof that the TLS session terminates on the intended device. [xref].

Evidence of software integrity is delivered in the form of a quote signed by the TPM 
itself.  Because the contents of the quote are signed inside the TPM, any external
modification (including reformatting to a different data format) will be detected
as tampering.

To prevent spoofing, the quote generated inside the TPM must by signed by 
a key that's different from the DevID, called an Attestation Key (AK).  But the 
binding between the AK and the same device must also be proven to 
prevent a man-in-the-middle attack (e.g. [Asokan]).








This is accomplished in RIV through use of an AK certificate with the same elements as the DevID (i.e., same manufacturer's serial number, signed by the same manufacturer's key), but containing the device's unique AK public key instead of the DevID public key.

These two keys and certificates are used together:

* The DevID is used to validate a TLS connection terminating on the device with a known serial number.
* The AK is used to sign attestation quotes, providing proof that the attestation evidence comes from the same device.

Replay attacks of attestation results are usually ensured by inclusion of a nonce in the request to the TPM for a quote.  The resulting quote signed by the TPM contains the nonce, allowing the verifier to determine freshness, i.e., that the resulting quote was generated in response to the verifier's specific request.  Time-Based Uni-directional Attestation [TUDA] provides an alternate mechanism to verify freshness without requiring a request/response cycle.

Requiring results of attestation of the operating software to be signed by a key known only to the TPM also removes the need to trust the device's operating software (beyond the first measurement; see below); any changes to the quote made by malicious device software, or in the path back to the verifier, will invalidate the signature on the quote.

Although RIV recommends that device manufacturers pre-provision devices with easily-verified DevID and AK certs, use of those credentials is not mandatory.  IEEE 802.1AR incorporates the idea of an Initial Device ID (IDevID), provisioned by the manufacturer, and a Local Device ID (LDevID) provisioned by the owner of the device.  RIV extends that concept by defining an Initial Attestation Key (IAK) and Local Attestation Key (LAK) with the same properties.

Device owners can use any method to provision the Local credentials.

* TCG doc [Tom's DevID; also Stan's Provisioning Doc] shows how the initial Attestation 
keys can be used to certify LDevID and LAK keys.  Use of the LDevID and LAK allows the device owner to use a uniform identity structure across device types from multiple manufacturers (in the same way that an "Asset Tag" is used by many enterprises use to identify devices they own).
* But device owners can use any other mechanism they want to assure themselves that Local identity certificates are inserted into the intended device, including physical inspection and programming in a secure location, if they prefer to avoid placing trust in the manufacturer-provided keys.

Clearly, Local keys can't be used for secure Zero Touch provisioning; installation of the Local keys can only be done by some process that runs before the device is configured for network operation.

On the other end of the device life cycle, provision should be made to wipe Local keys when a device is decommissioned, to indicate that the device is no longer owned by the enterprise.  The manufacturer's Initial identity keys must be preserved, as they contain no information that's not already printed on the device's serial number plate.

In addition to trustworthy provisioning of keys, RIV depends on other trust anchors

* Secure identity depends on mechanisms to prevent per-device secret keys from being compromised.  The TPM provides this capability as a Root of Trust for Storage
* Attestation depends on an unbroken chain of measurements, starting from the very first measurement.  That first measurement is made by code called the Root of Trust for Measurement, typically done by trusted firmware stored in boot flash.  Mechanisms for maintaining the trustworthiness of the RTM are out of scope for RIV, but could include immutable firmware, signed updates, or a vendor-specific hardware verification technique.
* RIV assumes some level of physical defense for the device.  If a TPM that has already been programmed with an authentic DevID is stolen and inserted into a counterfeit device, attestation of that counterfeit device may become indistinguishable from an authentic device.

RIV also depends on reliable reference measurements, as expressed by the RIM [xref].  The definition of trust procedures for RIMs is out of scope for RIV, and the device owner is free to use any policy to validate a set of reference measurements.  RIMs may be conveyed out-of-band or in-band, as part of the attestation process (see Section XX).  But for embedded devices, where software is usually shipped as a self-contained package, RIMs signed by the manufacturer and delivered in-band may be more convenient for the device owner.


--- back
