# 9.	Healthcare Entities

A Healthcare Entity (HCE) refers to any licensed healthcare provider or organization that is authorized by its respective state to deliver professional healthcare services. This includes:

Individual providers licensed to practice healthcare,

Healthcare organizations employing licensed professionals, and

eHealth Exchange organizations recognized by the state for providing licensed healthcare services.

A healthcare entity can only submit patient data requests and receive responses through RxCheck after it has been officially onboarded into the state’s RxCheck system.

When a new healthcare entity expresses interest in participating in RxCheck, the State PDMP Administrator can initiate onboarding by creating a new entity site. This is done by clicking the 
+ Add Site button located in the top right corner of the Healthcare Entities page.

Administrators can also view and manage existing healthcare entity records associated with their state. The full list of onboarded entities can be accessed by selecting the Healthcare Entities icon from the left-hand navigation panel.

The screenshot below displays an example list of onboarded healthcare entities within a state’s PDMP system. The accompanying table provides definitions for each column heading show in the interface.


| Heading | Description |
| --- | --- |
| Name | The name of the healthcare entity (HCE). |
| Code | A six-character code that follows the following format:<br>Two letters to represent the state code.<br>An underscore (_).<br>Three letters to represent a HCE site. |
| Status | Indicates the current status of an HCE. <br>Active- the HCE is currently active.<br>Inactive- the HCE is currently inactive.<br>Firewall Pending- the HCE is currently active but was recently set up. |
| Integration Type | Refers to the site type value that was selected when the HCE was created. This value will be displayed as one of the following:<br>EHR – Electronic Health Records<br>EMR – Electronic Medical Records<br>HIE – Health Information Exchange<br>PDS – Pharmacy Dispensing System |
| Vendor | The integration vendor for the healthcare entity. |
| Site Added | Date and time when the HCE site was created. |

## 9.1.	Add a new healthcare entity site


| Click on the Healthcare Entities button, located on the left-hand side of the screen. |  |
| --- | --- |
| Click on the + Add Site button. |  |
| Populate the Site Configuration Details for the new healthcare entity.<br>Refer to the “Breakdown of Healthcare entity site details” section below for field-specific guidance. |  |
| To populate the “Select Vendor” field, you must first click on the small lock symbol within the field. |  |
| To exit without saving, click the Cancel button. |  |
| To save the populated site information, press the Save button. |  |
| Wait patiently as your site is being created. |  |
| Populate additional details as requested in the corresponding data fields for each section.<br><br>Refer to the “Breakdown of Healthcare entity site details” section below for field-specific guidance. |  |

## 9.2.	Breakdown of Healthcare entity site details

Once a healthcare entity record is created, the user will be able to add, view and manage the following details by clicking on the respective menu options.

The following subsections provide a detailed breakdown of each data field, as displayed on each menu option/section of a healthcare entity’s record.

### 9.2.1.	Site Details

This section displays information related to this specific HCE.


| Heading | Description |
| --- | --- |
| Healthcare Entity Name | The name of the Healthcare Entity. |
| Site Code | A six-character code that follows the following format:<br>Two letters to represent the state code. This is auto-populated.<br>An underscore (_).<br>Three letters to represent a HCE site. These are entered by the PDMP administrator.<br>When deciding on the three letters to represent a HCE, think of the initials for the company. Planning is often beneficial to avoid creating abbreviations that lead to confusion. One site code can cover multiple individual facilities within a state.<br>Example: Walmart may be WLT or WAL, where Walgreens may be WGN or WAL. |
| Site Type | Refers to the site type. This value can be set as one of the following:<br>EHR – Electronic Health Records<br>EMR – Electronic Medical Records<br>HIE – Health Information Exchange<br>PDS – Pharmacy Dispensing System |
| Description | A simple description of the HCE site. |
| Status | Status that indicates if a site is Active or Inactive. |
| Interstate Query | When checked, the HCE will be able to send interstate data requests. |
| Select Vendor | The integration vendor providing services to this healthcare entity. |
| Number of Prescribers with DEA numbers | A count of prescribers with DEA numbers at that HCE. |
| Number of Pharmacists | A count of pharmacists at that HCE. |
| Number of Prescribers (Include All Providers With Prescriptive Authority) | A count of all prescribers at that HCE. |
| Select Interfaces | The type of connection the HCE is using to connect to RxCheck or third-party integrator. The following options are available:<br>NCPDP2017<br>HTML<br>FHIR3<br>FHIR4<br>PMIX2<br>JSON |

### 9.2.2.	Contact Details

This section contains the primary and secondary contact information for individuals to contact for further inquiries related to this specific HCE.


| Heading | Description |
| --- | --- |
| First Name | Individual contact person’s first name. |
| Last Name | Individual contact person’s last name. |
| Phone Number | Individual contact person’s phone number. |
| Extension | Individual contact person’s phone number extension, if any. |
| Email Address | Individual contact person’s email address. |

### 9.2.3.	Vendor Details

This section contains the SRS hosting details and indicates if the healthcare entity’s integration is managed by the HCE IT team, the state, or by a vendor.


| Heading | Description |
| --- | --- |
| HCE IT | This option indicates that the IT team of the HCE oversees the SRS hosting and managing responsibilities. |
| State | This option indicates that the IT team of the state oversees the SRS hosting and managing responsibilities. |
| Vendor | This option indicates that a third-party vendor (not the HCE) oversees the SRS hosting and managing responsibilities. |

Note: If the Vendor option is chosen, additional fields need to be populated.


| Heading | Description |
| --- | --- |
| Where is it Hosted | Refers to where the vendor hosts the SRS server for the HCE. The following options can be selected.<br>HCE IT INFRA – Hosted by the healthcare entity’s infrastructure.<br>Vendor IT INFRA – Hosted by the vendors infrastructure.<br>Private Cloud – Hosted on a private cloud, accessible by only the HCE and/or vendor.<br>Government Cloud – Hosted on a government cloud, accessed by individuals outside the HCE or state PDMP team. |
| Vendor Name | The name of the vendor hosting the SRS. |
| Heading | Description |
| Vendor Address | The address of the vendor hosting the SRS. |
| Vendor Contact | The name of the contact responsible for managing the SRS. |
| Are the servers being accessed outside the US? | A Yes or No question that asks if the SRS will be accessed for any reason outside the United States of America. |

### 9.2.4.	Manage Roles

This section enables the State PDMP Administrator to assign roles that authorize specific users within a healthcare entity to submit prescription data requests. Roles are assigned by selecting the appropriate tags associated with the healthcare entity.

Each tag corresponds to a recognized healthcare professional role or the type of services provided by the entity. These role assignments determine the level of access and functionality available to the entity within the RxCheck system.

All available roles are displayed by default as shown below. Clicking on a role will change the role to green. A green highlighted role is active or “Selected” and allows that role to initiate a query, while an off-white color indicates that the role is “Authorized” but inactive and cannot initiate a query.


| Button Name | Button Image | Functionality |
| --- | --- | --- |
| Assign All |  | Automatically selects all displayed roles. |
| Clear All |  | Automatically deselects all displayed roles. |
| Show List |  | Will display all available roles in two separate lists, an Authorized Roles list and a Selected Roles list. |
| Hide List |  | Will display all available roles as tags (default).<br>Note: This option is only available when the roles are displayed as two separate lists. |

A screenshot of the Show List option is shown below and will only be displayed if the Show List button is clicked.

Clicking on a blue arrow transfers a role from the Authorized Roles list to the Selected Roles list. Clicking on an orange arrow transfers a role from the Selected Roles list to the Authorized Roles list.

### 9.2.5.	Manage Facilities

This section provides details of the facilities related to this specific healthcare entity. These facilities and their active/ inactive statuses will be created and determined by the RxCheck PDMP Administrator or Super Administrator.

There are two buttons available to an RxConsole user.


| Button Name | Button Image | Functionality |
| --- | --- | --- |
| Add Facility |  | Will display the Facility popup to enter a single facility. |
| Add Multiple Facilities |  | Will redirect the PDMP administrator to the Add Facilities page. |

9.2.5.1. How to add a single healthcare facility


| Click on the Add Facility button. |  |
| --- | --- |
| In the pop-up window, enter the requested information in the appropriate data fields.<br><br>To see a description of each field, see the table below. |  |
| Click on the Save button to save the populated information. |  |


| Heading | Description |
| --- | --- |
| Name | Individual facility’s name. |
| Facility Type | Individual facility type. Options include:<br>EHR – Electronic Health Record<br>PDS – Pharmacy Dispensing Software |
| Facility Code | Code specific to this individual facility. The HCE code is auto-populated, but the facility code is entered as an alphanumeric value. |
| First Name | Contact person’s first name at this individual facility. |
| Last Name | Contact person’s last name at this individual facility. |
| Email | Contact person’s email at this individual facility. |
| Phone | Contact person’s phone number at this individual facility. |
| Extension | Contact person’s phone number extension at this individual facility, if any. |

9.2.5.2. How to add multiple healthcare facilities


| Click on the Add Multiple Facilities button. |  |
| --- | --- |
| You will be directed to the Add Facilities screen. |  |
|  |  |
| Click on the Standardized Facilities Template link to download a template to populate. The template will download in an Excel workbook format (.xlsx). <br><br>The first tab titled Facilities File Template contains columns to enter the same information available when adding a single facility. A table describing each heading is available in the previous subsection.<br><br>The second tab titled Field Definitions provides an abbreviated summary of each field, its requirement status, and an example. |  |
|  |  |
| Populate the Standardized Facilities Template with each facility occupying a single row. |  |
| Press the Click to select file button to choose the populated template to upload into the system. |  |
| If all facilities share a single contact person, you can check the box labeled One contact for all facilities and data fields for that individual person will appear.<br><br>A description of these fields can be found in the table in the previous subsection.<br><br>Note: If contact information is included in both the uploaded data file and the UI (via “One contact for all facilities”), the UI entry will override and apply to all created facilities. |  |
|  |  |
| Click the Upload button to import the data populated in the file you selected in step 5. |  |
| The Cancel button will discard any changes made on this screen and return the user to the previous page. |  |

### 9.2.6.	User Administration

This section lists details of the administrator(s) specific to this healthcare facility.


| Heading | Description |
| --- | --- |
| Email | The email address used by the user to log into the RxConsole application. |
| Name | The first and last name of the HCE user. |
| Site Name | The HCE site code. |
| Status | The status of the HCE user account. |
| User Type | The type of account the HCE user has. This is typically displayed as SUB_ADMIN. |

A State PDMP Administrator is allowed to add a new administrative user for a HCE following the steps below.


| Click the Add User button to open a popup window. |  |
| --- | --- |
| In the popup window, enter the requested information into the appropriate data field. <br><br>A description of each field is available in the following table. |  |
| Click the Save button to save the information populated in the fields. |  |


| Heading | Description |
| --- | --- |
| Email | The contact email for the HCE user and username for RxConsole. |
| Password | The password for the HCE user to access the RxConsole application. |
| Site Code | The site code for the HCE user. This field will be auto-populated. |
| First Name | The HCE user’s first name. |
| Middle Name | The HCE user’s middle name. |
| Last Name | The HCE user’s last name. |
| Status | The status of this HCE user’s account. Can be set to either Active or Inactive. |
| Phone Number | The HCE user’s phone number. |

## 9.3.	Open a healthcare entity record


| Click on the Healthcare Entities button, located on the left-hand side of the screen. |  |
| --- | --- |
| Find the healthcare entity using one of two methods:<br>Scroll through the list on the screen (may need to navigate to the next screen by using the navigation arrows at the bottom of the list)<br>Type the name of the HCE into the search bar labeled Global Filter in the top right. |  |
|  |  |
| Select the desired healthcare entity to view further details about that facility. |  |
| To edit a record, make your changes and click the Save button to ensure any new information is recorded.<br>To exit without saving, click on the Cancel button. |  |

## 9.4.	Export a list of your HCE’s and Facilities

RxConsole supports the ability for a State PDMP Administrator to export a list of their healthcare entities and the facilities under those healthcare entities.


| Click on the Healthcare Entities button, located on the left-hand side of the screen. |  |
| --- | --- |
| In the top-right corner, there are two buttons to extract either:<br>Export HCE’S—Downloads a list of healthcare entities, their HCE code, and their status.<br>Export Facilities—Downloads a list of Facilities, their site code, and their status.<br><br>Note: The HCE and facility lists are downloaded in a zipped folder. Please see the tables in previous sections for a description of the columns in these files. |  |
| Right-click on the zipped folder to view options |  |
| Select the “Extract All…” option. |  |

HCE Export Columns


| Heading | Description |
| --- | --- |
| Code | A six-character code that follows the following format:<br>Two letters to represent the state code.<br>An underscore (_).<br>Three letters to represent a HCE site. |
| Name | The name of the Healthcare Entity. |
| Status | Status that indicates if a site is Active or Inactive. |

Facility Export Columns


| Heading | Description |
| --- | --- |
| Code | A facility code specific to that individual healthcare facility. |
| Name | The name of the facility. |
| Status | Status that indicates if the facility is Active or Inactive. |

