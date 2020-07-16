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

The [Unclassified STIG Baseline](https://github.com/Mikej81/f5-securecloud-DO/blob/master/dist/general/U_STIG_Baseline.json) covers a good portion of required configuration items for STIGS / Secuity Requirements Guides (SRGs) tied to the Approved Product List.

This template has a heavy focus on port and service lockdown, and cipher security.

```json
        "sshd": {
            "class": "SSH",
            "banner": "You are accessing a U.S. Government (USG) Information System (IS) that is provided for USG-authorized use only. By using this IS (which includes any device attached to this IS), you consent to the following conditions: The USG routinely intercepts and monitors communications on this IS for purposes including, but not limited to, penetration testing, COMSEC monitoring, network operations and defense, personnel misconduct (PM), law enforcement (LE), and counterintelligence (CI) investigations. At any time, the USG may inspect and seize data stored on this IS. Communications using, or data stored on, this IS are not private, are subject to routine monitoring, interception, and search, and may be disclosed or used for any USG authorized purpose. This IS includes security measures (e.g., authentication and access controls) to protect USG interests--not for your personal benefit or privacy. Notwithstanding the above, using this IS does not constitute consent to PM, LE or CI investigative searching or monitoring of the content of privileged communications, or work product, related to personal representation or services by attorneys, psychotherapists, or clergy, and their assistants. Such communications and work product are private and confidential. See User Agreement for details.",
            "inactivityTimeout": 900,
            "ciphers": [
                "aes128-ctr",
                "aes192-ctr",
                "aes256-ctr"
            ],
            "logingraceTime": 60,
            "MACS": [
                "hmac-sha1",
                "hmac-ripemd160"
            ],
            "maxAuthTries": 3,
            "maxStartups": "5",
            "protocol": 2
        }
```

## [NIST 800-53 Example](https://nvd.nist.gov/800-53)

The [NIST 800-53 Baseline](https://github.com/Mikej81/f5-securecloud-DO/blob/master/dist/general/NIST_800_53_Baseline.json)  covers the currently supported items in DO for 800-53.  The goal is to have parity and take over for the NIST 800-53 iApp.  [Reference Deployment Guide](https://www.f5.com/services/resources/deployment-guides/nist-sp-800-53r4-compliance)

This template has a heavier focus on security controls and remote authentication security.

```json
{
    "schemaVersion": "1.0.0",
    "class": "Device",
    "async": true,
    "label": "BIG-IP NIST 800-53 Declarative Onboarding",
    "Common": {
        "class": "Tenant",
        "myAuth": {
            "class": "Authentication",
            "enabledSourceType": "radius",
            "fallback": true,
            "remoteUsersDefaults": {
                "partitionAccess": "all",
                "terminalAccess": "tmsh",
                "role": "resource-admin"
            },
            "radius": {
                "serviceType": "call-check",
                "servers": {
                    "primary": {
                        "server": "1.2.3.4",
                        "port": 1811,
                        "secret": "mySecret"
                    },
                    "secondary": {
                        "server": "my.second.server",
                        "secret": "anotherSecret",
                        "port": 1888
                    }
                }
            }
        }
    }
```

## Terraform Template Example

These example templates cover the current supported items in **DO** for STIGs and they are built around use within terraform as [templates_files](https://registry.terraform.io/providers/hashicorp/template/latest/docs/data-sources/file).

* [Terraform PAYG Baseline](https://github.com/Mikej81/f5-securecloud-DO/blob/master/dist/terraform/latest/payg_cluster.json)

* [Terraform BYOL Baseline](https://github.com/Mikej81/f5-securecloud-DO/blob/master/dist/terraform/latest/byol_cluster.json)

### Terraform Usage

```hcl
data http template {
  url = "https://raw.githubusercontent.com/Mikej81/f5-securecloud-DO/master/dist/terraform/latest/payg_cluster.json"
}

data template_file vm01_do_json {
  template = "${data.http.template.body}"
  vars = {
    host1           = var.host1_name
    host2           = var.host2_name
    local_host      = var.host1_name
    local_selfip    = var.f5vm01ext
    remote_host     = var.host2_name
    remote_selfip   = var.f5vm02ext
    externalGateway = local.ext_gw
    mgmtGateway     = local.mgmt_gw
    dns_server      = var.dns_server
    ntp_server      = var.ntp_server
    timezone        = var.timezone
    admin_user      = var.adminUserName
    admin_password  = var.adminPassword
    license         = var.licenses["license1"] != "" ? var.licenses["license1"] : ""
  }
}
```

## Filing Issues

If you find an issue, we would love to hear about it.
You have a choice when it comes to filing issues:

* Use the **Issues** link on the GitHub menu bar in this repository for items such as enhancement or feature requests and non-urgent bug fixes. Tell us as much as you can about what you found and how you found it.
