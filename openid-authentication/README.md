# OpenID Authentication for JIRA and Confluence

Hi,
I'm really happy that you are evaluating [OpenID Authentication](https://marketplace.atlassian.com/plugins/com.pawelniewiadomski.jira.jira-openid-authentication-plugin)

I tried to make this plugin self-explanatory but if I failed in that and you have any doubts or questions please [contact me](mailto:pawelniewiadomski@me.com) so I can answer them and also improve the plugin.

Cheers,
Pawel

[_security_considerations.md](../_security_considerations.md ':include')

[_usage_tracking.md](../_usage_tracking.md ':include')

## FAQ

### Can I use this for Service Desk?

Yes, you can log into JIRA and then use Service Desk. If you want to limit users to Service Desk only you can use [this plugin](https://marketplace.atlassian.com/plugins/easy.social.sign-ups.servicedesk/server/overview)

### I'm unable to use my custom OAuth 2 authentication provider

The custom OAuth authentication built into the plugin was created for Google Apps and may not work with some other implementations. If you want to use your own provider and it doesn't work out of the box please [contact me](mailto:pawelniewiadomski@me.com?Subject=OpenID%20Custom%20Provider) for support. I will happily fix the plugin to work with your provider.

### I'm getting HTTP/405 when authenticating with Google Apps

You probably didn't enable Google+ API in Google Developer Console.

### I'm getting SSL errors

There's couple of reasons you could get them:

- you're using a self signed certificate
- you're using a certificate signed by Certification Authoriting that isn't known for the Java version you use
- you're using 2048 bit certificate key which is only supported by latest Java 1.7 and 1.8 releases

### Can this plugin synchronize all users or groups?

No, it cannot. It will synchornize users details during authentication only. It does not synchronize
users or groups in the background. Also this plugin doesn't act as Crowd User Directory.

### Is this plugin compatible with custom `SSOSeraphAuthenticator`?

No, it is not. Users found that they do not work well together. I don't have plans to support custom authenticators at this time.

### Plugin doesn't work in JIRA 7.3.0

If you use recent PostgreSQL release you can face `com.atlassian.activeobjects.internal.ActiveObjectsInitException`. If you do please upgrade JDBC driver because the one shipped with JIRA is too old.

[_shared_faq.md](../_shared_faq.md ':include')

## EULA

Copied from Atlassian Marketplace Terms of Use

Last Updated: May 31, 2012

> Standard EULA

> (i) The Publisher is the licensor of the Marketplace Product and Atlassian is not a party to the Publisher EULA or this Standard EULA, as applicable.

> (ii) If the Marketplace Product does not include a Publisher EULA that specifies Marketplace Product license rights, Publisher grants you a limited, worldwide, non-exclusive, non-transferable and non-sublicensable license to download and use the Marketplace Product only on hardware systems owned, leased or controlled by you.

> (iii) Licenses granted by Publisher are granted subject to the condition that you must ensure the maximum number of Authorized Users that are able to access and use the Marketplace Product concurrently is equal to the number of User Licenses for which the necessary fees have been paid to Atlassian and/or its authorized partners (each, an "Atlassian Expert"). You may purchase additional User Licenses at any time on payment of the appropriate fees to Atlassian or an Atlassian Expert. "User License" means a license granted under this EULA to you to permit an Authorized User to use the Marketplace Product. The number of User Licenses granted to you is dependent on the fees paid by you. "Authorized User" means a person who accesses and uses a Marketplace Product under the EULA and for which the necessary fees have been paid to Atlassian and/or an Atlassian Expert.


> (iv) Any information that Publisher collects from you or your device will be subject to any Publisher EULA, privacy notice, or similar terms that the Publisher provides to you, and will not be subject to the Atlassian Privacy Policy (unless Atlassian is the Publisher).

> (v) You may not modify, reverse engineer, decompile or disassemble the Marketplace Product in whole or in part, or create any derivative works from or sublicense any rights in the Marketplace Product, unless otherwise expressly authorized in writing by Publisher.

> (vi) The Marketplace Product is protected by copyright and other intellectual property laws and treaties. Unless otherwise expressly stated in the Publisher EULA, Publisher or its licensors own all title, copyright and other intellectual property rights in the Marketplace Product, and the Marketplace Product is licensed to you directly by the Publisher, not sold.

> End of Standard EULA 