# Referrals

The referrals service is used to provide partner redirects
to Skyscanner pages based to provided request parameters.

*API endpoint*

The API is accessible at https://skyscanner.net/g/referrals/v1

There is one main endpoint with the following URL structure:

`GET /{vertical}/{pagetype}?associateid={{ associateId }}`

*TRY IT OUT*

[![Run in Postman](https://run.pstmn.io/button.svg)](https://app.getpostman.com/run-collection/31ff523d2ff9186107e1)

*REQUEST PARAMETERS*

| Parameter | Description |
| --------- | ------- |
| ```vertical``` <br><span class="required">REQUIRED</span> | The vertical you want to redirect to. Allowed values: flights, hotels, cars|
| ```pagetype``` <br><span class="required">OPTIONAL</span> | Page type supported by each vertical. E.g. for flights -> day-view, browse-view... take a look at the next table|
| ```associateid``` <br><span class="required">OPTIONAL</span> | Associate partner id to attribute traffic to|
| ```utm_term``` <br><span class="required">OPTIONAL</span> | Used to send through a unique variable that you can track back to your campaigns.|

*PAGE TYPES*

| Vertical | Pagetypes |
| --------- | ------- |
| flights | home, day-view, calendar-month-view, browse-view, multicity, booking-panel, cheap-flights-to, flights-airline |
| hotels | day-view, home-view, hotel-details |
| cars | home, day-view |

An example including some of the parameters looks like:

`GET /flights/day-view/?market=UK&currency=GBP&locale=en-GB&origin=cdg&destination=edi&outboundDate=2019-10-14&utm_term=summer&associateid=MY_ID_123`

`GET /flights/calendar-month-view/?market=UK&currency=GBP&locale=en-GB&origin=cdg&destination=edi&iym=1910&utm_term=summer&associateid=MY_ID_123`

`GET /cars/day-view/?pickupPlace=BCN&dropoffPlace=BCN&pickupTime=2019-09-10T10:00&dropoffTime=2019-09-15T10:00&driverAge=42&associateid=MY_ID_123`

`GET /hotels/day-view?entity_id=27536561&checkin=2019-09-10&checkout=2019-09-15&adults=2&rooms=1&associateid=MY_ID_123`

Specific request query parameters are provided in tables below.

*RESPONSE PARAMETERS*

A successful response contains no content and returns [HTTP 301](https://en.wikipedia.org/wiki/HTTP_301).
The URL to redirect to is provided in the Location header of the response.

<aside class="warning">
Please refer to our <a href="#response-codes">response codes</a> in case of unsuccessful response.
</aside>

## Flights Query Parameters

*Flights - API*

| API endpoint | Description  |
| --- | ---|
| [Flights Day View supported query parameters Schema](#flights-day-view-supported-query-parameters-schema) | Schema and Query Parameters Properties for Flights DayView|
| [Flights Calendar Month View supported parameters Schema](#flights-calendar-month-view-supported-query-parameters-schema) | Schema and Query Parameters Properties for Flights MonthView|
| [Flights Browse View supported parameters Schema](#flights-browse-view-supported-parameters-schema) | Schema and Query Parameters Properties for Flights BrowseView |
| [Flights Day View for multicity search Schema](#flights-day-view-for-multicity-search-schema) | Schema and Query Parameters Properties for Flights Multicity</b>. |




## Hotels Query Parameters

*Hotels - API*

| API endpoint | Description  |
| --- | ---|
| [Hotels Day View supported query parameters Schema](#hotels-day-view-supported-query-parameters-schema) | Schema and Query Parameters Properties for Hotels DayView</b>. |



## Cars Query Parameters

*Cars - API*

| API endpoint | Description  |
| --- | ---|
| [Carhire Day View supported query parameters Schema](#carhire-day-view-supported-query-parameters-schema) | Schema and Query Parameters Properties for CarHire DayView</b>. |
