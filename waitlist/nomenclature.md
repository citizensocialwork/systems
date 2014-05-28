Original Data Sources
=====================

Applicant Database
------------------

Google Workbook
---------------



1.1.1.	Data Model
1.1.2.	Entities (Fields)
1.1.2.1.	Applicants (Applicant ID, First Name, Last Name, Application Date, Uploaded Application, Documentation, Family Size)
1.1.2.2.	Attachments (Attachment, Last Updated )
1.1.2.3.	Check Ins (Check-In ID, Applicant ID, Check In Date, Check In Notes)
1.1.2.4.	Notification Letters (Letter ID, Applicant ID, Letter Date, Content, Staff ID)
1.1.2.5.	Eligibility (Eligibility ID, Applicant ID, Program ID, Eligibility Option ID, Letter Date, Reason)
1.1.2.6.	Move Ins (Entrance ID, Applicant ID, Move In Date, Property ID, Program ID)
1.1.2.7.	Interviews (Interview ID, Applicant ID, Interview Date, Interview Location, Interview Facilitators)
1.1.2.8.	Property Preference (Preference ID, Applicant ID, Property ID, Preference Order)
1.1.2.9.	Programs (Program ID, Program Name)
1.1.2.10.	Properties (Property ID, Property Name)
1.1.2.11.	Eligibility Options (Eligibility Option ID, Eligibility Option)
1.1.2.12.	Staff (First Name, Last Name, Position)
1.1.3.	Analysis
1.1.3.1.	Applicants, attachments, and eligibility results consumed 14.49%, 11.23%, and 18.51% of total space, respectively.
1.1.3.2.	Check in’s table consumes the bulk area in the database, taking 46.75% of our total space. 
1.1.3.3.	Remaining entities combined (eligibility options, interviews, notification letters, programs, properties and staff) consume less than 1% of total space.
1.1.3.4.	Original data from Microsoft access database (accdb) was located on a local network, accessible via office and through Remote Desktop Connection.  It took approximately 6 hours to complete a full transfer of all data from server (in its original form).  
1.1.3.5.	Check-in’s originally served two purposes. Record notes while application is processing and document regular “check-in calls” between case manager and applicant (as required by program). In reality, check-in’s were used to document most case notes throughout the application process. 
1.1.3.6.	Interviews
1.1.3.6.1.	220 of 8,957 check-in notes contained the word “interview”, with the most recent written the day of data extraction for analysis. In contrast, the last official interview record was created July 26, 2012, approximately 410 workdays before data extraction. More investigation into the content surrounding use of the word “interview” may clarify this inconsistency.
1.2.	
1.2.1.	Data Model
1.2.1.1.	The following was included in every worksheet:
1.2.1.1.1.	First Name – First name(s) of adults in applying household.
1.2.1.1.2.	Last Name – Last name(s) of adults in applying household.
1.2.1.1.3.	HH – Household Size of applying household.
1.2.1.1.4.	Application Received – Date application originally received by intake staff.
1.2.1.1.5.	Application Review – Date application eligibility first reviewed by intake staff. 
1.2.1.1.6.	AB – Indicating applications received through AuntBertha.com
1.2.1.1.7.	Language – Primary language spoken by applying household.
1.2.1.1.8.	Undoc – Indicating applications with undocumented adults in household.
1.2.1.1.9.	HUD Homeless – Indicating applications meeting criteria for HUD Homelessness
1.2.1.1.10.	YTD Mon/Yr – Year to date employment income received monthly and yearly.
1.2.1.1.11.	Ave Mon/Yr – Average employment income received monthly and yearly.
1.2.1.1.12.	Start Date – Employment income starting date.
1.2.1.1.13.	AE Debt – Indicating applications with outstanding debt owed to Austin Energy utility company.
1.2.1.1.14.	TXG Debt – Indicating applications with outstanding debt owed to Texas Gas Services.
1.2.1.1.15.	Prop1 – First preference for housing location.
1.2.1.1.16.	Prop2 – Second preference for housing location.
1.2.1.1.17.	Prop3 – Third preference for housing location.
1.2.1.1.18.	Phone – Phone number belonging to adult(s) in applying household.
1.2.1.1.19.	Email – Email address belonging to adult(s) in applying household.
1.2.1.1.20.	Check In – Date indicating most recent check in and attached comments documenting previous check-ins.
1.2.1.2.	Worksheet Specific Fields
1.2.1.2.1.	Waitlist
1.2.1.2.1.1.	Pregnancy – Indicating pregnancy and due date of applying household member.
1.2.1.2.2.	Moved In
1.2.1.2.2.1.	Moved In- Date applying household moved into property.
1.2.1.2.3.	Denied during leasing
1.2.1.2.3.1.	Reason for denial – Indicating specifics for denied eligibility.
1.3.	Family Matrix Data created 1/3/2007
2.	Same Data, New Model
2.1.	Data Model
2.1.1.	Unlike the original data model, the new model does not explicitly define each entity as hard coded values. Instead, details and tags serve as customizable core components that contain a range of information users can adapt and rearrange at any time –without effecting data quality.  (A previous version of the system used three core entities: details, tags and applications however, applications were determined unnecessary to represent the parent-child relationship between applicants and content related to their application.)
2.1.2.	Details represent every specific piece of information related to an application, from income and utility debt to eligibility and case notes, as well as the actual application itself. 
2.1.3.	Tags categorize details by assigning each Detail one (and only one) Tag.  Tags communicate the type of information users should enter as well as the type of information contained in existing data.  
2.2.	Strategy
2.2.1.	Analysis of data from original sources led to simplified data model, designed to optimize storage efficiency, simplify data entry and increase flexibility. 
3.	Quality Control
3.1.1.	Maintaining automatic quality control is essential to long-term system success. Control measures implemented as specific rules assigned to each Tag serve to limit the user’s ability to input ‘bad data’, handle the bulk of work.  For example, details tagged as ‘Utility debt’ will not allow entry of non-currency value. Tags clarify each details’ subject content as well as the type of information collected from the user.
3.1.2.	
3.2.	Application Names
3.2.1.	Original data split application names into first and last and frequently used slashes (/) and other indicators to represent multiple persons as heads of household. For example one applications’ fist name may be “Susana/Carlos” or “Susana and Carlos” while their last name is “Smith/Cruz” or “Smith and Cruz”.  Names were first combined to represent a single name for each application (“Susana Smith and Carlos Cruz”) as well as added individually as (Head of Household) contact records, “Susana Smith: Phone 555-5555”, “Carlos Cruz: Phone: 555-4455”, related to a given application, associated with specific emails and phone numbers. 
3.3.	Tags also serve as a storage center for interface options. Properties, programs, languages etc. are all stored as tags.
3.3.1.	Tags Specifics
3.3.1.1.	Applications represent a collection of information related to one applicant. The application serves as the central entity representing the applicant and their global status within the waitlist. The application entity consists of an application name, household size, application date and global status of either open or closed. 
3.3.1.2.	Contacts serve both as identifying individual adults within the household as well as additional context persons relevant to the application.  The primary reason to use the contacts entity is to store individual persons and their contact information.
3.3.1.3.	Debt communicates applications with utility debts, amount owed, and source.  In the future, a paid date Tag could be added to record ongoing status of debt payment.
4.	Transferring Data (See <doc link> for complete 
4.1.	Check In Notes
4.1.1.	Notes containing "Austin energy" were transferred as Utility Debt details with Austin Energy
4.1.2.	Notes containing "TX gas" were transferred as Utility Debt details with Texas Gas Services.
4.1.3.	Notes containing “YTD” were transferred as Employment Income records 
4.1.4.	Notes containing “pregnant” or “due date” were transferred as applicants with pregnancy records 
4.1.5.	Orphaned check-ins (without application IDs) were discarded
4.1.6.	Applicants with zero Check-in’s in the last 60 days are automatically tagged “60 Day Auto Denial” and removed from waitlist.
4.2.	Debt
4.2.1.	any notes containing "Austin energy" were recorded as having debt with Austin Energy
4.2.2.	any notes containing "TX gas" were recorded as having debt with Texas Gas
4.3.	income
4.3.1.	-any Notes containing “YTD” recorded as income records
4.3.2.	-if no content exits, find more info in case notes
4.4.	notes
4.5.	check-ins
4.5.1.	check-ins without dates were not recorded
4.5.2.	check-ins without application IDs were not recorded
4.6.	pregnancy
4.6.1.	-any notes containing "pregnant" or "due date" were added recorded as applicants with pregnancy records
4.7.	contacts
4.7.1.	-application first and last names were added as contacts for that application
4.8.	Edited incomes data
4.8.1.	retagged Incomes with OVT tags
4.8.2.	removed any instances of 'est'
4.8.3.	removed instances of 'average'
4.8.4.	Removed instances of 'monthly', took value and multiplied by 12.  (**if incorrect then divide value by 12 and perform correct calculations )


