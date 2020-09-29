
# Minimum guardrails for Government of Canada's cloud operationalization framework
https://canada-ca.github.io/cloud-guardrails/
(https://github.com/canada-ca/cloud-guardrails)
    ID.	Guardrail
    01	Protect root / global admins account
    02	Management of administrative privileges
    03	Cloud console access
    04	Enterprise monitoring accounts
    05	Data location
    06	Protection of data-at-rest
    07	Protection of data-in-transit
    08	Segment and separate
    09	Network security services
    10	Cyber defense services
    11	Logging and monitoring
    12	Configuration of cloud marketplaces


How this F5 solution complies with these guardrails...

# 01 Protect Root / Global Admins Account
- Implement multi-factor authentication (MFA) mechanism for root/master account.
- Implement a mechanism for enforcing access authorizations.
- Configure appropriate alerts on root/master accounts to detect a potential compromise, in accordance with the GC Event Logging Guidance
    Validation
    - Confirm policy for MFA is enabled through screenshots and compliance reports.
    Additional Considerations
    - Leverage enterprise services such as Administrative Access Control System (AACS) for Privileged Access Management (PAM), Attribute-based access control (ABAC).
    References
    - SPIN 2017-01, subsection 6.2.3
    - CSE Top 10 #3 (https://cyber.gc.ca/en/top-10-it-security-actions)
    - Refer to the Recommendations for Two-Factor User Authentication Within the Government of Canada Enterprise Domain
    - Refer to the following template for an example of a break glass emergency account management procedure.
    - Refer to the GC Event Logging Guidance
    - Related security controls: AC‑2, AC‑2(1), AC‑3, AC‑5, AC‑6, AC‑6(5), AC‑6(10), AC‑7, AC‑9, AC‑19, AC‑20(3), IA‑2, IA‑2(1), IA‑2(2), IA‑2(11), IA‑4, IA‑5, IA‑5(1), IA‑5(6), IA‑5(7), IA‑5(13), IA‑6, IA‑8

How this F5 solution complies with these guardrails...


# 07 Protection of Data-in-Transit
Objective: 
- Protect data transiting networks through the use of appropriate encryption and network safeguards.
Key Considerations
- Implement an encryption mechanism to protect the confidentiality and integrity of data when data are in transit to and from your solution.
- Use CSE-approved cryptographic algorithms and protocols.
- Encryption of data in transit by default (e.g. TLS v1.2, etc.) for all publicly accessible sites and external communications as per the direction on Implementing HTTPS for Secure Web Connections (ITPIN 2018-01).
- Encryption for all access to cloud services (e.g. Cloud storage, Key Management systems, etc.).
- Consider encryption for internal zone communication in the cloud based on risk profile and as per the direction in CCCS network security zoning guidance in ITSG-22 and ITSG-38.
- Implement key management procedures.
    Validation
    - Confirm policy for secure network transmission.
    Applicable Service Models
    - IaaS, PaaS, SaaS
    References
    1. SPIN 2017-01, subsection 6.2.4
    2. ITPIN 2018-01
    3. Refer to the cryptography guidance in 40.111 and 40.062.
    4. Refer to the network security zoning guidance in ITSG-22 and ITSG-38.
    5. Refer to the guidance in Considerations for Cryptography in Commercial Cloud Services.
    6. Related security controls: SC‑8, SC‑8(1), SC‑12, SC‑13, SC‑17

## How this F5 solution complies with guardrail 07:
In accordance with ITPIN 2018-01, ITSG-22 and ITSG-38, TLS cryptography is implemented with CSE-approved cryptographic algorithms and protocols to encrypt and protect the confidentiality and integrity of data when data are in transit to and from this F5 solution.
- [ ] add command with sample output showing the ciphers in use for the F5 virtual server, highlighting the fact that TLSv1.1 is not permitted?
- [ ] add reference or list of CSE-approved cryptographic algorithms and protocols.
- [ ] add reference to key management processes and procedures
- [ ] highlight how all external and management interfaces of the cloud-based service are identified and appropriately protected
