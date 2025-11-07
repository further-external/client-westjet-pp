# MFA Error Presented

### 

## Variable Definitions

| Attribute Name|Data Source Type|Data Source|Description|
| --- | --- | --- | --- |
|Error Counter|Static|1|Description not provided|

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