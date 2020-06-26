# Flight Deals

Returns a list of Flight Deals based on provided input parameters. Currently there is minimal filtering by the following fields:

* Start Date

* End Date

* Limit by number of deals

* Destination (for example, could provide the DDBID of a country and you will receive deals only in that country)


*API endpoint*

`/api/v1/deals/{market}/{locale}/flights/{origin}`

## Get Deals

```shell
GET "http://partners.api.skyscanner.net/apiservices/
    api/v1/deals/
      `{market}`/
      `{locale}`/
      flights/
      `{origin}`?
    limit={limit}&
    start_date={start_date}&
    end_date={end_date}&
    currency={currency}&
    sorting={sorting}"
```

*PATH PARAMETERS*

| Parameter | Description |
| --------- | ----------- |
| ```market``` <br><span class="required">REQUIRED</span> | The required market. Example values: `bg`, `uk`, `es`, etc. |
| ```locale``` <br><span class="required">REQUIRED</span> | The required locale. Example values: `en-GB`, `en-US`, `bg-BG`, etc. |
| ```origin``` <br><span class="required">REQUIRED</span> | The required origin in DDBID form. Example values: `95673668`, `95673503`, `95565050`, etc. Could be either a City DDBID or an Airport DDBID. If Airport then it provides Deals from just that Airport. If City then it provides Deals from Airports in that City.|

*REQUEST PARAMETERS*

| Parameter | Description |
| --------- | ------- |
| ```limit``` <br><span class="optional">OPTIONAL</span> | The number of Deals to be returned. Example values: `1`, `10`, `15`, etc. |
| ```start_date``` <br><span class="optional">OPTIONAL</span> | The start date for which to get Deals. Date format: `DD-MM-YYYY`. Example values: `23-12-2020`, `03-05-2021`, `31-01-2022`. If both `start_date` and `end_date` are not provided, the date range for which Deals are returned by default is "the next 90 days".|
| ```end_date``` <br><span class="optional">OPTIONAL</span> | The end date for which to get Deals. Date format: `DD-MM-YYYY`. Example values: `23-12-2020`, `03-05-2021`, `31-01-2022`. If both `start_date` and `end_date` are not provided, the date range for which Deals are returned by default is "the next 90 days".|
| ```currency``` <br><span class="optional">OPTIONAL</span> | The currency which you want the returned Deals to be in. Currency format: `ISO4217` Example values: `EUR`, `GBP`, `BGN`. If no currency is provided, the market default is applied. |
| ```sorting``` <br><span class="optional">OPTIONAL</span> | The way the returned list of Deals is sorted. Possible values are: `NONE` and `SHUFFLE`. By default is `NONE`. |

```json
[
  {
    "inboundDuration": "0 days 1 hours 35 minutes 0 seconds",
    "outboundDuration": "0 days 23 hours 40 minutes 0 seconds",
    "origin": "LHR",
    "destination": "NRT",
    "inboundSegments": 2,
    "inboundDepartureDate": "2020-11-08",
    "price": 408,
    "referralLink": "http://localhost:3000/v1/flights/deals?origin=LHR&destination=NRT&outboundDate=2020-10-25&dealId=39227272e9844b6283cc2808e497c686&inboundDate=2020-11-08",
    "imageUrl": "https://content.skyscnr.com/99b6d376df86c55006e1ca90a18c5902/GettyImages-479490111.jpg",
    "airlines": [
      "Iberia",
      "Japan Airlines",
      "British Airways"
    ],
    "outboundDepartureDate": "2020-10-25",
    "currency": "GBP",
    "tripDuration": "14 days 6 hours 15 minutes 0 seconds",
    "outboundSegments": 2,
    "quoteTimestamp": null
  }
]
```


*RESPONSE PARAMETERS*

| Parameter | Description |
| --- | --- |
| ```Places``` | Contains the list of markets (array of countries as name-value pairs). |


## Place Information

```shell
GET "http://partners.api.skyscanner.net/apiservices/
    autosuggest/v1.0/
     `{market}`/
     `{currency}`/
      `{locale}`?
    id={place_id}&
    apiKey={apiKey}"
```

*REQUEST PARAMETERS*

| Parameter | Description |
| --------- | ------- |
| ```id``` <br><span class="required">REQUIRED</span> | The place id. |
| ```apiKey``` <br><span class="required">REQUIRED</span> | The API Key to identify the customer (could be full or short). |

> Example response for id=cdg

```json
{
  "Places": [
    {
      "PlaceId": "CDG-sky",
      "PlaceName": "Paris Charles de Gaulle",
      "CountryId": "FR-sky",
      "CityId": "PARI-sky",
      "CountryName": "France"
    }
  ]
}
```


*RESPONSE PARAMETERS*

| Parameter | Description |
| --- | --- |
| ```Places``` | Contains the information about the place such as name (in chosen locale), city, country. |
