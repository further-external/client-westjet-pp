# Flight Booking Confirmed

### This event is part of the page load sequence, including virtual page loads in the case of single page apps, and must be pushed between the `Page Load Started` and `Page Load Completed` events.

## Javascript Code
```js
window.digitalEventData = window.digitalEventData || [];
digitalEventData.push({
  "event": "Flight Booking Confirmed",
    "airTravel": {
        "bookingLeadTime": "<bookingLeadTime>",
        "duration": "<duration>",
        "flightFareHoldId": "<flightFareHoldId>",
        "flightList": [
            {
                "combinedTaxes": "<combinedTaxes>",
                "cost": "<cost>",
                "fareBasisCode": "<fareBasisCode>",
                "flightFareBundle": "<flightFareBundle>",
                "flightRevenue": "<flightRevenue>",
                "flightSegmentEquipment": "<flightSegmentEquipment>",
                "numberOfBagsAddedOrPurchased": "<numberOfBagsAddedOrPurchased>",
                "numberOfReturningFlightFirstBagsAdded": "<numberOfReturningFlightFirstBagsAdded>",
                "numberOfReturningFlightSecondBagsAdded": "<numberOfReturningFlightSecondBagsAdded>",
                "quantity": "<quantity>",
                "tripId": "<tripId>",
                "upFareBundle": "<upFareBundle>"
            }
        ],
        "numAdults": "<numAdults>",
        "numChildren": "<numChildren>",
        "numInfants": "<numInfants>",
        "numSeatedGuests": <numSeatedGuests>
    },
    "booking": {
        "mtreservationId": "<mtreservationId>",
        "reservationId": "<reservationId>"
    },
    "product": {
        "tax": "<tax>"
    },
    "promoCode": {
        "discountCode": "<discountCode>"
    },
    "westJetData": {
        "ancillaryPaymentType": "<ancillaryPaymentType>",
        "atcPrice": "<atcPrice>",
        "bagPriceDesignatorCode": "<bagPriceDesignatorCode>",
        "bagPricesOffered": "<bagPricesOffered>",
        "bookingType": "<bookingType>",
        "buyUpRevMule": "<buyUpRevMule>",
        "carCompany": "<carCompany>",
        "connectionNonStop": "<connectionNonStop>",
        "depDest": "<depDest>",
        "departureCode": "<departureCode>",
        "departureDate": "<departureDate>",
        "destinationCode": "<destinationCode>",
        "digitalFlowType": "<digitalFlowType>",
        "exchangeFOP": "<exchangeFOP>",
        "exchangeFeeAmountPresented": "<exchangeFeeAmountPresented>",
        "fareClassUpsell": "<fareClassUpsell>",
        "flightFareBundleChange": "<flightFareBundleChange>",
        "lowHighSelectedFareToUpsellFarePerGuestPerDirection": "<lowHighSelectedFareToUpsellFarePerGuestPerDirection>",
        "numTravelers": "<numTravelers>",
        "originalBookingChannel": "<originalBookingChannel>",
        "paymentType": "<paymentType>",
        "productBookingType": "<productBookingType>",
        "returnDate": "<returnDate>",
        "scheduleChangeType": "<scheduleChangeType>",
        "seatVoucherType": "<seatVoucherType>",
        "ssrCode": "<ssrCode>",
        "totalPrice": "<totalPrice>",
        "travelInsurance": "<travelInsurance>",
        "typeOfExchange": "<typeOfExchange>",
        "upFareBundlePreUpsell": "<upFareBundlePreUpsell>",
        "voucherType": "<voucherType>",
        "wsdPartner": "<wsdPartner>",
        "wsdPercentage": "<wsdPercentage>",
        "wspCoverage": "<wspCoverage>"
    },
    "westJetEvents": {
        "addOnRevenue": "<addOnRevenue>",
        "addOnRevenueBags": "<addOnRevenueBags>",
        "addOnRevenueCars": "<addOnRevenueCars>",
        "addOnRevenueInsurance": "<addOnRevenueInsurance>",
        "addOnRevenueSeats": "<addOnRevenueSeats>",
        "animalInHold": <animalInHold>,
        "animalInHoldRevenue": "<animalInHoldRevenue>",
        "anonBooking": <anonBooking>,
        "apprSeats": <apprSeats>,
        "bagFree": <bagFree>,
        "bagPaid": <bagPaid>,
        "bagTotal": <bagTotal>,
        "bookingApp": <bookingApp>,
        "bookingReg": <bookingReg>,
        "buyUpFlightRevenue": "<buyUpFlightRevenue>",
        "carBooking": <carBooking>,
        "carDays": <carDays>,
        "cciaSuccess": <cciaSuccess>,
        "cmpBooking": <cmpBooking>,
        "cmpBookingNonOwner": <cmpBookingNonOwner>,
        "cmpBookingOwner": <cmpBookingOwner>,
        "departingFlightBag1PriceOffered": <departingFlightBag1PriceOffered>,
        "departingFlightBag2PriceOffered": <departingFlightBag2PriceOffered>,
        "dreamlinerBooking": <dreamlinerBooking>,
        "exchangeBagsRevenue": "<exchangeBagsRevenue>",
        "exchangeFeeAmount": <exchangeFeeAmount>,
        "exchangeRevenueAmount": "<exchangeRevenueAmount>",
        "exchangeStartBags": <exchangeStartBags>,
        "giftCardBkgWJ": <giftCardBkgWJ>,
        "giftCardRedeemRevenue": "<giftCardRedeemRevenue>",
        "guestNameChangesRevenue": "<guestNameChangesRevenue>",
        "hfHoldRevenue": <hfHoldRevenue>,
        "insuranceBooking": <insuranceBooking>,
        "insurancePolicies": <insurancePolicies>,
        "multicityBooking": <multicityBooking>,
        "numberOfAvailableCrewMember": <numberOfAvailableCrewMember>,
        "numberOfBuddyPassStandby": <numberOfBuddyPassStandby>,
        "numberOfCompanionConfirmed": <numberOfCompanionConfirmed>,
        "numberOfCompanionStandby": <numberOfCompanionStandby>,
        "numberOfDependentsConfirmed": <numberOfDependentsConfirmed>,
        "numberOfDependentsStandby": <numberOfDependentsStandby>,
        "numberOfEmployeeConfirmed": <numberOfEmployeeConfirmed>,
        "numberOfEmployeeStandby": <numberOfEmployeeStandby>,
        "numberOfGuestNameChangesMade": <numberOfGuestNameChangesMade>,
        "numberOfParentsStandby": <numberOfParentsStandby>,
        "oneWayBooking": <oneWayBooking>,
        "petInCabin": <petInCabin>,
        "petInCabinRevenue": "<petInCabinRevenue>",
        "profileBooking": <profileBooking>,
        "profileInfoModPymt": <profileInfoModPymt>,
        "promoCodeBooking": <promoCodeBooking>,
        "rbfCompSeatsAdded": <rbfCompSeatsAdded>,
        "rbfSeatsBkgComp": <rbfSeatsBkgComp>,
        "rbfSeatsBkgVoucher": <rbfSeatsBkgVoucher>,
        "rbfSeatsBkgVoucherComp": <rbfSeatsBkgVoucherComp>,
        "rbfVoucherSeatsAdded": <rbfVoucherSeatsAdded>,
        "roundtripBooking": <roundtripBooking>,
        "seatBasic": <seatBasic>,
        "seatBasicRevenue": "<seatBasicRevenue>",
        "seatBusiness": <seatBusiness>,
        "seatExit": <seatExit>,
        "seatExitRevenue": "<seatExitRevenue>",
        "seatFront": <seatFront>,
        "seatFrontRevenue": "<seatFrontRevenue>",
        "seatPreferred": <seatPreferred>,
        "seatPreferredRevenue": "<seatPreferredRevenue>",
        "seatPremium": <seatPremium>,
        "seatStandard": <seatStandard>,
        "seatStandardRevenue": "<seatStandardRevenue>",
        "seatsPurchased": <seatsPurchased>,
        "seatsTotalFree": "<seatsTotalFree>",
        "seatsTotalPaid": "<seatsTotalPaid>",
        "segments": <segments>,
        "unaccompaniedMinorAdded": <unaccompaniedMinorAdded>,
        "unaccompaniedMinorAddedRevenue": "<unaccompaniedMinorAddedRevenue>",
        "visacheckoutSuccess": <visacheckoutSuccess>,
        "wsdBooking": <wsdBooking>,
        "wsdFlightRevenue": "<wsdFlightRevenue>",
        "wsdTbCcBannerAmount": <wsdTbCcBannerAmount>,
        "wspSavingsAmount": <wspSavingsAmount>
    },
    "westjetData": {
        "typeOfExchange$": "<typeOfExchange$>"
    },
    "westjetEvents": {
        "exchangeConfirmationBags": <exchangeConfirmationBags>
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
|airTravel.flightList[n].combinedTaxes|string|All taxes applied|246.31|||||||
|airTravel.flightList[n].cost|string|The cost of the trip|140.00|||||||
|airTravel.flightList[n].fareBasisCode|string|Captures the Fare Basis Code for a given flight,  Alphanumeric code with 8 characters \(ie: LAVD0LBG\).|LAVD0LBG for One Way Trip, LAVD0LBG\~AAVD0LBH\~YAVD9LBU for Multi-City , LAVD0LBG\~AAVD0LBH for Round Trip|||||||
|airTravel.flightList[n].flightFareBundle|string|Flight Fare Bundle describes the fare bundle chosen by the user. e.g. Basic, Econo, EconoRewards|Basic, Econo, EconoRewards, EconoFlex, Premium|||||||
|airTravel.flightList[n].flightRevenue|string|Captures the flight revenue \(as metric\) which is ATC \(Air Transportation Charges\) at the time of the flight booking - includes Base Fares and other ATC.
DEV NOTE:
Set the value of the flight revenue for the first array position - index 0 in airTravel.flightList, fetching ATC value of the flight. If there are more than one flights involved in booking set value of flight revenue to 0.|2050.00, 1100|||||||
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
|airTravel.flightList[n].quantity|string|The quantity of the trip|1|||||||
|airTravel.flightList[n].tripId|string|A unique representation of the main departure and arrival points for all primary trip legs \(not including connections\). |SFO&gt;YYC:YYC&gt;SFO, SFO&gt;YYC, SFO&gt;YYC:YYC&gt;YXC:YKA&gt;SFO|^([A-Z]{3}>[A-Z]{3}:?)+$||||||
|airTravel.flightList[n].upFareBundle|string|Captures the upsell fare bundle as a comma delimited list of previous fare type and upgraded type.This is captured for each segment delimited by pipes\("\|"\).|Basic,Econo\|Basic,EconoFlex|||||||
|airTravel.numAdults|string|A count of adult travelers for a trip.|zero, 1, 2, 3, 4|^([0-9])|(zero)$||||||
|airTravel.numChildren|string|A count of child travelers for a trip.|zero, 1, 2, 3, 4|^([0-9])|(zero)$||||||
|airTravel.numInfants|string|A count of infant travelers for a trip.|zero, 1, 2, 3, 4|^([0-9])|(zero)$||||||
|airTravel.numSeatedGuests|integer|Number of required seats for all travelers on a trip.  Typically adults + children.|1, 2, 3, 4, 5||||1|||
|booking.mtreservationId|string|Captures the existing booking PNR, when the guest entered the Payment Portal.

DEV NOT to set Data layer:
1. If the guest entered the Payment Portal with an EXISTING PNR, pass the value of the said booking PNR \(e.g. 230810\_ABCDEF\).
2. If the guest entered the Payment Portal with a NEW, pass the value as "not available".|230810\_ABCDEF|||||||
|booking.reservationId|string|A unique identifier of a booking used for communication between guests. Captures the 6 digit PNR code with date stamp.
Format: YYMMDD\_6\_digit\_PNR\_Code|230810\_ABCDEF|||||||
|product.tax|string|Captures the taxes and fees applicable at time of booking a flight|195.63|||||||
|promoCode.discountCode|string|Discount code entered or applied||||||||
|westJetData.ancillaryPaymentType|string|Captures the type of payment used for the ancillary products.||||||||
|westJetData.atcPrice|string|Captures Air Transportation Charges at the time of the flight summary step. Includes Base Fares and other ATC.|2050.00, 1100|||||||
|westJetData.bagPriceDesignatorCode|string|Captures the designator code applied to the offered price of all bags \(for guest 1\) for both departing and returning flights of a booking. Format \(for bags with one designator code\): In the case where the bag price offered is the base price \(no designator code applied\), return 'NA'. Departing Bag1 Designator Code1,Departing Bag1 Designator Code2:DesignatorCodeDepartingBag1, DesignatorCodeDepartingBag2:Returning Bag1 Designator Code,Returning Bag2 Designator Code:DesignatorCodeReturningBag1,DesignatorCodeReturningBag2 Example with 1 designator code applied to each bag: AAAAAAAAAAA,NA:11111111111,NA:BBBBBBBBBBB,NA:22222222222,NA Format \(for bags with 2 designator codes\): Departing Bag1 Designator Code1,Departing Bag1 Designator Code2:Departing Bag2 Code1, Departing Bag2 Code2:Returning Bag1 Designator Code1,Returning Bag1 Designator Code2:Returning Bag2 Code1, Returing Bag2 Code2 Example with 2 designator codes applied to each bag: AAAAAAAAAA,BBBBBBBBBB:1111111111,2222222222:CCCCCCCCCC,DDDDDDDDDD:3333333333,44444444444 DEV NOTES: Each designator code can be between 10 - 11 characters long, alphanumeric. Return "NA" when there is no designator code, for 1 or both of the designator code slots for each bagIn the case where the bag price offered is the base price \(no designator code applied\), return 'NA'. Example where only 1 designator code is applied to departing bag 1 and returning bag 1, and no designator code is applied to departing bag 2 and returning bag 2: AAAAAAAAAAA,NA:NA,NA:BBBBBBBBBBB,NA:NA,NA \*For multi-city bookings, use the first and last flight leg as departing and returning flights In the case of there being multiple designator codes applied to a bag, return the latest 2 codes. For Premium\/Business guests who automatically receive 2 free bags \(and are not required to click and add bags\), fire NA for both designator codes. When "getOffers" API call fails, the offer prices for bags are not presented to guests. In this scenario, suppress the value of this data layer object in data layer - which means this data point will NOT be triggered in Data layer. The "getOFffers" API call will determine the sequence of events to trigger in DL for Bags Event ordering. Current ordering: Page Load Started, User Detected, Seat Selection Addition Completed, Flight Bags Displayed, Page Load Completed. "Flight Bags Displayed" will await response for "getOffers" API call overall. If "getOffers" API call enocunters error, we need to trigger error tracking "Error Encountered" DL event and ensure v87\/e70 are triggered in network beacon. For One way flights, returning flight string would have - NA,NA for 1st and 2nd bag.|AAAAAAAAAAA,NA:11111111111,NA:BBBBBBBBBBB,NA:22222222222,NA|||||||
|westJetData.bagPricesOffered|string|Capture the prices of all bags shown on the Bags page, structured as: FORMAT : Departing Bag 1 Price, Departing Bag 2 Price:Returning Bag 1 Price, Returning Bag 2 Price. If bag is free, return price as 0.|when first bag is free : 0,50:0,50 when price apply to both bags - 35,50:35,50|||||||
|westJetData.bookingType|string|Captures all types of booking scenarios. \(E.g., "flight+Insurance+seats+cars"\). Possible values include any combinations of the following: flights \/ seats \/ car \/ insurance"

The following scenarios outline the value to be captured:

Flight only purchase -&gt;  flight
Flight and seats purchased-&gt; flight+seats
Flight, seats and car rental purchased -&gt;	flight+seats+cars
Flight, travel insurance and seats purchased -&gt;	flight+insurance+seats
Flight and car rental purchased -&gt; flight+cars
Flight and travel insurance purchased -&gt;	flight+insurance
Flight, travel insurance, seats and car rental purchased -&gt;	flight+insurance+seats+cars
Flight, travel insurance and car rental purchased -&gt;	flight+insurance+cars|flight+Insurance+seats+cars, flight+cars, flight+seats|||||||
|westJetData.buyUpRevMule|string|Captures the buy-up revenue amount \(i.e. difference between selected fare and lowest available fare, for the flight selected\).||||||||
|westJetData.carCompany|string|Captures the car supplier\/company, when the booking includes a car, in the form of: supplier:company \(e.g. supplier:national\). |supplier:national, supplier:hertz, supplier:budget|||||||
|westJetData.connectionNonStop|string|Captures if a trip was connecting, non-stop, or direct.|connecting, non-stop, through|||||||
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
|westJetData.exchangeFOP|string|Captures the form of payment being returned to \(or multiple forms of payment involved\) .|travel\_bank, visa, mastercard, american\_express, discover|||||||
|westJetData.exchangeFeeAmountPresented|string|The amount of exchange fee presented. Used to capture the fees amount applicable to the scenario in the source currency \(i.e. "$50 CAD" or "$50 USD", etc.\)|"$50 CAD" or "$50 USD", etc.|||||||
|westJetData.fareClassUpsell|string|List of fare upsells|E-to-X,E-to-B|||||||
|westJetData.flightFareBundleChange|string|Capture the changed booked Fare Bundle after the flight interruption flow change completed.

Possible Values:

One way: YYC-YVR \(Econo\).    Value = Econo 
Round Trip: YVR-YYC-YEG \(Econo\): YEG-YYC-YVR  \(EconoFlex\).  
Value = Econo\|EconoFlex 
Round Trip: YVR-YYC-YEG \(EconoRewards\): YEG-YYC-YVR  \(EconoFlex\).  
Value = EconoRewards\|EconoFlex 
Multi-cities: YVR-YYC \(EconoFlex\), YYC-YEG-YWG \(Premium\), YYZ-YVR \(BusinessFlex\). 
Value = EconoFlex\|Premium\|BusinessFlex|One way: YYC-YVR \(Econo\).    Value = Econo    Round Trip: YVR-YYC-YEG \(Econo\): YEG-YYC-YVR  \(EconoFlex\).   Value = Econo\|EconoFlex    Round Trip: YVR-YYC-YEG \(EconoRewards\): YEG-YYC-YVR  \(EconoFlex\).  Value = EconoRewards\|EconoFlex    Multi-cities: YVR-YYC \(EconoFlex\), YYC-YEG-YWG \(Premium\), YYZ-YVR \(BusinessFlex\).   Value = EconoFlex\|Premium\|BusinessFlex|||||||
|westJetData.lowHighSelectedFareToUpsellFarePerGuestPerDirection|string|Capture the lowest and highest amount of the upsell offer per guest per direction shown on the upsell banner.The text is similar to "For only + 733.95 per person". 
Format of the value is lowest amount displayed +'\~' + highest amount displayed
Note: This amount is all-in-price including taxes \/ surcharges.|Return:  Departing Flight - "For only + 733.95 per person".   Returning Flight - "For only + 631.95 per person".  Value to be captured is 631.95\~733.95  One way:    Flight - "For only + 733.95 per person".  Value to be captured is 733.95.   Multi-city: \(it can get upto 5 flights\)  Flight1 - "For only + 300.95 per person".   Flight2 - "For only + 631.95 per person".   Flight2 - "For only + 731.95 per person".   Flight2 - "For only + 431.95 per person".  Value to be captured is 300.95\~731.95|||||||
|westJetData.numTravelers|string|Captures the number of adult, children and infants and total seats associated to flight booking. Format to capture : \#adults\|\#children\|\#infants\|\#seats|1\|1\|0\|2|||||||
|westJetData.originalBookingChannel|string|capture booking type \(i.e. contact centre, GDS or web bookings\).
Possible values: 
YCB - Canadian point of origin \(CAD currency\)
VHQ - Euro point of origin \(EUR currency\)
HWW - UK point of origin \(GBP currency\)
BAB - All other points of origin \(USD currency\)
TTY - gds booking

DEV NOTE: MT captures this data point baesed on sabre data from backend \(bookingServices\).|YCB - Canadian point of origin \(CAD currency\) VHQ - Euro point of origin \(EUR currency\) HWW - UK point of origin \(GBP currency\) BAB - All other points of origin \(USD currency\) TTY - gds booking|||||||
|westJetData.paymentType|string|Captures the type of payment used for the main flight products.|Visa, MasterCard, TB, Visa\|TB|||||||
|westJetData.productBookingType|string|Capture the type of booking made through the traffic source.
Booking type \(RevenueGuest, Confirmed or standby, etc.\)

Expected Booking Type Values in WJTP & LiveChat and definition :

	• WJTP Standby
	• WJTPConfirmed

LiveChat
	• RevenueGuest \(by default anyone entering payment portal not coming from WJTP\)|• WJTP Standby 	• WJTPConfirmed|||||||
|westJetData.returnDate|string|Date of return for the last segment of a round trip or multi-city routing.|03\|15\|2022, 10\|21\|2024|||||||
|westJetData.scheduleChangeType|string|Identify the schedule change Type \(v205\) in MT.  
IROP is irregular operation happens within 72 hours of departure that require flights change or due to airport operation matter.  
Major schedule change is a big schedule change happed around twice a year that impact booked guests further out to their travel dates. 
 
Possible values: 
•	IROP - when schedule change due to IROP situation. 
•	Major Schedule Change - when the PNR applied the major schedule change situation. 
•	None - Set by default when it is not IROP nor major schedule change. This can contain minor schedule change PNRs|Major schedule change, IROP, None|||||||
|westJetData.seatVoucherType|string|Captures the number and types of seat vouchers redeemed, on the confirmation step in RBF.

Possible values:
'Any' for number of Pre-Reserved Transferrable\/Non-Transferrable any seat vouchers used
'Standard' for number of Standard seat only vouchers used
'Complimentary' for number of seats redeemed via Platinum unlimited benefit

Format:  \(spaces not allowed\)
Any: \#redeemed\|Standard:\#redeemed\|Complimentary:\# redeemed

DEV NOTE: Page Name where this tracking is required to be set: mobile:booking:confirmation. \*Do not include parameters when they equal 0 \(ex. if no standard voucher is used, it should not be included in the value\). Include only seat voucher type redeemed, do not set value for the vouchers which are not redeemed.|Format:  \(spaces not allowed\) Any: \#redeemed\|Standard:\#redeemed\|Complimentary:\# redeemed  E.g. - If 1 of Any seat voucher, 1 Standard seat voucher and 1 Complimentary seat is redeemed, then fire as: Any: 1 \| Standard: 1 \| Complimentary: 1|||||||
|westJetData.ssrCode|string|Special Service Requests Code\(s\).|wchs, deaf, wchs\|wchs, blnd|||||||
|westJetData.totalPrice|string|Captures total price as displayed on the flight summary step. Includes all ATC charges BUT also all taxes, fees, and charges.|3156.82, 2361.92|||||||
|westJetData.travelInsurance|string|Indicates when travel insurance is selected.|No Insurance Selected, Cancellation & Interruption, Travel Within Canada Package, Deluxe Package, Classical Medical|||||||
|westJetData.typeOfExchange|string|Identifies the type of exchange made in a colon delimited format. Full exchange or partial exchange, to indicate if all flight segments of the trip are being exchanged or only some of the flight segments on the trip are exchanged.

Sample values \(any\/all combinations of the three values are to be captured\):
Full Exchange:Dates
Partial Exchange:Dates:Flights Full Exchange:Flights:O\/Ds|full exchange:dates . NOTE - Sample values \(any\/all combinations of the three values are to be captured\):|||||||
|westJetData.upFareBundlePreUpsell|string|"Captures the upsell fare bundle as a comma delimited list of previous selected by guest fare type and upgraded type. This is captured for each segment delimited by pipes\(\~\).

Example:
One way: YYC-YVR selected Econo before accept upsell to Premium.       
  Value = Econo 
Round Trip: 
  \[Departing\] YVR-YYC-YEG selected EconoFlex before accept upsell to Premium; 
  \[Returning\] YEG-YYC-YVR selected Econo before accept upsell to Premium.       
  Value = EconoFlex\~Econo
Multi-cities: 
  \[Flight1\] YVR-YYC selected Basic before accept upsell to Premium; 
  \[Flight2\] YYC-YEG-YWG selected EconoFlex before accept upsell to Premium;
  \[Flight3\] YYZ-YVR selected Econo before accept upsell to Premium;    
   Value = Basic\~EconoFlex\~Econo"|Example: One way: YYC-YVR selected Econo before accept upsell to Premium.          Value = Econo  Round Trip:    \[Departing\] YVR-YYC-YEG selected EconoFlex before accept upsell to Premium;    \[Returning\] YEG-YYC-YVR selected Econo before accept upsell to Premium.          Value = EconoFlex\~Econo Multi-cities:    \[Flight1\] YVR-YYC selected Basic before accept upsell to Premium;    \[Flight2\] YYC-YEG-YWG selected EconoFlex before accept upsell to Premium;   \[Flight3\] YYZ-YVR selected Econo before accept upsell to Premium;        Value = Basic\~EconoFlex\~Econo|||||||
|westJetData.voucherType|string|Captures the type of voucher selected on previous step|World Elite companion voucher, WestJet-wide companion voucher|||||||
|westJetData.wsdPartner|string|Captures what combination of WestJet and Partner airline flights were selected. Possible values: "WJ only", "Partner Only", or, "WJ and Partner"".|WJ only, Partner Only, WJ and Partner|||||||
|westJetData.wsdPercentage|string|Captures the percentage of available WSD the guest used towards their booking \( as a % value \).||||||||
|westJetData.wspCoverage|string|Capture how much of the tax the guest chooses to cover their points balance.
Possible values:
- 100: If guest toggles 100% and completes their booking
- 50: If guest toggles 50% and completes their booking
- Not Selected: Guest was offered to cover 50% and\/or 100% as they had sufficient WSP balance at time of purchase but chose not to select either toggle during purchase
- Not Eligible: Guest either did not have sufficient WSP balance to cover 50%\/100% and therefore was not offered option to cover taxes
OR guest was not signed in at time of purchase.|not eligible, not selected, 50, 100|||||||
|westJetEvents.addOnRevenue|string|Captures revenue from non-flight product purchases.|143, 90, 200, 1000|||||||
|westJetEvents.addOnRevenueBags|string|Used to capture the amount of revenue from the pre-paid baggage ancillary.|143, 90, 200, 1000|||||||
|westJetEvents.addOnRevenueCars|string|Used to capture the amount of revenue from the car rental ancillary.|143, 90, 200, 1000|||||||
|westJetEvents.addOnRevenueInsurance|string|Used to capture the amount of revenue from the insurance ancillary.|143, 90, 200, 1000|||||||
|westJetEvents.addOnRevenueSeats|string|Used to capture the amount of revenue from the pre-reserved seating \(PRS\) ancillary.|143, 90, 200, 1000|||||||
|westJetEvents.animalInHold|integer|Used to capture the total amount of Animal in Hold \(AVIH\) booked.||||||||
|westJetEvents.animalInHoldRevenue|string|Used to register revenue from a pet in cabin selected in the booking.||||||||
|westJetEvents.anonBooking|boolean|Captures if the completed flight booking was made without a profile.|TRUE, FALSE|||||||
|westJetEvents.apprSeats|integer|Used to capture the number of seats that qualify for APPR-mandated family seating.  |1, 2, 3|||||||
|westJetEvents.bagFree|integer|Used to indicate when a free bag is selected in the booking.|1, 2, 3|||||||
|westJetEvents.bagPaid|integer|Used to indicate when a paid bag is selected in the booking.|1, 2, 3|||||||
|westJetEvents.bagTotal|integer|Used to indicate the total amount of bags selected in the booking.|1, 2, 3|||||||
|westJetEvents.bookingApp|boolean|Captures if the completed flight booking was made via apps.|TRUE, FALSE|||||||
|westJetEvents.bookingReg|boolean|Captures if the completed flight booking was not made via apps.|TRUE, FALSE|||||||
|westJetEvents.buyUpFlightRevenue|string|Captures the flight revenue associated with bookings that included  a "buy-up".|143, 90, 200, 1000|||||||
|westJetEvents.carBooking|boolean|Indicates a car rental was purchased \(in-path\) along with the flight booking|TRUE, FALSE|||||||
|westJetEvents.carDays|integer|Indicates the \# of days the car has been rented for.|1, 2, 3|||||||
|westJetEvents.cciaSuccess|boolean|Captures a successful Mastercard Instant Adjudication when a booking is completed.|TRUE, FALSE|||||||
|westJetEvents.cmpBooking|boolean|Used to indicate Companion Voucher was used to make the booking|TRUE, FALSE|||||||
|westJetEvents.cmpBookingNonOwner|boolean|Used to indicate the booking contained a companion voucher redemption with the owner not travelling|TRUE, FALSE|||||||
|westJetEvents.cmpBookingOwner|boolean|Used to indicate the booking contained a companion voucher redemption with the owner travelling.|TRUE, FALSE|||||||
|westJetEvents.departingFlightBag1PriceOffered|number|Captures the price of departing flight bag 1 that is offered to the guest \(the price the guest sees that has\/has not been modified by a designator code. DEV NOTE: When "getOffers" API call fails, the offer prices for bags are not presented to guests. In this scenario, suppress the value of this data layer object in data layer - which means this data point will NOT be triggered in Data layer.|35, 50, 100|||||||
|westJetEvents.departingFlightBag2PriceOffered|number|Captures the price of departing flight bag 2 that is offered to the guest \(the price the guest sees that has\/has not been modified by a designator code. DEV NOTE: When "getOffers" API call fails, the offer prices for bags are not presented to guests. In this scenario, suppress the value of this data layer object in data layer - which means this data point will NOT be triggered in Data layer.|35, 50, 100|||||||
|westJetEvents.dreamlinerBooking|boolean|Indicates that at least one flight on the booking is a Dreamliner segment.|TRUE, FALSE|||||||
|westJetEvents.exchangeBagsRevenue|string|Captures the revenue from bags purchased on the exchanged booking.||||||||
|westJetEvents.exchangeFeeAmount|number|Captures the Change fee on exchange booking.||||||||
|westJetEvents.exchangeRevenueAmount|string|Captures the exchange revenue added between original trip amount to the changed trip amount on the exchanged booking.||||||||
|westJetEvents.exchangeStartBags|integer|Captures the number of bags on the original booking being exchanged .||||||||
|westJetEvents.giftCardBkgWJ|boolean|Used to indicate if the gift card funds were used towards the booking.|TRUE, FALSE|||||||
|westJetEvents.giftCardRedeemRevenue|string|Used to capture the amount of Gift Card funds used towards the booking|143, 90, 200, 1000|||||||
|westJetEvents.guestNameChangesRevenue|string|Used to capture the amount of revenue from Guest Name Change transactions via Live Chat \/ Payment Portal||||||||
|westJetEvents.hfHoldRevenue|boolean|Used to indicate that the previously held flights are now fully confirmed\/booked.|TRUE, FALSE|||||||
|westJetEvents.insuranceBooking|boolean|Indicates travel insurance wa purchased \(in-path\) along with the flight booking|TRUE, FALSE|||||||
|westJetEvents.insurancePolicies|integer|Captures the number of travel Insurance policies purchased, for bookings with travel insurance.|1, 2, 3|||||||
|westJetEvents.multicityBooking|boolean|Only set if the reservation is a mutli-city trip|TRUE, FALSE|||||||
|westJetEvents.numberOfAvailableCrewMember|number|The purpose of this requirement is to know number of Available Crew Member on a PNR in WJTP booking on Payment Confirmation step.DEV NOTE - DO NOT trigger this event if Product Booking Type is RevenueGuest.
If Available Crew Member is NOT in the booking, pass value 0.|2,1,0|||||||
|westJetEvents.numberOfBuddyPassStandby|number|Captures number of guests on the booking is a buddy pass guest flying standby for WJTP. DEV NOTE - DO NOT trigger this event if Product Booking Type is RevenueGuest. If buddy pass standby is NOT in the booking, pass value 0.|2,1,0|||||||
|westJetEvents.numberOfCompanionConfirmed|number|Captures the total number of companion confirmed on a WJTP booking entering payment portal.
DEV NOTE - DO NOT trigger this event if Product Booking Type is RevenueGuest.
If confirmed companion is NOT in the booking, pass value 0.|2,1,0|||||||
|westJetEvents.numberOfCompanionStandby|number|Captures number of guests on the booking is an companion flying standby for WJTP.

DEV NOTE - DO NOT trigger this event if Product Booking Type is RevenueGuest.
If companion standby is NOT in the booking, pass value 0.|2,1,0|||||||
|westJetEvents.numberOfDependentsConfirmed|number|Captures the total number of dependents confirmed on a WJTP booking entering payment portal.
DEV NOTE - DO NOT trigger this event if Product Booking Type is RevenueGuest.
If dependent confirmed is NOT in the booking, pass value 0.|0,1,2|||||||
|westJetEvents.numberOfDependentsStandby|number|Captures number of guests on the booking is a dependent flying standby for WJTP. DEV NOTE - DO NOT trigger this event if Product Booking Type is RevenueGuest. If dependent standby is NOT in the booking, pass value 0.|2,1,0|||||||
|westJetEvents.numberOfEmployeeConfirmed|number|Captures the total number of employee confirmed on a WJTP booking entering payment portal.
DEV NOTE - DO NOT trigger this event if Product Booking Type is RevenueGuest.
If employee confirmed is NOT in the booking, pass value 0.|2, 1 ,0 etc.|||||||
|westJetEvents.numberOfEmployeeStandby|number|Captures number of guests on the booking is an employee flying standby for WJTP.

DEV NOTE - DO NOT trigger this event if Product Booking Type is RevenueGuest.
If employee standby is NOT in the booking, pass value 0.|2,1,0|||||||
|westJetEvents.numberOfGuestNameChangesMade|integer|Used to capture the number of guest name changes made via Live Chat and paid in Payment Portal||||||||
|westJetEvents.numberOfParentsStandby|number|Captures number of guests on the booking is a parent flying standby for WJTP. DEV NOTE - DO NOT trigger this event if Product Booking Type is RevenueGuest. If parents standby is NOT in the booking, pass value 0.|2,1,0|||||||
|westJetEvents.oneWayBooking|boolean|Only set if the reservation is a one-way trip|TRUE, FALSE|||||||
|westJetEvents.petInCabin|integer|Used to capture the total amount of Pets in Cabin \(PETC\) booked.||||||||
|westJetEvents.petInCabinRevenue|string|Used to register revenue from a pet in cabin selected in the booking.||||||||
|westJetEvents.profileBooking|boolean|Captures if the completed flight booking was made with a profile.|TRUE, FALSE|||||||
|westJetEvents.profileInfoModPymt|boolean|Used to indicate that the guest was prompted to save new information they added on the previous Payment step \(regardless of whether or not they saved info they added\)|TRUE, FALSE|||||||
|westJetEvents.promoCodeBooking|boolean|Captures if the promo code was successfully applied to the booking.|TRUE, FALSE|||||||
|westJetEvents.rbfCompSeatsAdded|integer|The number of complimentary seats purchased.|1, 2, 3, 4, 5|||||||
|westJetEvents.rbfSeatsBkgComp|boolean|Indicates only complimentary seats were included in the booking. 
DEV NOTE: Update to ensure this event only fires when all seats are purchased using the Platinum rewards member complimentary seat benefit. \(This is requirement post Sunrise\).|TRUE, FALSE|||||||
|westJetEvents.rbfSeatsBkgVoucher|boolean|Indicates only PRS voucher seats were included in the booking. 
DEV NOTE: Update to ensure this event only fires when all seats are purchased using only Any seat or Standard seat vouchers. \(this is requirement post Sunrise\).|TRUE, FALSE|||||||
|westJetEvents.rbfSeatsBkgVoucherComp|boolean|Indicates complimentary Seats and PRS seats purchased. 
DEV NOTE: Update to ensure this only fires when all seats are purchased using only seat vouchers or platinum rewards member complimentary seat benefit.|TRUE, FALSE|||||||
|westJetEvents.rbfVoucherSeatsAdded|integer|Capture the  total \# of all vouchers used \(Non-transferrable any seat voucher, transferrable any seat voucher, Standard seat voucher, platinum seat benefit\).
Example: If 1 transferrable seat voucher and 2 standard seat vouchers are redeemed, set in data layer as 3.|Example: If 1 transferrable seat voucher and 2 standard seat vouchers are redeemed, set in data layer as 3.|||||||
|westJetEvents.roundtripBooking|boolean|Only set if the reservation is a round-trip|TRUE, FALSE|||||||
|westJetEvents.seatBasic|integer|Used to indicate when a basic seat is selected in the booking.|1, 2, 3|||||||
|westJetEvents.seatBasicRevenue|string|Used to register revenue from a basic seat selected in the booking. |143, 90, 200, 1000|||||||
|westJetEvents.seatBusiness|integer|Used to indicate when a business seat is selected in the booking.|1, 2, 3|||||||
|westJetEvents.seatExit|integer|Used to indicate when an exit seat is selected in the booking.|1, 2, 3|||||||
|westJetEvents.seatExitRevenue|string|Used to register revenue from an exit seat selected in the booking.|143, 90, 200, 1000|||||||
|westJetEvents.seatFront|integer|Used to indicate when a front of cabin seat is selected in the booking.|1, 2, 3|||||||
|westJetEvents.seatFrontRevenue|string|Used to register revenue from a front of cabin seat selected in the booking.|143, 90, 200, 1000|||||||
|westJetEvents.seatPreferred|integer|Used to indicate when a preferred seat is selected in the booking.|1, 2, 3|||||||
|westJetEvents.seatPreferredRevenue|string|Used to register revenue from a preferred seat selected in the booking.|143, 90, 200, 1000|||||||
|westJetEvents.seatPremium|integer|Used to indicate when a premium seat is selected in the booking.|1, 2, 3|||||||
|westJetEvents.seatStandard|integer|Used to indicate when a standard seat is selected in the booking.|1, 2, 3|||||||
|westJetEvents.seatStandardRevenue|string|Used to register revenue from a standard seat selected in the booking.|143, 90, 200, 1000|||||||
|westJetEvents.seatsPurchased|integer|Used to capture the total number of seats purchased\/added, for bookings with seats \(regardless of type of seats\).|1, 2, 3|||||||
|westJetEvents.seatsTotalFree|string|Captures the total \# of free seats within a booking.||||||||
|westJetEvents.seatsTotalPaid|string|Total number of paid seats within a booking||||||||
|westJetEvents.segments|integer|Captures the number of segments for the reservation. Each flight number and each person in a reservation constitutes one segment.|1, 2, 3|||||||
|westJetEvents.unaccompaniedMinorAdded|integer|Used to capture the number of unaccompanied minors added via Live Chat and paid in Payment Portal.||||||||
|westJetEvents.unaccompaniedMinorAddedRevenue|string|Used to capture the amount of revenue from unaccompanied minor fee transactions via Live Chat \/ Payment Portal.|1,  2 etc.|||||||
|westJetEvents.visacheckoutSuccess|boolean|Captures successful log-ins \(and consequently, bookings\) from users using Visa Checkout \(digital wallet\) as their chosen type of payment.|TRUE, FALSE|||||||
|westJetEvents.wsdBooking|boolean|Used to indicate WestJet Dollars were used toward the flight portion of the booking.|TRUE, FALSE|||||||
|westJetEvents.wsdFlightRevenue|string|Used to capture the amount of WestJet dollars used for the flight only portion of the booking.|143, 90, 200, 1000|||||||
|westJetEvents.wsdTbCcBannerAmount|boolean|Used to indicate if the user used the recommended amounts from WSD + TB+ CC banner contextual message that appeared on the FOP page.|TRUE, FALSE|||||||
|westJetEvents.wspSavingsAmount|number|Capture the $ value saved through redeeming WSP. to cover ATC, Seats and Bags.
DEV NOTE:  For Live Chat\/WJTP Entry: Capture the $ value saved through redeeming WSP to cover ATC, Seats and Bags|0, 1, 2, 3, 4|||||||
|westjetData.typeOfExchange$|string|Used to capture the type of exchange in terms of one of the following three types .
Possible Values -
Add Collect
Even Exchange
Refund|Add Collect, Even Exchange,  Refund|||||||
|westjetEvents.exchangeConfirmationBags|integer|Captures the number of bags on the exchanged booking.||||||||

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
