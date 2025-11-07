# Flight Booking Seats Info

### This event is part of the page load sequence, including virtual page loads in the case of single page apps, and must be pushed between the `Page Load Started` and `Page Load Completed` events.

## Javascript Code
```js
window.digitalEventData = window.digitalEventData || [];
digitalEventData.push({
  "event": "Flight Booking Seats Info",
    "seatList": [
        {
            "ancillaryDocumentNumber": "<ancillaryDocumentNumber>",
            "directionalOD": "<directionalOD>",
            "flightFareBundle": "<flightFareBundle>",
            "flightNumber": "<flightNumber>",
            "flightSegment": "<flightSegment>",
            "flightSegmentEquipment": "<flightSegmentEquipment>",
            "seatDesignatorCode": "<seatDesignatorCode>",
            "seatNumberOnAircraftSeatMap": "<seatNumberOnAircraftSeatMap>",
            "seatPositionInAircraftSeatMap": "<seatPositionInAircraftSeatMap>",
            "seatPrice": <seatPrice>,
            "seatQuantity": "<seatQuantity>",
            "seatType": "<seatType>"
        }
    ]
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|seatList[n].ancillaryDocumentNumber|string|Captures the Ancillary Document Number for each individual seat purchased, from that transaction under each specific seat.||||||||
|seatList[n].directionalOD|string|Capture the the Directional OD as its own dimension. Examples: YYZ&gt;YVR YVR&gt;YYZ YYC&gt;YVR|YYZ&gt;YVR , YVR&gt;YYZ, YYC&gt;YVR|||||||
|seatList[n].flightFareBundle|string|Flight Fare Bundle describes the fare bundle chosen by the user. e.g. Basic, Econo, EconoRewards.

DEV NOTE : Update the value to not concatenate both flight legs with \~, track at the individual flight leg level. Just include one segment - whereas we have all segments today in airTravel.flightList\[n\] array.

Example :
If the guest is flying EconoFlex for their departing flight leg from YYZ&gt;YVR, on all flights involved in that flight leg, fire ECONOFLEX.|Basic, Econo, EconoRewards, EconoFlex, Premium|||||||
|seatList[n].flightNumber|string|Capture the specific flight number that pertains to the seat being shown on the seat map. Ex. WS679, WS001, etc. DEV NOTE: On Seat map page - capture for each available seat shown on the seat map. Flight Bags page to Confirmation page - capture only the seats that were selected on the seat map page..|Ex. WS679, WS001, etc.|||||||
|seatList[n].flightSegment|string|Capture the Origin and Destination of the specific flight \(not the overall OD\). For example: If the guest booked a flight from YYZ to YVR with a layover in YYC. Example: When booking seats on the flight from YYZ to YYC capture YYZ&gt;YYC When booking seats on the second flight, from YYC to YVR, capture YYC&gt;YVR|If the guest booked a flight from YYZ to YVR with a layover in YYC. Example: When booking seats on the flight from YYZ to YYC capture YYZ&gt;YYC When booking seats on the second flight, from YYC to YVR, capture YYC&gt;YVR|||||||
|seatList[n].flightSegmentEquipment|string|The equipment that flies a flight segment. \(e.g. Boeing 737 MAX 8\). Update the data capture to include RES Equip code appended at the end using : \(colon\) as a delimiter. Updated Format: Equip Code:Aircraft:RES.

DEV NOTE: Update to not concatenate both flight legs with \~, track at the individual flight leg level.|If selecting a seat on 737 MAX 8 seat map, capture only 7M8:737-MAX 8:MM2|||||||
|seatList[n].seatDesignatorCode|string|Capture the specific designator code that applies to each individual seat. In the case that there is more than 1 designator code applying to a seat, capture only the 2 latest codes, separated by a \~ delimiter. Example: If DAAEEDCDND is a designator code that applies a discount on all extended comfort seats, then all extended comfort seats should capture: DAAEEDCDND If both DAAEECDND and DXEEDCDN apply to extended comfort seats, all extended comfort seats should capture: DAAEECDND\~DXEEDCDN. DEV NOTE: On Seat map page - capture for each available seat shown on the seat map. Flight Bags page to Confirmation page - capture only the seats that were selected on the seat map page.|xample: If DAAEEDCDND is a designator code that applies a discount on all extended comfort seats, then all extended comfort seats should capture: DAAEEDCDND If both DAAEECDND and DXEEDCDN apply to extended comfort seats, all extended comfort seats should capture: DAAEECDND\~DXEEDCDN.|||||||
|seatList[n].seatNumberOnAircraftSeatMap|string|For each individual seat, capture the specific seat \# based on the row and column of that seat. 
Examples:
1A, 22B, 31C, etc.

DEV NOTE: On Seat map page - capture for each available seat shown on the seat map. 
Flight Bags page to Confirmation page - capture only the seats that were selected on the seat map page.|1A, 22B, 31C, etc.|||||||
|seatList[n].seatPositionInAircraftSeatMap|string|Capture whether or not the seat is an Aisle, Middle or Window seat. Example: Any seat between two other seats is a Middle seat - pass value for Seat Position = Middle Any seat adjacent to a window is a Window seat - pass value for Seat Position = Window Any seat adjacent to an aisle is an Aisle seat - pass value for Seat Position = Aisle DEV NOTE: On Seat map page - capture for each available seat shown on the seat map. Flight Bags page to Confirmation page - capture only the seats that were selected on the seat map page.|Any seat between two other seats is a Middle seat - pass value for Seat Position = Middle. Any seat adjacent to a window is a Window seat - pass value for Seat Position = Window. Any seat adjacent to an aisle is an Aisle seat - pass value for Seat Position = Aisle.|||||||
|seatList[n].seatPrice|number|Captures the price for each seat selected during flight booking.|51.71, 60.00|||||||
|seatList[n].seatQuantity|string|Captures the number of seats purchased, for each guest per segment. 
DEV NOTE: Always set value to 1.|1|||||||
|seatList[n].seatType|string|Capture the seat type as the seat selected during flight booking.
Examples: Extended Comfort Seat Front of Cabin Seat Standard Seat Exit Row Seat DEV NOTE: On Seat map page - capture for each available seat shown on the seat map. Flight Bags page to Confirmation page - capture only the seats that were selected on the seat map page.|Extended Comfort Seat, Front Of Cabin, Standard Seat, Exit Row Seat|||||||




