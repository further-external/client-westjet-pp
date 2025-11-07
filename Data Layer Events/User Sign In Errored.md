# User Sign In Errored

### 

## Javascript Code
```js
window.digitalEventData = window.digitalEventData || [];
digitalEventData.push({
  "event": "User Sign In Errored",
    "user": {
        "loginStatus": "<loginStatus>",
        "mfaMethod": "<mfaMethod>",
        "signInError": "<signInError>",
        "system": "<system>"
    },
    "westJetEvents": {
        "loginAttempt": <loginAttempt>,
        "mfaLoginAttempt": <mfaLoginAttempt>,
        "smNoLinkedAccount": <smNoLinkedAccount>
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|user.loginStatus|string|Describes the login state of the user|logged in, logged out, guest|||||||
|user.mfaMethod|string|Captures whether the guest uses Email or SMS as their MFA method.

DEV NOTE:
Guest who is enrolled in MFA, attempts to log in \(step 2 of sign-in flow\).|Email, SMS|||||||
|user.signInError|string|The type of failure that occured during a sign in attempt||||||||
|user.system|string|Describes the system that the user is logged into.  \(rarely used\). |admin, shop, member|||||||
|westJetEvents.loginAttempt|boolean|Set whenever a user attempts to login \(regardless of a successful or failed authentication\)|TRUE, FALSE|||||||
|westJetEvents.mfaLoginAttempt|boolean|Set whenever a guest attempts to login using MFA \(regardless of a successful or failed authentication\).|TRUE, FALSE|||||||
|westJetEvents.smNoLinkedAccount|boolean|Set when a failed sign-in attempt occurs due to the user trying to login using a social media profile that is not yet connected to his or her WestJet ID|TRUE, FALSE|||||||




