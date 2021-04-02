---
path: /docs/self-hosted/email-setup
title: Setting up Email Channel
---

# Configuring Email Channel

_Email channels require_ [_conversation continuity configured_](https://github.com/chatwoot/docs/tree/2d5c23bd385463751573600a0f937188aace738f/docs/conversation-continuity/README.md)

1. Enable `channel_email` \(Login to rails console and execute the following\)

```text
account = Account.find(1)
account.enabled_features // This would list enabled features.
account.enable_features('channel_email')
account.save!
```

1. Now head over to inboxes page and create an email inbox with the support email as care@your-domain.com
2. Now create a forward rule in your care@your-domain.com inbox to forward emails to the address obtained at inbox creation step
3. You should be able to receive emails in your newly created email inbox in chatwoot. 

## Sendgrid

You can send out emails only from a verified email address in SendGrid. For sending emails from wildcard domain, do verification at domain level instead of individual email.

