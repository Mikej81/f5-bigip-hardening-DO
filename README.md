# BIG-IP Secure Cloud Architecture Hardening Declarative Onboarding Examples

* [Introduction](#introduction)
  * [What is Secure Cloud Architecture?](#What-is-Secure-Cloud-Architecture)
  * [What is Declarative Onboarding?](#What-is-Declarative-Onboarding)
    * [Declarative Onboarding Documentation](#Declarative-Onboarding-Documentation)
* [Department of Defense Unclassified Security Technical Implementation Guide (STIG) Example](#Department-of-Defense-Unclassified-Security-Technical-Implementation-Guide-(STIG)-Example)
* [NIST 800-53 Example](#NIST-800-53-Example)
* [Terraform Template Example](#Terraform-Template-Example)
  * [Terraform Usage](#Terraform-Usage)
* [Filing Issues](#Filing-Issues)

## Introduction

### What is Secure Cloud Architecture

Secure Cloud Architecture is valdiated pattern from Secure / Cloud Architects within F5 that brings together robustness, depth of security, and visibility to the modern datacenter with the agility and service-based model of the public cloud.  

It’s built on a foundation of advanced app services that enable the automatable security, performance, and visibility of the entire data path to the application.

### What is Declarative Onboarding

[F5 Declarative Onboarding](https://github.com/F5Networks/f5-declarative-onboarding) (**DO**) uses a declarative model to initially configure a BIG-IP device with all of the required settings to get up and running. This includes system settings such as licensing and provisioning, network settings such as VLANs and Self IPs, and clustering settings if you are using more than one BIG-IP system.

### Declarative Onboarding Documentation

For the documentation on Declarative Onboarding, including download, installation, and usage instructions, see the Declarative Onboarding [User Guide](https://clouddocs.f5.com/products/extensions/f5-declarative-onboarding/latest).

## [Department of Defense Unclassified Security Technical Implementation Guide (STIG) Example](https://public.cyber.mil/stigs/downloads/)

* [Unclassified STIG Baseline](https://github.com/Mikej81/f5-securecloud-DO/blob/master/dist/general/U_STIG_Baseline.json) This covers a good portion of required configuration items for STIGS / Secuity Requirements Guides (SRGs) tied to the Approved Product List.

## [NIST 800-53 Example](https://nvd.nist.gov/800-53)

* [NIST 800-53 Baseline](https://github.com/Mikej81/f5-securecloud-DO/blob/master/dist/general/NIST_800_53_Baseline.json)  This covers the currently supported items in DO for 800-53.  Remote Auth is supported but not included currently.  The goal is to have parity and take over for the NIST 800-53 iApp.  [Reference Deployment Guide](https://www.f5.com/services/resources/deployment-guides/nist-sp-800-53r4-compliance)

## Terraform Template Example

These example templates cover the current supported items in **DO** for STIGs and they are built around use within terraform as [templates_files](https://registry.terraform.io/providers/hashicorp/template/latest/docs/data-sources/file).

* [Terraform PAYG Baseline](https://github.com/Mikej81/f5-securecloud-DO/blob/master/dist/terraform/latest/payg_cluster.json)

* [Terraform BYOL Baseline](https://github.com/Mikej81/f5-securecloud-DO/blob/master/dist/terraform/latest/byol_cluster.json)

### Terraform Usage

![TF Example](/img/tf_example.png)

## Filing Issues

If you find an issue, we would love to hear about it.
You have a choice when it comes to filing issues:

* Use the **Issues** link on the GitHub menu bar in this repository for items such as enhancement or feature requests and non-urgent bug fixes. Tell us as much as you can about what you found and how you found it.
