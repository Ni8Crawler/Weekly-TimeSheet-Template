# TimeSheet
A Power apps based timesheet app for logging employee's Timesheet.

## Features

This sample illustrates the following concepts:

* Creating an appealing home screen for your applications
* Creating a timesheet application that you can use for your production needs
* Sends Email with link of the Timesheet request for Approval/Reject
* Once Approved/Rejected noitify the requester.

## Prerequisites

You'll need to make sure to update the data sources (see below)

## Data Sources
 
This app uses SharePoint as a data source and requires three SharePoint Lists with the following fields:

### BillTo List

This list contains the lookup data to associate a timesheet entry with a job or client to bill to.  Set the list up as follows:

|Type|Internal Name|Required|
|---|---|:---:|
|Single line of text|Title|Yes|

### TimeEntries List

This list contains the timesheet entries.  Set the list up as follows:

|Type|Internal Name|Required|
|---|---|:---:|
|Single line of text|Title|Yes|
|Number|Mon|No|
|Number|Tues|No|
|Number|Weds|No|
|Number|Thurs|No|
|Number|Fri|No|
|Number|Sat|No|
|Number|Sun|No|
|Multi line of text|Comments|No|
|Choice|Status|No|
|Person or Group|Employee|No|
|Person or Group|Manager|No|
|Lookup|BillTo|No|
|Date|WeekStart|No|
|Number|Total|No|

### AppAdmins

This list contains the employee and their role. Set the list up as follows:

|Type|Internal Name|Required|
|---|---|:---:|
|Single line of text|Title|Yes|
|Lookup|Email|Yes|
|Single line of text|Role|Yes|

## Steps to import the template

* [Download](https://github.com/Ni8Crawler/Weekly-TimeSheet-Template/blob/main/Weekly%20Timesheet.msapp) the `.msapp` from the `solution` folder
* Use the `.msapp` file using **File** > **Open** > **Browse** within Power Apps Studio.
* Select the **Data** tab
* Remove the `BillTo` and `TimesheetEntries` data sources from the app
* Add new data sources for the `BillTo` and `TimesheetEntries` SharePoint Lists you created in your environment
* Save and Publish
