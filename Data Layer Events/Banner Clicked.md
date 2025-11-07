# Banner Clicked

### 

## Javascript Code
```js
window.digitalEventData = window.digitalEventData || [];
digitalEventData.push({
  "event": "Banner Clicked",
    "westJetEvents": {
        "minCreditBannerClick": <minCreditBannerClick>
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|westJetEvents.minCreditBannerClick|boolean|Used to indicate when the “Min Credit Card”variation of the WSD + TB + CC banner contextual message is clicked on payment FOP.NOTE: This event must fire in conjunction with event537 ONLY if the“Min Credit Card”banner is clicked.|TRUE, FALSE|||||||

## Attached Notes

<p>When user meets the requirements for WSD+TB+CC message banner appears. This <strong>Banner clicked </strong>event triggers on <strong>Payment FOP&nbsp;</strong> when :</p>
<ul>
<li>WSD + TB + CC banner is clicked</li>
<li>Max TB banner is clicked</li>
<li>Max WSD banner is clicked</li>
<li>Min Credit Banner is clicked</li>
</ul>
<p>&nbsp;</p>
<table style="width: 99.9971%;" width="100%">
<tbody>
<tr>
<td style="width: 26.0005%;" width="156">
<p><strong>Events (on-click)</strong></p>
</td>
<td style="width: 51.038%;" width="320">
<p><strong>&nbsp;</strong></p>
</td>
<td style="width: 22.974%;" width="136">
<p><strong>&nbsp;</strong></p>
</td>
</tr>
<tr>
<td style="width: 26.0005%;" width="156">
<p>WSD + TB + CC Banner Click</p>
</td>
<td style="width: 51.038%;" width="320">
<p>Used to indicate when the WSD + TB+ CC banner contextual message is clicked on the Payment page.</p>
</td>
<td style="width: 22.974%;" width="136">
<p>wsdTbCcBannerClick</p>
</td>
</tr>
<tr>
<td style="width: 26.0005%;" width="156">
<p>Max Travel Bank Banner Click</p>
</td>
<td style="width: 51.038%;" width="320">
<p>Used to indicate when the &ldquo;Max Travel Bank&rdquo; variation of the WSD + TB + CC banner contextual message is clicked on payment FOP.</p>
<p><strong>NOTE: This event must fire in conjunction with wsdTbCcBannerClick ONLY if the &ldquo;Max Travel Bank&rdquo; banner is clicked.</strong></p>
</td>
<td style="width: 22.974%;" width="136">
<p>maxTbBannerClick</p>
</td>
</tr>
<tr>
<td style="width: 26.0005%;" width="156">
<p>Max WSD Banner Click</p>
</td>
<td style="width: 51.038%;" width="320">
<p>Used to indicate when the &ldquo;Max WSD&rdquo; variation of the WSD + TB + CC banner contextual message is clicked on payment FOP.</p>
<p><strong>NOTE: This event must fire in conjunction with wsdTbCcBannerClick ONLY if the &ldquo;Max WSD&rdquo; banner is clicked.</strong></p>
</td>
<td style="width: 22.974%;" width="136">
<p>maxWsdBannerClick</p>
</td>
</tr>
<tr>
<td style="width: 26.0005%;" width="156">
<p>Min Credit Card Banner Click</p>
</td>
<td style="width: 51.038%;" width="320">
<p>Used to indicate when the &ldquo;Min Credit Card&rdquo; variation of the WSD + TB + CC banner contextual message is clicked on payment FOP.</p>
<p><strong>NOTE: This event must fire in conjunction with wsdTbCcBannerClick ONLY if the &ldquo;Min Credit Card&rdquo; banner is clicked.</strong></p>
</td>
<td style="width: 22.974%;" width="136">
<p>minCreditBannerClick</p>
</td>
</tr>
</tbody>
</table>
