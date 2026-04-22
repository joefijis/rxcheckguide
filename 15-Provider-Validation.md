# 15.	Provider Validation

The term “Provider” refers to a licensed healthcare professional or organization legally authorized to deliver medical services to the public. Federal regulations recognize a wide range of provider types, including pharmacies, physicians, and nurse practitioners.

Most providers in the US are uniquely identified by a 10-digit National Provider Identifier (NPI), issued by the Centers for Medicare and Medicaid Services (CMS). Additionally, the Drug Enforcement Agency (DEA) in the US also assigns practitioners with a DEA Registration Number, authorizing them to prescribe controlled substances. Providers must also hold a valid state license, evidenced by a State License Number (SL#) specific to the state in which they practice.

Whenever a healthcare entity sends or receives a prescription data request via RxCheck, the provider’s NPI, DEA, and/or SL# is included in the data payload.

The Provider Validation feature in RxConsole allows State PDMP Administrators to configure whether the validation of the NPI, DEA, SL# and/or OTHER# is required, optional, or not validated prior to processing a request.

The following section explains each option in detail.

## 15.1.	View and add a datasource for provider validation


| Click on the Provider Management button, followed by the Provider Datasource option, located on the left-hand side of the screen. |  |
| --- | --- |
| The Datasources screen allows you to view previously uploaded datasources.<br><br>Refer to the following table for a description of each column header. |  |
|  |  |
| To add a new provider datasource, press the Add Datasource button.<br>For instructions on adding a new datasource, see the subsection titled, Add a new Datasource file later in this guide. |  |
| To view a previously entered datasource, click on a datasource name in the List of Datasources. |  |


| Header | Description |
| --- | --- |
| Datasource Name | The name entered by the PDMP administrator referencing this unique datasource. |
| Datasource Type | Identifies the datasource type as a File or API. |
| API URL | The URL for the API to call for provider identification. |
| Auth Type | The authorization method for calling the API. |
| Records | The number of records on the datasource in this row. |
| Created Date | The date and time the datasource was added into the RxConsole. |

### 15.2.	View, delete, and search an existing datasource


| Follow steps 1, 2, and 4 under the section titled View and add a datasource for provider validation in this guide to view an existing datasource. | Follow steps 1, 2, and 4 under the section titled View and add a datasource for provider validation in this guide to view an existing datasource. |
| --- | --- |
| The new screen will look similar to the Add Datasource screen, but includes a section labeled Search Provider. | The new screen will look similar to the Add Datasource screen, but includes a section labeled Search Provider. |
|  |  |
| To see if an existing datasource file contains a provider, you can enter the DEA#, NPI#, SL# or OTHER# in the Search Provider section to see if that provider exists on the datasource you are viewing.<br>If the provider is on the list, you will see their information returned under the Search Provider section.<br>If the provider is not on the list, you will see “No Provider found.” Under the Search Provider section.<br><br>Note: The datasource search feature is only available for datasource files and cannot be used on a datasource API. |  |

### 15.2.1.	Create a datasource file


| Open Microsoft Excel on your computer. |  |
| --- | --- |
| Create a new blank workbook. |  |
| Add your desired headers in any order you prefer. The names of the possible headers are:<br>First Name<br>Last Name<br>NPI#<br>DEA#<br>SL#<br>OTHER#<br><br>Note: The header names should be entered in cells A1, B1, C1, D1, E1 and F1.<br><br>Note: Not all header names are required and any combination of headers can be used (For example, if a state administrator does not want to use the DEA number, the may elect to remove that header completely. |  |
| Populate the relevant information under the corresponding column.<br><br>Note: Duplications in the First Name and Last Name column are expected and will not affect provider validation. |  |
| When finished building your datasource file, save the file as either a .csv (Comma Separated Values (CSV)) or .xlsx (Excel workbook). |  |

### 15.2.2.	Add a new datasource file


| Follow steps 1-3 under the section titled View and add a datasource for provider validation in this guide. |  |
| --- | --- |
| Select the “File” option under the Datasource Type dropdown.<br><br>Note: Selecting the File option, allows a PDMP administrator to upload a .csv (CSV) or .xlsx (Excel workbook) . |  |
| Enter a name for your datasource file in the text field labeled, Datasource Name. <br><br>Note: The name does not need to match your datasource file. The name in this field can be up to 15 alphanumeric characters (Spaces and special characters are not allowed). |  |
| Press the Select File button under the Data Upload section. <br>Find your datasource file using the system dialog window. |  |
| Select your import type:<br>Full – will import the entire datasource file under the name you entered in step 3.<br>Delta – this is only available when viewing a previous datasource (see previous section titled, View and add a datasource for provider validation for instructions to view a previous datasource). |  |
| Check the fields that are present in your datasource file. If you did not include a field, you can leave box unchecked.<br>After checking the box, you will need to set the sequence. This refers to the order of the columns in your datasource file. <br><br>Note: Column A is sequence “0”, Column B is sequence “1”, etc.<br><br>Example: Using step 3 from the previous subsection, you can see how the sequence is populated in the screenshot for this step. |  |
| Press the Save button on the right corner of the screen to add your datasource file to the RxConsole for your state. |  |
| Alternatively, if you do not wish to add your data source you can press the Cancel button to discard changes and return to the previous screen. |  |
| Verify your datasource file was successfully added by looking for the Alert that states, “Provider Data is Uploaded”<br><br>You will also return to the Datasource screen and should see your datasource in the List of Datasources. |  |

### 15.2.3.	Add a datasource API


| Follow steps 1-3 under the section titled View and add a datasource for provider validation in this guide. |  |
| --- | --- |
| Select the “API” option under the Datasource Type dropdown. |  |
| Enter the API URL into the field labeled API URL. |  |
| Select the appropriate authorization type using the Auth Type dropdown. |  |
| For BASIC authorization, enter the username and password. |  |
|  |  |
| For OAUTH2 authorization, enter the Client ID, Client Secret, and Auth URL into their respective fields. | For OAUTH2 authorization, enter the Client ID, Client Secret, and Auth URL into their respective fields. |
|  |  |
| Press the Save button on the right corner of the screen to add your datasource API to the RxConsole for your state. |  |
| Alternatively, if you do not wish to add an API you can press the Cancel button to discard changes and return to the previous screen. |  |
| Verify the datasource API was successfully added by looking for the Alert that states, “Datasource Created”.<br><br>You will also return to the Datasource screen and should see your datasource in the List of Datasources. |  |

## 15.3.	Configure provider validation options

### 15.3.1.	Modify an existing provider validation


| Click on the Provider Management button, followed by the Provider Validation option, located on the left-hand side of the screen. |  |
| --- | --- |
| The Provider Validation screen allows you to view a list of existing validations that have been added and includes a button to add a new provider validation.<br><br>Note: The names of the headers are described in the table following these steps. |  |
| To view and/or modify an existing validation, click on the name of a validation. |  |
| The following screen allows you to change settings related to the existing validation.<br>Name – change the name of the validation settings.<br>Select Roles – change the roles that are subject to validation.<br>Validation Type – if Mandatory is chosen, a query will fail if the fields are not present, while Validate will stop a query if the validation check fails.<br>Datasource – allows you to select a datasource to reference for the validation check. (Only present if validate is chosen for the Validation Type.)<br>Selection – if All is chosen, all boxes checked in the Validation Field(s) selection will be checked for validation. If Any is chosen, only one of the numbers must pass for the validation to be successful.<br>Validation Field(s) – allows you to check which ID numbers are subject to validation. | a) <br>b) <br>c) <br>d) <br>e) <br>f) |
| Press the Save button on the right corner of the screen to record your changes to provider validation to the RxConsole for your state. |  |
| Alternatively, if you do not wish to proceed with your changes, you can press the Cancel button to discard changes and return to the previous screen. |  |
| Verify the Provider Validation was successfully updated by looking for the Alert that states, “Provider Validation Updated”.<br><br>You will also return to the Provider Validation screen and should see your changes in the List of Provider Validations. |  |


| Header | Description |
| --- | --- |
| Name | The name given to this specific set of validation rules. |
| Datasource Name | The name of the datasource that is referenced for validation. |
| Validation Fields | The identification numbers that are subject to validation. |
| Validate Type | The type of validation occurring, Mandatory will stop a query if the fields are not present, while Validate will stop a query if the validation check fails. |
| Created Date | The date and time the validation rules were created. |

### 15.3.2.	Add a new provider validation


| Click on the Provider Management button, followed by the Provider Validation option, located on the left-hand side of the screen. |  |  |
| --- | --- | --- |
| To add a new set of validation rules, click on the Add Provider Validation button. |  |
| The following screen allows you to add settings related to the new validation rules.<br>Name – assigns a name to the validation settings.<br>Select Roles – add the roles that are subject to validation. Clicking the checkbox next to the search box will select/deselect all.<br>Validation Type – if Mandatory is chosen, a query will fail if the fields are not present, while Validate will stop a query if the validation check fails.<br>Datasource – allows you to select a datasource to reference for the validation check. (Only present if validate is chosen for the Validation Type.)<br>Selection – if All is chosen, all boxes checked in the Validation Field(s) selection will be checked for validation. if Any is chosen, only one of the numbers must pass for the validation to be successful.<br>Validation Field(s) – allows you to check which ID numbers are subject to validation. | a) <br>b) <br>c) <br>d) <br>e) <br>f) |
| Press the Save button on the right corner of the screen to add your new provider validation rules to the RxConsole for your state. |  |
| Alternatively, if you do not wish to proceed, you can press the Cancel button to discard changes and return to the previous screen. |  |
| Verify the Provider Validation was successfully created by looking for the Alert that states, “Provider Validation Created”.<br><br>You will also return to the Provider Validation screen and should see your new rules in the List of Provider Validations. |  |

