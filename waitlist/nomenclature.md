Original Data Sources
---------------------


1. Applicant Database


![partial data model](https://certsys.blob.core.windows.net/screenshots/waitlist old version data model.png "partial data model")

Entities (Fields)
	
	
	Applicants
	    - Applicant ID
	    - First Name
	    - Last Name
	    + Application Date, Uploaded Application, Documentation, Family Size)
	Attachments (Attachment, Last Updated )
	Check Ins (Check-In ID, Applicant ID, Check In Date, Check In Notes)
	Notification Letters (Letter ID, Applicant ID, Letter Date, Content, Staff ID)
	Eligibility (Eligibility ID, Applicant ID, Program ID, Eligibility Option ID, Letter Date, Reason)
	Move Ins (Entrance ID, Applicant ID, Move In Date, Property ID, Program ID)
	Interviews (Interview ID, Applicant ID, Interview Date, Interview Location, Interview Facilitators)
	Property Preference (Preference ID, Applicant ID, Property ID, Preference Order)
	Programs (Program ID, Program Name)
	Properties (Property ID, Property Name)
	Eligibility Options (Eligibility Option ID, Eligibility Option)
	Staff (First Name, Last Name, Position)


2. Google Workbook
------------------
![Google Workbook Spreadsheets](https://certsys.blob.core.windows.net/screenshots/google workbook.png "Google workbook")

The following elements included in every worksheet
    
    - First Name: First name(s) of adults in applying household.
    - Last Name: Last name(s) of adults in applying household.
    - HH: Household Size of applying household.
	- Application Received: Date application originally received by intake staff.
	- Application Review: Date application eligibility first reviewed by intake staff. 
	- AB: Indicating applications received through AuntBertha.com
	- Language: Primary language spoken by applying household.
	- Undoc: Indicating applications with undocumented adults in household.
	- HUD Homeless: Indicating applications meeting criteria for HUD Homelessness
	- YTD Mon/Yr: Year to date employment income received monthly and yearly.
	- Ave Mon/Yr: Average employment income received monthly and yearly.
	- Start Date: Employment income starting date.
	- AE Debt: Indicating applications with outstanding debt owed to Austin Energy utility company.
	TXG Debt: Indicating applications with outstanding debt owed to Texas Gas Services.
	Prop1: First preference for housing location.
	Prop2: Second preference for housing location.
	Prop3: Third preference for housing location.
	Phone: Phone number belonging to adult(s) in applying household.
	Email: Email address belonging to adult(s) in applying household.
	Check In – Date indicating most recent check in and attached comments documenting previous check-ins.
