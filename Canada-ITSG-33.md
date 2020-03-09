# Canada ITSG Security Control Compliancy
Annex 3A - Security Control Catalogue (ITSG-33)
( https://cyber.gc.ca/en/guidance/annex-3a-security-control-catalogue-itsg-33, equivalent to NIST: https://nvd.nist.gov/800-53 )

## 3.1 FAMILY: ACCESS CONTROL
### AC-2 ACCOUNT MANAGEMENT
#### AC-2(1) ACCOUNT MANAGEMENT | AUTOMATED SYSTEM ACCOUNT MANAGEMENT
This F5 solution employs automated mechanisms to support the management of information system accounts.
Authentication and authorization of all information system accounts is done via their directory service, including accounts used to access the individual infrastructure components of the solution such as the F5 appliances, the servers and the firewalls, as well as for access to the applications serviced and contained within this infrastructure.
When users are terminated or transferred, the F5 solution automatically and immediately reflects the change in authorization for the corresponding accounts and enforces the corresponding actions (authorize or deny access).
The F5 solution captures audit and logging reports detailing the account usage.

#### AC-2(2) ACCOUNT MANAGEMENT | REMOVAL OF TEMPORARY / EMERGENCY ACCOUNTS
This F5 solution automatically disables temporary and emergency accounts that have expired without requiring the intervention of a systems administrator. This is accomplished by leveraging the directory service attributes that identify the status of each account and by programing the desired logic in the F5 Visual Policy Editor, such as setting the appropriate expiry time for the authorized access after the temporary or emergency account has been successfully authorized, and this is enforced for access to the individual infrastructure components of the solution such as the F5 appliances, the servers and the firewalls, as well as for access to the applications serviced and contained within this infrastructure.

#### AC-2(3) ACCOUNT MANAGEMENT | DISABLE INACTIVE ACCOUNTS
This F5 solution automatically disables inactive accounts after the defined time period has elapsed.
This is accomplished by leveraging the directory service attributes that identify the last successful login of each account and by programing the desired logic in the F5 Visual Policy Editor to automatically deny access to an account that has been inactive for longer than the defined time period after the account has been successfully authorized, and this is enforced for access to the individual infrastructure components of the solution such as the F5 appliances, the servers and the firewalls, as well as for access to the applications serviced and contained within this infrastructure.

#### AC-2(5) ACCOUNT MANAGEMENT | INACTIVITY LOGOUT
This F5 solution automatically logs out users when the defined time-period of inactivity has elapsed.
This is accomplished by configuration of the "Inactivity Timeout" setting in the Access policy and is enforced for access to the individual infrastructure components of the solution such as the F5 appliances, the servers and the firewalls, as well as for access to the applications serviced and contained within this infrastructure.

#### AC-2(6) ACCOUNT MANAGEMENT | DYNAMIC PRIVILEGE MANAGEMENT
This F5 solution automatically, dynamically and immediately enforces access controls continuously over the entire duration of a user's authorized session. This is also commonly referred to as the "Zero Trust" access model. The solution also enforces "step-up authentication" to dynamically adjust the privileges of users based on any number of parameters, including time of day, sub-systems they are attempting to access, or changes in their device's posture, such as disabling their client anti-virus software or becoming infected with malware, and allows for the encryption of the communications to be changed, including changing the encryption keys and requesting client-provided certificate authentication, also referred to as "mutual authentication". This is accomplished with the configuration of the corresponding logic in the F5 access policy definition and is enforced for access to the individual infrastructure components of the solution such as the F5 appliances, the servers and the firewalls, as well as for access to the applications serviced and contained within this infrastructure.

#### AC-2(7) ACCOUNT MANAGEMENT | ROLE-BASED SCHEMES
This F5 solution automatically, dynamically and continually enforces access controls continuously over the entire duration of a user's authorized session and in accordance with the user's assigned roles, as defined in their directory service by the organization. Accordingly, the F5 solution grants or denies access for privileged user accounts as applicable and as defined by the organization. When privileged role assignments change and access becomes no longer appropriate, the F5 solution denies access. This is accomplished with the configuration of the corresponding logic in the F5 access policy definition and is enforced for access to the individual infrastructure components of the solution such as the F5 appliances, the servers and the firewalls, as well as for access to the applications serviced and contained within this infrastructure.

#### AC-2(8) ACCOUNT MANAGEMENT | DYNAMIC ACCOUNT CREATION
This F5 solution federates identity and authorization of accounts with their directory service to dynamically create information system accounts for entities that were previously unknow. This is accomplished with the configuration of the corresponding logic in the F5 access policy definition and is enforced for access to the individual infrastructure components of the solution such as the F5 appliances, the servers and the firewalls, as well as for access to the applications serviced and contained within this infrastructure.

#### AC-2(9) ACCOUNT MANAGEMENT | RESTRICTIONS ON USE OF SHARED GROUPS / ACCOUNTS
This F5 solution only allows access for shared/group accounts that meet the conditions as defined by the organization in their directory service. This is accomplished with the configuration of the corresponding logic in the F5 access policy definition and is enforced for access to the individual infrastructure components of the solution such as the F5 appliances, the servers and the firewalls, as well as for access to the applications serviced and contained within this infrastructure.

#### AC-2(11) ACCOUNT MANAGEMENT | USAGE CONDITIONS
This F5 solution enforces circumstances and/or usage conditions for information system accounts as defined by the organization in their directory service, including restricting usage to certain days of the week, time of day or specific durations of time. This is accomplished with the configuration of the corresponding logic in the F5 access policy definition and is enforced for access to the individual infrastructure components of the solution such as the F5 appliances, the servers and the firewalls, as well as for access to the applications serviced and contained within this infrastructure.

#### AC-2(12) ACCOUNT MANAGEMENT | ACCOUNT MONITORING / ATYPICAL USAGE
This F5 solution monitors and reports information system accounts for atypical use as defined by the organization, including attempts to access at certain times of the day and from locations that are not consistent with the normal usage patterns of individuals working in organizations. This is accomplished with the configuration of the corresponding logic in the F5 access policy definition and is enforced for access to the individual infrastructure components of the solution such as the F5 appliances, the servers and the firewalls, as well as for access to the applications serviced and contained within this infrastructure.

#### AC-2(13) ACCOUNT MANAGEMENT | DISABLE ACCOUNTS FOR HIGH-RISK INDIVIDUALS
This F5 solution disables access for accounts immediately upon the organization identifying in their directory service that the corresponding user poses a significant risk. This is accomplished with the configuration of the corresponding logic in the F5 access policy definition and is enforced for access to the individual infrastructure components of the solution such as the F5 appliances, the servers and the firewalls, as well as for access to the applications serviced and contained within this infrastructure.

### AC-3 ACCESS ENFORCEMENT
#### AC-3(2) ACCESS ENFORCEMENT | DUAL AUTHORIZATION
This F5 solution enforces dual authorization, also known as two-person control, for organization-defined privileged commands and/or actions. This is accomplished with the configuration of the corresponding logic in the F5 access policy definition, including notification of request for authorization to the two persons, and is enforced for access to the individual infrastructure components of the solution such as the F5 appliances, the servers and the firewalls, as well as for access to the applications serviced and contained within this infrastructure.

#### AC-3(3) ACCESS ENFORCEMENT | MANDATORY ACCESS CONTROL
This F5 solution enforces… 

The information system enforces [Assignment: organization-defined mandatory access control policies] over all subjects and objects where the policy specifies that:

The policy is uniformly enforced across all subjects and objects within the boundary of the information system;
A subject that has been granted access to information is constrained from doing any of the following;
Passing the information to unauthorized subjects or objects;
Granting its privileges to other subjects;
Changing one or more security attributes on subjects, objects, the information system, or information system components;
Choosing the security attributes and attribute values to be associated with newly created or modified objects; or
Changing the rules governing access control; and
[Assignment: Organized-defined subjects] may explicitly be granted [Assignment: organization-defined privileges (i.e., they are trusted subjects)] such that they are not limited by some or all of the above constraints.
Enhancement Supplemental Guidance Mandatory access control as defined in this control enhancement is synonymous with nondiscretionary access control, and is not constrained only to certain historical uses (e.g., implementations using the Bell-LaPadula Model). The above class of mandatory access control policies constrains what actions subjects can take with information obtained from data objects for which they have already been granted access, thus preventing the subjects from passing the information to unauthorized subjects and objects. This class of mandatory access control policies also constrains what actions subjects can take with respect to the propagation of access control privileges; that is, a subject with a privilege cannot pass that privilege to other subjects. The policy is uniformly enforced over all subjects and objects to which the information system has control. Otherwise, the access control policy can be circumvented. This enforcement typically is provided via an implementation that meets the reference monitor concept (see AC-25). The policy is bounded by the information system boundary (i.e., once the information is passed outside of the control of the system, additional means may be required to ensure that the constraints on the information remain in effect). The trusted subjects described above are granted privileges consistent with the concept of least privilege (see AC-6). Trusted subjects are only given the minimum privileges relative to the above policy necessary for satisfying organizational mission/business needs. The control is most applicable when there is a mandate (e.g., law, Executive Order, directive, or regulation) that establishes a policy regarding access to sensitive/classified information and that some users of the information system are not authorized access to all sensitive/classified information resident in the information system. This control can operate in conjunction with AC-3 (4). A subject that is constrained in its operation by policies governed by this control is still able to operate under the less rigorous constraints of AC-3 (4), but policies governed by this control take precedence over the less rigorous constraints of AC-3 (4). For example, while a mandatory access control policy imposes a constraint preventing a subject from passing information to another subject operating at a different sensitivity label, AC-3 (4) permits the subject to pass the information to any subject with the same sensitivity label as the subject. Related controls: AC-25, SC-11.

#### AC-3(4) ACCESS ENFORCEMENT | DISCRETIONARY ACCESS CONTROL
This F5 solution enforces… 

The information system enforces [Assignment: organization-defined discretionary access control policies] over defined subjects and objects where the policy specifies that a subject that has been granted access to information can do one or more of the following:

Pass the information to any other subjects or objects;
Grant its privileges to other subjects;
Change security attributes on subjects, objects, the information system, or the information system’s components;
Choose the security attributes to be associated with newly created or revised objects; or
Change the rules governing access control.
Enhancement Supplemental Guidance: When discretionary access control policies are implemented, subjects are not constrained with regard to what actions they can take with information for which they have already been granted access. Thus, subjects that have been granted access to information are not prevented from passing (i.e., the subjects have the discretion to pass) the information to other subjects or objects. This control enhancement can operate in conjunction with AC-3 (3). A subject that is constrained in its operation by policies governed by AC-3 (3) is still able to operate under the less rigorous constraints of this control enhancement. Thus, while AC-3 (3) imposes constraints preventing a subject from passing information to another subject operating at a different sensitivity level, AC-3 (4) permits the subject to pass the information to any subject at the same sensitivity level. The policy is bounded by the information system boundary. Once the information is passed outside of the control of the information system, additional means may be required to ensure that the constraints remain in effect. While the older, more traditional definitions of discretionary access control require identity-based access control, that limitation is not required for this use of discretionary access control.

#### AC-3(5) ACCESS ENFORCEMENT | SECURITY-RELEVANT INFORMATION
This F5 solution prevents access to organization-defined security-relevant information except during secure, non-operable system states. This is accomplished with the configuration of the corresponding logic in the F5 access policy definition, including configuration of services such as SSH and RDP gateway to access the security-relevant information in a secure manner, and is enforced for access to the individual infrastructure components of the solution such as the F5 appliances, the servers and the firewalls, as well as for access to the applications serviced and contained within this infrastructure.

#### AC-3(7) ACCESS ENFORCEMENT | ROLE-BASED ACCESS CONTROL
This F5 solution enforces a role-based access control policy over defined subjects and objects and controls access based up organization-defined roles and users authorized to assume such roles, as defined in the organization's directory service. This is accomplished with the configuration of the corresponding logic in the F5 access policy definition and is enforced for access to the individual infrastructure components of the solution such as the F5 appliances, the servers and the firewalls, as well as for access to the applications serviced and contained within this infrastructure.

#### AC-3(8) ACCESS ENFORCEMENT | REVOCATION OF ACCESS AUTHORIZATIONS
This F5 solution enforces the revocation of access authorizations resulting from changes to the security attributes of subjects and objects based on organization-defined rules, immediately following the modification of the corresponding attributes defined in the organization's directory service or following the modification of the corresponding F5 access policy definition. This is accomplished with the configuration of the corresponding logic in the F5 access policy definition and is enforced for access to the individual infrastructure components of the solution such as the F5 appliances, the servers and the firewalls, as well as for access to the applications serviced and contained within this infrastructure.

#### AC-3(10) ACCESS ENFORCEMENT | AUDITED OVERRIDE OF ACCESS CONTROL MECHANISMS
This F5 solution automatically and continuously logs and provides audit reports when automated access control mechanisms are overridden under organization-defined conditions. This is accomplished with the configuration of the corresponding logic in the F5 access policy definition and is enforced for access to the individual infrastructure components of the solution such as the F5 appliances, the servers and the firewalls, as well as for access to the applications serviced and contained within this infrastructure.

### AC-4 INFORMATION FLOW ENFORCEMENT
#### AC-4(1) INFORMATION FLOW ENFORCEMENT | OBJECT SECURITY ATTRIBUTES
This F5 solution uses organization-defined security attributes associated with organization-defined information, source, and destination objects, as defined in their directory service and in the F5 Access policy definition, to enforce organization-defined information flow control policies. This is accomplished with the configuration of the corresponding logic in the F5 access policy definition and is enforced for access to the individual infrastructure components of the solution such as the F5 appliances, the servers and the firewalls, as well as for access to the applications serviced and contained within this infrastructure.

#### AC-4(2) INFORMATION FLOW ENFORCEMENT | PROCESSING DOMAINS
This F5 solution uses protected processing domains to enforce organization-defined information flow control policies as a basis for flow control decisions. This is accomplished with the configuration of the corresponding logic in the F5 access policy definition, F5 Route Domains, Azure Virtual Networks and Azure Network Security Groups and is enforced for access to the individual infrastructure components of the solution such as the F5 appliances, the servers and the firewalls, as well as for access to the applications serviced and contained within this infrastructure.

#### AC-4(3) INFORMATION FLOW ENFORCEMENT | DYNAMIC INFORMATION FLOW CONTROL
This F5 solution enforces dynamic information flow control based on organization-defined policies. This is accomplished with the configuration of the corresponding logic in the F5 access policy definition, including the detection of potentially harmful or adverse events such as of brute-force login attempts, and is enforced for access to the individual infrastructure components of the solution such as the F5 appliances, the servers and the firewalls, as well as for access to the applications serviced and contained within this infrastructure.

#### AC-4(4) INFORMATION FLOW ENFORCEMENT | CONTENT CHECK ENCRYPTED INFORMATION
This F5 solution prevents encrypted information from bypassing content-checking mechanisms by decrypting the information, blocking the flow of the encrypted information, terminating communications sessions attempting to pass encrypted information and/or applying any number of other organization-defined procedures or methods. This is accomplished with the configuration of the corresponding logic in the F5 SSL Orchestrator policy definition and is enforced for access to the individual infrastructure components of the solution such as the F5 appliances, the servers and the firewalls, as well as for access to the applications serviced and contained within this infrastructure.

#### AC-4(5) INFORMATION FLOW ENFORCEMENT | EMBEDDED DATA TYPES
This F5 solution enforces organization-defined limitations on embedding data types within other data types. This is accomplished with the configuration of the corresponding logic in the F5 SSL Orchestrator policy definition, which automatically scans the data contents and determines if other data types are embedded, and is enforced for access to the individual infrastructure components of the solution such as the F5 appliances, the servers and the firewalls, as well as for access to the applications serviced and contained within this infrastructure.

#### AC-4(6) INFORMATION FLOW ENFORCEMENT | METADATA
This F5 solution enforces information flow control based on organization-defined metadata. This is accomplished with the configuration of the corresponding logic in the F5 access policy definition, which reads the metadata information corresponding to the data being transmitted in each flow, and is enforced for access to the individual infrastructure components of the solution such as the F5 appliances, the servers and the firewalls, as well as for access to the applications serviced and contained within this infrastructure.

#### AC-4(8) INFORMATION FLOW ENFORCEMENT | SECURITY POLICY FILTERS
This F5 solution enforces information flow control using organization-defined security policy filters as a basis for flow control decisions for organization-defined information flows. This is accomplished with the configuration of the corresponding parameters and logic in the F5 WAF policy definition, and is enforced for access to the individual infrastructure components of the solution such as the F5 appliances, the servers and the firewalls, as well as for access to the applications serviced and contained within this infrastructure.

#### AC-4(9) INFORMATION FLOW ENFORCEMENT | HUMAN REVIEWS
This F5 solution enforces the use of human reviews for organization-defined information flows under organization-defined conditions. This is accomplished with the configuration of the corresponding parameters and logic in the F5 access and/or WAF policy definition, and is enforced for access to the individual infrastructure components of the solution such as the F5 appliances, the servers and the firewalls, as well as for access to the applications serviced and contained within this infrastructure.

#### AC-4(10) INFORMATION FLOW ENFORCEMENT | ENABLE / DISABLE SECURITY POLICY FILTERS
This F5 solution provides the capability for privileged administrators to enable/disable organization-defined security policy filters under organization-defined conditions. This is accomplished with the configuration of the corresponding parameters and logic in the F5 access and/or WAF policy definition, and is enforced for access to the individual infrastructure components of the solution such as the F5 appliances, the servers and the firewalls, as well as for access to the applications serviced and contained within this infrastructure.

#### AC-4(11) INFORMATION FLOW ENFORCEMENT | CONFIGURATION OF SECURITY POLICY FILTERS
This F5 solution provides the capability for privileged administrators to configure organization-defined security policy filters to support different security policies. This is accomplished with the configuration of the corresponding parameters and logic in the F5 access and/or WAF policy definition, and is enforced for access to the individual infrastructure components of the solution such as the F5 appliances, the servers and the firewalls, as well as for access to the applications serviced and contained within this infrastructure.

#### AC-4(12) INFORMATION FLOW ENFORCEMENT | DATA TYPE IDENTIFIERS
This F5 solution, when transferring information between different security domains, uses organization-defined data type identifiers to validate data essential for information flow decisions. This is accomplished with the configuration of the corresponding parameters and logic in the F5 access and/or WAF policy definition, and is enforced for access to the individual infrastructure components of the solution such as the F5 appliances, the servers and the firewalls, as well as for access to the applications serviced and contained within this infrastructure.

#### AC-4(13) INFORMATION FLOW ENFORCEMENT | DECOMPOSITION INTO POLICY-RELEVANT SUBCOMPONENTS
The information system, when transferring information between different security domains, decomposes information into [Assignment: organization-defined policy-relevant subcomponents] for submission to policy enforcement mechanisms.

Enhancement Supplemental Guidance: Policy enforcement mechanisms apply filtering, inspection, and/or sanitization rules to the policy-relevant subcomponents of information to facilitate flow enforcement prior to transferring such information to different security domains. Parsing transfer files facilitates policy decisions on source, destination, certificates, classification, attachments, and other security-related component differentiators.


### AC-5 SEPARATION OF DUTIES
### AC-6 LEAST PRIVILEGE
This F5 solution enables an external directory service to authenticate BIG-IP management users. The directory service may also store RBAC roles for users. (Even when you enable an external directory service, the BIG-IP system continues to support local user accounts.)
The default role for users not assigned a specific role by the remote directory service is "No Access" and as a result will be forbiden access even if succesfully authenticated.
Users do not have access to he TMSH (CLI) console by default.

### AC-7 UNSUCCESSFUL LOGIN ATTEMPTS
### AC-8 SYSTEM USE NOTIFICATION
### AC-9 PREVIOUS LOGON (ACCESS) NOTIFICATION
### AC-10 CONCURRENT SESSION CONTROL
### AC-11 SESSION LOCK
### AC-12 SESSION TERMINATION
### AC-13 SUPERVISION AND REVIEW — ACCESS CONTROL
### AC-14 PERMITTED ACTIONS WITHOUT IDENTIFICATION OR AUTHENTICATION
### AC-15 AUTOMATED MARKING
### AC-16 SECURITY ATTRIBUTES
### AC-17 REMOTE ACCESS
### AC-18 WIRELESS ACCESS
### AC-19 ACCESS CONTROL FOR MOBILE DEVICES
### AC-20 USE OF EXTERNAL INFORMATION SYSTEMS
### AC-21 USER-BASED COLLABORATION AND INFORMATION SHARING
### AC-22 PUBLICLY ACCESSIBLE CONTENT
### AC-23 DATA MINING PROTECTION
### AC-24 ACCESS CONTROL DECISIONS
### AC-25 REFERENCE MONITOR

## 3.2 FAMILY: AWARENESS AND TRAINING
### AT-1 SECURITY AWARENESS AND TRAINING POLICY AND PROCEDURES
### AT-2 SECURITY AWARENESS
### AT-3 ROLE BASED SECURITY TRAINING
### AT-4 SECURITY TRAINING RECORDS
### AT-5 CONTACTS WITH SECURITY GROUPS AND ASSOCIATIONS

## 3.3 FAMILY: AUDIT AND ACCOUNTABILITY
### AU-1 AUDIT AND ACCOUNTABILITY POLICY AND PROCEDURES
### AU-2 AUDITABLE EVENTS
### AU-3 CONTENT OF AUDIT RECORDS
### AU-4 AUDIT STORAGE CAPACITY
### AU-5 RESPONSE TO AUDIT PROCESSING FAILURES
### AU-6 AUDIT REVIEW, ANALYSIS, AND REPORTING
### AU-7 AUDIT REDUCTION AND REPORT GENERATION
### AU-8 TIME STAMPS
### AU-9 PROTECTION OF AUDIT INFORMATION
### AU-10 NON-REPUDIATION
### AU-11 AUDIT RECORD RETENTION
### AU-12 AUDIT GENERATION
### AU-13 MONITORING FOR INFORMATION DISCLOSURE
### AU-14 SESSION AUDIT
### AU-15 ALTERNATE AUDIT CAPABILITY
### AU-16 CROSS-ORGANIZATIONAL AUDITING

## 3.4 FAMILY: SECURITY ASSESSMENT AND AUTHORIZATION
### CA-1 SECURITY ASSESSMENT AND AUTHORIZATION POLICIES AND PROCEDURES
### CA-2 SECURITY ASSESSMENTS
### CA-3 INFORMATION SYSTEM CONNECTIONS
### CA-4 SECURITY CERTIFICATION
### CA-5 PLAN OF ACTION AND MILESTONES
### CA-6 SECURITY AUTHORIZATION
### CA-7 CONTINUOUS MONITORING
### CA-8 PENETRATION TESTING
### CA-9 INTERNAL SYSTEM CONNECTIONS

## 3.5 FAMILY: CONFIGURATION MANAGEMENT
### CM-1 CONFIGURATION MANAGEMENT POLICY AND PROCEDURES
### CM-2 BASELINE CONFIGURATION
### CM-3 CONFIGURATION CHANGE CONTROL
### CM-4 SECURITY IMPACT ANALYSIS
### CM-5 ACCESS RESTRICTIONS FOR CHANGE
This F5 solution enforces a role-based access control policy over defined subjects and objects and controls access based up organization-defined roles and users authorized to assume such roles, as defined in the organization's directory service. This is accomplished with the configuration of the corresponding logic in the F5 access policy definition and is enforced for access to the individual infrastructure components of the solution such as the F5 appliances, the servers and the firewalls, as well as for access to the applications serviced and contained within this infrastructure.

### CM-6 CONFIGURATION SETTINGS
### CM-7 LEAST FUNCTIONALITY
### CM-8 INFORMATION SYSTEM COMPONENT INVENTORY
### CM-9 CONFIGURATION MANAGEMENT PLAN
### CM-10 SOFTWARE USAGE RESTRICTIONS
### CM-11 USER INSTALLED SOFTWARE

## 3.6 FAMILY: CONTINGENCY PLANNING (CONTINUITY PLANNING)
### CP-1 CONTINGENCY PLANNING POLICY AND PROCEDURES
### CP-2 CONTINGENCY PLAN
### CP-3 CONTINGENCY TRAINING
### CP-4 CONTINGENCY PLAN TESTING AND EXERCISES
### CP-5 CONTINGENCY PLAN UPDATE
### CP-6 ALTERNATE STORAGE SITE
### CP-7 ALTERNATE PROCESSING SITE
### CP-8 TELECOMMUNICATIONS SERVICES
### CP-9 INFORMATION SYSTEM BACKUP
### CP-10 INFORMATION SYSTEM RECOVERY AND RECONSTITUTION
### CP-11 ALTERNATE COMMUNICATIONS PROTOCOLS
### CP-12 SAFE MODE
### CP-13 ALTERNATIVE SECURITY MECHANISMS

## 3.7 FAMILY: IDENTIFICATION AND AUTHENTICATION
### IA-1 IDENTIFICATION AND AUTHENTICATION POLICY AND PROCEDURES
### IA-2 IDENTIFICATION AND AUTHENTICATION (ORGANIZATIONAL USERS)
This F5 solution uniquely identifies and authenticates organizational users (or processes acting on behalf of organizational users).
The information system implements multifactor authentication for:
- network access to privileged accounts
- network access to non-privileged accounts
- access to privileged accounts
- local access to non-privileged accounts
Individuals use individual authenticators as a second level of authentication to mitigate the risk of using group authenticators.
To reduce the likelihood of compromising authentication credentials stored on the system, the information system implements multifactor authentication for network access and also for remote access to privileged and also to non-privileged accounts such that one of the factors is provided by a device separate from the system gaining access and the device meets the organization-defined strength of mechanism requirements.
The information system implements replay-resistant authentication mechanisms for network access to privileged and also non-privileged accounts by using Transport Layer Security (TLS) and time synchronous or challenge-response one-time authenticators, making it impractical to achieve successful authentication by replaying previous authentication messages.
The information system provides a single sign-on capability for organization-defined lists of information system accounts and services, enbling users to log in once and gain access to multiple information system resources.
The information system accepts and electronically verifies Personal Identity Verification (PIV) credentials issued by federal departments or agencies that conform to FIPS Publication 201 and supporting guidance documents.
The information system implements organization-defined out-of-band authentication such as SMS messaging or 3rd-party authenticator applications on the user's cell phone to verify that the requested action originated from the user, under organization-defined conditions, based on factors that can include suspicious activities, new threat indicators or elevated threat levels, or the impact level or classification level of information in requested transactions.

### IA-3 DEVICE IDENTIFICATION AND AUTHENTICATION
The information system uniquely identifies and authenticates organization-defined specific and/or types of devices before establishing a local, remote or network connection using bidirectional authentication that is cryptographically based.
The F5 solution provides SSL VPN access with dynamic address allocation lease information and the lease duration assigned to devices is in accordance with organization-defined lease information and lease duration and supports audits of the lease information when assigned to a device.
The F5 solution supports device attestation handled by an organization-defined configuration management process to identify and authente a device based on its configuration and known operating state

### IA-4 IDENTIFIER MANAGEMENT
### IA-5 AUTHENTICATOR MANAGEMENT
This F5 solution supports secure local password policies for passwords of BIG-IP local user accounts when the organization choses not to leverage external directory services that  enforce their own password-strength policies. The solution allows the organization to define the how long a user's password should be valid, how many password changes are required before a previously used password can be reused, and what are the minimum number of different characters required for passwords, including the total password lenght, lowercase, uppercase, special chars and digit characters.

    Control:

    The organization manages information system authenticators by verifying, as part of the initial authenticator distribution, the identity of the individual, group, role, or device receiving the authenticator.
    The organization manages information system authenticators by establishing initial authenticator content for authenticators defined by the organization.
    The organization manages information system authenticators by ensuring that authenticators have sufficient strength of mechanism for their intended use.
    The organization manages information system authenticators by establishing and implementing administrative procedures for initial authenticator distribution, for lost/compromised or damaged authenticators, and for revoking authenticators.
    The organization manages information system authenticators by changing the default content of authenticators prior to information system installation.
    The organization manages information system authenticators by establishing minimum and maximum lifetime restrictions and reuse conditions for authenticators.
    The organization manages information system authenticators by changing/refreshing authenticators [Assignment: organization-defined time period by authenticator type].
    The organization manages information system authenticators by protecting authenticator content from unauthorized disclosure and modification.
    The organization manages information system authenticators by requiring individuals to take, and having devices implement, specific security safeguards to protect authenticators.
    The organization manages information system authenticators by changing authenticators for group/role accounts when membership to those accounts changes.
    Supplemental Guidance: Individual authenticators include, for example, passwords, tokens, biometrics, Public Key Infrastructure (PKI) certificates, and key cards. Initial authenticator content is the actual content (e.g., the initial password) as opposed to requirements about authenticator content (e.g., minimum password length). In many cases, developers ship information system components with factory default authentication credentials to allow for initial installation and configuration. Default authentication credentials are often well known, easily discoverable, and present a significant security risk. The requirement to protect individual authenticators may be implemented via control PL-4 or PS-6 for authenticators in the possession of individuals and by controls AC-3, AC-6, and SC-28 for authenticators stored within organizational information systems (e.g., passwords stored in hashed or encrypted formats, files containing encrypted or hashed passwords accessible with administrator privileges). Information systems support individual authenticator management by organization-defined settings and restrictions for various authenticator characteristics including, for example, minimum password length, password composition, validation time window for time synchronous one-time tokens, and number of allowed rejections during the verification stage of biometric authentication. Specific actions that can be taken to safeguard authenticators include, for example, maintaining possession of individual authenticators, not loaning or sharing individual authenticators with others, and reporting lost, stolen, or compromised authenticators immediately. Authenticator management includes issuing and revoking, when no longer needed, authenticators for temporary access such as that required for remote maintenance. Device authenticators include, for example, certificates and passwords. Related controls: AC-2, AC-3, AC-6, CM-6, IA-2, IA-4, IA-8, PL-4, PS-5, PS-6, SC-12, SC-13, SC-17, SC-28.

    Control Enhancements:

    AUTHENTICATOR MANAGEMENT | PASSWORD-BASED AUTHENTICATION
    The information system, for password-based authentication, enforces minimum password complexity of [Assignment: organization-defined requirements for case sensitivity, number of characters, mix of upper-case letters, lower-case letters, numbers, and special characters, including minimum requirements for each type];
    The information system, for password-based authentication, enforces at least the following number of changed characters when new passwords are created: [Assignment: organization-defined number];
    The information system, for password-based authentication, stores and transmits only cryptographically-protected passwords;
    The information system, for password-based authentication, enforces password minimum and maximum lifetime restrictions of [Assignment: organization-defined numbers for lifetime minimum, lifetime maximum];
    The information system, for password-based authentication prohibits password reuse for [Assignment: organization-defined number] generations; and
    The information system, for password-based authentication allows the use of a temporary password for system logons with an immediate change to a permanent password.
    Enhancement Supplemental Guidance: This control enhancement applies to single-factor authentication of individuals using passwords as individual or group authenticators, and in a similar manner, when passwords are part of multifactor authenticators. This control enhancement does not apply when passwords are used to unlock hardware authenticators (e.g., Personal Identity Verification cards). The implementation of such password mechanisms may not meet all of the requirements in the enhancement. Cryptographically-protected passwords include, for example, encrypted versions of passwords and one-way cryptographic hashes of passwords. The number of changed characters refers to the number of changes required with respect to the total number of positions in the current password. Password lifetime restrictions do not apply to temporary passwords. To mitigate certain brute force attacks against passwords, organizations may also consider salting passwords. Related control: IA-6.

    AUTHENTICATOR MANAGEMENT | PKI-BASED AUTHENTICATION
    The information system, for PKI-based authentication, validates certifications by constructing and verifying a certification path to an accepted trust anchor including checking certificate status information;
    The information system, for PKI-based authentication, enforces authorized access to the corresponding private key;
    The information system, for PKI-based authentication, maps the authenticated identity to the account of the individual or group; and
    The information system, for PKI-based authentication, implements a local cache of revocation data to support path discovery and validation in case of inability to access revocation information via the network.
    Enhancement Supplemental Guidance: Status information for certification paths includes, for example, certificate revocation lists or certificate status protocol responses. For PIV cards, validation of certifications involves the construction and verification of a certification path to the Common Policy Root trust anchor including certificate policy processing. Related control: IA-6.

    AUTHENTICATOR MANAGEMENT | IN-PERSON OR TRUSTED THIRD-PARTY REGISTRATION
    The organization requires that the registration process to receive [Assignment: organization-defined types of and/or specific authenticators] be conducted [Selection: in person; by a trusted third party] before [Assignment: organization-defined registration authority] with authorization by [Assignment: organization-defined personnel or roles].

    AUTHENTICATOR MANAGEMENT | AUTOMATED SUPPORT FOR PASSWORD STRENGTH DETERMINATION
    The organization employs automated tools to determine if password authenticators are sufficiently strong to satisfy [Assignment: organization-defined requirements].

    Enhancement Supplemental Guidance: This control enhancement focuses on the creation of strong passwords and the characteristics of such passwords (e.g., complexity) prior to use, the enforcement of which is carried out by organizational information systems in IA-5 (1). Related controls: CA-2, CA-7, RA-5.

    AUTHENTICATOR MANAGEMENT | CHANGE AUTHENTICATORS PRIOR TO DELIVERY
    The organization requires developers/installers of information system components to provide unique authenticators or change default authenticators prior to delivery/installation.

    Enhancement Supplemental Guidance: This control enhancement extends the requirement for organizations to change default authenticators upon information system installation, by requiring developers and/or installers to provide unique authenticators or change default authenticators for system components prior to delivery and/or installation. However, it typically does not apply to the developers of commercial off-the-shelve information technology products. Requirements for unique authenticators can be included in acquisition documents prepared by organizations when procuring information systems or system components.

    AUTHENTICATOR MANAGEMENT | PROTECTION OF AUTHENTICATORS
    The organization protects authenticators commensurate with the security category of the information to which use of the authenticator permits access.

    Enhancement Supplemental Guidance: For information systems containing multiple security categories of information without reliable physical or logical separation between categories, authenticators used to grant access to the systems are protected commensurate with the highest security category of information on the systems.

    AUTHENTICATOR MANAGEMENT | NO EMBEDDED UNENCRYPTED STATIC AUTHENTICATORS
    The organization ensures that unencrypted static authenticators are not embedded in applications or access scripts or stored on function keys.

    Enhancement Supplemental Guidance: Organizations exercise caution in determining whether embedded or stored authenticators are in encrypted or unencrypted form. If authenticators are used in the manner stored, then those representations are considered unencrypted authenticators. This is irrespective of whether that representation is perhaps an encrypted version of something else (e.g., a password).

    AUTHENTICATOR MANAGEMENT | MULTIPLE INFORMATION SYSTEM ACCOUNTS
    The organization implements [Assignment: organization-defined security safeguards] to manage the risk of compromise due to individuals having accounts on multiple information systems.

    Enhancement Supplemental Guidance: When individuals have accounts on multiple information systems, there is the risk that the compromise of one account may lead to the compromise of other accounts if individuals use the same authenticators. Possible alternatives include, for example: (i) having different authenticators on all systems; (ii) employing some form of single sign-on mechanism; or (iii) including some form of one-time passwords on all systems.

    AUTHENTICATOR MANAGEMENT | CROSS-ORGANIZATION CREDENTIAL MANAGEMENT
    The organization coordinates with [Assignment: organization-defined external organizations] for cross-organization management of credentials.

    Enhancement Supplemental Guidance: Cross-organization management of credentials provides the capability for organizations to appropriately authenticate individuals, groups, roles, or devices when conducting cross-organization activities involving the processing, storage, or transmission of information.

    AUTHENTICATOR MANAGEMENT | DYNAMIC CREDENTIAL ASSOCIATION
    The information system dynamically provisions identities.

    Enhancement Supplemental Guidance: Authentication requires some form of binding between an identity and the authenticator used to confirm the identity. In conventional approaches, this binding is established by pre-provisioning both the identity and the authenticator to the information system. For example, the binding between a username (i.e., identity) and a password (i.e., authenticator) is accomplished by provisioning the identity and authenticator as a pair in the information system. New authentication techniques allow the binding between the identity and the authenticator to be implemented outside an information system. For example, with smartcard credentials, the identity and the authenticator are bound together on the card. Using these credentials, information systems can authenticate identities that have not been pre-provisioned, dynamically provisioning the identity after authentication. In these situations, organizations can anticipate the dynamic provisioning of identities. Pre-established trust relationships and mechanisms with appropriate authorities to validate identities and related credentials are essential.

    AUTHENTICATOR MANAGEMENT | HARDWARE TOKEN-BASED AUTHENTICATION
    The information system, for hardware token-based authentication, employs mechanisms that satisfy [Assignment: organization-defined token quality requirements].

    Enhancement Supplemental Guidance: Hardware token-based authentication typically refers to the use of PKI-based tokens, such as the U.S. Government Personal Identity Verification (PIV) card. Organizations define specific requirements for tokens, such as working with a particular PKI.

    AUTHENTICATOR MANAGEMENT | BIOMETRIC AUTHENTICATION
    The information system, for biometric-based authentication, employs mechanisms that satisfy [Assignment: organization-defined biometric quality requirements].

    Enhancement Supplemental Guidance: Unlike password-based authentication which provides exact matches of user-input passwords to stored passwords, biometric authentication does not provide such exact matches. Depending upon the type of biometric and the type of collection mechanism, there is likely to be some divergence from the presented biometric and stored biometric which serves as the basis of comparison. There will likely be both false positives and false negatives when making such comparisons. The rate at which the false accept and false reject rates are equal is known as the crossover rate. Biometric quality requirements include, for example, acceptable crossover rates, as that essentially reflects the accuracy of the biometric.

    AUTHENTICATOR MANAGEMENT | EXPIRATION OF CACHED AUTHENTICATORS
    The information system prohibits the use of cached authenticators after [Assignment: organization-defined time period].

    AUTHENTICATOR MANAGEMENT | MANAGING CONTENT OF PKI TRUST STORES
    The organization, for PKI-based authentication, employs a deliberate organization-wide methodology for managing the content of PKI trust stores installed across all platforms including networks, operating systems, browsers, and applications.

### IA-6 AUTHENTICATOR FEEDBACK
This F5 solution enables an external directory service to authenticate BIG-IP management users. The directory service may also store RBAC roles for users. (Even when you enable an external directory service, the BIG-IP system continues to support local user accounts.)
The default role for users not assigned a specific role by the remote directory service is "No Access" and as a result will be forbiden access even if succesfully authenticated.
Users do not have access to he TMSH (CLI) console by default.

### IA-7 CRYPTOGRAPHIC MODULE AUTHENTICATION
### IA-8 IDENTIFICATION AND AUTHENTICATION (NON-ORGANIZATIONAL USERS)
### IA-9 SERVICE IDENTIFICATION AND AUTHENTICATION
### IA-10 ADAPTIVE IDENTIFICATION AND AUTHENTICATION
### IA-11 RE-AUTHENTICATION

## 3.8 FAMILY: INCIDENT RESPONSE
### IR-1 INCIDENT RESPONSE POLICY AND PROCEDURES
### IR-2 INCIDENT RESPONSE TRAINING
### IR-3 INCIDENT RESPONSE TESTING AND EXERCISES
### IR-4 INCIDENT HANDLING
### IR-5 INCIDENT MONITORING
### IR-6 INCIDENT REPORTING
### IR-7 INCIDENT RESPONSE ASSISTANCE
### IR-8 INCIDENT RESPONSE PLAN
### IR-9 INFORMATION SPILLAGE RESPONSE
### IR-10 INTEGRATED INFORMATION SECURITY ANALYSIS TEAM

## 3.9 FAMILY: MAINTENANCE
### MA-1 SYSTEM MAINTENANCE POLICY AND PROCEDURES
### MA-2 CONTROLLED MAINTENANCE
### MA-3 MAINTENANCE TOOLS
### MA-4 NON-LOCAL MAINTENANCE
### MA-5 MAINTENANCE PERSONNEL
### MA-6 TIMELY MAINTENANCE

## 3.10 FAMILY: MEDIA PROTECTION
### MP-1 MEDIA PROTECTION POLICY AND PROCEDURES
### MP-2 MEDIA ACCESS
### MP-3 MEDIA MARKING
### MP-4 MEDIA STORAGE
### MP-5 MEDIA TRANSPORT
### MP-6 MEDIA SANITIZATION
### MP-7 MEDIA USE
### MP-8 MEDIA DOWNGRADING

## 3.11 FAMILY: PHYSICAL AND ENVIRONMENTAL PROTECTION
### PE-1 PHYSICAL AND ENVIRONMENTAL PROTECTION POLICY AND PROCEDURES
### PE-2 PHYSICAL ACCESS AUTHORIZATIONS
### PE-3 PHYSICAL ACCESS CONTROL
### PE-4 ACCESS CONTROL FOR TRANSMISSION MEDIUM
### PE-5 ACCESS CONTROL FOR OUTPUT DEVICES
### PE-6 MONITORING PHYSICAL ACCESS
### PE-7 VISITOR CONTROL
### PE-8 ACCESS RECORDS
### PE-9 POWER EQUIPMENT AND POWER CABLING
### PE-10 EMERGENCY SHUTOFF
### PE-11 EMERGENCY POWER
### PE-12 EMERGENCY LIGHTING
### PE-13 FIRE PROTECTION
### PE-14 TEMPERATURE AND HUMIDITY CONTROLS
### PE-15 WATER DAMAGE PROTECTION
### PE-16 DELIVERY AND REMOVAL
### PE-17 ALTERNATE WORK SITE
### PE-18 LOCATION OF INFORMATION SYSTEM COMPONENTS
### PE-19 INFORMATION LEAKAGE
### PE-20 ASSET MONITORING AND TRACKING

## 3.12 FAMILY: PLANNING
### PL-1 SECURITY PLANNING POLICY AND PROCEDURES
### PL-2 SYSTEM SECURITY PLAN
### PL-3 SYSTEM SECURITY PLAN UPDATE
### PL-4 RULES OF BEHAVIOUR
### PL-5 PRIVACY IMPACT ASSESSMENT
### PL-6 SECURITY-RELATED ACTIVITY PLANNING
### PL-7 SECURITY CONCEPTS OF OPERATION
### PL-8 INFORMATION SECURITY ARCHITECTURE
### PL-9 CENTRAL MANAGEMENT

## 3.13 FAMILY: PERSONNEL SECURITY
### PS-1 PERSONNEL SECURITY POLICY AND PROCEDURES
### PS-2 POSITION CATEGORIZATION
### PS-3 PERSONNEL SCREENING
### PS-4 PERSONNEL TERMINATION
### PS-5 PERSONNEL TRANSFER
### PS-6 ACCESS AGREEMENTS
### PS-7 THIRD-PARTY PERSONNEL SECURITY
### PS-8 PERSONNEL SANCTIONS

## 3.14 FAMILY: RISK ASSESSMENT
### RA-1 RISK ASSESSMENT POLICY AND PROCEDURES
### RA-2 SECURITY CATEGORIZATION
### RA-3 RISK ASSESSMENT
### RA-4 RISK ASSESSMENT UPDATE
### RA-5 VULNERABILITY SCANNING
### RA-6 TECHNICAL SURVEILLANCE COUNTERMEASURES SURVEY

## 3.15 FAMILY: SYSTEM AND SERVICES ACQUISITION
### SA-1 SYSTEM AND SERVICES ACQUISITION POLICY AND PROCEDURES
### SA-2 ALLOCATION OF RESOURCES
### SA-3 SYSTEM DEVELOPMENT LIFECYCLE
### SA-4 ACQUISITION PROCESS
### SA-5 INFORMATION SYSTEM DOCUMENTATION
### SA-6 SOFTWARE USAGE RESTRICTIONS
### SA-7 USER-INSTALLED SOFTWARE
### SA-8 SECURITY ENGINEERING PRINCIPLES
### SA-9 EXTERNAL INFORMATION SYSTEM SERVICES
### SA-10 DEVELOPER CONFIGURATION MANAGEMENT
### SA-11 DEVELOPER SECURITY TESTING
### SA-12 SUPPLY CHAIN PROTECTION
### SA-13 TRUSTWORTHINESS
### SA-14 CRITICALITY ANALYSIS
### SA-15 DEVELOPMENT PROCESS, STANDARDS, AND TOOLS
### SA-16 DEVELOPER PROVIDED TRAINING
### SA-17 DEVELOPER SECURITY ARCHITECTURE AND DESIGN
### SA-18 TAMPER RESISTANCE AND DETECTION
### SA-19 COMPONENT AUTHENTICITY
### SA-20 CUSTOMIZED DEVELOPMENT OF CRITICAL COMPONENTS
### SA-21 DEVELOPER SCREENING
### SA-22 UNSUPPORTED SYSTEM COMPONENTS

## 3.16 FAMILY: SYSTEM AND COMMUNICATIONS PROTECTION
### SC-1 SYSTEM AND COMMUNICATIONS PROTECTION POLICY AND PROCEDURES
### SC-2 APPLICATION PARTITIONING
### SC-3 SECURITY FUNCTION ISOLATION
### SC-4 INFORMATION IN SHARED RESOURCES
### SC-5 DENIAL OF SERVICE PROTECTION
### SC-6 RESOURCE AVAILABILITY
### SC-7 BOUNDARY PROTECTION
### SC-8 TRANSMISSION CONFIDENTIALITY AND INTEGRITY
### SC-9 TRANSMISSION CONFIDENTIALITY
### SC-10 NETWORK DISCONNECT
### SC-11 TRUSTED PATH
### SC-12 CRYPTOGRAPHIC KEY ESTABLISHMENT AND MANAGEMENT
### SC-13 CRYPTOGRAPHIC PROTECTION
### SC-14 PUBLIC ACCESS PROTECTIONS
### SC-15 COLLABORATIVE COMPUTING DEVICES
### SC-16 TRANSMISSION OF SECURITY ATTRIBUTES
### SC-17 PUBLIC KEY INFRASTRUCTURE CERTIFICATES
### SC-18 MOBILE CODE
### SC-19 VOICE OVER INTERNET PROTOCOL
### SC-20 SECURE NAME / ADDRESS RESOLUTION SERVICE (AUTHORITATIVE SOURCE)
### SC-21 SECURE NAME / ADDRESS RESOLUTION SERVICE (RECURSIVE OR CACHING RESOLVER)
### SC-22 ARCHITECTURE AND PROVISIONING FOR NAME / ADDRESS RESOLUTION SERVICE
### SC-23 SESSION AUTHENTICITY
### SC-24 FAIL IN KNOWN STATE
### SC-25 THIN NODES
### SC-26 HONEYPOTS
### SC-27 PLATFORM-INDEPENDENT APPLICATIONS
### SC-28 PROTECTION OF INFORMATION AT REST
### SC-29 HETEROGENEITY
### SC-30 CONCEALMENT AND MISDIRECTION
### SC-31 COVERT CHANNEL ANALYSIS
### SC-32 INFORMATION SYSTEM PARTITIONING
### SC-33 TRANSMISSION PREPARATION INTEGRITY
### SC-34 NON-MODIFIABLE EXECUTABLE PROGRAMS
### SC-35 HONEYCLIENTS
### SC-36 DISTRIBUTED PROCESSING AND STORAGE
### SC-37 OUT-OF-BAND CHANNELS
### SC-38 OPERATIONS SECURITY
### SC-39 PROCESS ISOLATION
### SC-40 WIRELESS LINK PROTECTION
### SC-41 PORT AND I/O DEVICE ACCESS
### SC-42 SENSOR CAPABILITY AND DATA
### SC-43 USAGE RESTRICTIONS
### SC-44 DETONATION CHAMBERS
### SC-100 SOURCE AUTHENTICATION
### SC-101 – UNCLASSIFIED TELECOMMUNICATIONS SYSTEMS IN SECURE FACILITIES

## 3.17 FAMILY: SYSTEM AND INFORMATION INTEGRITY
### SI-1 SYSTEM AND INFORMATION INTEGRITY POLICY AND PROCEDURES
### SI-2 FLAW REMEDIATION
### SI-3 MALICIOUS CODE PROTECTION
### SI-4 INFORMATION SYSTEM MONITORING
### SI-5 SECURITY ALERTS, ADVISORIES, AND DIRECTIVES
### SI-6 SECURITY FUNCTIONAL VERIFICATION
### SI-7 SOFTWARE, FIRMWARE, AND INFORMATION INTEGRITY
### SI-8 SPAM PROTECTION
### SI-9 INFORMATION INPUT RESTRICTIONS
### SI-10 INFORMATION INPUT VALIDATION
### SI-11 ERROR HANDLING
### SI-12 INFORMATION OUTPUT HANDLING AND RETENTION
### SI-13 PREDICTABLE FAILURE PREVENTION
### SI-14 NON-PERSISTENCE
### SI-15 INFORMATION OUTPUT FILTERING
### SI-16 MEMORY PROTECTION
### SI-17 FAIL-SAFE PROCEDURES