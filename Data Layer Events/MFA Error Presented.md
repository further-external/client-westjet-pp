# MFA Error Presented

### 

## Javascript Code
```js
window.digitalEventData = window.digitalEventData || [];
digitalEventData.push({
  "event": "MFA Error Presented",
    "error": {
        "errorCode": "<errorCode>"
    },
    "user": {
        "custKey": "<custKey>",
        "loginStatus": "<loginStatus>",
        "mfaMethod": "<mfaMethod>",
        "signInError": "<signInError>",
        "system": "<system>"
    },
    "westJetEvents": {
        "loginAttempt": <loginAttempt>
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|error.errorCode|string|Error code or Error message presented to the user|Credit Card Authorization Failed , EC345, Form is incomplete|||||||
|user.custKey|string|Unique identifier of a customer.  Any id's considered PII must be hashed. ||||||||
|user.loginStatus|string|Describes the login state of the user|logged in, logged out, guest|||||||
|user.mfaMethod|string|Captures whether the guest uses Email or SMS as their MFA method.

DEV NOTE:
Guest who is enrolled in MFA, attempts to log in \(step 2 of sign-in flow\).|Email, SMS|||||||
|user.signInError|string|The type of failure that occured during a sign in attempt||||||||
|user.system|string|Describes the system that the user is logged into.  \(rarely used\). |admin, shop, member|||||||
|westJetEvents.loginAttempt|boolean|Set whenever a user attempts to login \(regardless of a successful or failed authentication\)|TRUE, FALSE|||||||

## Attached Notes

<p><span data-teams="true">When signin errors, we rely on the MFA errored event to capture the error.&nbsp;</span>Moreso when they are triggered.</p>
<ul>
<li>User Sign In Error is triggered&nbsp;
<ul>
<li><s>when Username/password login fails.&nbsp;</s>This is now covered by MFA Error Presented.</li>
<li>when auth succeeds but subsequent profile data calls fail</li>
</ul>
</li>
</ul>
<p><strong>NEW MFA sign in flow:</strong></p>
<ol>
<li>Sign in to get accessToken
<ol>
<li>on error
<ol>
<li><s>trigger User Sign In Errored</s></li>
<li>trigger MFA error presented (migrate data points from above event into this one)</li>
</ol>
</li>
</ol>
</li>
<li>Use accessToken to retrieve profile data
<ol>
<li>on error
<ol>
<li>trigger User Sign In Errored</li>
</ol>
</li>
</ol>
</li>
</ol>
<p>Per above flow change, the below attributes are now added to MFA Error Presented DL event.</p>
<ol>
<li>user signin errors - e50</li>
<li>login attempt - e60</li>
<li>userid- v28</li>
<li>user sign in status - v63</li>
<li>user athenication system prop - prop50</li>
<li>user sign in error - prop55</li>
</ol>
