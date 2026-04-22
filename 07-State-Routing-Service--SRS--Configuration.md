# 7.	State Routing Service (SRS) Configuration

Every state PDMP officially onboarded into the RxCheck system will have a routing service installed that allows it to send and receive messages from other states. Message content between states is encrypted for privacy and security purposes and can only be accessed and decrypted by the state intended to receive the message.

Note: If your state does not have an SRS currently installed, one will need to be installed before connecting to the RxCheck Hub. While you can log into the RxConsole application, some functionality will not work without the PDMP connected. The latest SRS installation files can be found here: https://rx-check.org/Hub/ConnectionTools.

One of the initial responsibilities assigned to a State PDMP Admin is the configuration of their State Routing Service (SRS). The State Routing Service is a software that facilitates the successful transmission of messages between Health Care Entities and PDMP states. Configuring the SRS is a six-step process, and each of these steps is listed below, as well as graphically depicted in the diagram on the left.

To configure the State Routing Service, the State PDMP Admin will need to enter the requested information into the data fields present under each section of the State Routing Service Configuration page. A detailed explanation of each section and its corresponding data fields are provided below.

State Routing Service Configuration Process for a PDMP State:

Site Unique Identifier/ Description.

SRS Outbound Sender Endpoint.

RxCheck Hub Service Host Endpoint.

SRS Inbound Sender Endpoint.

Site PDMP Application Endpoint.

SRS Certificate.

The following subsections contain instructions on how to configure the State Routing Service in the RxConsole application. For additional clarity, each step is accompanied by a corresponding image or screenshot that depicts the action described.

## 7.1.	Site unique identifier / description

This section covers general information about the site for which the SRS is to be configured. All data fields in this section are auto-populated based on the data that was entered by the Super Administrator when the site was initially created. The State Admin users can review the auto-populated data in this section and contact the RxCheck technical team if there are any questions or concerns.

The following screenshot depicts the configuration process for the Site Unique Identifier/ Description section. For additional clarity, the ensuing table provides a definition of each data field present in the screenshot.


| Data Field Name | Description |
| --- | --- |
| Name | The official two-letter state abbreviation code assigned to each state. <br><br>E.g., New Jersey: NJ, California: CA<br>This field is auto-populated. |
| Type | The Site Type assigned to each state is PDMP (Prescription Drug Monitoring Program).<br>This field is auto-populated. |
| Description | A brief description of the site.<br>This field is auto-populated. |
| API Key | An Application Programming Interface (API) key serves as a unique identifier for the site and is generated when the site is created. The first two letters of an API key will always represent the Name of the site.<br><br>It is a security key that is validated for SRS connections.<br>This field is auto-populated. |

## 7.2	SRS Outbound Sender Endpoint

This section enlists the standards and interfaces that are supported by the RxCheck application for all request and response transactions. This step allows State PDMP Administrators to select/enter specific details pertaining to their unique PDMP site environment.

Currently, RxConsole supports the following interfaces:

PMIX/NIEM – National Information Exchange Model

NCPDP 2017 – National Council for Prescription Drug Programs

HL7 FHIR – Health Level Seven International (HL7) Fast Healthcare Interoperability Resources (FHIR)

HTML5 – Hypertext Markup Language 5

A brief description of each type of interface is listed below:

PMIX: The PMIX Standards Organization supports the sharing of Prescription Drug Monitoring (PDMP) program Data among PDMP organizations and their stakeholders by establishing and maintaining the PMIX National Architecture and related guidelines, policies and standards to minimize the cost and complexity of sharing PDMP data across organizational, vendor, geographic and operational boundaries; enable secure, trusted exchanges of PDMP data and promote consistency among PDMPs.

NIEM: NIEM is an XML information exchange standard which specifies the foundation and building blocks for interoperable information exchange by serving as a common XML vocabulary, integrated with established information exchange standards and processes, to support cross-domain information sharing and efficient information exchange between inter-related public and private service domains (e.g., law enforcement, public safety, healthcare, etc.). NIEM enables agencies to share information that crosses system, agency, and jurisdictional borders. NIEM improves decision-making, agility, and efficiency in satisfying business needs. NIEM supports interoperability and reuse, reducing costs.

NCPDP: NCPDP is a not-for-profit, multi-stakeholder forum for developing and promoting industry standards and business solutions that improve patient safety and health outcomes, while also decreasing costs. NCPDP uses a consensus-building process to create national standards for real-time, electronic exchange of healthcare information. Their primary focus is on information exchange for prescribing, dispensing, monitoring, managing, and paying for medications and pharmacy services crucial to quality healthcare.

HL7/FHIR: HL7 are a set of international standards used to transfer and share data between various healthcare providers. It supports clinical practice and the management, delivery, and evaluation of health services by providing a framework (and related standards) for the information exchange, system integration, data sharing, and retrieval 

of electronic health information. HL7 helps bridge the gap between health IT applications and makes sharing healthcare data easier and more efficient when compared to older methods.

HTML5: It supports the rendering of information received by the user into an understandable & readable format by displaying the data on a user interface.

To configure the SRS Outbound Sender Endpoint section, the State PDMP Administrator must enter the requested information into the active data fields that fall under this section. All URL Paths and Outbound URLs for each interface are auto populated. Should there be any questions or concerns, please contact the RxCheck technical team for further assistance.

The following Screenshot depicts the configuration process for the SRS Outbound Sender Endpoint section. For additional clarity, the ensuing table provides a definition of each data field present in the screenshot.


| Heading | Data Field Name | Description |
| --- | --- | --- |
|  | Protocol | Protocols define a standardized set of rules for formatting and handling data during transmission.<br><br>State PDMP Administrators must select one of the following options from the dropdown menu:<br>HTTP (HyperText Transfer Protocol) – A basic protocol used for transmitting text-based data between a client (e.g. browser) and a server. HTTP does not provide encryption, making it less secure for transmitting sensitive information.<br>HTTPS (HyperText Transfer Protocol Secure) – An enhanced version of HTTP that uses encryption and authentication mechanisms. HTTPS ensure secure communication be leveraging Secure Socket Layer (SSL) or Transport Layer Security (TLS), and is the recommended protocol for transmitting PDMP data within the RxCheck infrastructure. |
|  | Domain | The domain name of the server on which the SRS is running.<br>This field is optional – If no domain is specified the system will use the IP Address.<br>E.g. New Jersey: NJ.gov |
|  | Port Number | A port is a communication endpoint, and a port number is a logical number assigned to it. The port number indicates the dedicated port that will be used by the SRS software for communication purposes.<br>Port numbers are used to direct incoming network traffic to the appropriate process or service on a server, ensuring that messages reach the correct application for handling. |
|  | IP Address | An Internet Protocol (IP) Address is a unique numerical identifier assigned to each device that is connected to a network that uses the Internet Protocol for communication.<br>The IP Address field is populated as “localhost” by default. |
| Heading | Data Field Name | Description |
| NIEM | PMIX Outbound URL | A fully qualified URL for the NIEM Service on Outbound SRS.<br>This field is auto-populated. |
| NCPDP-2017 | NCPDP-2017 Outbound URL | A fully qualified URL for the NCPDP 2017 Service on Outbound SRS.<br>This field is auto-populated. |
| HL7 FHIR | FHIR Outbound URL | A fully qualified URL for the FHIR Service on Outbound SRS.<br>This field is auto-populated. |
| HTML | HTML Outbound URL | A fully qualified URL for the HTML Service on Outbound SRS.<br>This field is auto-populated. |
| Security Credentials: (HTTP Basic Authentication) | Outbound Username | A username to authenticate the SRS connection on the RxCheck network. |
| Security Credentials: (HTTP Basic Authentication) | Outbound Password | A password to authenticate the SRS connection on the RxCheck network. |

## 7.3.	RxCheck Hub Service Host Endpoint

The RxCheck Hub Service Host Endpoint section is a critical part of configuring the hub connection with the RxConsole application. The RxCheck Hub, a core component of the PMIX architecture, functions as a fully operational data-sharing system that allows states to securely and efficiently exchange Prescription Drug Monitoring Program (PDMP) data with other states and integration partners (e.g. Health Information Exchanges (HIE) and Electronic Health Records (EHR).

All data fields in this section are auto-populated by the system, based on the information originally entered by the Super Administrator during site creation. State PDMP Administrators can review this information and should contact the RxCheck technical team if any discrepancies or concerns arise.

The screenshot below shows the configuration interface for this section. The accompanying table provides details descriptions for each data field presented.


| Data Field Name | Description |
| --- | --- |
| Protocol | This value cannot be changed and is set to “HTTPS”. |
| Domain | This value cannot be changed and is automatically set to the hub domain name. |
| Port Number | This value cannot be changed and is automatically set to the port on which the Hub is running. |
| IP Address | This value cannot be changed and is automatically set to the IP address for the Hub. |
| PMIX2 Hub Endpoint URL | This field is auto-populated. It is a fully qualified URL for the PMIX2 NIEM4 service on the RxCheck Hub. |

## 7.4.	SRS Inbound Sender Endpoint

The SRS Inbound Sender Endpoint configuration enables the State PDMP system to receive incoming queries initiated by other states. To complete this configuration, the State PDMP Administrator must input the required information into the specified data fields within this section.

The screenshot below illustrates the configuration interface for the Inbound Sender Endpoint. For additional clarity, the following table provides detailed descriptions of each data field shown in the screenshot.


| Heading | Data Field Name | Description |
| --- | --- | --- |
|  | Protocol | This value can be set to “HTTP” or “HTTPS”. |
|  | Domain | The official website address of the PDMP’s Inbound Service instance.<br>This field is optional – if the domain is not provided, the system will automatically take the IP address. |
|  | Port Number | Port number where the Inbound Service is configured. |
|  | IP Address | IP address where the Inbound SRS is hosted. |
|  | PMIX2 Inbound URL | This field is auto-populated based on the values selected/entered in the Protocol, Domain, IP address, and Port number fields. It is a fully qualified URL for PMIX2 NIEM4 Service on Inbound. |
|  | IEPD | This field is auto-populated based on IEPD option selected by Super Administrator at the time of PDMP Site creation. The value indicates the type of PDMP site. This indicates the PMIX version supported by PDMP. |
| Rate Limiting | Rate Limit | If a value is entered for this field, it indicates the number of Requests to the inbound with respect to the defined time unit. |
| Rate Limiting | Time Unit | Defines the unit for the value entered in the Rate Limit field. Can be set to Second, Minute, Hour, Day, or Month. |


| Heading | Data Field Name | Description |
| --- | --- | --- |
| Enable Loopback (Same Site Outbound can call same site inbound) | Enable Loopback | This is a toggle button. When enabled (blue), it indicates that the users in the PDMP state can make Prescription Data requests to the same PDMP State. <br>For example, if it is enabled for the PDMP State of NJ, it will indicate that NJ users can send the Prescription Data Requests to NJ.<br>If the box is gray, it is disabled. |
| Security Credentials (HTTP Basic Authentication) | Inbound Username | A username to authenticate the SRS connection in the RxCheck network. |
| Security Credentials (HTTP Basic Authentication) | Inbound Password | A password to authenticate the SRS connection in the RxCheck network. |

## 7.5.	Site PDMP Application Endpoint

This section defines the technical parameters of the state’s PDMP application necessary for message routing and integration. To configure this section, the State PDMP Administrator must enter the required information into the designated data fields.

The screenshot below demonstrates the configuration interface for this section. For additional clarity, the accompanying table provides descriptions for each data field shown in the screenshot.


| Heading | Data Field Name | Description |
| --- | --- | --- |
|  | Protocol | This value can be set to “HTTP” or “HTTPS”. |
|  | Domain | The website address of the PDMP state.<br>This field is optional – if the domain is not provided, the system will automatically take the IP address. |
|  | Port Number | Port number where the website is hosted. |
| Heading | Data Field Name | Description |
|  | IP Address | IP address of the state PDMP server where the website is hosted. |
|  | URL Path | This is the base URL or path for the PDMP Application endpoint for all the requests. The value for this field is based on the IEPD option selected by Super Administrator at the time of PDMP Site creation. |
|  | PDMP URL | This field is auto-populated based on the values selected/entered in Protocol, Domain/IP Address, Port Number. |
| Security Credentials (HTTP Basic Authentication) | Inbound Username | A username and is an optional parameter which enables basic authentication on PDMP Site. |
| Security Credentials (HTTP Basic Authentication) | Inbound Password | A password and is an optional parameter which enables basic authentication on PDMP Site. |

## 7.6.	SRS Certificate

Each state is responsible for generating its own digital certificate using Microsoft PowerShell. Detailed instructions for this process are provided in the SRS Installation Guide for PDMP.

The certificate, created by the PDMP state implementing the SRS software, supports secure end-to-end message encryption. The SRS certificate uses a public key/private key infrastructure:

The public key (contained in the certificate) is used to encrypt outgoing messages.

The private key is used by the receiving system to decrypt the message.

Important: The certificate includes two components:

Private Key—Must be kept confidential and never shared, including within the RxCheck Network.

Public Key—Uploaded to the RxConsole and shared with other participating states in the RxCheck Network.

The State PDMP Administrator must input the required data into the fields provided under the SRS Certificate section.

The screenshot below illustrates the configuration interface for this section. For added clarity, the subsequent table provides descriptions for each data field shown in the screenshot.


| Data Field Name | Description |
| --- | --- |
| Private Key Subject | The key generated at the time of Site Certificate creation. The private key is in .pfx format. The Private key must be kept confidential by the PDMP State. |
| Public key (DER Format) | The key generated at the time of Site Certificate creation and is in .der format. The Public key is shared by the PDMP State with other PDMP States in the RxConsole Application. |
| Certificate Expiry Date | The date when the uploaded certificate expires. |

## 7.7.	Configure the SRS

Once the previous sections have been populated on the State Routing Service Configuration page, the State PDMP Administrator can save the details and complete the configuration process.


| Click on the State Routing Service Configuration button, located on the left-hand side of the screen. |  |
| --- | --- |
| Enter all required information. Mandatory fields are designated by a red asterisk (*) and need to be populated for the form to be saved successfully.<br>You may need to click on the box for each step to expand that section and reveal the fields. |  |
| Click the Save button |  |

## 7.8.	Configuring the required fields

Each State PDMP Administrator can configure the PMIX fields required in the request message to search for a patient in the PDMP system. The name-matching algorithm implemented within the PDMP system determines these required fields.

A PDMP administrator can configure these fields by navigating to the SRS Configuration page and clicking on the Patient Required Fields button.

Set the required fields for the patient prescription drug history (PPDH) and the patient prescription picklist (PPPL) queries.

When processing an integration request involving a federated query, you can choose to enforce your state’s data requirements by enabling the Home State Priority option. This will reject the entire request if it does not meet the required fields defined by your state.

## 7.9.	Heartbeat and Health Monitoring

RxConsole includes the functionality to monitor the SRS when one is connected (See previous section titled Configure the SRS for steps on connecting the SRS). Monitoring is important to gain a better understanding of how the SRS and RxCheck are functioning and if there are any issues with integrations. The subsections below explain the health monitoring available to RxConsole users.

### 7.9.1	Current Site Monitoring


| Click on the State Routing Service button, followed by the Heartbeat & Health Monitoring option, located on the left-hand side of the screen. |  |
| --- | --- |
| By default, you will be at the current site SRS: Heartbeat and Health Monitoring screen. | By default, you will be at the current site SRS: Heartbeat and Health Monitoring screen. |
|  |  |
| This screen includes various graphs to show the current status of the SRS. <br><br>Note: The table at the end of this section includes additional information regarding what is monitored in each graph. | This screen includes various graphs to show the current status of the SRS. <br><br>Note: The table at the end of this section includes additional information regarding what is monitored in each graph. |
| A user can click the Refresh button to get the most up to date information regarding their SRS. |  |
| A user can click the Show last 10 Pings button to view a table of the last 10 pings to the SRS. <br><br>Note: The headers in the table are described in the following table. |  |


| Header | Description |
| --- | --- |
| DeviceID | An identification code that references the device that pinged the SRS. |
| Host | A reference code to identify the RxConsole state and version that pinged the SRS. |
| InstanceID | Identification of the instance of the SRS that was pinged. |
| IP# | The IP address of the instance of the SRS that was pinged. |
| Site Code | The two letter code that references the state. |
| Time Stamp | The date and time the ping occurred. |


| Graph Title | X-Axis | Y-Axis | Description |
| --- | --- | --- | --- |
| Status over a period of time with Timeline Bar | Time | Status—Up/Down | The status of the SRS over a period of time. |
| Instance Status | Time | Status—Up/Down | The status of the SRS over a period of time, allows you to use the dropdown to switch the instance. |
| JVM Threads | Time | Number of JVM Threads | Displays the number of active Java Virtual Machine (JVM) threads at regular time intervals. Rising lines may indicate increased load or usage and falling lines may suggest stable or reduced activity. |


| Graph Title | X-Axis | Y-Axis | Description |
| --- | --- | --- | --- |
| Garbage Collectors | Time | Time spent collecting and releasing the memory | Indicates how much time garbage collection took. Helps to identify memory issues which can impact application responsiveness. |
| CPU | Time | Percent usage | The amount of processing power used over time. |
| JVM Memory | Time | Size of JVM memory | Helps to detect trends such as memory growth, potential memory leaks, or inefficient memory usage patterns. |
| Disk Space Used | Time | Size of disk space | Helps identify storage trends, which may signal the need for a cleanup or capacity planning. |

### All Sites Monitoring

To navigate to All Sites monitoring, follow the steps below.


| Click on the State Routing Service button, followed by the Heartbeat & Health Monitoring option, located on the left-hand side of the screen. |  |
| --- | --- |
| Click on the All Sites button in the top right corner of the screen. | Click on the All Sites button in the top right corner of the screen. |
|  |  |
| The next screen is the SRS: Heartbeat and Health Monitoring screen and includes a United States Map. | The next screen is the SRS: Heartbeat and Health Monitoring screen and includes a United States Map. |
|  |  |
| The map allows you to hover your cursor over a state and get the current status of their SRS server.<br><br>Note: The states are color coordinated based on their SRS status. Please see the following table to better understand the colors. |  |
| Scrolling down on this screen, you are able to see a list of the States and their connection status in a table. The table also allows you to see the most recent query to or from a state.<br><br>Note: The following table includes a description of each of the table headers. | Scrolling down on this screen, you are able to see a list of the States and their connection status in a table. The table also allows you to see the most recent query to or from a state.<br><br>Note: The following table includes a description of each of the table headers. |
|  |  |
| You can search for a specific site by:<br>Finding the state on the list using the page buttons under the table, or<br>Searching for the state in the search box above the table. |  |
| Scrolling down further, the last table displays a list of the connected healthcare entities and the last time a query was received from them. A healthcare entity can be found by:<br>Using the page buttons on the bottom of the table and looking for the entity, or<br>Search for the site in the search bar above the table. |  |


| Status | Color Code | Color |
| --- | --- | --- |
| Up | Green |  |
| Down | Yellow |  |
| N/A | Gray |  |
| Currently Hovering | Blue |  |

PDMP Transaction Status Table


| Heading | Description |
| --- | --- |
| Name | Name and 2 letter abbreviation for the state. |
| From [State Code] (Outbound) | The date and time of the last query from your state to listed state. |
| To [State Code] (Inbound) | The date and time of the last query from this state to the users state. |
| Connection Status | The current status of that states SRS. |

HCE Transaction Status to TT (Inbound)


| Heading | Description |
| --- | --- |
| Name | The HCE code to identify the appropriate healthcare entity. |
| Last Transaction Timestamp | The date and time of the last query from the healthcare entity to your state PDMP. |

## 7.10.	Heartbeat notifications

Using the Heartbeat Notifications feature, the PDMP Administrator can subscribe to receive email notifications and text messages about the PDMP and HCE connections.

To navigate to the Heartbeat notifications, follow the instructions below.


| Click on the State Routing Service button, followed by the Heartbeat Notifications option, located on the left-hand side of the screen. |  |
| --- | --- |


| Select the desired boxes to subscribe to that notification.<br>If the Email option is checked, the user will receive emails to the mailbox associated with their RxConsole application login.<br>If the SMS option is checked, the user will receive text messages on the mobile phone number specified in their RxConsole application profile.<br><br>Note: You will need to email the RxCheck admin to add a phone number to enable the SMS notifications option. |  |
| --- | --- |
| After making any changes, a user will want to press the Save button to process any changes made to notifications. |  |

The table below explains the different subscription options that a PDMP administrator can subscribe to.


| Heading | Subscription Option | Description |
| --- | --- | --- |
| PDMP Connection | Your PDMP SRS | Receive alerts for connection disruptions that affect your state connection to the Hub. |
| PDMP Connection | Performance | Receive alerts for performance degradation in SRS instances affecting your state connection. |
| PDMP Connection | Partnering PDMP SRS | Receive alerts for connection disruptions for partnering states connected to yours. |
| HCE Connection | Integration SRS | Receive alerts for connection disruptions that affect integration connection to the Hub. |

Note: Notifications are not immediate. A subscribed user will receive an email or SMS notification approximately 15 minutes after the first missed heartbeat is detected.

