# User Detected

### This event is part of the page load sequence, including virtual page loads in the case of single page apps, and must be pushed between the `Page Load Started` and `Page Load Completed` events.

## Javascript Code
```js
window.digitalEventData = window.digitalEventData || [];
digitalEventData.push({
  "event": "User Detected",
    "user": {
        "custKey": "<custKey>",
        "loginStatus": "<loginStatus>",
        "userType": "<userType>"
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|user.custKey|string|Unique identifier of a customer.  Any id's considered PII must be hashed. ||||||||
|user.loginStatus|string|Describes the login state of the user|logged in, logged out, guest|||||||
|user.userType|string|Describes the type of the user.  Often used to differentiate customers from employees or associates. |employee, guest, agent, customer|||||||

## Attached Notes

<p><strong>User Detected</strong>&nbsp;is triggered on each page load, irrespective of user is loggedIn or loggedOut.&nbsp;<em>&nbsp;</em></p>
<p><strong>Possible values for userSignInStatus :&nbsp;<em>{A side note, in current RBF implementation, loginStatus is also known as : loggedInState}</em></strong></p>
<ul>
<li>Logged In</li>
<li>Not Logged In</li>
</ul>
<p>&nbsp;</p>
<p><strong>Note:</strong>&nbsp;If guest is not logged in, the&nbsp;<strong>userType&nbsp;</strong>attribute should still exist in data layer, but should be set to "unknown".</p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p><strong>Possible values for userType:&nbsp;<em>{A side note, in current RBF implementation,userType is also known as : Member Tier}</em></strong></p>
<ul>
<li>Teal</li>
<li>Silver</li>
<li>Gold</li>
<li>Platinum</li>
</ul>
