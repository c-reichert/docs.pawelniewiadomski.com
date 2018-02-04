# OpenID Authentication for JIRA and Confluence

Hi,
I'm really happy that you are evaluating [OpenID Authentication](https://marketplace.atlassian.com/plugins/com.pawelniewiadomski.jira.jira-openid-authentication-plugin)

I tried to make this plugin self-explanatory but if I failed in that and you have any doubts or questions please [contact me](mailto:pawelniewiadomski@me.com) so I can answer them and also improve the plugin.

Cheers,
Pawel

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