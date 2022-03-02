Revelation helpdesk is a web-based helpdesk ticketing application available in cloud and on-premise. This connector allows you to create and update items in your Revelation helpdesk ticketing system such as tickets, clients, users and assets by connecting to the Revelation helpdesk API using OAuth authentication. 
New Tickets can be logged, action notes added and you can reassign or change the priority / status of existing tickets. You can also take advantage of the extensive list of triggers allowing you to integrate your business processes based on events that occur in Revelation helpdesk.


## Prerequisites

You will need a Revelation helpdesk account in order to use this connector. If you are not yet signed up for Revelation helpdesk you can [get a free 30 day trial here.](https://revelationhelpdesk.com/prime-free-trial#form)

## How to get credentials

To use the connector you will need the URL to your Revelation helpdesk instance and you will need a Super Admin account.
If you have signed up for a Trial the URL will be 'https://trial.revelationhelpdesk.com' and your username will be the email address you used to sign up with. You will be promped to change your default password the first time you sign in to your trial account through the web interface.
  

## Getting started

<p>To start using the Revelation helpdesk connector create a new flow and add a new step. Then search for "Revelation helpdesk" and select any of the available actions. </p>
<img src="http://revelationhelpdesk.com/images/api/screenshots/Step1 - Choose action.png"  width="400">

#### Connect to Revelation helpdesk

<p>The first step when adding a new action or trigger is to create a connection to your instance of Revelation helpdesk. When prompted, enter your Revelation helpdesk URL and make sure to enter a secure URL (HTTPS://) and the url does not end with '/'</p>
<img src="http://revelationhelpdesk.com/images/api/screenshots/Step2 - Connect.png"  width="400">


<p>After you enter your Revelation helpdesk URL click 'Sign In' and you will see a popup login form. Enter your Revelation URL again and your Revelation username and password.</p>
<img src="http://revelationhelpdesk.com/images/api/screenshots/Auth Combined.png" width="600">

<p>Once you have signed in successfully you will be able to interact with the chosen action.</p>

#### Log a new Ticket
Here is a simple example of how to log a new ticket using the 'Log a new Ticket' action. Simply select the Client, Project, End User, enter a Ticket description and choose a ticket status. When the flow runs it will create a new ticket for this end user and assign it to the selected project.</p>
<img src="http://revelationhelpdesk.com/images/api/screenshots/Step5 - LogATicket.png?v2" width="400">

#### Advanced ticket logging
<p>Here is an advanced scenario where we log a new ticket from an email. When a new email arrives it will trigger the flow and use the 'Find a user' action to find the user in Revelation helpdesk by the email's FROM address. 
  
The 'Log a new Ticket' action then logs a ticket to the End User using the output (The User Id) from the previous step. The ticket description will be the subject line of the email and the Client and Project fields can be left blank because these will get set automatically based on the end user of the ticket.
  
Next we will use the "Add an Action" action to add a note to the newly logged ticket in the previous step. The 'Ticket Id' is the ID of the ticket logged in the previous step and the Notes are set to be the body of the email.</p>
<img src="http://revelationhelpdesk.com/images/api/screenshots/Advanced logATicket.png" width="400">

<p>The ticket that is logged in Revelation helpdesk will look similar to this</p>
<img src="http://revelationhelpdesk.com/images/api/screenshots/Step6 - Advanced.png"  width="400">

#### Trigger scenario
<p>A common scenario for using triggers would be to alert a team or manager when a ticket is due or at risk. In the following example we've added the "When a Ticket is Due" trigger which would start the flow as soon as any open ticket reaches its due date.

A conditional step has been added to check the Department name for the ticket, if it is for HR it will continue, if not it will terminate the flow. This is just an example of the type of logic statements that can occur based on ticket data.

Finally the last step is set to post a new message in a Teams Channel which includes a message that the ticket is due and also includes the Ticket # and Ticket description in the message body</p>
<img src="http://revelationhelpdesk.com/images/api/screenshots/Trigger - ticket due.png"  width="800">


## Known issues and limitations

* Actions and Trigger names in the connector don't reflect the phrases configured in Revelation helpdesk however, the field names for all the actions and triggers will reflect the custom phrases. For example the word "Ticket" can be changed to "Issue" but the action name "Log a new Ticket" won't change. The field names in that action like "Client", "Project" and "End User" will be updated dynamically based on your Revelation helpdesk phrase configuration. 
* This connector only support Revelation helpdesk V22.3 (Cloud) and Revelation server 2022 (On-Premise). There are further requirements in order to use the connector with the on-premise version of Revelation helpdesk. 

## Support

For further assistence or support please contact support@revelationhelpdesk.com

