# Flight Booking Confirmed

### 

## Variable Definitions

| Attribute Name|Data Source Type|Data Source|Description|
| --- | --- | --- | --- |
|Add 'purchase' to s.events|Static|1|Description not provided|
|Flight Booking Confirmed|Static|1|Description not provided|
|Set category to 'flight'|Static|Flight|Static value 'Flight' used as category within the adobe analytics product string.
When Flight is selected - from Flight summary onwards - set value "Flight".|
|Set category to 'payment'|Static|Flight|Static value 'Flight' used as category within the adobe analytics product string.
When Flight is selected - from Flight summary onwards - set value "Flight".|
|Set productID using Payment ID|Static|Flight|Static value 'Flight' used as category within the adobe analytics product string.
When Flight is selected - from Flight summary onwards - set value "Flight".|
|holdToConfirmedReservationId|Static|D=v159|Captures the Booking reservation ID that was created on hold when the guest entered the RBF Payment Portal for the first time.
Ideally this value is the same as we see in evar159.|

## Attached Notes

<p>This event is triggered on the Confirmation Step in&nbsp; payment portal.</p>
<p><strong>Event attribute notes:</strong></p>
<ul>
<li><strong>rbfVoucherSeatsAdded&nbsp;</strong>- Used to capture the number of PRS Voucher Seats added, for bookings with seats<br><strong>NOTE:&nbsp;</strong>To be set only when applicable. If no voucher seats are selected, set "rbfVoucherSeatsAdded" attribute to an empty string. Pass $0 to&nbsp;<strong>rbfCompSeatsAdded&nbsp;</strong>when guests are offered complimentary seats – especially for&nbsp;<em>premium seats, seat vouchers(PRS vouchers).</em></li>
<li><strong>rbfSeatsBkgComp -&nbsp;</strong>this is a counter event. Indicates that the booking contained&nbsp;<em>complimentary seats only</em><br><strong>NOTE:&nbsp;</strong>To be set only when applicable&nbsp;</li>
<li><strong>rbfSeatsBkgVoucher</strong>&nbsp; - is a counter event that indicates that the booking contained&nbsp;<em>PRS voucher seats&nbsp;</em><strong>and&nbsp;</strong><em>complimentary seats</em>&nbsp;.</li>
<li><strong>rbfCompSeatsAdded&nbsp;</strong>- Used to capture the number of&nbsp;<em>Complimentary Seats&nbsp;</em>added, for bookings with seats.&nbsp;<strong>NOTE</strong>: To be set only when applicable</li>
<li><strong>rbfSeatsBkgVoucherComp</strong>&nbsp;- Indicates that the booking contained&nbsp;<em>PRS voucher seats</em>&nbsp;and&nbsp;<em>complimentary seats.</em><strong>NOTE:&nbsp;</strong>To be set only when applicable</li>
<li><strong>seatBooking</strong>&nbsp;- Indicates seats were purchased/added (in-path) along with the flight booking (regardless of types of seats involved).&nbsp;<strong>NOTE:&nbsp;</strong>To be set only when applicable&nbsp;</li>
</ul>
<hr>
<p><strong>connection Non-Stop attribute settings :</strong></p>
<table width="680">
<tbody>
<tr>
<td width="188">
<p><strong>Scenario</strong></p>
</td>
<td width="170">
<p><strong>Value to be captured</strong></p>
</td>
<td width="321">
<p><strong>Comments</strong></p>
</td>
</tr>
<tr>
<td width="188">
<p>Non-Stop flights only</p>
</td>
<td width="170">
<p>non-stop</p>
</td>
<td width="321" rowspan="3">
<p>Values are applicable for all trip scenarios, regardless of the number of flights (i.e. one-way, round-trip or multi-city)</p>
</td>
</tr>
<tr>
<td width="188">
<p>Non-Stop and Connection flights</p>
</td>
<td width="170">
<p>non-stop + connection</p>
</td>
</tr>
<tr>
<td width="188">
<p>Connection flights only</p>
</td>
<td width="170">
<p>connection</p>
</td>
</tr>
</tbody>
</table>
<hr>
<p><strong>Form of Payment Tracking and Ancillary Form of Payment Tracking:</strong></p>
<p>The table outlines the actual values to be captured for the Form of Payment tracking. For split payments a pipe delimiter (“|”) is to be used to separate the multiple form of payment values.<br><em><br>NOTE: Please refer to the second screenshot/table shown below to see the proper way in which to capture split payment values (the intention is to avoid capturing the same split payment values in different ways) { screenshot to be attached later when feature is available}<strong><br><br></strong></em></p>
<table width="343">
<tbody>
<tr>
<td width="343" colspan="2">
<p><strong>Form of Payment Tracking Values</strong></p>
</td>
</tr>
<tr>
<td width="158">
<p><strong>FOP</strong></p>
</td>
<td width="185">
<p><strong>Value to be captured</strong></p>
</td>
</tr>
<tr>
<td width="158">
<p>Visa</p>
</td>
<td width="185">
<p>visa</p>
</td>
</tr>
<tr>
<td width="158">
<p>MasterCard</p>
</td>
<td width="185">
<p>mastercard</p>
</td>
</tr>
<tr>
<td width="158">
<p>American Express</p>
</td>
<td width="185">
<p>amex</p>
</td>
</tr>
<tr>
<td width="158">
<p>Discover</p>
</td>
<td width="185">
<p>discover</p>
</td>
</tr>
<tr>
<td width="158">
<p>Travel Bank</p>
</td>
<td width="185">
<p>tb</p>
</td>
</tr>
<tr>
<td width="158">
<p>WestJet Dollars</p>
</td>
<td width="185">
<p>wsd</p>
</td>
</tr>
<tr>
<td width="158">
<p>Gift Card</p>
</td>
<td width="185">
<p>giftcard</p>
</td>
</tr>
</tbody>
</table>
<hr>
<p><strong>Type of Booking Tracking :</strong></p>
<p>&nbsp;</p>
<p>The table outlines the actual values to be captured for the Type of Booking tracking.<strong><em><br><br></em></strong></p>
<table width="544">
<tbody>
<tr>
<td width="544" colspan="2">
<p><strong>Type of Booking</strong><strong>&nbsp;Tracking Values</strong></p>
</td>
</tr>
<tr>
<td width="330">
<p><strong>Scenario</strong></p>
</td>
<td width="214">
<p><strong>Value to be captured</strong></p>
</td>
</tr>
<tr>
<td width="330">
<p>Flight only purchased</p>
</td>
<td width="214">
<p>flight</p>
</td>
</tr>
<tr>
<td width="330">
<p>Flight and seats purchased</p>
</td>
<td width="214">
<p>flight+seats</p>
</td>
</tr>
<tr>
<td width="330">
<p>Flight, seats and car rental purchased</p>
</td>
<td width="214">
<p>flight+seats+cars</p>
</td>
</tr>
<tr>
<td width="330">
<p>Flight, travel insurance and seats purchased</p>
</td>
<td width="214">
<p>flight+insurance+seats</p>
</td>
</tr>
<tr>
<td width="330">
<p>Flight and car rental purchased</p>
</td>
<td width="214">
<p>flight+cars</p>
</td>
</tr>
<tr>
<td width="330">
<p>Flight and travel insurance purchased</p>
</td>
<td width="214">
<p>flight+insurance</p>
</td>
</tr>
<tr>
<td width="330">
<p>Flight, travel insurance, seats and car rental purchased</p>
</td>
<td width="214">
<p>flight+insurance+seats+cars</p>
</td>
</tr>
<tr>
<td width="330">
<p>Flight, travel insurance and car rental purchased</p>
</td>
<td width="214">
<p>flight+insurance+cars</p>
</td>
</tr>
</tbody>
</table>
<hr>
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
<hr>
<p><strong>Instructions to set value for Flight Fare Hold Id (evar159), MT Booking PNR (evar132) and Booking Reservation ID (evar33) on Confirmation Step:</strong></p>
<p><em>Background info:</em></p>
<p>When guest enters the Payment Portal flow, the URL will include a unique token. This Unique url with token will determine if the guest entering the payment portal flow has an&nbsp;existing booking&nbsp;or doing a&nbsp;new booking.</p>
<p>&nbsp;</p>
<ul>
<li><strong>NEW Booking Attempt</strong>
<ul>
<li>If the guest enters Payment Portal with intention to pursue a NEW booking, we set the value of&nbsp;<code>Flight Fare Hold (evar159)/flightFareHoldId (attribute)</code>&nbsp;with a new PNR in format -&nbsp;<code>YYMMDD_6DigitCode</code>.</li>
<li>We also pass value in data layer for attribute&nbsp;<code>mtReservationId</code>&nbsp;to "<code>not available</code>".</li>
<li>The value of <code>bookingReservationID</code> (attribute) should be set to value available in <code>flightFareHoldID</code>.</li>
</ul>
</li>
<li><strong>Existing Booking (Modification)</strong>
<ul>
<li>If the guest enters Payment Portal with an existing PNR, we set values for&nbsp;<code>MT Booking PNR (evar132)/ mtreservationId (attribute)</code>&nbsp;on this page, with the value of the PNR of the said booking.</li>
<li>We also pass value in data layer for attribute&nbsp; of&nbsp;<code>flightFareHoldId&nbsp;</code>to "<code>not available</code>".</li>
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
<p>&nbsp;</p>
<hr>
<p><strong>Instructions to set the data layer events </strong>westJetEvents.numberOfGuestNameChangesMade<strong> and </strong>westJetEvents.guestNameChangesRevenue</p>
<p>The events <code>westJetEvents.numberOfGuestNameChangesMade</code> and <code>westJetEvents.guestNameChangesRevenue</code> are part of release 2 of payment portal and includes guest ability to change the name of guests on an <span style="text-decoration: underline;">existing booking through through a Live Chat agent</span>. Therefore, these two events MUST only be set for EXISTING Booking scenarios, and&nbsp; DO NOT SET for New Bookings scenarios.</p>
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
<p><strong>WJTP Requirements :</strong></p>
<p>&nbsp;</p>
<p>Setting value of Product Booking Type -&nbsp;</p>
<div>Capture the type of booking made through the traffic source in WJTP.</div>
<div>&nbsp;</div>
<div>Booking type (RevenueGuest, WJTP Standby, WJTP Confirmed, etc.)</div>
<div><strong>Expected Booking Type Values in WJTP:</strong><br>&nbsp; &nbsp; • WJTP Standby<br>&nbsp; &nbsp; • WJTPConfirmed</div>
<div>&nbsp;</div>
<div><strong>LiveChat</strong></div>
<div>• RevenueGuest (by default anyone entering payment portal not coming from WJTP)"</div>
<hr>
<p><strong>Setting the count of guest type in booking:</strong></p>
<ul>
<li>DO NOT trigger the below events if Product Booking Type is <code>RevenueGuest</code>.</li>
<li>If any of the below guest type is NOT in a booking, then pass value 0 for them.</li>
</ul>
<table width="285">
<tbody>
<tr>
<td width="285" style="width: 565.957px;"><br><code>digitalEventData.computedState.westJetEvents.numberOfEmployeeConfirmed</code></td>
</tr>
<tr>
<td width="285" style="width: 565.957px;"><br><code>digitalEventData.computedState.westJetEvents.numberOfEmployeeStandby</code></td>
</tr>
<tr>
<td width="285" style="width: 565.957px;"><br><code>digitalEventData.computedState.westJetEvents.numberOfCompanionConfirmed</code></td>
</tr>
<tr>
<td width="285" style="width: 565.957px;"><br><code>digitalEventData.computedState.westJetEvents.numberOfCompanionStandby</code></td>
</tr>
<tr>
<td width="285" style="width: 565.957px;"><br><code>digitalEventData.computedState.westJetEvents.numberOfDependentsConfirmed</code></td>
</tr>
<tr>
<td width="285" style="width: 565.957px;"><br><code>digitalEventData.computedState.westJetEvents.numberOfDependentsConfirmed</code></td>
</tr>
<tr>
<td width="285" style="width: 565.957px;"><br><code>digitalEventData.computedState.westJetEvents.numberOfParentsStandby</code></td>
</tr>
<tr>
<td width="285" style="width: 565.957px;"><br><code>digitalEventData.computedState.westJetEvents.numberOfBuddyPassStandby</code></td>
</tr>
<tr>
<td width="285" style="width: 565.957px;"><br><code>digitalEventData.computedState.westJetEvents.numberOfAvailableCrewMember</code></td>
</tr>
</tbody>
</table>
<p>&nbsp;</p>
<hr>
<p><strong>Flight Fare Bundle:</strong> - Requirement for WJTP New Booking Widget and Shared RBF Steps (WJTP Phase 2)</p>
<p><strong>DEV NOTE:</strong><br>&nbsp;When guests select a Standby flight on Flight Search Results page, flight fare bundle should reflect their fare class as "Standby".</p>
<p>&nbsp;</p>
<hr>
<p><strong>Setting value of Digital Flow Type (digitalEventData.computedState.westJetData.digitalFlowType) when RBF pages Deep links to Payment Portal</strong></p>
<p>Pass value RBF, when RBF deeplinks to Payment Portal.&nbsp;</p>
<p>&nbsp;</p>
<hr>
<p><strong>Setting value of Digital Flow Type (digitalEventData.computedState.westJetData.digitalFlowType) when MT pages Deep links to Payment Portal</strong></p>
<p>For MT Seats Flow - pass value MT Seats</p>
<p>For MT Bags Flow - pass value MT Bags</p>
<p>For MT Exchange Flow - pass value MT Exchange</p>