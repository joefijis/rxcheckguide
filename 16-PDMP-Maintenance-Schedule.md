# 16.	PDMP Maintenance Schedule

The Maintenance Schedule feature in RxConsole enables State PDMP administrators to create and manage scheduled maintenance events. These events may include activities such as application updates, software installations, or operating system configurations.

During a maintenance window, the PDMP system will be taken offline, meaning it will not be able to process incoming requests or generate responses. If a request is received during this time, the system will return an error code “DM”, indicating a processing error due to scheduled maintenance. Once the maintenance period concludes, the system will resume normal operations and process all pending and new requests.

The screenshot below shows an example Maintenance Schedule for a test site, “TT”. The accompanying table provides descriptions for each column heading displayed in the interface.


| Heading | Description |
| --- | --- |
| From | The date and time for when the maintenance event will begin. |
| To | The date and time for when the maintenance event will end. |
| Type | The event type for which the maintenance event is scheduled. |
| Message | The user can add an informative note about the respective event. |
| Status | The status of the scheduled event, such as “Completed” or “Cancelled”. |

The following subsection contains step-by-step instructions on how to add a PDMP maintenance schedule entry in the RxConsole application. For additional clarity, each step is accompanied by a corresponding image or screenshot that depicts the action described.

## 16.1.	Create and modify a maintenance event


| Click on the PDMP Maintenance Schedule button, located on the left-hand side of the screen. |  |
| --- | --- |
| Click on the Add Maintenance button located on the top right-hand corner of the screen. |  |
| Note: You can only create a new maintenance event if no other upcoming event is scheduled. If there’s a conflict, an alert message will appear. |  |
| A pop-up screen titled Maintenance will appear. |  |
|  |  |
| Select the start date and time by making appropriate selections in the calendar by clicking the blue calendar in the field labeled From Date&Time. |  |
| Select the end date and time by making appropriate selections in the calendar by clicking the blue calendar in the field labeled To Date&Time. |  |
| Select the reason for the maintenance event by clicking on one of the dropdown options for the field labeled, Reason Type. |  |


| Add a note into the text box labeled, Reason Message to add context to the maintenance event. | Add a note into the text box labeled, Reason Message to add context to the maintenance event. |
| --- | --- |
|  |  |
| Press the Save button to add the new maintenance event to the maintenance schedule in the RxConsole. |  |
| Alternatively, you can press the Close button to discard changes and return to the previous screen. |  |
| To modify an already existing maintenance event. | To modify an already existing maintenance event. |
| Click on an event listed in the Maintenance Schedule. |  |
|  |  |
| Modify any information in the Maintenance popup similar to if you were adding a new event. |  |
| Press the Save button to record the changes to the maintenance event in the RxConsole. |  |
| Alternatively, you can press the Close button to discard changes and return to the previous screen. |  |
| Press the Complete button to mark the event as completed. |  |
| Press the Cancel button to cancel the event in the maintenance schedule. |  |

