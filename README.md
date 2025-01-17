# Office of Personnel Management (OPM) Retirement Services (RS) for Case Management using IVR Phone Tree as a Demo that is powered by Twilio - ASP.NET MVC and Microsoft App Dynamics

<a href="https://www.twilio.com">
  <img src="https://static0.twilio.com/marketing/bundles/marketing/img/logos/wordmark-red.svg" alt="Twilio" width="250" />
</a>

[![Build status](https://ci.appveyor.com/api/projects/status/ktdh5pqmkc39ljng?svg=true)](https://ci.appveyor.com/project/TwilioDevEd/ivr-phone-tree-csharp)

An example application implementing an automated phone line using Twilio.

[Read the full tutorial here](https://www.twilio.com/docs/tutorials/walkthrough/ivr-phone-tree/csharp/mvc)!

## USE CASE SCENARO: Leveraging the technology; CRM, Knowledge Management, Telephony, & Computer Telephony Integration (CTI).
<b>1. Interactive Voice Response (IVR)</b><br>
IVR status request inquiry: Customer wants to know where they are in the process <br>
Customer enters their case number in the IVR<br>
Ability to transfer to Agent customers<br>
Automatic call back feature <br>
Natural Language Processing<br>

<b>2. Agent - Support Timely Response to Customer Questions</b><br>
Answers the phone<br>
Records the customer demographics and question in the CRM tool <br>
Searches the Knowledge Base to find an article to answer the customers question<br>
Attaches the article to the record<br>
Emails the article to the customer<br>
Reviews real time data <br>
Performs caller authentication<br>
Review dashboard/analytics information for telephony & CRM<br>
Repeat caller: show contact record associated with incoming customer contact<br>
Transfer/escalate a call<br>

<b>3. Manager, Leadership, & Miscellaneous</b><br>
Manage team performance metrics for telephony & CRM<br>
Review dashboard/analytics information for telephony & CRM <br>
Review dashboard/analytics information for telephony & CRM <br>
Create an article <br>
Create a Knowledge Management report top 5 articles searched <br>
Self Service Options <br>
Manager & Agent communication feature <br>
Customer Satisfaction Survey Distribution <br>

## Local development

This project is built using the [ASP.NET MVC](http://www.asp.net/mvc) web framework.

1. First clone this repository and `cd` into its directory:
   ```
   git clone git@github.com:TwilioDevEd/ivr-phone-tree-csharp.git
   cd ivr-phone-tree-csharp
   ```

1. Build the solution.

1. Expose your application to the wider internet using [ngrok](http://ngrok.com). This step
  is important because the application won't work as expected if you run it through
  localhost.

  To start using `ngrok` in our project you'll have execute to the following line in the _command prompt_.

  ```shell
  ngrok http 1112 -host-header="localhost:1112"
  ```

  Keep in mind that our endpoint is:

  ```
  http://<your-ngrok-subdomain>.ngrok.io/ivr/welcome
  ```

  Remember to update the Local.config file with the generated <your-ngrok-subdomain>.

1. Configure Twilio to call your webhooks.

  You will also need to configure Twilio to call your application when calls are
  received in your [*Twilio Number*](https://www.twilio.com/user/account/messaging/phone-numbers).
  The voice url should look something like this:

  ```
  http://<your-ngrok-subdomain>.ngrok.io/ivr/welcome
  ```

  ![Configure Voice](http://howtodocs.s3.amazonaws.com/twilio-number-config-all-med.gif)

## Unit Tests

To run the unit tests within Visual Studio, install the NUnit 3 Test Adapter:
https://marketplace.visualstudio.com/items?itemName=NUnitDevelopers.NUnit3TestAdapter

## Meta

* No warranty expressed or implied. Software is as is. Diggity.
* [MIT License](http://www.opensource.org/licenses/mit-license.html)
* Lovingly crafted by Twilio Developer Education.
