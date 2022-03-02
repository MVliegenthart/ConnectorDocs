Revelation helpdesk is a web-based helpdesk application available in cloud and on premise. This connector allows you to create and update items in your Revelation helpdesk ticketing system such as tickets, clients, users and assets by connecting to the Revelation helpdesk API using OAuth authentication. 
New Tickets can be logged, action notes added and you can reassign or change the priority / status of existing tickets. You can also take advantage of the extensive list of triggers allowing you to integrate your business processes based on events that occur in Revelation helpdesk.


## Prerequisites

You will need a Revelation helpdesk account in order to use this connector. If you are not yet signed up for Revelation helpdesk you can [get a free 30 trial here] (https://revelationhelpdesk.com/prime-free-trial#form)

## How to get credentials

To use the connector you will need the URL to your Revelation helpdesk instance and you will need a Super Admin account.
If you have signed up for a Trial the URL will be 'https://trial.revelationhelpdesk.com' and your username will be the email address you used to sign up. You will be promped to change your default password the first time you sign in to your trial account.
  

## Get started with your connector

To start using the Revelation helpdesk connector create a new Flow and add an action. Then search for "Revelation helpdesk" and select any of the available actions. 
<img src="http://revelationhelpdesk.com/images/api/screenshots/Step1 - Choose action.png" align="left"  width="400">  

The first step when adding a new action or trigger is to create a connection to your instance of Revelation helpdesk. When prompted, enter your Revelation helpdesk URL and make sure the url does not end with '/'
<img src="http://revelationhelpdesk.com/images/api/screenshots/Step2 - Connect.png" align="left"  width="400">

After you enter your Revelation helpdesk URL click 'Sign In' and you will see a popup login form. Enter your Revelation URL again and your Revelation username and password.
<img src="http://revelationhelpdesk.com/images/api/screenshots/Step3 - Auth.png" align="left"  width="400">
<img src="http://revelationhelpdesk.com/images/api/screenshots/Step4 - Login.png" align="left"  width="400">

Once you have signed in successfully you will be able to interact with the chosen action. Here is a simple example of how to log a new ticket  using the 'Log a new Ticket' action
<img src="http://revelationhelpdesk.com/images/api/screenshots/Step5 - LogATicket.png" align="left"  width="400">

Here is an advanced scenario where we log a new ticket from an email. When a new email arrives it will trigger the flow and use the 'Find a user' action to find the user in Revelation helpdesk by their (FROM) email address. The 'Log a new Ticket' action then logs a ticket to the End User using the output (The User Id) from the previous action. The ticket description will be the subject line of the email and the Client and Project fields can be left blank because these will get set automatically based on the end user of the ticket.
Next we will use the "Add an Action" action to add a note to the newly logged ticket in the previous step. The 'Ticket Id' is the ID of the ticket logged in the previous step and the Notes are set to be the body of the email.
<img src="http://revelationhelpdesk.com/images/api/screenshots/Advanced logATicket.png" align="left"  width="400">

The ticket that is logged in Revelation helpdesk will look similar to this
<img src="http://revelationhelpdesk.com/images/api/screenshots/Step6 - Advanced.png" align="left"  width="400">



## Known issues and limitations

* Actions and Trigger names in the connector don't reflect the phrases configured in Revelation helpdesk. The parameter names for all the actions and triggers will however reflect the custom phrases setup in Revelation helpdesk. For example the word "Ticket" can be changed to "Issue" but the action name "Log a new Ticket" won't change, however the first parameter in that action is "Client" which will be phrased correctly. 
* This connector only support Revelation helpdesk V22.3 (Cloud) and Revelation server 2022 (On-Premise). There are further requirements in order to use the connector with the on-premise version of Revelation helpdesk. 

## Common errors and remedies

Highlight any errors that might commonly occur when using the connector (such as HTTP status code errors), and what the user should do to resolve the error.

## FAQ

Provide a breakdown of frequently asked questions and their respective answers here. This can cover FAQs about interacting with the underlying service or about the connector itself.