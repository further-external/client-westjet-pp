# MFA Enrollment Completed

### 

## Javascript Code
```js
window.digitalEventData = window.digitalEventData || [];
digitalEventData.push({
  "event": "MFA Enrollment Completed",
    "westJetEvents": {
        "mfaEnrollmentComplete": <mfaEnrollmentComplete>
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|westJetEvents.mfaEnrollmentComplete|boolean|Captures the MFA enrollment completions. 

To be set when - while registering for MFA, guest enters code, clicks "Confirm" CTA and "Successfully enrolled messaging appears.|TRUE, FALSE|||||||




