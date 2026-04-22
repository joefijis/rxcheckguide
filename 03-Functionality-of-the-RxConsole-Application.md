# 3.	Functionality of the RxConsole Application

RxConsole provides PDMP administrators and authorized users with a comprehensive set of tools to manage and monitor prescription data sharing activities within the RxCheck interstate network. The following high-level functionalities are available through the RxConsole interface:


|  | RxCheck Dashboard Monitoring |
| --- | --- |
|  | View a summary of all incoming and outgoing prescription requests associated with your PDMP on the RxCheck Dashboard. |
|  | Analytical Insights |
|  | Generate and view anonymized prescription analytics by patient or prescriber, with filtering options by county and ZIP code. |
|  | State Routing Service (SRS) Configuration |
|  | Set up and manage State Routing Service parameters for data transmission and routing.<br>Establish heartbeat and health monitoring and notifications for site connectivity and IT diagnostics. |
|  | Hub Audit Logs |
|  | Access, filter, and export comprehensive Hub Audit Logs detailing data transaction activities. |
|  | Health Care Entity (HCE) Management |
|  | Create and manage HCE site profiles.<br>Define and manage user roles associated with each HCE.<br>Configure and manage HIE subsite facilities under each HCE. |
|  | Interstate Data Sharing Control |
|  | Grant or revoke access to HCE sites for interstate data exchange.<br>Manage roles and permissions for interstate sharing. |
|  | Interstate Data Sharing Role Management |
|  | Manage roles and permissions for interstate sharing. |
|  | Integration Request Management |
|  | Review and approve or deny integration requests submitted by HCEs seeking connectivity. |
|  | Interstate Data Sharing Request Management |
|  | Review and approve or deny requests from HCEs to share data across state lines. |
|  | PDMP User Management |
|  | Administer PDMP user accounts and manage user-specific settings. |


|  | Provider Validation Management |
| --- | --- |
|  | Configure validation settings for providers using DEA numbers, National Provider Identifiers (NPI), and state license numbers. |
|  | Maintenance Scheduling |
|  | Create, monitor, and track system maintenance events. |
|  | Taxonomy Code Search |
|  | Search and view mappings related to the NCPDP Taxonomy Code. |
|  | System Status Monitoring |
|  | View system information and connectivity status for all integrated PDMP sites. |

## 3.1.	RxConsole Home Page

## 3.2.	User Roles and Privileges in the RxConsole Application

The RxConsole provides the minimum necessary privileges needed to perform their work to the individuals accessing the application. This differentiation is achieved with user roles. Within RxConsole, there are 4 main user roles:

SUPER_ADMIN *Only available to the developers of the RxCheck system.

ADMIN

VENDOR_USER

SUB_ADMIN

USER

Note: SUPER_ADMIN information is included for informational purposes only.

The ADMIN role can be further broken down into 2 sub-roles:

State—State employees or contractors with a state email address.

Vendor—Company responsible for overseeing the management of the PDMP software.

The tables below outlines the privileges by user role in the RxConsole application.


| RxCheck Console Module | ADMIN - State | ADMIN - Vendor | VENDOR_USER | SUB_ADMIN | USER |
| --- | --- | --- | --- | --- | --- |
| RxCheck Dashboard | X | X | - | - | - |
| Analytical Insights | X | - | - | - | - |
| State Routing Service | X | X | X | X | - |
| Hub Audit Logs | X | X | X | X | X |
| Healthcare Entities | X | X (view-only) | X (view-only) | - | - |
| Interstate Data Sharing | X | X | - | - | - |
| Interstate Data Sharing—Role Management | X | X | - | - | - |
| Integration Requests | X | - | - | - | - |
| Approve Interstate Data Sharing for Healthcare Entities | X | - | - | - | - |
| User Management | X | - | - | - | - |
| Provider Management | X | - | - | - | - |
| PDMP Maintenance Schedule | X | X | - | - | - |
| NCPDP Taxonomy Code Mapping | X | X | X | X | X |
| System Information | X | X | X | X | X |

A SUPER_ADMIN account is like the ADMIN-STATE role in that it has access to all the RxCheck Modules and is only available to the RxCheck system developers. Additionally, the SUPER_ADMIN role has the following privileges not available within the RxConsole Modules:

Manage State connections and HCE’s

Manage PMIX roles

Manage Bridge Connections (FEDERAL, STATE, HUB2HUB, MULTI-STATE-HCE)

Manage provider data for the state

Manage push notifications

View the state’s usage dashboard

Access to interstate data-sharing for a state for debugging

Access to interstate role management for a state for debugging

Integration requests received for a state

User management – only for creating PDMP Administrators

Admin Configuration – real-time connection status monitoring, versions, sync protocol versions, jvm parms

NCPDP Taxonomy Code Mapping

System Information

User lookup and password change

Activity logs

