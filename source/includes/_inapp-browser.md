# Inapp Browser

> Definition

```text
https://portal.fabriq.io/#/?access_token={ACCESS_TOKEN}
```

To simplify the experience of a user configuring his or her FABRIQ account, you can launch
an in-app browser that's directed to a custom FABRIQ portal.  There, the user can add/remove
contacts, change account settings, etc.

When the in-app browser is closed, your app should refresh the user and settings objects to get the latest
changes made to their account.

The in-app browser should be directed to the following URL:

<code style="margin:auto;">
https://portal.fabriq.io/#/?access_token={ACCESS_TOKEN}
</code>

<br/>

ARGUMENTS ||
---------:        | -----------
access_token <br>**required**  | The user's access_token
