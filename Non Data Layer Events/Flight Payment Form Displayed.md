# Flight Payment Form Displayed

### 

## Variable Definitions

| Attribute Name|Data Source Type|Data Source|Description|
| --- | --- | --- | --- |
|Flight Payment Form Displayed|Static|1|Description not provided|
|Set category to 'flight'|Static|Flight|Static value 'Flight' used as category within the adobe analytics product string.
When Flight is selected - from Flight summary onwards - set value "Flight".|

## Attached Notes

<p><strong>Tracking for Flight Segment Equipment:</strong></p>
<p>Please use the reference document&nbsp;<a aria-label="Link https://apiw.westjet.com/flight-segments/equipment-labels" rel="noopener noreferrer" href="https://apiw.westjet.com/flight-segments/equipment-labels" title="https://apiw.westjet.com/flight-segments/equipment-labels" tabindex="-1">https://apiw.westjet.com/flight-segments/equipment-labels</a>&nbsp;to set the Flight Segment Equipment (<strong>"flightSegmentEquipment")&nbsp;</strong>values.&nbsp;</p>
<p>For when bookingi involves multiple segments on a flight, the format for "flightSegmentEquipment" should be : "key/code<strong>:</strong>shortName<strong>|</strong>key/code:shortName".&nbsp;</p>
<p><strong>Format for data capture:&nbsp;</strong>Equip Code:Aircraft<strong>:RES Code</strong></p>
<p><strong>Example values:</strong></p>
<ul>
<li class="ewa-rteLine"><em><strong>One way:</strong></em>&nbsp;73H:737-800<strong>:M2H</strong></li>
<li class="ewa-rteLine"><em><strong>Round trip (regular) :</strong></em>&nbsp;73H:737-800<strong>:M2H</strong>~73W:737-700<strong>:M2W</strong></li>
<li class="ewa-rteLine"><em><strong>Round trip (with swoop Max) :</strong></em>&nbsp;73H:737-800<strong>:M2H</strong>~7M8:737-Max8<strong>:SM8</strong></li>
<li class="ewa-rteLine"><em><strong>Multi city trip (regular) :</strong></em>&nbsp;73W:737-700<strong>:M2W</strong>~73H:737-800<strong>:M2H</strong>~73H:737-800<strong>:M2H</strong></li>
<li class="ewa-rteLine"><em><strong>Multi City trip (regular) :&nbsp;</strong></em>73W:737-700<strong>:M2W</strong>~73H:737-800<strong>:M2H</strong>~7M8:737-Max8<strong>:SM8</strong></li>
</ul>
<p>&nbsp;</p>
<hr>
<p>&nbsp;</p>
<p><strong>Instructions to set value for Flight Fare Hold Id (evar159), MT Booking PNR (evar132) on Form of Payment Step:</strong></p>
<p><em>Background info:</em></p>
<p>When guest enters the Payment Portal flow, the URL will include a unique token. This Unique url with token will determine if the guest entering the payment portal flow has an&nbsp;existing booking&nbsp;or doing a&nbsp;new booking.</p>
<p>&nbsp;</p>
<ul>
<li><strong>NEW Booking Attempt</strong>
<ul>
<li>If the guest enters Payment Portal with intention to pursue a NEW booking, we set the value of&nbsp;<code>Flight Fare Hold (evar159)/flightFareHoldId (attribute)</code>&nbsp;with a new PNR in format -&nbsp;<code>YYMMDD_6DigitCode</code>.</li>
<li>We also pass value in data layer for attribute <code>mtReservationId</code>&nbsp;to "<code>not available</code>".</li>
</ul>
</li>
<li><strong>Existing Booking (Modification)</strong>
<ul>
<li>If the guest enters Payment Portal with an existing PNR, we set values for&nbsp;<code>MT Booking PNR (evar132)/ mtreservationId (attribute)</code>&nbsp;on this page, with the value of the PNR of the said booking.</li>
<li>We also pass value in data layer for attribute&nbsp; of <code>flightFareHoldId </code>to "<code>not available</code>".</li>
</ul>
</li>
</ul>
<p>The below table summarizes the possible value to be set in data layer based on above described summary on FORM OF PAYMENT STEP.&nbsp;</p>
<table border="5">
<tbody>
<tr>
<td width="312">
<p><strong>NEW bookings&nbsp;</strong></p>
</td>
<td width="312">
<p><strong>Existing Bookings</strong></p>
</td>
</tr>
<tr>
<td width="312">
<p>1. evar132(MT Booking PNR)=not available.</p>
<p>2. evar159 (Flight Fare Hold ID) = 231006_ABCDEF(<em>New Hold PNR created</em>)</p>
<p>&nbsp;</p>
</td>
<td width="312">
<p>1.&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; evar132(MT Booking PNR) = 231006_LMNOPQ</p>
<p>2.&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; evar159(Hold ID) = not available</p>
<p>&nbsp;</p>
</td>
</tr>
</tbody>
</table>
<hr>
<p>Instructions for setting values for Original Booking Channel in Data layer : <code>digitalEventData.computedState.westJetData.originalBookingChannel</code></p>
<p><strong>Possible Values:</strong></p>
<ul>
<li class="ewa-rteLine">YCB - Canadian point of origin (CAD currency)</li>
<li class="ewa-rteLine">VHQ - Euro point of origin (EUR currency)</li>
<li class="ewa-rteLine">HWW - UK point of origin (GBP currency)</li>
<li class="ewa-rteLine">BAB - All other points of origin (USD currency) TTY -</li>
<li class="ewa-rteLine">gds booking</li>
</ul>
<hr>
<p><strong>Setting value of Digital Flow Type (digitalEventData.computedState.westJetData.digitalFlowType) when RBF pages Deep links to Payment Portal</strong></p>
<p>Pass value RBF, when RBF deeplinks to Payment Portal.&nbsp;</p>
<p>&nbsp;</p>
<hr>
<p><strong>Setting value of Digital Flow Type (digitalEventData.computedState.westJetData.digitalFlowType) when MT pages Deep links to Payment Portal</strong></p>
<p>For MT Seats Flow - pass value MT Seats</p>
<p>For MT Bags Flow - pass value MT Bags</p>
<p>For MT Exchange Flow - pass value MT Exchange</p>
<p>&nbsp;</p>