# User Signed In

### 

## Javascript Code
```js
window.digitalEventData = window.digitalEventData || [];
digitalEventData.push({
  "event": "User Signed In",
    "user": {
        "custKey": "<custKey>",
        "loginStatus": "<loginStatus>",
        "mfaMethod": "<mfaMethod>",
        "system": "<system>",
        "userType": "<userType>"
    },
    "westJetData": {
        "wsdTbBalance": "<wsdTbBalance>"
    },
    "westJetEvents": {
        "loginAttempt": <loginAttempt>,
        "mfaLoginAttempt": <mfaLoginAttempt>
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|user.custKey|string|Unique identifier of a customer.  Any id's considered PII must be hashed. ||||||||
|user.loginStatus|string|Describes the login state of the user|logged in, logged out, guest|||||||
|user.mfaMethod|string|Captures whether the guest uses Email or SMS as their MFA method.

DEV NOTE:
Guest who is enrolled in MFA, attempts to log in \(step 2 of sign-in flow\).|Email, SMS|||||||
|user.system|string|Describes the system that the user is logged into.  \(rarely used\). |admin, shop, member|||||||
|user.userType|string|Describes the type of the user.  Often used to differentiate customers from employees or associates. |employee, guest, agent, customer|||||||
|westJetData.wsdTbBalance|string|Captures the Travel Bank balance and WestJet Dollar \(WSD\) balance upon guest signs in. This value will be collected in v17 delineating with a pipe \(ie: eVar17 = 622WSD\|0TB\).|345, 0, 3456|||||||
|westJetEvents.loginAttempt|boolean|Set whenever a user attempts to login \(regardless of a successful or failed authentication\)|TRUE, FALSE|||||||
|westJetEvents.mfaLoginAttempt|boolean|Set whenever a guest attempts to login using MFA \(regardless of a successful or failed authentication\).|TRUE, FALSE|||||||

## Attached Notes

<p><strong>Notes for userType -&nbsp;</strong></p>
<p>Capture the tier level of the member logged in.</p>
<p><strong>Possible values for userType&nbsp;</strong>{<em>formally known as member tier in current RBF implementation}</em></p>
<ul>
<li>Teal</li>
<li>Silver</li>
<li>Gold</li>
<li>Platinum</li>
</ul>
<p><strong>Note:</strong>&nbsp;If guest is not logged in, the&nbsp;<strong>userType&nbsp;</strong>attribute should still exist in data layer, but should be set to "unknown".</p>
