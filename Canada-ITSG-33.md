# Canada ITSG Security Control Compliancy
Annex 3A - Security Control Catalogue (ITSG-33)
( https://cyber.gc.ca/en/guidance/annex-3a-security-control-catalogue-itsg-33, equivalent to NIST: https://nvd.nist.gov/800-53 )

## 3.1 FAMILY: ACCESS CONTROL
### AC-1 - Access Control Policy and Procedures
This control would be implemented outside of this F5 solution.

### AC-2 ACCOUNT MANAGEMENT
The lifecycle of user accounts and roles associated with them is the focus of this control. This F5 solution enables configuration of authentication sources (local, LDAP, RADIUS, etc.) as well as inactivity timeout and remote role assignment in support of this control.

#### AC-2(1) ACCOUNT MANAGEMENT | AUTOMATED SYSTEM ACCOUNT MANAGEMENT
This F5 solution employs automated mechanisms to support the management of information system accounts.
Authentication and authorization of all information system accounts is done via the organization's directory service, including accounts used to access the individual infrastructure components of the solution such as the F5 appliances, the servers and the firewalls, as well as for access to the applications serviced and contained within this infrastructure.
When users are terminated or transferred, the F5 solution automatically and immediately reflects the change in authorization for the corresponding accounts and enforces the corresponding actions (authorize or deny access).
The F5 solution captures audit and logging reports detailing the account usage.

#### AC-2(2) ACCOUNT MANAGEMENT | REMOVAL OF TEMPORARY / EMERGENCY ACCOUNTS
This F5 solution automatically disables temporary and emergency accounts that have expired without requiring the intervention of a systems administrator. This is accomplished by leveraging the directory service attributes that identify the status of each account and by programing the desired logic in the F5 Visual Policy Editor, such as setting the appropriate expiry time for the authorized access after the temporary or emergency account has been successfully authorized, and this is enforced for access to the individual infrastructure components of the solution such as the F5 appliances, the servers and the firewalls, as well as for access to the applications serviced and contained within this infrastructure.

#### AC-2(3) ACCOUNT MANAGEMENT | DISABLE INACTIVE ACCOUNTS
This F5 solution automatically disables inactive accounts after the defined time period has elapsed.
This is accomplished by leveraging the directory service attributes that identify the last successful login of each account and by programing the desired logic in the F5 Visual Policy Editor to automatically deny access to an account that has been inactive for longer than the defined time period after the account has been successfully authorized, and this is enforced for access to the individual infrastructure components of the solution such as the F5 appliances, the servers and the firewalls, as well as for access to the applications serviced and contained within this infrastructure.

#### AC-2(5) ACCOUNT MANAGEMENT | INACTIVITY LOGOUT
This F5 solution automatically logs out users when the defined time-period of inactivity has elapsed and different time-period values can be be specified for connections to the system's management services: web-based Configuration utility, SSH connections, Console and TMSH. For other individual infrastructure components such as the servers and firewalls, as well as for access to the appications services and contained within this infrastructure, this is accomplished by configuration of the "Inactivity Timeout" setting in the Access policy.

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
Access to this F5 solution must be made through approved means. Related to AC-2, remote authentication and role determination help satisfy this control.

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
This control addresses information flow within and between systems. The iApp supports this control mainly by enforcing boundary protections; see SC-7.

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
Encourages use of role-based access control (RBAC). This F5 solution supports a variety of different security roles. Users may be assigned roles on the system or by reference to a central authority (for example, mapping via an LDAP attribute).

### AC-6 LEAST PRIVILEGE
This F5 solution supports this control using role-based access control, Administrative Partitions, and auditing.
This F5 solution enables an external directory service to authenticate management users. The directory service may also store RBAC roles for users. (Even when you enable an external directory service, the system continues to support local user accounts.)
The default role for users not assigned a specific role by the remote directory service is "No Access" and as a result will be forbiden access even if succesfully authenticated.
Users do not have access to he TMSH (CLI) console by default.

### AC-7 UNSUCCESSFUL LOGIN ATTEMPTS
To protect account credentials against brute-force attacks you should lock accounts after a certain number of unsuccessful login attempts. 
If the organization opts not to leveraged their external directory server to, this F5 solution provides the ability to disable a local user account after some number of failed login attempt.

### AC-8 SYSTEM USE NOTIFICATION
You should warn users about policies governing their access to the system.
This F5 solution provides the ability to alter the banner messages which appear to users of the management web GUI or the command line.

### AC-9 PREVIOUS LOGON (ACCESS) NOTIFICATION
Upon logon, users should be notified of their last successful logon time plus additional logon history. 
This F5 solution displays the last logon time to SSH and console users. Additional logon history information is available via TMSH and shell.

### AC-10 CONCURRENT SESSION CONTROL
Limit the number of concurrent sessions by user or account type.
This F5 solution provides the ability to limit the number of concurrent users of the management web GUI and also for access to the other individual infrastructure components of the solution such as the servers and the firewalls, as well as for access to the applications serviced and contained within this infrastructure.

### AC-11 SESSION LOCK
Session locking differs from automatic logout due to idleness because the user's session state is maintained. This F5 solution does not have this feature. A screen- or client-locking feature on the user's workstation could help meet this control.

### AC-12 SESSION TERMINATION
This F5 solution automatically displays a suitable message and terminates the network connection associated with a communications session at the end of the session or logs out users when the defined time-period of inactivity has elapsed and different time-period values can be be specified for connections to the system's management services: web-based Configuration utility, SSH connections, Console and TMSH. For other individual infrastructure components such as the servers and firewalls, as well as for access to the appications services and contained within this infrastructure, this is accomplished by configuration of the "Inactivity Timeout" setting in the Access policy.

### AC-13 SUPERVISION AND REVIEW — ACCESS CONTROL
This control appeared in earlier revisions of ITSG-33, but has been withdrawn.

### AC-14 PERMITTED ACTIONS WITHOUT IDENTIFICATION OR AUTHENTICATION
This control addresses actions, if any, available without user authentication or authorization. This F5 solution does not offer any services to unauthenticated/unauthorized users.

### AC-15 AUTOMATED MARKING
This control appeared in earlier revisions of ITSG-33, but has been withdrawn.

### AC-16 SECURITY ATTRIBUTES
This control relates to associating security attributes to information in storage, in process, and in transmission.

### AC-17 REMOTE ACCESS
Addressing this control will go beyond this F5 solution. However, all remote management access uses encrypted transport (AC-17(2)) except SNMP. Also see SC-7 for boundary protection which also controls remote access.

### AC-18 WIRELESS ACCESS
This F5 solution has no configuration options specifically related to wireless networking. This control would mainly be addressed outside this F5 solution and by compliance to SC-7.

### AC-19 ACCESS CONTROL FOR MOBILE DEVICES
This F5 solution has no configuration options specifically related to mobile devices. This control would mainly be addressed outside of this F5 solution and by compliance to AC-3 and SC-7.

### AC-20 USE OF EXTERNAL INFORMATION SYSTEMS
This control relates to communications with systems in other administrative domains. This F5 solution's management only operates in a single administrative domain so no configuration options are responsive.

### AC-21 USER-BASED COLLABORATION AND INFORMATION SHARING
This control would be implemented outside of this F5 solution.

### AC-22 PUBLICLY ACCESSIBLE CONTENT
This control would be implemented outside of this F5 solution.

### AC-23 DATA MINING PROTECTION
This control would be implemented outside of this F5 solution.

### AC-24 ACCESS CONTROL DECISIONS
This control would be implemented outside of this F5 solution.

### AC-25 REFERENCE MONITOR
This control concerns the incorporation of the “reference monitor” concept into system design and implementation.

## 3.2 FAMILY: AWARENESS AND TRAINING
None of the controls (AT-nn) in this section are relevant to this F5 solution.

## 3.3 FAMILY: AUDIT AND ACCOUNTABILITY
### AU-1 AUDIT AND ACCOUNTABILITY POLICY AND PROCEDURES
This control would be implemented outside of this F5 solution.

### AU-2 AUDITABLE EVENTS
This F5 solution provides the ability to activate audit event recording for management actions. Typically you enable TMSH and MCP audit logs. MCP logs record changes initiated via any user inerface. Only if you do not have a syslog server to accept log messages should you consider disabling logs to save disk space.

### AU-3 CONTENT OF AUDIT RECORDS
The contents of this F5 solution's audit records are basically fixed.

### AU-4 AUDIT STORAGE CAPACITY
Space for storing audit records (logs) on this F5 solution is not directly configurable, but you should send audit records to a remote server (see AU-9) and apply this control that context.

### AU-5 RESPONSE TO AUDIT PROCESSING FAILURES
This F5 solution has no configuration options specifically related to this control.

### AU-6 AUDIT REVIEW, ANALYSIS, AND REPORTING
This control would be implemented outside of this F5 solution.

### AU-7 AUDIT REDUCTION AND REPORT GENERATION
This control would be implemented outside of this F5 solution.

### AU-8 TIME STAMPS
To meet this control you may configure compliant (ISO) time stamps for audit messages (also see AU-12) and configure NTP server(s) as sources of accurate time.
This F5 solution provides the ability to specify the IP addresses of your primary and (if available) alternate NTP servers. A working NTP configuration is vital to this F5 solution's management (and application) security.
This F5 solution provides the ability to enable the use of ISO-format dates in log messages (generally required for ITSG-33 compliance). You may also add syslog servers to receive log messages.

### AU-9 PROTECTION OF AUDIT INFORMATION
User roles (AC-6) control access to audit information on this F5 solution. You should send audit records to a remote server and apply this control in that context. This F5 solution provides the ability to enable the use of ISO-format dates in log messages (generally required for ITSG-33 compliance). You may also add syslog servers to receive log messages.

### AU-10 NON-REPUDIATION
This F5 solution has no configuration options specifically related to this control.

### AU-11 AUDIT RECORD RETENTION
Audit record log rollover is not directly configurable in this F5 solution. You should send audit records to a remote server and apply this control in that context (see AU-9).

### AU-12 AUDIT GENERATION
This control would mostly be implemented outside of this F5 solution. This F5 solution provides the ability to enable the use of ISO-format dates in log messages (generally required for ITSG-33 compliance). You may also add syslog servers to receive log messages.

### AU-13 MONITORING FOR INFORMATION DISCLOSURE
This control would be implemented outside of this F5 solution.

### AU-14 SESSION AUDIT
This F5 solution does not provide the capability envisioned by this control. A portion of this information could be selected from the audit message stream (see AU-2, AU-12).

### AU-15 ALTERNATE AUDIT CAPABILITY
This F5 solution retains copies of audit messages sent to remote servers for a few days, typically (see AU-4). An alternate procedure to retrieve audit data from BIG-IP could be defined in case a remote audit log server is unavailable or damaged.

### AU-16 CROSS-ORGANIZATIONAL AUDITING
This control would be implemented outside of this F5 solution.

## 3.4 FAMILY: SECURITY ASSESSMENT AND AUTHORIZATION
These controls would be implemented outside of this F5 solution.

## 3.5 FAMILY: CONFIGURATION MANAGEMENT
### CM-1 CONFIGURATION MANAGEMENT POLICY AND PROCEDURES
These controls would be implemented outside of this F5 solution.

### CM-2 BASELINE CONFIGURATION
This F5 solution supports UCS and SCF files that may furnish data required to implement these controls. F5 BIG-IQ may also be utilized.

### CM-3 CONFIGURATION CHANGE CONTROL
These controls would be implemented outside of this F5 solution.

### CM-4 SECURITY IMPACT ANALYSIS
These controls would be implemented outside of this F5 solution.

### CM-5 ACCESS RESTRICTIONS FOR CHANGE
This F5 solution enforces a role-based access control policy over defined subjects and objects and controls access based up organization-defined roles and users authorized to assume such roles, as defined in the organization's directory service. This is accomplished with the configuration of the corresponding logic in the F5 access policy definition and is enforced for access to the individual infrastructure components of the solution such as the F5 appliances, the servers and the firewalls, as well as for access to the applications serviced and contained within this infrastructure.
This F5 solution provides the ability to configure audit logging of management actions. Typically you enable TMSH and MCP audit logs. Only if you do not have a syslog server to accept log messages should you consider disabling logs to save disk space.
This F5 solution supports signature verification for TMOS software updates (CM-5(3)).

### CM-6 CONFIGURATION SETTINGS
These controls would be implemented outside of this F5 solution.

### CM-7 LEAST FUNCTIONALITY
This F5 solution lets you adjust the services accessible on self IP addresses so you can constrain the functionality of BIG-IP in the network.

### CM-8 INFORMATION SYSTEM COMPONENT INVENTORY
These controls would be implemented outside of this F5 solution. However, F5 BIG-IQ may be utilized in the implementation of these controls.

### CM-9 CONFIGURATION MANAGEMENT PLAN
These controls would be implemented outside of this F5 solution.

### CM-10 SOFTWARE USAGE RESTRICTIONS
These controls would be implemented outside of this F5 solution.

### CM-11 USER INSTALLED SOFTWARE
These controls would be implemented outside of this F5 solution.

## 3.6 FAMILY: CONTINGENCY PLANNING (CONTINUITY PLANNING)
Most of the controls (CP-nn) in this family would be implemented outside of this F5 solution. Some exceptions are noted here.

### CP-7 ALTERNATE PROCESSING SITE
This F5 solution supports configuration synchronization and functional failover device groups, as well as global traffic management (F5 BIG-IP DNS), so f5 customers can build highly-reliable systems within and among different processing sites (“data centers”).

### CP-9 INFORMATION SYSTEM BACKUP
This F5 solution does not store user data and generally the device configuration is all that must be backed up to enable service recovery in the event of a failure. Logs may be backed up through remote syslog. BIG-IQ may be used to automate backup of device configuration and historical statistical data.

### CP-10 INFORMATION SYSTEM RECOVERY AND RECONSTITUTION
You may recover this F5 solution automatically in certain high-availability scenarios, by hand, or using F5 BIG-IQ.

## 3.7 FAMILY: IDENTIFICATION AND AUTHENTICATION
### IA-1 IDENTIFICATION AND AUTHENTICATION POLICY AND PROCEDURES
These controls would be implemented outside of this F5 solution.

### IA-2 IDENTIFICATION AND AUTHENTICATION (ORGANIZATIONAL USERS)
This F5 solution uniquely identifies and authenticates organizational users (or processes acting on behalf of organizational users).
This F5 solution supports user authentication to local or external directories using single- or multi-factor credentials.
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
This F5 solution secures access to external authentication/directory services using TLS/SSL or shared-secret schemes for mutual authentication.
The F5 solution provides SSL VPN access with dynamic address allocation lease information and the lease duration assigned to devices is in accordance with organization-defined lease information and lease duration and supports audits of the lease information when assigned to a device.
The F5 solution supports device attestation handled by an organization-defined configuration management process to identify and authente a device based on its configuration and known operating state

### IA-4 IDENTIFIER MANAGEMENT
These controls would be implemented outside of this F5 solution.

### IA-5 AUTHENTICATOR MANAGEMENT
This F5 solution supports secure local password policies for passwords of local user accounts when the organization choses not to leverage external directory services that  enforce their own password-strength policies. The solution allows the organization to define the how long a user's password should be valid, how many password changes are required before a previously used password can be reused, and what are the minimum number of different characters required for passwords, including the total password lenght, lowercase, uppercase, special chars and digit characters.
This F5 solution lets you configure password policy for local authentication as well as security for authentication data used with external authentication/directory services.

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
This F5 solution enables an external directory service to authenticate management users. The directory service may also store RBAC roles for users.
The default role for users not assigned a specific role by the remote directory service is "No Access" and as a result will be forbiden access even if succesfully authenticated.
Users do not have access to he TMSH (CLI) console by default.

### IA-7 CRYPTOGRAPHIC MODULE AUTHENTICATION
The information system implements mechanisms for authentication to a cryptographic module that meet the requirements of applicable GC legislation and TBS policies, directives, and standards for such authentication.
-> add F5 FIPS and HSM details here?

### IA-8 IDENTIFICATION AND AUTHENTICATION (NON-ORGANIZATIONAL USERS)
Control:

A. The information system uniquely identifies and authenticates non-organizational users (or processes acting on behalf of non-organizational users).

    Supplemental Guidance: Non-organizational users include information system users other than organizational users explicitly covered by IA-2. These individuals are uniquely identified and authenticated for accesses other than those accesses explicitly identified and documented in AC-14. Authentication of non-organizational users accessing federal information systems may be required to protect federal, proprietary, or privacy-related information (with exceptions noted for national security systems). Organizations use risk assessments to determine authentication needs and consider scalability, practicality, and security in balancing the need to ensure ease of use for access to GC information and information systems with the need to protect and adequately mitigate risk. IA-2 addresses identification and authentication requirements for access to information systems by organizational users. Related controls: AC-2, AC-14, AC-17, AC-18, IA-2, IA-4, IA-5, MA-4, RA-3, SA-12, SC-8.

    Control Enhancements:

    Enhancement Supplemental Guidance: The TBS Standard on Identity and Credential Assurance [Reference 60] establishes requirements for organizations to adopt a common methodology for assessing their identity and credential risks and selecting appropriate controls or arrangements to mitigate those risks using a standardized assurance level framework. The standard is supported by the TBS Guideline on Defining Authentication Requirements [Reference 61] and the TBS Guideline on Identity Assurance [Reference 62]. These guidelines are intended to be used in conjunction with CSE ITSB-31: User Authentication for IT Systems [Reference 18].

    1. IDENTIFICATION AND AUTHENTICATION | ACCEPTANCE OF PIV CREDENTIALS FROM OTHER AGENCIES
    Not applicable to the GC.

    2. IDENTIFICATION AND AUTHENTICATION | ACCEPTANCE OF THIRD-PARTY CREDENTIALS
    Not applicable to the GC.

    3. IDENTIFICATION AND AUTHENTICATION | USE OF FICAM-APPROVED PRODUCTS
    Not applicable to the GC.

    4. IDENTIFICATION AND AUTHENTICATION | USE OF FICAM-ISSUED PROFILES
    Not applicable to the GC.

    5. IDENTIFICATION AND AUTHENTICATION | ACCEPTANCE OF PIV-I CREDENTIALS
    Not applicable to the GC.

    100. In accordance with the TBS Standard on Identity and Credential Assurance (including Appendix B and C) [Reference 60], the organization determines the required identity and credential assurance levels and selects appropriate controls using the standardized assurance levels specified in Appendix B, and implements the minimum requirements for establishing an identity assurance level specified in Appendix C.


### IA-9 SERVICE IDENTIFICATION AND AUTHENTICATION
Control:

A. The organization identifies and authenticates [Assignment: organization-defined information system services] using [Assignment: organization-defined security safeguards].

    Supplemental Guidance: This control supports service-oriented architectures and other distributed architectural approaches requiring the identification and authentication of information system services. In such architectures, external services often appear dynamically. Therefore, information systems should be able to determine in a dynamic manner, if external providers and associated services are authentic. Safeguards implemented by organizational information systems to validate provider and service authenticity include, for example, information or code signing, provenance graphs, and/or electronic signatures indicating or including the sources of services.

    Control Enhancements:

    1. SERVICE IDENTIFICATION AND AUTHENTICATION | INFORMATION EXCHANGE
    The organization ensures that service providers receive, validate, and transmit identification and authentication information.

    2. SERVICE IDENTIFICATION AND AUTHENTICATION | TRANSMISSION OF DECISIONS
    The organization ensures that identification and authentication decisions are transmitted between [Assignment: organization-defined services] and are consistent with organizational policies.

    Enhancement Supplemental Guidance: For distributed architectures (e.g., service-oriented architectures), the decisions regarding the validation of identification and authentication claims may be made by services separate from the services acting on those decisions. In such situations, it is necessary to provide the identification and authentication decisions (as opposed to the actual identifiers and authenticators) to the services that need to act on those decisions. Related control: SC-8.

### IA-10 ADAPTIVE IDENTIFICATION AND AUTHENTICATION
Control:

A. The organization requires that individuals accessing the information system employ [Assignment: organization-defined supplemental authentication techniques or mechanisms] under specific [Assignment: organization-defined circumstances or situations].

    Supplemental Guidance: Adversaries may compromise individual authentication mechanisms and subsequently attempt to impersonate legitimate users. This situation can potentially occur with any authentication mechanisms employed by organizations. To address this threat, organizations may employ specific techniques/mechanisms and establish protocols to assess suspicious behaviour (e.g., individuals accessing information that they do not typically access as part of their normal duties, roles, or responsibilities, accessing greater quantities of information than the individuals would routinely access, or attempting to access information from suspicious network addresses). In these situations when certain pre-established conditions or triggers occur, organizations can require selected individuals to provide additional authentication information. Another potential use for adaptive identification and authentication is to increase the strength of mechanism based on the number and/or types of records being accessed. Related controls: AU-6, SI-4.

-> add details on per-request policies and Zero-trust, Identity aware gateway, etc...


### IA-11 RE-AUTHENTICATION
Control:

A. The organization requires users and devices to re-authenticate when [Assignment: organization-defined circumstances or situations requiring re-authentication].

    Supplemental Guidance: In addition to the re-authentication requirements associated with session locks, organizations may require re-authentication of individuals and/or devices in other situations including, for example: (i) when authenticators change; (ii), when roles change; (iii) when security categories of information systems change; (iv), when the execution of privileged functions occurs; (v) after a fixed period of time; or (vi) periodically. Related control: AC-11.

-> add details on per-request policies and Zero-trust, Identity aware gateway, etc...


## 3.8 FAMILY: INCIDENT RESPONSE
These controls would be implemented outside of this F5 solution.

## 3.9 FAMILY: MAINTENANCE
These controls would be implemented outside of this F5 solution.

## 3.10 FAMILY: MEDIA PROTECTION
These controls would be implemented outside of this F5 solution.

## 3.11 FAMILY: PHYSICAL AND ENVIRONMENTAL PROTECTION
These controls would be implemented outside of this F5 solution.

## 3.12 FAMILY: PLANNING
These controls would be implemented outside of this F5 solution.

## 3.13 FAMILY: PERSONNEL SECURITY
These controls would be implemented outside of this F5 solution.

## 3.14 FAMILY: RISK ASSESSMENT
These controls would be implemented outside of this F5 solution.

## 3.15 FAMILY: SYSTEM AND SERVICES ACQUISITION
These controls would be implemented outside of this F5 solution.

## 3.16 FAMILY: SYSTEM AND COMMUNICATIONS PROTECTION
Most of the controls (SC-nn) in this family would be implemented outside of this F5 solution. Important exceptions are noted here.

### SC-5 DENIAL OF SERVICE PROTECTION
This F5 solution is hardened against certain Denial of Service attacks.

### SC-7 BOUNDARY PROTECTION
This F5 solution provides the ability to control from which IP addresses the management network interface accepts connections (to the management web GUI or command line, of to the SNMP service), as well as services accessible on self IP addresses.

    4. BOUNDARY PROTECTION | EXTERNAL TELECOMMUNICATIONS SERVICES
    The organization implements a managed interface for each external telecommunication service;
    The organization establishes a traffic flow policy for each managed interface;
    The organization protects the confidentiality and integrity of the information being transmitted across each interface;
    The organization documents each exception to the traffic flow policy with a supporting mission/business need and duration of that need; and
    The organization reviews exceptions to the traffic flow policy [Assignment: organization-defined frequency] and removes exceptions that are no longer supported by an explicit mission/business need.
    Enhancement Supplemental Guidance: Related control: SC-8.

    5. BOUNDARY PROTECTION | DENY BY DEFAULT / ALLOW BY EXCEPTION
    The information system at managed interfaces denies network communications traffic by default and allows network communications traffic by exception (i.e., deny all, permit by exception).

    Enhancement Supplemental Guidance: This control enhancement applies to both inbound and outbound network communications traffic. A deny-all, permit-by-exception network communications traffic policy ensures that only those connections which are essential and approved are allowed.
    7. BOUNDARY PROTECTION | PREVENT SPLIT TUNNELLING FOR REMOTE DEVICES
    The information system, in conjunction with a remote device, prevents the device from simultaneously establishing non-remote connections with the system and communicating via some other connection to resources in external networks.

    Enhancement Supplemental Guidance: This control enhancement is implemented within remote devices (e.g., notebook computers) through configuration settings to disable split tunnelling in those devices, and by preventing those configuration settings from being readily configurable by users. This control enhancement is implemented within the information system by the detection of split tunnelling (or of configuration settings that allow split tunnelling) in the remote device, and by prohibiting the connection if the remote device is using split tunnelling. Split tunnelling might be desirable by remote users to communicate with local information system resources such as printers/file servers. However, split tunnelling would in effect allow unauthorized external connections, making the system more vulnerable to attack and to exfiltration of organizational information. The use of VPNs for remote connections, when adequately provisioned with appropriate security controls, may provide the organization with sufficient assurance that it can effectively treat such connections as non-remote connections from the confidentiality and integrity perspective. VPNs thus provide a means for allowing non-remote communications paths from remote devices. The use of an adequately provisioned VPN does not eliminate the need for preventing split tunnelling.

    8. BOUNDARY PROTECTION | ROUTE TRAFFIC TO AUTHENTICATED PROXY SERVERS
    The information system routes [Assignment: organization-defined internal communications traffic] to [Assignment: organization-defined external networks] through authenticated proxy servers at managed interfaces.

    Enhancement Supplemental Guidance: External networks are networks outside of organizational control. A proxy server is a server (i.e., information system or application) that acts as an intermediary for clients requesting information system resources (e.g., files, connections, web pages, or services) from other organizational servers. Client requests established through an initial connection to the proxy server are evaluated to manage complexity and to provide additional protection by limiting direct connectivity. Web content filtering devices are one of the most common proxy servers providing access to the Internet. Proxy servers support logging individual Transmission Control Protocol (TCP) sessions and blocking specific Uniform Resource Locators (URLs), domain names, and Internet Protocol (IP) addresses. Web proxies can be configured with organization-defined lists of authorized and unauthorized websites. Related controls: AC-3, AU-2.

    9. BOUNDARY PROTECTION | RESTRICT THREATENING OUTGOING COMMUNICATIONS TRAFFIC
    The information system detects and denies outgoing communications traffic posing a threat to external information systems; and
    The information system audits the identity of internal users associated with denied communications.
    Enhancement Supplemental Guidance: Detecting outgoing communications traffic from internal actions that may pose threats to external information systems is sometimes termed extrusion detection. Extrusion detection at information system boundaries as part of managed interfaces includes the analysis of incoming and outgoing communications traffic searching for indications of internal threats to the security of external systems. Such threats include, for example, traffic indicative of denial of service attacks and traffic containing malicious code. Related controls: AU-2, AU-6, SC-38, SC-44, SI-3, SI-4.

    10. BOUNDARY PROTECTION | PREVENT UNAUTHORIZED EXFILTRATION
    The organization prevents the unauthorized exfiltration of information across managed interfaces.

    Enhancement Supplemental Guidance: Safeguards implemented by organizations to prevent unauthorized exfiltration of information from information systems include, for example: (i) strict adherence to protocol formats; (ii) monitoring for beaconing from information systems; (iii) monitoring for steganography; (iv) disconnecting external network interfaces except when explicitly needed; (v) disassembling and reassembling packet headers; and (vi) employing traffic profile analysis to detect deviations from the volume/types of traffic expected within organizations or call backs to command and control centres. Devices enforcing strict adherence to protocol formats include, for example, deep packet inspection firewalls and XML gateways. These devices verify adherence to protocol formats and specification at the application layer and serve to identify vulnerabilities that cannot be detected by devices operating at the network or transport layers. This control enhancement is closely associated with cross-domain solutions and system guards enforcing information flow requirements. Related control: SI-3.

    11. BOUNDARY PROTECTION | RESTRICT INCOMING COMMUNICATIONS TRAFFIC
    The information system only allows incoming communications from [Assignment: organization-defined authorized sources] routed to [Assignment: organization-defined authorized destinations].

    Enhancement Supplemental Guidance: This control enhancement provides determinations that source and destination address pairs represent authorized/allowed communications. Such determinations can be based on several factors including, for example, the presence of source/destination address pairs in lists of authorized/allowed communications, the absence of address pairs in lists of unauthorized/disallowed pairs, or meeting more general rules for authorized/allowed source/destination pairs. Related control: AC-3.

    13. BOUNDARY PROTECTION | ISOLATION OF SECURITY TOOLS / MECHANISMS / SUPPORT COMPONENTS
    The organization isolates [Assignment: organization-defined information security tools, mechanisms, and support components] from other internal information system components by implementing physically separate sub-networks with managed interfaces to other components of the system.

    Enhancement Supplemental Guidance: Physically separate sub-networks with managed interfaces are useful, for example, in isolating computer network defences from critical operational processing networks to prevent adversaries from discovering the analysis and forensics techniques of organizations. Related controls: SA-8, SC-2, SC-3.

    15. BOUNDARY PROTECTION | ROUTE PRIVILEGED NETWORK ACCESSES
    The information system routes all networked, privileged accesses through a dedicated, managed interface for purposes of access control and auditing.

    Enhancement Supplemental Guidance: Related controls: AC-2, AC-3, AU-2, SI-4.

    16. BOUNDARY PROTECTION | PREVENT DISCOVERY OF COMPONENTS / DEVICES
    The information system prevents discovery of specific system components composing a managed interface.

    Enhancement Supplemental Guidance: This control enhancement protects network addresses of information system components that are part of managed interfaces from discovery through common tools and techniques used to identify devices on networks. Network addresses are not available for discovery (e.g., network address not published or entered in domain name systems), requiring prior knowledge for access. Another obfuscation technique is to periodically change network addresses.

    17. BOUNDARY PROTECTION | AUTOMATED ENFORCEMENT OF PROTOCOL FORMATS
    The information system enforces adherence to protocol formats.

    Enhancement Supplemental Guidance: Information system components that enforce protocol formats include, for example, deep packet inspection firewalls and XML gateways. Such system components verify adherence to protocol formats/specifications (e.g., IEEE) at the application layer and identify significant vulnerabilities that cannot be detected by devices operating at the network or transport layers. Related control: SC-4.

    18. BOUNDARY PROTECTION | FAIL SECURE
    The information system fails securely in the event of an operational failure of a boundary protection device.

    Enhancement Supplemental Guidance: Fail secure is a condition achieved by employing information system mechanisms to ensure that in the event of operational failures of boundary protection devices at managed interfaces (e.g., routers, firewalls, guards, and application gateways residing on protected sub-networks commonly referred to as demilitarized zones), information systems do not enter into insecure states where intended security properties no longer hold. Failures of boundary protection devices cannot lead to, or cause information external to the devices to enter the devices, nor can failures permit unauthorized information releases. Related controls: CP-2, SC-24.

    19. BOUNDARY PROTECTION | BLOCKS COMMUNICATION FROM NON-ORGANIZATIONALLY CONFIGURED HOSTS
    The information system blocks both inbound and outbound communications traffic between [Assignment: organization-defined communication clients] that are independently configured by end users and external service providers.

    Enhancement Supplemental Guidance: Communication clients independently configured by end users and external service providers include, for example, instant messaging clients. Traffic blocking does not apply to communication clients that are configured by organizations to perform authorized functions.

    20. BOUNDARY PROTECTION | DYNAMIC ISOLATION / SEGREGATION
    The information system provides the capability to dynamically isolate/segregate [Assignment: organization-defined information system components] from other components of the system.

    Enhancement Supplemental Guidance: The capability to dynamically isolate or segregate certain internal components of organizational information systems is useful when it is necessary to partition or separate certain components of dubious origin from those components possessing greater trustworthiness. Component isolation reduces the attack surface of organizational information systems. Isolation of selected information system components is also a means of limiting the damage from successful cyber-attacks when those attacks occur.

    21. BOUNDARY PROTECTION | ISOLATION OF INFORMATION SYSTEM COMPONENTS
    The organization employs boundary protection mechanisms to separate [Assignment: organization-defined information system components] supporting [Assignment: organization-defined missions and/or business functions].

    Enhancement Supplemental Guidance: Organizations can isolate information system components performing different missions and/or business functions. Such isolation limits unauthorized information flows among system components and also provides the opportunity to deploy greater levels of protection for selected components. Separating system components with boundary protection mechanisms provides the capability for increased protection of individual components and to more effectively control information flows between those components. This type of enhanced protection limits the potential harm from cyber-attacks and errors. The degree of separation provided varies depending upon the mechanisms chosen. Boundary protection mechanisms include, for example, routers, gateways, and firewalls separating system components into physically separate networks or sub-networks, cross-domain devices separating sub-networks, virtualization techniques, and encrypting information flows among system components using distinct encryption keys. Related controls: CA-9, SC-3.

    22. BOUNDARY PROTECTION | SEPARATE SUBNETS FOR CONNECTING TO DIFFERENT SECURITY DOMAINS
    The information system implements separate network addresses (i.e., different subnets) to connect to systems in different security domains.

    Enhancement Supplemental Guidance: Decomposition of information systems into subnets helps to provide the appropriate level of protection for network connections to different security domains containing information with different security categories or classification levels.

    23. BOUNDARY PROTECTION | DISABLE SENDER FEEDBACK ON PROTOCOL VALIDATION FAILURE
    The information system disables feedback to senders on protocol format validation failure.

    Enhancement Supplemental Guidance: Disabling feedback to senders when there is a failure in protocol validation format prevents adversaries from obtaining information which would otherwise be unavailable.

### SC-8 TRANSMISSION CONFIDENTIALITY AND INTEGRITY
    Control:

    The information system protects the [Selection (one or more): confidentiality; integrity] of transmitted information.
    Supplemental Guidance: This control applies to both internal and external networks and all types of information system components from which information can be transmitted (e.g., servers, mobile devices, notebook computers, printers, copiers, scanners, facsimile machines). Communication paths outside the physical protection of a controlled boundary are exposed to the possibility of interception and modification. Protecting the confidentiality and/or integrity of organizational information can be accomplished by physical means (e.g., by employing protected distribution systems) or by logical means (e.g., employing encryption techniques). Organizations relying on commercial providers offering transmission services as commodity services rather than as fully dedicated services (i.e., services which can be highly specialized to individual customer needs), may find it difficult to obtain the necessary assurances regarding the implementation of needed security controls for transmission confidentiality/integrity. In such situations, organizations determine what types of confidentiality/integrity services are available in standard, commercial telecommunication service packages. If it is infeasible or impractical to obtain the necessary security controls and assurances of control effectiveness through appropriate contracting vehicles, organizations implement appropriate compensating security controls or explicitly accept the additional risk. Related controls: AC-17, PE-4.

    Control Enhancements:

    1. TRANSMISSION CONFIDENTIALITY AND INTEGRITY | CRYPTOGRAPHIC OR ALTERNATE PHYSICAL PROTECTION
    The information system implements cryptographic mechanisms to [Selection (one or more): prevent unauthorized disclosure of information; detect changes to information] during transmission unless otherwise protected by [Assignment: organization-defined alternative physical safeguards]. The cryptography must be compliant with the requirements of control SC-13.

    Enhancement Supplemental Guidance: Encrypting information for transmission protects information from unauthorized disclosure and modification. Cryptographic mechanisms implemented to protect information integrity include, for example, cryptographic hash functions which have common application in digital signatures, checksums, and message authentication codes. Alternative physical security safeguards include, for example, protected distribution systems. Related control: SC-13.

    2. TRANSMISSION CONFIDENTIALITY AND INTEGRITY | PRE / POST TRANSMISSION HANDLING
    The information system maintains the [Selection (one or more): confidentiality; integrity] of information during preparation for transmission and during reception.

    Enhancement Supplemental Guidance: Information can be either unintentionally or maliciously disclosed or modified during preparation for transmission or during reception including, for example, during aggregation, at protocol transformation points, and during packing/unpacking. These unauthorized disclosures or modifications compromise the confidentiality or integrity of the information. Related control: AU-10.

    3. TRANSMISSION CONFIDENTIALITY AND INTEGRITY | CRYPTOGRAPHIC PROTECTION FOR MESSAGE EXTERNALS
    The information system implements cryptographic mechanisms to protect message externals unless otherwise protected by [Assignment: organization-defined alternative physical safeguards].

    Enhancement Supplemental Guidance: This control enhancement addresses protection against unauthorized disclosure of information. Message externals include, for example, message headers/routing information. This control enhancement prevents the exploitation of message externals and applies to both internal and external networks or links that may be visible to individuals who are not authorized users. Header/routing information is sometimes transmitted unencrypted because the information is not properly identified by organizations as having significant value or because encrypting the information can result in lower network performance and/or higher costs. Alternative physical safeguards include, for example, protected distribution systems. Related controls: SC-12, SC-13.

    4. TRANSMISSION CONFIDENTIALITY AND INTEGRITY | CONCEAL / RANDOMIZE COMMUNICATIONS
    The information system implements cryptographic mechanisms to conceal or randomize communication patterns unless otherwise protected by [Assignment: organization-defined alternative physical safeguards].

    Enhancement Supplemental Guidance: This control enhancement addresses protection against unauthorized disclosure of information. Communication patterns include, for example, frequency, periods, amount, and predictability. Changes to communications patterns can reveal information having intelligence value especially when combined with other available information related to missions/business functions supported by organizational information systems. This control enhancement prevents the derivation of intelligence based on communications patterns and applies to both internal and external networks or links that may be visible to individuals who are not authorized users. Encrypting the links and transmitting in continuous, fixed/random patterns prevents the derivation of intelligence from the system communications patterns. Alternative physical safeguards include, for example, protected distribution systems. Related controls: SC-12, SC-13.

### SC-9 TRANSMISSION CONFIDENTIALITY
Withdrawn: Incorporated into SC-8(4).

### SC-10 NETWORK DISCONNECT
This F5 solution automatically terminates the network connection associated with a communications session at the end of the session or logs out users when the defined time-period of inactivity has elapsed and different time-period values can be be specified for connections to the system's management services: web-based Configuration utility, SSH connections, Console and TMSH. For other individual infrastructure components such as the servers and firewalls, as well as for access to the appications services and contained within this infrastructure, this is accomplished by configuration of the "Inactivity Timeout" setting in the Access policy.

### SC-17 PUBLIC KEY INFRASTRUCTURE CERTIFICATES
This F5 solution does not manage TLS/SSL PKI certificates or cryptographic material as such. However, you can select the appropriate certificates and keys for single-ended and mutual authentication of connections to external authentication/directory services.


### SC-100 SOURCE AUTHENTICATION
Control:

A. The information system allows a message recipient to verify the claimed source identifier in a message.
    Supplemental Guidance: Source authentication prevents an unauthorized party from sending a message impersonating another party. This control applies to non-session based communications and can be implemented in protocols at any layer, from IP packets to electronic mail. Related controls: IA-1, IA-2, IA-3, IA-4, IA-5, SC-8, SC-13.

    Control Enhancements:

    1. Authentication of the claimed identifier in the message is cryptographically based.
    2. The organization employs CMVP-certified cryptography for digital signature generation and verification. Refer to control SC-13.
    3. The organization employs CSE-approved cryptography and protocols to implement the authentication. Refer to control SC-13.

## 3.17 FAMILY: SYSTEM AND INFORMATION INTEGRITY
These controls would be implemented outside of this F5 solution.
