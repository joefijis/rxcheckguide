# 6.	Analytical Insights

The Analytical Insights dashboard allows each state to analyze prescription trends and patterns at a high level. It provides visibility into how prescriptions from other states are being dispensed within the state, as well as how the state’s own prescriptions are being filled outside its borders. This feature supports the identification of individuals traveling from other states to fill prescriptions and highlights out-of-state pharmacies dispensing prescriptions written in the user’s state.

It is important to note that all posted data and visualizations are based on:

Aggregate data

Anonymized data

No PHI or PII data is disclosed

For the Analytical Insights dashboard to function in the RxConsole, a state will need to send Non-PHI and Non-PII data to the Insights API, where it can then be added to the database and displayed within the RxConsole.

A state PDMP Administrator wishing to participate in this module, will need to submit data to the RxCheck Team. This data should be free of PHI and PII before being submitted. The following data is required for the Analytical Insights dashboard to begin functioning:

The month for which the data is submitted

The PDMP that is posting the data

Zip code, county, or state from where the prescriptions were dispensed

Total number of dispenses by zip code, county, or state

Total number of out-of-state dispenses (for patients and/or providers) by the zip code, county, or state

Total number of providers, patients, and prescriptions

Some information to keep in mind regarding the Analytical Insights Feature:

A state’s participation is voluntary

Data does not contain PHI or PII

Access is limited to authorized PDMP staff members from a participating PDMP and Tetra Ventures for system administration

The PDMP controls their data and determines:

Level of detail (Rx general location information) for the data

Which other PDMPs to engage

No cost is imposed to participate or use this tool

Free assistance is available to develop the data file

If desired, a state can request a user agreement for this tool detailing access and use parameters for PDMPs

Below, there is an example for a submission for provider information submitted from Kentucky (sample data).

{

“PDMPAnalyticsData”: {

“FilledDate”: “03/17/2023”,

“PublishState”: “KY”,

“DispenseDataByZip”: {

“dispenseZip”: “41008”,

“totalDispense”: “100”,

“totalOutofStateDispense”: “5”,

“ProvidersFilledFromOutState”: [

{

“filledStateCode”: “WV”,

“filledFromZip”: “24712”,

“totalProviders”: “2”,

“totalPrescriptions”: “3”

}, {

“filledStateCode”: “TN”,

“filledFromZip”: “37011”,

“totalProviders”: “1”,

“totalPrescriptions”: “1”

}, {

“filledStateCode”: “IN”,

“filledFromZip”: “46077”,

“totalProviders”: “1”,

“totalPrescriptions”: “1”

}

]

}

}

}

After data has been submitted, the map should begin to populate in the Analytical Insights module within RxConsole.

## 6.1.	View patient and provider prescriptions data in analytical insights


| Click the area graph icon on the left-hand side of the screen to access the RxCheck Dashboard. |  |
| --- | --- |
| Click on the Patient or Provider button located in the top middle of the page, depending on the information you would like to display. |  |
| Click on the filter button in the top right corner. |  |
| After clicking the filter button, you can view the search filters. |  |
| The Incoming and Outgoing buttons allow you to filter the request type.<br><br>Note: The Incoming option is selected and displayed by default. |  |
| Use the Time Range dropdown to select a period you want to display. |  |
| Prescription information can be searched by County or Zip Code. |  |
| How to search by county |  |
| Click on the County radio button.<br><br>Note: The County button is selected by default. |  |
| Click on the downward-facing arrow for the filter titled “County” to reveal a list of counties. |  |
| Select your County(ies) by:<br>Scrolling through the dropdown options and checking the box, or<br>Typing in the search bar to filter results. |  |
| Click the Search button to display prescription counts for patients based on the counties selected. |  |
| Results are displayed on the map with the user’s state highlighted green and the connected states in orange. | Results are displayed on the map with the user’s state highlighted green and the connected states in orange. |
|  |  |
| How to search by Zip Code |  |
| Click on the Zip Code radio button. |  |
| Enter the zip code and the desired distance in miles around the zip code to be searched. |  |
| Click the Search button to display prescription counts for patients based on the zip code and range entered. |  |
| Results are displayed on the map with the user’s state highlighted green and the connected states in orange. | Results are displayed on the map with the user’s state highlighted green and the connected states in orange. |
|  |  |
| Note: Click on the Reset Filters button to return all selections to the default values. |  |

