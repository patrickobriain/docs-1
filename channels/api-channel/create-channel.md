---
path: /docs/channels/api/configure
title: How to create an API channel inbox?
---

# create-channel

Setting up an API channel consists of the following steps.

1. Create API Channel inbox
2. Send messages using Chatwoot APIs
3. Receive webhooks on new messages from Chatwoot

This document allows you to create and configure an API channel inbox in Chatwoot installations.

**Step 1**: Go to Settings &gt; Inboxes and click on "Add Inbox".

**Step 2**: Select **API** from the list of channels.

![select-api-inbox](../../.gitbook/assets/select-api-inbox.png)

**Step 3**: Provide an name for the channel and a callback URL \(the events and corresponding payload is defined in the subsequent articles\)

![configure-screen](../../.gitbook/assets/configure-screen.png)

**Step 4**: Add agents to the inbox.

![add-agents](../../.gitbook/assets/add-agents.png)

**Step 5**: Hooray!! The inbox setup is complete.

![take-me-there](../../.gitbook/assets/take-me-there.png)

![inbox-welcome-screen](../../.gitbook/assets/inbox-welcome-screen.png)

Now the channel setup is complete, let us try to send a message using Chatwoot APIs. Read more about it [here](https://github.com/chatwoot/docs/tree/2d5c23bd385463751573600a0f937188aace738f/docs/channels/api/send-messages/README.md)

