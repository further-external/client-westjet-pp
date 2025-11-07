# User Signed In

### 

## Variable Definitions

| Attribute Name|Data Source Type|Data Source|Description|
| --- | --- | --- | --- |
|Count MFA Sign Ins|Static|1|Captures the number of times that an MFA enrolled user, successfully signs in.|
|Count Sign Ins|Static|1|Description not provided|

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