---
path: /docs/channels/whatsapp-sms-twilio
title: How to create a Whatsapp/SMS channel with Twilio?
---

# whatsapp-sms-twilio

**Step 1**. Click on "Add Inbox" button from Settings &gt; Inboxes page.

![sms\_create](../.gitbook/assets/inbox_create%20%282%29.png)

**Step 2**. Click on "Twilio" icon.

![list\_of\_channels](../.gitbook/assets/list_of_channels%20%282%29.png)

**Step 3**. Configure the inbox.

These are the inputs required to create this channel:

 \| Input \| Description \| Where can I find it \| \| ------------ \| --------------------------------------------------------------------------------------------------------------------- \| ---------------------------------------------------------------------------------------------- \| \| Channel Name \| This is the name inbox, this will be used across the application. \| N/A \| \| Channel Type \| Select SMS, if you are integrating an SMS channel. Select Whatsapp, if you have a verified Whatsapp number in Twilio. \| N/A \| \| Phone Number \| This is the number you will be using to communicate with your customer. This has to be verified in Twilio. \| Enter your number as in the Twilio Dashboard \| \| Account SID \| Account SID in Twilio Console \| Login to Twilio Console. Here, you would be able to see the Account SID and the Auth Token \| \| Auth Token \| Auth token for the account \| Login to the Twilio Console. Here, you would be able to see the Account SID and the Auth Token \|

![create\_twilio](../.gitbook/assets/create_twilio_inbox.png)

**Step 4**. "Add agents" to your inbox.

![add\_agents](../.gitbook/assets/add_agents.png)

**Step 6**. Hooray! You have successfully created a whatsapp/sms inbox.

![finish\_inbox](../.gitbook/assets/finish_inbox%20%282%29.png)

If it is an SMS Channel, then you don't need to do anything else. You will start receiving the messages in the dashboard whenever a customer sends you one.

If you are connecting a **Whatsapp** channel, you have to configure a callback URL in the Twilio inbox:

* Login to your Twilio Console.
* Go to `Programmable SMS > Whatsapp > Senders`.
* You will be able to see your phone number. Click on it, it will display a field like the one shown below.

![twilio\_console](../.gitbook/assets/twilio_console.png)

* Provide `https://app.chatwoot.com/twilio/callback` as the value for `WHEN A MESSAGE COMES IN` input.

**Step 7**. If you want to update the agents who have access to the inbox, you can go to Settings &gt; Inboxes.

![inbox\_settings](../.gitbook/assets/inbox_settings%20%282%29.png)

