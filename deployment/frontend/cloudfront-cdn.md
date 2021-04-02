---
path: /docs/deployment/cdn/cloudfront
title: Configuring Cloudfront with Chatwoot
---

# cloudfront-cdn

This document helps you to configure Cloudfront as the asset host for Chatwoot. If you have a high traffic website, we would recommend setting up a CDN for Chatwoot.

## Configure a Cloudfront distribution

**Step 1**: Create a Cloudfront distribution.

![create-distribution](../../.gitbook/assets/create-distribution.png)

**Step 2**: Select "Web" as delivery method for your content.

![web-delivery-method](../../.gitbook/assets/web-delivery-method.png)

**Step 3**: Configure the Origin Settings as the following.

![origin-settings](../../.gitbook/assets/origin-settings.png)

* Provide your Chatwoot Installation URL under Origin Domain Name.
* Select "Origin Protocol Policy" as Match Viewer.

**Step 4**: Configure Cache behaviour.

![cache-behaviour](../../.gitbook/assets/cache-behaviour.png)

* Configure **Allowed HTTP methods** to use _GET, HEAD, OPTIONS_.
* Configure **Cache and origin request settings** to use _Use legacy cache settings_.
* Select **Whitelist** for _Cache Based on Selected Request Headers_.
* Add the following headers to the **Whitelist Headers**.

  ![extra-headers](../../.gitbook/assets/extra-headers.png)

  * **Access-Control-Request-Headers**
  * **Access-Control-Request-Method**
  * **Origin**

**Step 5**: Click on **Create Distribution**. You will be able to see the distribution as shown below. Use the **Domain name** listed in the details as the **ASSET\_CDN\_HOST** in Chatwoot.

![cdn-distribution-settings](../../.gitbook/assets/cdn-distribution-settings.png)

## Add ASSET\_CDN\_HOST in Chatwoot

Your Cloudfront URL will be of the format `<distribution>.cloudfront.net`.

Set

```bash
ASSET_CDN_HOST=<distribution>.cloudfront.net
```

in the environment variables.

