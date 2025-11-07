# Flight Payment Summary Displayed

### This event is part of the page load sequence, including virtual page loads in the case of single page apps, and must be pushed between the `Page Load Started` and `Page Load Completed` events.

## Javascript Code
```js
window.digitalEventData = window.digitalEventData || [];
digitalEventData.push({
  "event": "Flight Payment Summary Displayed",
    "airTravel": {
        "bookingLeadTime": "<bookingLeadTime>",
        "duration": "<duration>",
        "flightFareHoldId": "<flightFareHoldId>",
        "flightList": [
            {
                "flightFareBundle": "<flightFareBundle>",
                "flightSegmentEquipment": "<flightSegmentEquipment>",
                "numberOfBagsAddedOrPurchased": "<numberOfBagsAddedOrPurchased>",
                "numberOfReturningFlightFirstBagsAdded": "<numberOfReturningFlightFirstBagsAdded>",
                "numberOfReturningFlightSecondBagsAdded": "<numberOfReturningFlightSecondBagsAdded>",
                "tripId": "<tripId>",
                "upFareBundle": "<upFareBundle>"
            }
        ],
        "numAdults": "<numAdults>",
        "numChildren": "<numChildren>",
        "numInfants": "<numInfants>"
    },
    "booking": {
        "mtreservationId": "<mtreservationId>"
    },
    "product": {
        "tax": "<tax>"
    },
    "promoCode": {
        "discountCode": "<discountCode>"
    },
    "westJetData": {
        "bagPriceDesignatorCode": "<bagPriceDesignatorCode>",
        "bagPricesOffered": "<bagPricesOffered>",
        "buyUpRevMule": "<buyUpRevMule>",
        "depDest": "<depDest>",
        "departureCode": "<departureCode>",
        "departureDate": "<departureDate>",
        "destinationCode": "<destinationCode>",
        "digitalFlowType": "<digitalFlowType>",
        "lowHighSelectedFareToUpsellFarePerGuestPerDirection": "<lowHighSelectedFareToUpsellFarePerGuestPerDirection>",
        "originalBookingChannel": "<originalBookingChannel>",
        "productBookingType": "<productBookingType>",
        "returnDate": "<returnDate>",
        "voucherType": "<voucherType>"
    },
    "westJetEvents": {
        "departingFlightBag1PriceOffered": <departingFlightBag1PriceOffered>,
        "departingFlightBag2PriceOffered": <departingFlightBag2PriceOffered>,
        "scAdd": <scAdd>
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|airTravel.bookingLeadTime|string|Number of days ahead of departure for the first segment of a trip.|zero, 1, 20, 22, 33|^([0-9])|(zero)$||||||
|airTravel.duration|string|Number of days from the first segment departure to the final segment departure. For One-Way trips and Round Trip same day trips the duration is always 0.|zero, 1, 2, 5, 13, 20|||||||
|airTravel.flightFareHoldId|string|A unique identifier of a temporary hold placed on a flight fare.
The PNR will prepend with date format in YYMMDD.
Format : YYMMDD\_6\_digitPNRCode
DEV NOTE:
                If the guest enters the Payment Portal for a NEW booking, set the Flight Fare Hold ID value of hold PNR. Example - 230810\_ABCDEF.
                If the guest enters the Payment Portal for an existing booking, set value to "not available" on Payment Summary Step, Form of Payment Step and on Payment Confirmation step.|ABCDEF,|||||||
|airTravel.flightList[n].flightFareBundle|string|Flight Fare Bundle describes the fare bundle chosen by the user. e.g. Basic, Econo, EconoRewards|Basic, Econo, EconoRewards, EconoFlex, Premium|||||||
|airTravel.flightList[n].flightSegmentEquipment|string|The equipment that flies a flight segment. \(e.g. Boeing 737 MAX 8\).

Update the data capture to include RES Equip code appended at the end using : \(colon\) as a delimiter.

Updated Format: Equip Code:Aircraft:RES Code

Example Values:
- one way: 73H:737-800:M2H
- round trip \(regular\) : 73H:737-800:M2H\~73W:737-700:M2W
- round trip \(with swoop Max\) : 73H:737-800:M2H\~7M8:737-Max8:SM8
- multi trip \(regular\) : 73W:737-700:M2W\~73H:737-800:M2H\~73H:737-800:M2H
- multi trip \(regular\) : 73W:737-700:M2W\~73H:737-800:M2H\~7M8:737-Max8:SM8"|one way: 73H:737-800:M2H - round trip \(regular\) : 73H:737-800:M2H\~73W:737-700:M2W - round trip \(with swoop Max\) : 73H:737-800:M2H\~7M8:737-Max8:SM8 - multi trip \(regular\) : 73W:737-700:M2W\~73H:737-800:M2H\~73H:737-800:M2H - multi trip \(regular\) : 73W:737-700:M2W\~73H:737-800:M2H\~7M8:737-Max8:SM8|||||||
|airTravel.flightList[n].numberOfBagsAddedOrPurchased|string|Captures the number of net new bags added on RBF Bags page. Format: DB1 added,DB2 added:RB1 added,RBF2 added DEV NOTE: Persist across each page load from extras page to booking confirmation within the product string. Count bags regardless of if they're free or not, this is a count of total bags. If Premium\/Business where guest automatically receives 2 free bags and is not required to interact with the bags page, fire 0. Example: If 2 guests add 1 first returning bag each, this event should fire 2. When "getOffers" API call fails, the value in Data layer will be set to 0 \(as guest will not be able to add bags\). For multi-city Bags page is not presented, so Flight Bags Displayed is not fired. Number of bags added\/purchased is set to 0 for the airTravel in the rest of the flow. Include ONLY net new bags added. For example, if a booking with 1 guest already had 1 departing and 1 returning bag in RBF \(Ex. 1,0:1,0\), if the guest adds a second departing and returning bag in MT, fire \(Ex. 0,1:0,1\). If the guest added a net new 3rd bag in DCI for both departing and returning flight legs, fire 0,0:0,0 \| 1,0:1,0|Ex. 1,0:1,0\) \(Ex. 0,1:0,1\). 0,0:0,0 \| 1,0:1,0|||||||
|airTravel.flightList[n].numberOfReturningFlightFirstBagsAdded|string|Captures the number of first returning bags that were added on the bags page, persist across each page load from extras page to booking confirmation within the product string as a conversion event. DEV NOTE: Currently the product string duplicates the flight on all pages before confirmation page, please ensure the value is only recorded once before confirmation step. That means, suppress the product string to appear only once. Count bags regardless of if they're free or not, this is a count of total bags. If Premium\/Business where guest automatically receives 2 free bags and is not required to interact with the bags page, fire 0. Example: If 2 guests add 1 first returning bag each, this event should fire 2. When "getOffers" API call fails, the value in Data layer will be set to 0 \(as guest will not be able to add bags\). For multi-city Bags page is not presented, so Flight Bags Displayed is not fired. \# of departing\/returning bags added is set to 0 for the airTravel events in the rest of the flow.|2|||||||
|airTravel.flightList[n].numberOfReturningFlightSecondBagsAdded|string|Captures the number of second returning bags that were added on the bags page, persist across each page load from extras page to booking confirmation within the product string as a conversion event. DEV NOTE: Currently the product string duplicates the flight on all pages before confirmation page, please ensure the value is only recorded once before confirmation step. Suppress the value of product string to appear once. Count bags regardless of if they're free or not, this is a count of total bags If Premium\/Business where guest automatically receives 2 free bags and is not required to interact with the bags page, fire 0. Example: If 2 guests add 1 second returning bag each, this event should fire 2. When "getOffers" API call fails, the value in Data layer will be set to 0 \(as guest will not be able to add bags\). For multi-city Bags page is not presented, so Flight Bags Displayed is not fired. \# of departing\/returning bags added is set to 0 for the airTravel events in the rest of the flow.|2|||||||
|airTravel.flightList[n].tripId|string|A unique representation of the main departure and arrival points for all primary trip legs \(not including connections\). |SFO&gt;YYC:YYC&gt;SFO, SFO&gt;YYC, SFO&gt;YYC:YYC&gt;YXC:YKA&gt;SFO|^([A-Z]{3}>[A-Z]{3}:?)+$||||||
|airTravel.flightList[n].upFareBundle|string|Captures the upsell fare bundle as a comma delimited list of previous fare type and upgraded type.This is captured for each segment delimited by pipes\("\|"\).|Basic,Econo\|Basic,EconoFlex|||||||
|airTravel.numAdults|string|A count of adult travelers for a trip.|zero, 1, 2, 3, 4|^([0-9])|(zero)$||||||
|airTravel.numChildren|string|A count of child travelers for a trip.|zero, 1, 2, 3, 4|^([0-9])|(zero)$||||||
|airTravel.numInfants|string|A count of infant travelers for a trip.|zero, 1, 2, 3, 4|^([0-9])|(zero)$||||||
|booking.mtreservationId|string|Captures the existing booking PNR, when the guest entered the Payment Portal.

DEV NOT to set Data layer:
1. If the guest entered the Payment Portal with an EXISTING PNR, pass the value of the said booking PNR \(e.g. 230810\_ABCDEF\).
2. If the guest entered the Payment Portal with a NEW, pass the value as "not available".|230810\_ABCDEF|||||||
|product.tax|string|Captures the taxes and fees applicable at time of booking a flight|195.63|||||||
|promoCode.discountCode|string|Discount code entered or applied||||||||
|westJetData.bagPriceDesignatorCode|string|Captures the designator code applied to the offered price of all bags \(for guest 1\) for both departing and returning flights of a booking. Format \(for bags with one designator code\): In the case where the bag price offered is the base price \(no designator code applied\), return 'NA'. Departing Bag1 Designator Code1,Departing Bag1 Designator Code2:DesignatorCodeDepartingBag1, DesignatorCodeDepartingBag2:Returning Bag1 Designator Code,Returning Bag2 Designator Code:DesignatorCodeReturningBag1,DesignatorCodeReturningBag2 Example with 1 designator code applied to each bag: AAAAAAAAAAA,NA:11111111111,NA:BBBBBBBBBBB,NA:22222222222,NA Format \(for bags with 2 designator codes\): Departing Bag1 Designator Code1,Departing Bag1 Designator Code2:Departing Bag2 Code1, Departing Bag2 Code2:Returning Bag1 Designator Code1,Returning Bag1 Designator Code2:Returning Bag2 Code1, Returing Bag2 Code2 Example with 2 designator codes applied to each bag: AAAAAAAAAA,BBBBBBBBBB:1111111111,2222222222:CCCCCCCCCC,DDDDDDDDDD:3333333333,44444444444 DEV NOTES: Each designator code can be between 10 - 11 characters long, alphanumeric. Return "NA" when there is no designator code, for 1 or both of the designator code slots for each bagIn the case where the bag price offered is the base price \(no designator code applied\), return 'NA'. Example where only 1 designator code is applied to departing bag 1 and returning bag 1, and no designator code is applied to departing bag 2 and returning bag 2: AAAAAAAAAAA,NA:NA,NA:BBBBBBBBBBB,NA:NA,NA \*For multi-city bookings, use the first and last flight leg as departing and returning flights In the case of there being multiple designator codes applied to a bag, return the latest 2 codes. For Premium\/Business guests who automatically receive 2 free bags \(and are not required to click and add bags\), fire NA for both designator codes. When "getOffers" API call fails, the offer prices for bags are not presented to guests. In this scenario, suppress the value of this data layer object in data layer - which means this data point will NOT be triggered in Data layer. The "getOFffers" API call will determine the sequence of events to trigger in DL for Bags Event ordering. Current ordering: Page Load Started, User Detected, Seat Selection Addition Completed, Flight Bags Displayed, Page Load Completed. "Flight Bags Displayed" will await response for "getOffers" API call overall. If "getOffers" API call enocunters error, we need to trigger error tracking "Error Encountered" DL event and ensure v87\/e70 are triggered in network beacon. For One way flights, returning flight string would have - NA,NA for 1st and 2nd bag.|AAAAAAAAAAA,NA:11111111111,NA:BBBBBBBBBBB,NA:22222222222,NA|||||||
|westJetData.bagPricesOffered|string|Capture the prices of all bags shown on the Bags page, structured as: FORMAT : Departing Bag 1 Price, Departing Bag 2 Price:Returning Bag 1 Price, Returning Bag 2 Price. If bag is free, return price as 0.|when first bag is free : 0,50:0,50 when price apply to both bags - 35,50:35,50|||||||
|westJetData.buyUpRevMule|string|Captures the buy-up revenue amount \(i.e. difference between selected fare and lowest available fare, for the flight selected\).||||||||
|westJetData.depDest|string|Captures the departure & final destination points as a pair \(i.e. SJC&gt;YYC\).|SJC&gt;YYC|||||||
|westJetData.departureCode|string|Tracks the origin city searched for.|YYX, YYZ, ATL|||||||
|westJetData.departureDate|string|Date of departure for the first segment of a trip.|03\|17\|2022, 10\|28\|2024|||||||
|westJetData.destinationCode|string|Tracks the destination city searched for.|YYX, YYZ, ATL|||||||
|westJetData.digitalFlowType|string|Indicates from which digital product the guest enters Flight Search from \(RBF, MT, DCI, LiveChat, WJTP\).

Possible values for WJTP entry: depending on which of these are selected on the flight search Widget
WJTP Parent, 
WJTP Buddy Pass
WJTP Employee
WJTP Crew

Possible value on Payment Portal Pages - when guest enters from Live Chat:
LiveChat|depending on which of these are selected on the flight search Widget WJTP Parent,  WJTP Buddy Pass WJTP Employee WJTP Crew ; when guest enters from Live Chat: LiveChat|||||||
|westJetData.lowHighSelectedFareToUpsellFarePerGuestPerDirection|string|Capture the lowest and highest amount of the upsell offer per guest per direction shown on the upsell banner.The text is similar to "For only + 733.95 per person". 
Format of the value is lowest amount displayed +'\~' + highest amount displayed
Note: This amount is all-in-price including taxes \/ surcharges.|Return:  Departing Flight - "For only + 733.95 per person".   Returning Flight - "For only + 631.95 per person".  Value to be captured is 631.95\~733.95  One way:    Flight - "For only + 733.95 per person".  Value to be captured is 733.95.   Multi-city: \(it can get upto 5 flights\)  Flight1 - "For only + 300.95 per person".   Flight2 - "For only + 631.95 per person".   Flight2 - "For only + 731.95 per person".   Flight2 - "For only + 431.95 per person".  Value to be captured is 300.95\~731.95|||||||
|westJetData.originalBookingChannel|string|capture booking type \(i.e. contact centre, GDS or web bookings\).
Possible values: 
YCB - Canadian point of origin \(CAD currency\)
VHQ - Euro point of origin \(EUR currency\)
HWW - UK point of origin \(GBP currency\)
BAB - All other points of origin \(USD currency\)
TTY - gds booking

DEV NOTE: MT captures this data point baesed on sabre data from backend \(bookingServices\).|YCB - Canadian point of origin \(CAD currency\) VHQ - Euro point of origin \(EUR currency\) HWW - UK point of origin \(GBP currency\) BAB - All other points of origin \(USD currency\) TTY - gds booking|||||||
|westJetData.productBookingType|string|Capture the type of booking made through the traffic source.
Booking type \(RevenueGuest, Confirmed or standby, etc.\)

Expected Booking Type Values in WJTP & LiveChat and definition :

	• WJTP Standby
	• WJTPConfirmed

LiveChat
	• RevenueGuest \(by default anyone entering payment portal not coming from WJTP\)|• WJTP Standby 	• WJTPConfirmed|||||||
|westJetData.returnDate|string|Date of return for the last segment of a round trip or multi-city routing.|03\|15\|2022, 10\|21\|2024|||||||
|westJetData.voucherType|string|Captures the type of voucher selected on previous step|World Elite companion voucher, WestJet-wide companion voucher|||||||
|westJetEvents.departingFlightBag1PriceOffered|number|Captures the price of departing flight bag 1 that is offered to the guest \(the price the guest sees that has\/has not been modified by a designator code. DEV NOTE: When "getOffers" API call fails, the offer prices for bags are not presented to guests. In this scenario, suppress the value of this data layer object in data layer - which means this data point will NOT be triggered in Data layer.|35, 50, 100|||||||
|westJetEvents.departingFlightBag2PriceOffered|number|Captures the price of departing flight bag 2 that is offered to the guest \(the price the guest sees that has\/has not been modified by a designator code. DEV NOTE: When "getOffers" API call fails, the offer prices for bags are not presented to guests. In this scenario, suppress the value of this data layer object in data layer - which means this data point will NOT be triggered in Data layer.|35, 50, 100|||||||
|westJetEvents.scAdd|boolean|Indicates that a cart addition occurred.|TRUE, FALSE|||||||

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
<hr>
<p><strong>Instructions to set value for Flight Fare Hold Id (evar159), MT Booking PNR (evar132) on Payment Summary Step:</strong></p>
<p>Background info:</p>
<p>When guest enters the Payment Portal flow, the URL will include a unique token. This Unique url with token will determine if the guest entering the payment portal flow has an <span style="text-decoration: underline;">existing booking</span> or doing a <span style="text-decoration: underline;">new booking</span>.</p>
<ul>
<li><strong>NEW Booking Attempt</strong>
<ul>
<li>If the guest enters Payment Portal with intention to pursue a NEW booking, we set the value of&nbsp;<code>Flight Fare Hold (evar159)/flightFareHoldId (attribute)</code>&nbsp;with a new PNR in format -&nbsp;<code>YYMMDD_6DigitCode</code>.</li>
<li>We also pass value in data layer for attribute&nbsp;<code>mtReservationId</code>&nbsp;to "<code>not available</code>".</li>
</ul>
</li>
<li><strong>Existing Booking (Modification)</strong>
<ul>
<li>If the guest enters Payment Portal with an existing PNR, we set values for&nbsp;<code>MT Booking PNR (evar132)/ mtreservationId (attribute)</code>&nbsp;on this page, with the value of the PNR of the said booking.</li>
<li>We also pass value in data layer for attribute&nbsp; of&nbsp;<code>flightFareHoldId&nbsp;</code>to "<code>not available</code>".</li>
</ul>
</li>
</ul>
<p>The below table summarizes the possible value to be set in data layer based on above described summary on PAYMENT SUMMARY STEP.</p>
<table border="5" style="border-collapse: collapse; float: left;">
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
<p>&nbsp;</p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p>&nbsp;</p>
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
