# Page Load Started

### 

## Variable Definitions

| Attribute Name|Data Source Type|Data Source|Description|
| --- | --- | --- | --- |
|Host Name (s.server)|Custom Code|hostname;|Description not provided|

## Attached Notes

<p>This event should be triggered on each page load.</p>
<p>Instructions to set the <strong>pageName </strong>attribute:</p>
<div class="ewa-rteLine"><strong>Format:&nbsp; [Site]:[Section Identifier if applicable]:[Value]</strong></div>
<div class="ewa-rteLine">&nbsp;</div>
<ul>
<li class="ewa-rteLine">Always set value of&nbsp;<strong> [Site] </strong>(for payment portal flow to be)<strong> =</strong><code> payment-portal</code></li>
<li class="ewa-rteLine"><strong>[Section Identifier if applicable] </strong>- set value from <code>pageCategory</code></li>
<li class="ewa-rteLine"><strong>[Value] -&nbsp;</strong>dynamic value of the page name.</li>
</ul>
<div class="ewa-rteLine">&nbsp;</div>
<div class="ewa-rteLine"><strong>Below is the expected value of page name that applies to all steps of Payment Portal:</strong></div>
<div class="ewa-rteLine">&nbsp;</div>
<ul>
<li class="ewa-rteLine"><strong>Payment summary Step:&nbsp;</strong>payment-portal:bookings:payment-summary</li>
<li class="ewa-rteLine"><strong>Form of Payment Step:&nbsp;</strong>payment-portal:bookings:fop</li>
<li class="ewa-rteLine"><strong>Booking Confirmation Step:</strong> payment-portal:bookings:confirmation</li>
</ul>
<hr>
<p>&nbsp;</p>
<p><strong>Setting value of siteBuilderIdentifier Attribute:</strong></p>
<p>For payment portal flow, please set value of attribute <code>sitePageBuilderIdentifier</code> to&nbsp; <code>Payment Portal Vue</code></p>
<hr>
<p><strong>Setting value of siteName Attribute:</strong></p>
<p>For payment portal flow, please set value of siteName attribute to&nbsp; <code>payment portal</code></p>
<hr>
<p><strong>Setting value of pageName (digitalEventData.computedState.page.pageName) when RBF payment steps deeplink to Payment portal.</strong></p>
<ul>
<li><strong>For Payment Summary step </strong>- pass value of page name as : <code>mobile:booking:payment:summary</code></li>
<li><strong>For Payment FOP step </strong>- pass value of page name as : <code>mobile:booking:payment:fop</code></li>
<li><strong>For Confirmation step </strong>- pass value of page name as : <code>mobile:booking:confirmation</code></li>
</ul>
<hr>
<p>&nbsp;</p>
<p><strong>Setting value of siteSection (digitalEventData.computedState.page.pageCategory)when RBF payment steps deeplink to Payment portal.</strong></p>
<ul>
<li><strong>For Payment Summary step </strong>- pass value of page name as :<code> Mobile:Bookings</code></li>
<li><strong>For Payment FOP step </strong>- pass value of page name as : <code>Mobile:Bookings</code></li>
<li><strong>For Confirmation step </strong>- pass value of page name as : <code>Mobile:Bookings</code></li>
</ul>
<hr>
<p><strong>Setting value of Site Name (digitalEventData.computedState.page.siteName) when RBF payment steps deeplink to Payment portal.</strong></p>
<ul>
<li><strong>For Payment Summary step </strong>- pass value of page name as :<code> Mobile</code></li>
<li><strong>For Payment FOP step </strong>- pass value of page name as : <code>Mobile</code></li>
<li><strong>For Confirmation step </strong>- pass value of page name as : <code>Mobile</code></li>
</ul>