# F5 Secure Cloud Declarative Onboarding

[F5 Declarative onboarding](https://github.com/F5Networks/f5-declarative-onboarding) uses a declarative model to initially configure a BIG-IP device with all of the required settings to get up and running. This includes system settings such as licensing and provisioning, network settings such as VLANs and Self IPs, and clustering settings if you are using more than one BIG-IP system.

## Documentation

For the documentation on Declarative Onboarding, including download, installation, and usage instructions, see the Declarative Onboarding [User Guide](https://clouddocs.f5.com/products/extensions/f5-declarative-onboarding/latest).

## Unclass STIG Example

* [Unclass STIG Baseline](https://github.com/Mikej81/f5-securecloud-DO/blob/master/source/U_STIG_Baseline.json) This covers a good portion of required configuration items for STIGS / SRGS tied to DODIN APL.

## NIST 800-53 Example

* [NIST 800-53 Baseline](https://github.com/Mikej81/f5-securecloud-DO/blob/master/source/NIST_800_53_Baseline.json)  This covers the currently supported items in DO for 800-53.  Remote Auth is supported but not included currently.  The goal is to have parity and take over for the NIST 800-53 iApp.  [Reference Deployment Guide](https://www.f5.com/services/resources/deployment-guides/nist-sp-800-53r4-compliance)

## Terraform Template Example

* [Terraform PAYG Baseline](https://github.com/Mikej81/f5-securecloud-DO/blob/master/dist/terraform/latest/payg_cluster.json) This covers the current supported items in DO for STIG and is built around use within IaC tools within a template.

* [Terraform BYOL Baseline](https://github.com/Mikej81/f5-securecloud-DO/blob/master/dist/terraform/latest/byol_cluster.json)

## Filing Issues

If you find an issue, we would love to hear about it.
You have a choice when it comes to filing issues:

* Use the **Issues** link on the GitHub menu bar in this repository for items such as enhancement or feature requests and non-urgent bug fixes. Tell us as much as you can about what you found and how you found it.