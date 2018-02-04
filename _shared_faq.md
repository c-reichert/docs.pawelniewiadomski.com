### I'm getting "Oops, you've found a dead link" when I try to log in

Let's imagine that you have configured Google provider (or any other to be specific), you then access your JIRA and click Google button. In return you get HTTP/404 server response and an error page. When inspecting the location bar in the browser you can still see that it is your JIRA's address.

Lets imainge you host your JIRA on `https://jira.mycompany.com`

You can see that the browser points to `https://jira.mycompany.com/o/oauth2/auth?scope=openid+email+profile&response_type=code&state=d3fc17ad-1a4b-4449-8eb6-0d0d3eca9809&redirect_uri=https%3A%2F%2Fjira.mycompany.com%2Fopenid%2Foauth2-callback%2Fgoogle&prompt=select_account&client_id=…`

This means that you host JIRA behind reverse proxy and the proxy rewrote the address back to your JIRA instead of passing it through, because plugin returned following address:

`https://accounts.google.com/o/oauth2/auth?scope=openid+email+profile&response_type=code&state=d3fc17ad-1a4b-4449-8eb6-0d0d3eca9809&redirect_uri=https%3A%2F%2Fjira.mycompany.com%2Fopenid%2Foauth2-callback%2Fgoogle&prompt=select_account&client_id=…`

Please fix reverse proxy configuration and the plugin will function properly.

### How to debug the plugin?

Go to `Logging and profiling` and use `Configure logging level for another package` to enable logging for this plugin. Use `com.pawelniewiadomski` for package name and select `TRACE` for logging level. Once configured the plugin will log additional information to `atlassian-jira.log`