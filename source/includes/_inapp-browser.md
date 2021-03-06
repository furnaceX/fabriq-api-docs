# Inapp Browser

> **Definition**

```text
https://portal.fabriq.io/#/?client_id={CLIENT_ID}&access_token={ACCESS_TOKEN}
```

To simplify the experience of a user configuring his or her FABRIQ account, you can launch
an in-app browser that's directed to a custom FABRIQ portal.  There, the user can add/remove
contacts, change account settings, etc.

When the in-app browser is closed, your app should refresh the user and settings objects to get the latest
changes made to their account.

The in-app browser should be directed to the following URL:

<code style="display:block;text-align:center;margin-top:20px;color:#000;padding:10px;white-space:nowrap;">
https://portal.fabriq.io/#/?client_id={CLIENT_ID}&access_token={ACCESS_TOKEN}
</code>

<br/>

ARGUMENTS ||
---------:        | -----------
client_id<br>**required**  | Your app `client_id`<br>*URL parameter*
access_token<br>**required**  | The user's `access_token`<br>*URL parameter*
