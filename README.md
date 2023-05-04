# radsystem-msal
Implement Azure AD - MSAL plugin on RADSystem application based
This method currently support for SPA based application
Other application mode need to improve!!!

# prerequisite
Setup Azure app or use existing azure app
Allow api permission to User.Read scope

# how-to-use
Copy these files on /frontpage folder of RadSystem generated project folder<br/>
Edit file authConfig.js<br/>
Set CLIENTID & Authority URL based on Azure App Registrations<br/>
any page/route that need to protected just add (see router/index.js for implementation) <br/>
...<br/>
meta : {	requiresAuth: true }, <br/>
...<br/>

Done

# to-do
Logout link/url, put these on button.vue and set on click event to logoutRedirect function

example
import { msalInstance } from "src/authConfig"

const logoutRedirect = () => {
  msalInstance.logoutRedirect();
}

...

