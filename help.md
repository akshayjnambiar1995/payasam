HELP
----

The Content Management System (CMS) was originally developed to power the Tathva'12 website (Tathva is the annual tech. fest of NIT Calicut). 


Features of the CMS include:

1. Managing content in the website through various accounts created by the respective event managers. Each event manager creates a unique 	account to manage the content of his/her event and has access to only that event.	

2. Proofread content by having access to all the events.

3. An Admin account who validates/invalidates users after verifying his/her identity and thereby ensuring security to the system.

4. Events can also be validated/invalidated from the admin account to be displayed in the website.

5. CMS is powered with a HTML editor written in Jquery. The editor enables users to convert content into HTML enabling users to enter content 	without  any prior knowledge of HTML.

6. On updation of the content, a view of the content entered is displayed.

7. For the purpose of separating content into various sections with appropriate titles, the CMS is designed as various section boxes which 	compise the body of the content. The body content comprising of the section titles and it respective contents are stored in 'LONGDESC' column in the events table and as illustrated  in the following example,

	What you enter in the CMS:

		Section title: Introduction
		Section Content:Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure 		dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non 			proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
		Section title: Rules
		Section Content:Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo. Nem enim ipsam voluptatem quia 		voluptas sit aspernatur aut odit aut fugit, sed quia consequuntur magni.

	How it is stored in the database, EVENTS table, 'LONGDESC' column:
		
		Introduction||ttl||
		Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
		||sec||

		Rules||ttl||
		Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo. Nem enim ipsam voluptatem quia voluptas sit aspernatur aut odit aut fugit, sed quia consequuntur magni.
		||sec||

	**Note**: Please note that the spaces have been provided for clarity. ||sec|| is used as a separator for sections and ||ttl|| is used for 		separating the titles from the content within a section. So while using this data for the website, use the split function in Jquery and 	separate the content using the ||sec|| tag, which separates the content into various sections and further split using ||ttl|| tag which 	splits the section into section title and section content.

8. Short description,contact and prizes if required can be entered.

9. Tags can be entered which can be used for searching for various event content.

10. Can be used to send group mails.
First you can add a group of email ids under a tag in the 'Add new emails' section. Then in the 'group mail' section you can select email ids from the appropriate selector tag. The emails which were selected under the selector tag and which are to be send can be assigned a sent marker tag. The next time the email ids are populated from the appropriate selector tag, those with the sent marker tag are not populated. The idea is to avoid the email ids which are already sent under the same selector tag.

11. A facility has been provided for editing college names and migrating existing registered people to a different college ID. This is for people using ambigous college names when registering for the Fest. 
	
	For example in the college column:

		College Id 		College name 								Student Name
		101				NIT Calicut									John Doe
		102				National Institute Of Technology Calicut	Jane Doe

	Either NIT Calicut can be edited to National Institute Of Technology Calicut
	or NIT Calicut can be migrated to ID 102.
	If there is repetition then 'ignore' can be used.
	For the Addition of a new College into the auto completion list of colleges under online registration in the website, use 'validate'.

