# 8.	Hub Audit Logs

The Hub Audit Log captures detailed records of all incoming and outgoing transactions processed through the RxCheck Hub. This feature provides State PDMP Administrators with visibility into:

The number of requests received by their state,

The number of requests sent to other states, and

The status of each transaction (e.g., Successful, Access Denied, Deferred, Failed due to Connection Error, etc.)

An Audit ID is automatically generated for each transaction that reaches the RxCheck Hub. These records are summarized and displayed in the Hub Audit Log section of the RxConsole application.

By clicking on an Audit ID, administrators can view a detailed summary of the associated transaction, including both request and response details involving the PDMP state. The Hub Audit Logs are also a valuable tool for diagnosing failed transactions and identifying the root cause of communication issues.

The following subsection provides step-by-step instructions for viewing the Hub Audit Logs within the RxConsole interface. Each step is accompanied by a screenshot to assist with navigation and understanding.

## 8.1.	Read the hub audit logs

The following screenshot displays two hub audit log entries.

Clicking on the blue hyperlink text will display additional information about its column.

For example, clicking on View will display the following Log Summary pop-up page. The Log Summary contains additional information about the respective transaction and may add further insight (in the “Message” section) as to why a transaction was not successful.

The following table details the role of each column title displayed in the Hub Audit Log.


| Title | Description |
| --- | --- |
| Summary | Provides details about the transaction and any errors. |
| Request ID | The ID provided in a request transaction that is made to obtain prescription data of an individual patient. |
| Requesting Site | The state code of the State that initiated the data request. |
| Disclosing Site | The state code of the State to which the data request is being sent to. |
| Requestor | The name of the healthcare professional who submitted the request. |
| Role | The role of the healthcare professional who submitted the request. |
| DEA | The Drug Enforcement Administration number of the healthcare professional who submitted the request. |
| NPI | The National Provider Identification number of the healthcare professional who submitted the request. |
| SLN | The State License number of the healthcare professional who submitted the request. |
| Request DateTime | The date and time the request was initiated. |
| Response DateTime | The date and time the response was sent. |
| Response Status | The status of the transaction. |

The following table describes what each of the available Request Status options translates to.


| Status | Description |
| --- | --- |
| Provided | A query was received, and a result was returned without issue. |
| Deferred | *Internal only- for debugging purposes |
| Not Found | A query was received, but a patient match was not found. In some cases, Not Found will also be the response when too many patients were found and a guaranteed match could not be established. |
| Disallowed | *Internal only- for debugging purposes |
| Invalid Document | *Internal only- for debugging purposes |
| Invalid Response | *Internal only- for debugging purposes |
| No Route Found | There is no message route found to forward the request to a PDMP. |
| Access Denied | A query was received, but the disclosing state denied the request (often due to not allowing the requestor’s role access to data). |
| Outbound Certificate Expired | The sending state’s certificate has expired. |
| Inbound Certificate Expired | The receiving state’s certificate has expired. |
| Invalid Site Code | An invalid site code was sent in the message. |
| Max Limit Reached | When the number of messages reaches the threshold that the PDMP Administrator sets in the hub. |
| Timeout | The request timed out while waiting for the response. |
| Connection Error | There was an error connecting the requesting entity to the SRS. |
| Validation Failed | A query was received, but the requestor did not pass validation rules set up in the RxConsole for the state. |
| Version Mismatch | *Internal only- for debugging purposes |
| Error | *Internal only- for debugging purposes |
| Connection Reset | There is a TCP/IP connection reset that occurred. |
| Service Not Available | Displays when any of the internal services are not available to process the message. |
| Site not found | An invalid site code was sent in the message. |

## 8.2.	Filter the hub audit logs


| Click on the Hub Audit Logs button, located on the left-hand side of the screen. |  |
| --- | --- |
| Select the appropriate Site Selector option:<br>All Site- Lists all incoming and outgoing requests to/from your state.<br>Requesting Site- A state that sent a request to your state.<br>Disclosing Site- A state that received a request from your state.<br><br>Note: This is a required field and is set to All Site by default. |  |
| Select the Site Code by clicking the down arrow and then:<br>Scrolling through the dropdown options and checking the box, or <br>Typing in the search bar to filter results.<br><br>Note: This filter is only active when Disclosing Site or Requesting Site is selected in the Site Selector in step 2 above. This field is required. |  |
| Select the date and time range to filter the audit log:<br>From DateTime – Start date and time<br>To DateTime – End date and time<br><br>Click the blue calendar icon to choose a date. Use the left/right arrows to switch months. Adjust the time using the up/down arrows below the calendar (24-hour format: HH:MM). |  |
| Clicking on the More>>> link located below the Site Selector filter will provide additional filtering options. |  |
| The following additional filter options are available:<br>Message ID<br>Request ID<br>Requestor<br>Roles<br>DEA#<br>NPI#<br>SL#<br>Other#<br>Status Types<br>Enter an appropriate value into your desired filter option field. An explanation of each field is listed in a table following these steps. | The following additional filter options are available:<br>Message ID<br>Request ID<br>Requestor<br>Roles<br>DEA#<br>NPI#<br>SL#<br>Other#<br>Status Types<br>Enter an appropriate value into your desired filter option field. An explanation of each field is listed in a table following these steps. |
|  |  |
|  |  |
| Click on the Filter button to apply the selected Hub audit log criteria. |  |

## 8.3.	Download the hub audit logs

The RxConsole application allows PDMP Administrators to download a copy of their audit logs. When downloaded, the audit logs are packaged as a zipped file.

After downloading the zipped file, users can extract its contents and save them to a preferred location on their computer. The extracted file is in Comma-Separated Values (.csv) format and can be opened using Microsoft Excel or any other software that supports CSV files.


| Perform any filtering desired using the steps in the previous section. |  |
| --- | --- |
| Click on the download button on the right-hand side of the screen. |  |
| The hub audit logs will be saved to your computer in a zipped folder. |  |
| Right-click on the zipped folder to view options |  |
| Select the “Extract All…” option. |  |

## 8.4.	Exporting the logs to an sFTP server

RxConsole enables PDMP Administrators to export RxCheck Hub audit logs to their state’s sFTP server by providing the required sFTP configuration—hostname, port, username, and password—via the “Log Extract” section on the Hub Audit Logs page.

After clicking the Log Extract button, you will see the following window.

The following table includes a description of each of the fields available.


| Field | Description |
| --- | --- |
| Host Name | The domain name or IP address of the remote SFTP server. <br>Example: sftp.example.com or 192.168.1.100. |
| Port | The port number used for the sFTP connection. The default is “22”, but it can be configured to other values by the server administrator. |
| File Path | The directory path on the remote server where files will be uploaded to or downloaded from. <br>Example: /home/sftp,_user/uploads, or /data/incoming. |
| Username | The login name used to authenticate the user with the SFTP server. It is typically assigned by the server administrator. |
| Password | The secret key or password corresponding to the username for authentication. This can be omitted if key-based authentication is used. |
| Active | Allows a user to enable and disable the log extract function. When the box is green, it is enabled. When red, the functionality is disabled. |


| After the sFTP configuration is saved, the system will activate the Export Logs (sFTP) button for the PDMP administrator. To initiate the log export, click this button. The system will process the request and send an email notification once the export is complete. |  |
| --- | --- |

## 8.5.	Using an API to download the logs

RxConsole also allows a PDMP Administrator to enable an API endpoint to download audit logs from the RxCheck Hub. To access this API, an API key is required.


| From the log extract window, select the API Key tab. |  |
| --- | --- |
| Press the Key button to generate an API key. |  |
| To copy the API Key, press the copy button. |  |
| To create a new unique API key, press the ReGenerateAPIKey. |  |
| To remove your API, press the Delete key. |  |

Note: The system generates a sample API request to be used as a reference for developing a module to download Hub audit logs.

