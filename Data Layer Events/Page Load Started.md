# Page Load Started

### Page Load Started is part of the page load sequence, including virtual page loads in the case of single page apps, and must be the first event pushed in the page load event sequence.

## Javascript Code
```js
window.digitalEventData = window.digitalEventData || [];
digitalEventData.push({
  "event": "Page Load Started",
    "page": {
        "pageCategory": "<pageCategory>",
        "pageName": "<pageName>",
        "siteCurrency": "<siteCurrency>",
        "siteName": "<siteName>"
    },
    "westJetData": {
        "languageLocale": "<languageLocale>",
        "sitePageBuilderIdentifier": "<sitePageBuilderIdentifier>"
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|page.pageCategory|string|General category or Site Section of the page. Top level of page hierarchy.|Home, About Us, Shop, Account, Blog, Investors|||||||
|page.pageName|string|Describes the page and its content specifically. |product - XYZ123, Mens - Tops - Sweaters, Order Confirmation|||||||
|page.siteCurrency|string|Currency in which prices are displayed.  ISO 4217 \(3 character alpha\), uppercase|USD, CAD, EUR, GBP, CHF|^[A-Z]{3}$||||||
|page.siteName|string|Common language used within the business to refer to the website. May be specific County Sites.|Prospecting-EU, Prospecting-US, Member Portal, Shop-CA, Shop-US, Shop-EU|||||||
|westJetData.languageLocale|string|The locale is the combination of the Language \(present URL prefix\) + Country Code \(i.e. “EN-AG” for English version of Antigua and Barbuda site\)|en-ag, en-ca|||||||
|westJetData.sitePageBuilderIdentifier|string|Indicates how analytics is injected to the page – via the scode or with TMS Adobe Launch using data layer and describes the technology stack applicable. 

Possible values: Unavailable  – indicates the page analytics is NOT injected via Adobe Launch.  AEM – indicates the page analytics is injected via Adobe Launch and AEM is the supporting CMS \(applicable to AEM CMS only\). DCI Angular – indicates the page analytics is injected via Adobe Launch and technology support is Angular JS \(applicable to DCI flow only\). RBF Vue – indicates the page analytics is injected via Adobe Launch and is supporting Vue JS technology \(applicable to RBF flow only\). 
Payment Portal Vue - indicates the page analytics are injected via Adobe Launch and is supporting Vue JS technology.
WVI xx – indicates the page analytics is injected via Adobe Launch and is supporting xx technology \(applicable to WVI flow only\)|RBF|||||||

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
