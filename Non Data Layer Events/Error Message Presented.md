# Error Message Presented

### 

## Variable Definitions

| Attribute Name|Data Source Type|Data Source|Description|
| --- | --- | --- | --- |
|Error Counter|Static|1|Description not provided|

## Attached Notes

<p>Although errors are not planned, they do occasionally happen. Error tracking applies to both general errors as well as web forms to capture validation, processing or other errors.</p>
<p>One each page load if there is error encountered, this event is required to be triggered.</p>
<p>&nbsp;</p>
<p>The&nbsp;<strong>errorCode&nbsp;</strong>should be captured in following format:</p>
<p>&nbsp;</p>
<p><code>errorCode = pageName|elementName|fieldname|errorDescription</code></p>
<table border="1">
<tbody>
<tr>
<td><strong>Item</strong></td>
<td><strong>Description</strong></td>
</tr>
<tr>
<td>pageName</td>
<td>Name of page where the form element is placed.</td>
</tr>
<tr>
<td>fieldName</td>
<td>Name of data field that failed validation.NOTE: If the error doesn’t involve a form/form field, this value should be left blank (but pipe delimiters are to remain)</td>
</tr>
<tr>
<td>errorDescription</td>
<td>This is the text of the errormessage presented to the Guest (an abbreviated format is fine, as long as the value is intuitive enough to understand the type of error/issue)</td>
</tr>
</tbody>
</table>
<p>&nbsp;</p>
<p>The error message details should be included as a single string of pipe ‘|’ delimited values in the “description:” field, such as:<strong>pageName|elementName|fieldname|errorDescription</strong></p>
<p><strong>Example</strong>:random-page|promo-registration-form|postal-code|special-character-issueExample of a Non-form related error (notice the empty values with pipe delimiters maintained):random-page|||random-description-of-error</p>
<p>&nbsp;</p>
<hr>
<p><strong>Error Tracking Notes for Sunrise - Points Redemption</strong></p>
<div class="ewa-rteLine"><strong>Format:&nbsp;</strong><code>pageName|elementName|fieldname|errorDescription</code></div>
<div class="ewa-rteLine">&nbsp;</div>
<div class="ewa-rteLine"><strong>DEV NOTE:</strong>&nbsp;Set below possible values, depending on the error applicable. Multiple possible errors that can be triggered are as below:</div>
<div class="ewa-rteLine"><code>pageName|minimum-not-reached</code></div>
<div class="ewa-rteLine"><code>pageName|maximum-reached</code></div>
<div class="ewa-rteLine"><code>pagename|error-in-applying</code></div>
<div class="ewa-rteLine"><code>pageName|error-in-fetching-redeemable-points</code></div>