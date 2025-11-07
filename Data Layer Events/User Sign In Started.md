# User Sign In Started

### 

## Javascript Code
```js
window.digitalEventData = window.digitalEventData || [];
digitalEventData.push({
  "event": "User Sign In Started",
    "westJetEvents": {
        "mfaEnrollmentComplete": <mfaEnrollmentComplete>,
        "rbfOptionalSignInStep": <rbfOptionalSignInStep>
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|westJetEvents.mfaEnrollmentComplete|boolean|Captures the MFA enrollment completions. 

To be set when - while registering for MFA, guest enters code, clicks "Confirm" CTA and "Successfully enrolled messaging appears.|TRUE, FALSE|||||||
|westJetEvents.rbfOptionalSignInStep|boolean|Indicates the sign in modal was presented as an optional step during a booking flow.|TRUE, FALSE|||||||

## Attached Notes

<p>This event should be triggered on the Optional Sign in Step {Lightbox overlay} step in Payment Portal.</p>
