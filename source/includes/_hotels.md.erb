# Hotels Live Prices

This service responsible for finding the best hotels with rates around a given entity. It provides endpoints to search prices, a map version of it and a hotel prices one.

## Endpoint

The Hotels API provides a global endpoint: https://www.skyscanner.net/g/hotels/{version}/ where version points to a specific release.

## Headers

The API expects the header:

- **x-user-agent**: Required. Indicates which is the device related to the client. The format for that header is device;B2B, where device can be:
	- T for tablet
	- D for desktop
	- M for mobile
	- N if you are not able to detect the device type

For example:

`x-user-agent: M;B2B`

## Use flow

All the /prices endpoints are intended to be queried using a polling mechanism using the same parameters as the one that started the polling. The flow of the service is described below:

1. On the first request that a user does, the service will reply with empty results and the status attribute inside the meta object set to *PENDING*. `Metadata PENDING state`.
3. The client needs to keep polling the service with the same query while the status attribute inside the meta object in the response is *PENDING*. On each query, the number of results will grow. `Metadata PENDING state, partial results`.
4. The status attribute will eventually change to *COMPLETED*. Meaning that the search cycle has finished. `Metadata COMPLETED state`.
5. Clients should implement a self-healing mechanism that should include:
    - Finish the polling after X seconds in the scenarios of having the status *PENDING* for so long.
    - Retry mechanism in the scenario of a service failure (Ex: retry after 1 seconds)

## Search Prices

### Entity Request

Given an entity_id, this endpoint will give back hotels with prices around the provided entity. The supported entities are any, from cities, islands, nations, places to Hotels.

The Hotels API, first of all, tries to search for the hotels related to an entity using an explicit relation - cities, administration zones, and nations, and if the results are less than a minimum number of hotels the query turns out in a geographical query.
This geographical query seeks for hotels using different distances, from 500 meters to 50km, till finding this minimum amount or get the maximum distance.

When a Hotel is used as the entity queried for, the service will treat this as an ad-hoc case. The hotel used as an entity will be serialized into the *hotel_pivot* object with its offers. Meanwhile, it will be removed from the results object.

The following URL shows how the search prices endpoint can be used to retrieve prices for those hotels that are placed in Barcelona

*API endpoint*

B2B partner, please use v1 endpoint

`GET /v1/prices/search/entity/{entity_id}`

V3 is a new endpoint that supports direct booking and cug overriding.

`GET /v3/prices/search/entity/{entity_id}`

```shell
GET "https://www.skyscanner.net/g/hbe-bellboy/v1/prices/search/entity/{entity_id}
  ?market={market}&locale={locale}&checkin_date={checkin_date}&checkout_date={checkout_date}
  &currency={currency}&adults={adults}&rooms={rooms}&images={images}&image_resolution={resolution}
  &image_type={type}&boost_official_partners={boost}&sort={sort_method}&limit={limit}&offset={offset}
  &partners_per_hotel={num_partners}&enhanced={enhanced}"
```

*TRY IT OUT*

[![Run in Postman](https://run.pstmn.io/button.svg)](https://app.getpostman.com/run-collection/a3262c8af4a48eece516)

*HEADER VALUES*

| Header | Value |
| --- | --- |
| `x-user-agent` <br><span class="required">REQUIRED</span> | Indicates which is the device and the platform related to the client. The format for that header is `device;B2B`, where:<br>Device is:<br>`T` for tablet<br>`D` for desktop<br>`M` for mobile<br>`N` if you are not able to detect the device type |


*URI PARAMETERS*

| Parameter | Description |
| --------- | ------- |
| `entity_id` <br><span class="required">REQUIRED</span> | Entity to search for hotels prices in it |
| `version` <br><span class="required">REQUIRED</span> | API version |

*QUERY PARAMETERS*

| Parameter | Description |
| --------- | ------- |
| `market` <br><span class="required">REQUIRED</span> | Matching [A-Z]{2} |
| `locale` <br><span class="required">REQUIRED</span> | Matching [a-z]{2}-[A-Z]{2} |
| `currency` <br><span class="required">REQUIRED</span> | Currency code |
| `checkin_date` <br><span class="required">REQUIRED</span> | YYYY-MM-DD |
| `checkout_date` <br><span class="required">REQUIRED</span> | YYYY-MM-DD |
| `rooms` <br><span class="required">REQUIRED</span> | Number of rooms<br>default: 1 |
| `adults` <br><span class="required">REQUIRED</span> | Number of adults<br>default: 2 |
| `apikey` <br><span class="required">REQUIRED</span> | This parameter is required to be on every single request any client does |
| `images` <br><span class="optional">OPTIONAL</span> | Maximum number of images to retrieve for each hotel<br>between 1-30, default: 1 |
| `image_resolution` <br><span class="optional">OPTIONAL</span> | Resolution options<br>high or low, default: high |
| `image_type` <br><span class="optional">OPTIONAL</span> | The format of the images<br>thumbnail or gallery or dynamic |
| `boost_official_partners` <br><span class="optional">OPTIONAL</span> | Indicates whether prices from official partners must be shown in the first place [1] or not [0]<br>default: 0 |
| `sort` <br><span class="optional">OPTIONAL</span> | Sort by a given attribute. By default the relevance sorting is applied<br>One of: relevance, -relevance, price, -price, distance, -distance, rating, -rating, stars, -stars |
| `price_min` <br><span class="optional">OPTIONAL</span> | Filter. Return only hotels where the cheaper price is at least price_min (included). Cannot be used together with price_buckets |
| `price_max` <br><span class="optional">OPTIONAL</span> | Filter. Return only hotels where the cheaper price is at most price_max (included). Cannot be used together with price_buckets |
| `price_buckets` <br><span class="optional">OPTIONAL</span> | OR filter. Return only hotels with offers inside the specified buckets. Cannot be used together with price_min/price_max |
| `price_bucket_step` <br><span class="optional">OPTIONAL</span> | Fix step for the buckets. Need to be used together with price_buckets, default step will be dynamic |
| `price_bucket_number` <br><span class="optional">OPTIONAL</span> | This parameter allows you to set the price buckets number, default: 5 |
| `price_buckets_strategy` <br><span class="optional">OPTIONAL</span> | price_buckets_strategy is 2 means use the new price buckets thread (split most 30 buckets), others use old price bucket thread (split into price_bucket_number buckets at most) |
| `price_buckets_min` <br><span class="optional">OPTIONAL</span> | Filter. Return only hotels where the cheaper price is at least price_buckets_min (included). Would not be applied if price_buckets_strategy is not 2 |
| `price_buckets_max` <br><span class="optional">OPTIONAL</span> | Filter. Return only hotels where the cheaper price is at most price_buckets_max (included). Would not be applied if price_buckets_strategy is not 2 |
| `district` <br><span class="optional">OPTIONAL</span> | OR filter. Return only results where a district matches |
| `stars` <br><span class="optional">OPTIONAL</span> | OR filter. Return only results where a star category matches. The values must be TravelAPI ids |
| `city` <br><span class="optional">OPTIONAL</span> | OR filter. When the search is done for an entity that contains different cities, this filter is available. Returns only results where the cities match. The values must be TravelAPI entity ids |
| `chain` <br><span class="optional">OPTIONAL</span> | OR filter. Return only results where a hotel chains matches. The values must be TravelAPI ids |
| `amenities` <br><span class="optional">OPTIONAL</span> | AND filter. Return only results where all amenities match. The values must be TravelAPI ids |
| `cancellation` <br><span class="optional">OPTIONAL</span> | OR filter. Return only results where a cancellation policies matches. Options are:<br>free_cancellation, non_refundable, refundable, special_conditions |
| `meal_plan` <br><span class="optional">OPTIONAL</span> | OR filter. Return only results where a meal plan matches. Options are:<br>room_only, breakfast_included, half_board, full_board, all_inclusive |
| `property_type` <br><span class="optional">OPTIONAL</span> | OR filter. Return only results where an accommodation type matches. The values must be TravelAPI ids |
| `guest_rating` <br><span class="optional">OPTIONAL</span> | OR filter. Return only results where a guest rating matches. The values must be TravelAPI ids |
| `guest_type` <br><span class="optional">OPTIONAL</span> | OR filter. Return only results where a guest type matches. The values must be TravelAPI ids |
| `hotel_name` <br><span class="optional">OPTIONAL</span> | Filter. Return only results where hotel name matches |
| `limit` <br><span class="optional">OPTIONAL</span> | Number of results to retrieve<br>between 1-30, default: 15 |
| `offset` <br><span class="optional">OPTIONAL</span> | How many results to skip from the first position. Useful for paginating<br>default: 0 |
| `partners_per_hotel` <br><span class="optional">OPTIONAL</span> | Maximum numbers of partners to retrieve per each hotel. Note that 0 means all the available partners<br>default: 3 |
| `enhanced` <br><span class="optional">OPTIONAL</span> | This parameter allows you to add additional content to the default response. Available options are:<br>filters: Returns extra object in the response including the filters like stars, district, city, etc.<br>price_slider: Return the price_slider.<br>partners: Returns information about the active partners in the system. is_official, the logo, the name and the website_id.<br>images: Returns images for the hotels. With the partner website_id and the urls.<br>amenities: Returns the hotels amenities.<br>query_location: Returns the location (higher level entities according to the searched entity) and map boundary (the coordinates of the search area).<br>extras: Returns the hotel chain of the hotels.<br>translations: Returns a dictionary with all literals and their corresponding translations using the request locale. <br>detailed_reviews: Returns information from the hotel reviews provided by Trustyou (http://www.trustyou.com/)|
| `index` <br><span class="optional">OPTIONAL</span> | Mark the times of the same requests sent to bellboy, start from 1, default: 0 |
| `sorting_version` <br><span class="optional">OPTIONAL</span> | (B2B partner needn't set the value) Hotel sorting score calculation options<br>mr4: RelevanceContainerScoring,<br>mr5: IronRankScoring,<br>mr6: IronCatRankScoring,<br>mr4a: RelevanceContainerHotelModelScoring,<br>mr7: HotelBookingModelScoring,<br>mr8: IronTrainModelScoring,<br>default: mr4 |
| `t_version` <br><span class="optional">OPTIONAL</span> | (B2B partner needn't set the value) Used for ABTesting, default is '' |
| `app_name` <br><span class="optional">OPTIONAL</span> | (B2B partner needn't set the value) This parameter allows you to set the app name, default is '' |
| `appVersion` <br><span class="optional">OPTIONAL</span> | (B2B partner needn't set the value) This parameter allows you to set the app version, default is '' |
| `search_id` <br><span class="optional">OPTIONAL</span> | (B2B partner needn't set the value) Elasticsearch ID, for the same request, first time needn't set the value, second time can get the value from prior response, default is '' |
| `cug_segments` <br><span class="optional">OPTIONAL</span> | (B2B partner needn't set the value) Only v3 supports, it allows you to add special cug segments for user. Options are:<br>mobile, logged_in, business, apps, flight_booked |
| `cug` <br><span class="optional">OPTIONAL</span> | (B2B partner needn't set the value) This parameter allows you to reorder hotels by cug price. Options are:<br>1: cug hotels would be ranked ahead, 2: high cug hotels would be ranked ahead. <br>default is 0, order by parameter sort |

**Note**: The OR and AND filters allow multiple values coma separated. For example: *&amenities=Lift,Bar*

### Response

> Example response:

```json
{
    "correlation_id": "3889f7d3-65d2-40e8-8034-4accb18bade9",
    "meta": {
        "status": "COMPLETED",
        "search_id": "915c591f9fd48c64c9c0ad748d6e6851f09f5dbc4d608495479f1a07e1e7a968",
        "total": 311,
        "completion_percentage": 100,
        "total_available": 73,
        "hotels_filtered": 73,
        "offers": 459,
        "total_available_filtered": 73,
        "request_id": "e3f5c49b-3139-4311-99e1-5ca746541f58"
    },
    "results": {
        "location": [
            {
                "entity_type": "Island",
                "entity_id": "81972530",
                "name": "Malta Island"
            },
            {
                "entity_type": "Nation",
                "entity_id": "29475371",
                "name": "Malte"
            }
        ],
        "hotels": [
            {
                "coordinates": [
                    14.50658,
                    35.91218
                ],
                "stars": "3",
                "offer_types": [
                    "META"
                ],
                "district": "[]",
                "reviews_count": 868,
                "city": "33349710",
                "cheapest_offer_type": "META",
                "amenities": [
                    "Lift",
                    "ConciergeService",
                    "Laundry",
                    ...
                ],
                "property_type": "Hotel",
                "distance": 6142.49539734,
                "rating": {
                    "desc": "rating_satisfactory",
                    "value": 6.9
                },
                "name": "Roma Hotel",
                "hotel_id": "47053033",
                "images": [
                    {
                        "gallery": "https://d2xf5gjipzd8cd.cloudfront.net/available/353235256/mca.jpg",
                        "provider": "h_ct",
                        "category": "Beach",
                        "dynamic": "https://d2xf5gjipzd8cd.cloudfront.net/available/353235256/353235256_WxH.jpg",
                        "thumbnail": "https://d2xf5gjipzd8cd.cloudfront.net/available/353235256/mt.jpg"
                    },
                    ...
                ],
                "offers": [
                    {
                        "partner_id": "h_hc",
                        "price": 78,
                        "price_gbp": 69,
                        "available": null,
                        "strike_through": null,
                        "meal_plan": "breakfast_included",
                        "is_official": true,
                        "closed_user_groups": null,
                        "dbook_link": null,
                        "room_type": [
                            "triple_room"
                        ],
                        "deeplink": "www.skyscanner.fr/hotel_deeplink/4.0/FR/fr-FR/EUR/h_hc/47053033/2019-06-18/2019-06-19/hotel/hotel/hotels?guests=1&rooms=1&legacy_provider_id=17&request_id=e3f5c49b-3139-4311-99e1-5ca746541f58&q_datetime_utc=2019-06-13T02%3A44%3A29&appName=mobileweb&appVersion=2.0&ticket_price=78&deeplink_data=eyJ1cmwiOiAiaHR0cHM6Ly9mci5ob3RlbHMuY29tL1BQQ0hvdGVsRGV0YWlscz9hZHVsdHNQZXJSb29tPTEmdmlldz1wcmljZXMmbXBoPTAmcG9zPUhDT01fRlImbnVtYmVyT2ZSb29tcz0xJnJhdGVwbGFuaWQ9MjA2Nzc3OTk1JmhvdGVsaWQ9Mjk5NTg4JmRlcGFydHVyZURhdGU9MTkvMDYvMjAxOSZsb2NhbGU9ZnJfRlImYXJyaXZhbERhdGU9MTgvMDYvMjAxOSIsICJmaWVsZHMiOiB7InNpZ25hdHVyZSI6ICJmNTkyYjZiNjU0OWUxMDBiYTNkNzM1NDNhOGZmNGNmOSJ9fQ%3D%3D&max_price=78.0&channel=website&max_price=78.0&channel=website",
                        "cancellation_text": null,
                        "cancellation": "non_refundable"
                    },
                    ...
                ],
                "relevance": 2000000.3686611408
            },
            ...
        ],
        "price_includes": [
            "vat",
            "other_taxes"
        ],
        "average_min_price": 139.73,
        "filters": {
            "stars": [
                {
                    "id": "5",
                    "max_price": null,
                    "count": 7,
                    "min_price": 182
                },
                ...
            ],
            "chain": [
                {
                    "id": "Corinthia",
                    "max_price": null,
                    "count": 1,
                    "min_price": 182
                }
            ],
            "price_buckets": [
                {
                    "id": "PR_BK_0",
                    "max_price": 50,
                    "count": 7,
                    "min_price": null
                },
                ...
            ],
            "district": [],
            "city": [
                {
                    "id": "33350111",
                    "max_price": null,
                    "count": 27,
                    "min_price": 36
                },
                ...
            ],
            "meal_plan": [
                {
                    "id": "breakfast_included",
                    "max_price": null,
                    "count": 43,
                    "min_price": 28
                },
                ...
            ],
            "guest_rating": [
                {
                    "id": "6",
                    "text": "rating_satisfactory",
                    "count": 3,
                    "min_price": null,
                    "max_price": null
                },
                ...
            ],
            "amenities": [
                {
                    "id": "WifiService",
                    "max_price": null,
                    "count": 70,
                    "min_price": 20
                },
                ...
            ],
            "property_type": [
                {
                    "id": "Hotel",
                    "max_price": null,
                    "count": 42,
                    "min_price": 50
                },
                ...
            ],
            "guest_type": [
                {
                    "id": "solo",
                    "max_price": null,
                    "count": 1,
                    "min_price": null
                },
                ...
            ],
            "cancellation": [
                {
                    "id": "free_cancellation",
                    "max_price": null,
                    "count": 26,
                    "min_price": 28
                },
                ...
            ]
        },
        "partners": [
            {
                "website_id": "h_ay",
                "is_dbook": false,
                "logo": "www.skyscanner.fr/images/websites/220x80/h_ay.png",
                "name": "ibis Styles",
                "is_official": true,
                "partner_type": "Group"
            },
            ...
        ],
        "hotel_pivot": null,
        "map_boundary": {
            "s_w_lng": 14.448729,
            "s_w_lat": 35.893651,
            "n_e_lat": 35.913651,
            "n_e_lng": 14.51241
        },
        "closed_user_group_deals": [],
        "entity": {
            "name": "Luqa",
            "entity_type": "City",
            "centroid": {
                "type": "Point",
                "coordinates": [
                    14.4886111132,
                    35.858888893
                ]
            },
            "entity_id": "46395655",
            "official_center": {
                "type": "Point",
                "coordinates": [
                    14.4892913,
                    35.859653
                ]
            }
        }
    },
    "count": 15,
    "translations": {
        "CUG_create_account_to_unlock_deals_msg": "Créez un compte pour avoir accès à des offres exclusives",
        "CUG_deal": "OFFRE",
        ...
    }
}
```

*RESPONSE PARAMETERS*

| Element | Detail |
| ------- | ------ |
| `correlation_id` | An identifier of the request |
| `meta` | Contains metadata regarding the search cycle such as it's status |
| `count` | Number of hotels |
| `results` | An object containing the hotels and the enhancers if requested |
| `translations` | Only with the `translations` enhanced. Dictionary with all literals that can be translated |


### Location Request

This endpoint gives back hotels with prices too but instead from an entity, around specific coordinates.
It takes the coordinades as an input to provide the hotels.
Provides the search by current location functionality.

*API endpoint*

`GET /v1/prices/search/location/{lon,lat}`

```shell
GET "https://www.skyscanner.net/g/hotels/v1/prices/search/location/{lon,lat}
  ?market={market}&locale={locale}&checkin_date={checkin_date}&checkout_date={checkout_date}
  &currency={currency}&adults={adults}&rooms={rooms}&images={images}&image_resolution={resolution}
  &image_type={type}&boost_official_partners={boost}&sort={sort_method}&limit={limit}&offset={offset}
  &partners_per_hotel={num_partners}&enhanced={enhanced}"
```

*TRY IT OUT*

[![Run in Postman](https://run.pstmn.io/button.svg)](https://app.getpostman.com/run-collection/378efb1ead00baf8e120)

*HEADER VALUES*

| Header | Value |
| --- | --- |
| `apikey` <br><span class="required">REQUIRED</span> | This header is required to be on every single request any client does (it could also be accepted via query parameter) |
| `x-user-agent` <br><span class="required">REQUIRED</span> | Indicates which is the device and the platform related to the client. The format for that header is `device;B2B`, where:<br>Device is:<br>`T` for tablet<br>`D` for desktop<br>`M` for mobile<br>`N` if you are not able to detect the device type |

*URI PARAMETERS*

| Parameter | Description |
| --------- | ------- |
| `location` <br><span class="required">REQUIRED</span> | Location to search hotels near it. Following the format: lon,lat |
| `version` <br><span class="required">REQUIRED</span> | API version |

*QUERY PARAMETERS*

| Parameter | Description |
| --------- | ------- |
| `market` <br><span class="required">REQUIRED</span> | Matching [A-Z]{2} |
| `locale` <br><span class="required">REQUIRED</span> | Matching [a-z]{2}-[A-Z]{2} |
| `currency` <br><span class="required">REQUIRED</span> | Currency code |
| `checkin_date` <br><span class="required">REQUIRED</span> | YYYY-MM-DD |
| `checkout_date` <br><span class="required">REQUIRED</span> | YYYY-MM-DD |
| `rooms` <br><span class="required">REQUIRED</span> | Number of rooms<br>default: 1 |
| `adults` <br><span class="required">REQUIRED</span> | Number of adults<br>default: 2 |
| `apikey` <br><span class="required">REQUIRED</span> | This parameter is required to be on every single request any client does |
| `images` <br><span class="optional">OPTIONAL</span> | Maximum number of images to retrieve per each hotel<br>between 1-30, default: 3 |
| `image_resolution` <br><span class="optional">OPTIONAL</span> | Resolution options<br>high or low, default: high |
| `image_type` <br><span class="optional">OPTIONAL</span> | The format of the images<br>thumbnail or gallery |
| `boost_official_partners` <br><span class="optional">OPTIONAL</span> | Indicates whether prices from official partners must be shown in the first place [1] or not [0]<br>default: 0 |
| `sort` <br><span class="optional">OPTIONAL</span> | Sort by a given attribute. By default the relevance sorting is applied<br>One of: relevance, -relevance, price, -price, distance, -distance, rating, -rating, stars, -stars |
| `price_min` <br><span class="optional">OPTIONAL</span> | Filter. Return only hotels where the cheaper price is at least price_min (included). Cannot be used together with price_buckets |
| `price_max` <br><span class="optional">OPTIONAL</span> | Filter. Return only hotels where the cheaper price is at most price_max (included). Cannot be used together with price_buckets |
| `price_buckets` <br><span class="optional">OPTIONAL</span> | OR filter. Return only hotels with offers inside the specified buckets. Cannot be used together with price_min/price_max |
| `district` <br><span class="optional">OPTIONAL</span> | OR filter. Return only results where a district matches |
| `stars` <br><span class="optional">OPTIONAL</span> | OR filter. Return only results where a star category matches. The values must be TravelAPI ids |
| `city` <br><span class="optional">OPTIONAL</span> | OR filter. When the search is done for an entity that contains different cities, this filter is available. Returns only results where the cities match. The values must be TravelAPI entity ids |
| `chain` <br><span class="optional">OPTIONAL</span> | OR filter. Return only results where a hotel chains matches. The values must be TravelAPI ids |
| `amenities` <br><span class="optional">OPTIONAL</span> | AND filter. Return only results where all amenities match. The values must be TravelAPI ids |
| `cancellation` <br><span class="optional">OPTIONAL</span> | OR filter. Return only results where a cancellation policies matches. Options are:<br>free_cancellation, non_refundable, refundable, special_conditions |
| `meal_plan` <br><span class="optional">OPTIONAL</span> | OR filter. Return only results where a meal plan matches. Options are:<br>room_only, breakfast_included, half_board, full_board, all_inclusive |
| `property_type` <br><span class="optional">OPTIONAL</span> | OR filter. Return only results where an accommodation type matches. The values must be TravelAPI ids |
| `hotel_name` <br><span class="optional">OPTIONAL</span> | Filter. Return only results where hotel name matches |
| `limit` <br><span class="optional">OPTIONAL</span> | Number of results to retrieve<br>between 1-30, default: 30 |
| `offset` <br><span class="optional">OPTIONAL</span> | How many results to skip from the first position. Useful for paginating<br>default: 0 |
| `partners_per_hotel` <br><span class="optional">OPTIONAL</span> | Maximum numbers of partners to retrieve per each hotel. Note that 0 means all the available partners<br>default: 3 |
| `enhanced` <br><span class="optional">OPTIONAL</span> | This parameter allows you to add additional content to the default response. The available options are:<br>filters: Returns extra object in the response including the filters like stars, district, city, etc.<br>price_slider: Return the price_slider.<br>partners: Returns information about the active partners in the system. is_official, the logo, the name and the website_id.<br>images: Returns images for the hotels. With the partner website_id and the urls.<br>amenities: Returns the hotels amenities.<br>query_location: Returns the location (higher level entities according to the searched entity) and map boundary (the coordinates of the search area).<br>extras: Returns the hotel chain of the hotels.<br>translations: Returns a dictionary with all literals and their corresponding translations using the request locale. |

**Note**: The OR and AND filters allow multiple values coma separated. For example: *&amenities=Lift,Bar*

### Response

> The response is the same as the search entity one but without the *hotel_pivot*

*RESPONSE PARAMETERS*

| Element | Detail |
| ------- | ------ |
| `correlation_id` | An identifier of the request |
| `meta` | Contains metadata regarding the search cycle such as it's status |
| `count` | Number of hotels |
| `results` | An object containing the hotels and the enhancers if requested |
| `translations` | Only with the `translations` enhanced. Dictionary with all literals that can be translated |

## Search Prices, map version

### Entity Request

Given an entity, this endpoint will give you back the hotels with prices around the provided entity, having the same intentions than the regular search prices but modifying the response to suit it in environments where the information has to be rendered in a map.
These differences can be summarized into the following points:

- Every hotel will have one price (the cheapest).
- The default total amount of hotels returned per page will be 100.
- Support for bounding box queries to filter hotels that are inside of an area, the coordinates passed are serialized as *left, bottom, right, top*

*API endpoint*

`GET /v1/prices/map/entity/{entity_id}`

```shell
GET "https://www.skyscanner.net/g/hotels/v1/prices/map/entity/{entity_id}
  ?market={market}&locale={locale}&checkin_date={checkin_date}&checkout_date={checkout_date}
  &currency={currency}&adults={adults}&rooms={rooms}&images={images}&image_resolution={resolution}
  &image_type={type}&boost_official_partners={boost}&sort={sort_method}&limit={limit}&offset={offset}
  &partners_per_hotel={num_partners}&enhanced={enhanced}&bbox={left,bottom,right,top}"
```

*TRY IT OUT*

[![Run in Postman](https://run.pstmn.io/button.svg)](https://app.getpostman.com/run-collection/44864263fb0a0624becf)

*HEADER VALUES*

| Header | Value |
| --- | --- |
| `apikey` <br><span class="required">REQUIRED</span> | This header is required to be on every single request any client does (it could also be accepted via query parameter) |
| `x-user-agent` <br><span class="required">REQUIRED</span> | Indicates which is the device and the platform related to the client. The format for that header is `device;B2B`, where:<br>Device is:<br>`T` for tablet<br>`D` for desktop<br>`M` for mobile<br>`N` if you are not able to detect the device type |

*URI PARAMETERS*

| Parameter | Description |
| --------- | ------- |
| `entity_id` <br><span class="required">REQUIRED</span> | Entity to search for hotels prices in it |
| `version` <br><span class="required">REQUIRED</span> | API version |

*QUERY PARAMETERS*

| Parameter | Description |
| --------- | ------- |
| `market` <br><span class="required">REQUIRED</span> | Matching [A-Z]{2} |
| `locale` <br><span class="required">REQUIRED</span> | Matching [a-z]{2}-[A-Z]{2} |
| `currency` <br><span class="required">REQUIRED</span> | Currency code |
| `checkin_date` <br><span class="required">REQUIRED</span> | YYYY-MM-DD |
| `checkout_date` <br><span class="required">REQUIRED</span> | YYYY-MM-DD |
| `rooms` <br><span class="required">REQUIRED</span> | Number of rooms<br>default: 1 |
| `adults` <br><span class="required">REQUIRED</span> | Number of adults<br>default: 2 |
| `apikey` <br><span class="required">REQUIRED</span> | This parameter is required to be on every single request any client does |
| `images` <br><span class="optional">OPTIONAL</span> | Maximum number of images to retrieve per each hotel<br>between 1-30, default: 3 |
| `image_resolution` <br><span class="optional">OPTIONAL</span> | Resolution options<br>high or low, default: high |
| `image_type` <br><span class="optional">OPTIONAL</span> | The format of the images<br>thumbnail or gallery |
| `boost_official_partners` <br><span class="optional">OPTIONAL</span> | Indicates whether prices from official partners must be shown in the first place [1] or not [0]<br>default: 0 |
| `sort` <br><span class="optional">OPTIONAL</span> | Sort by a given attribute. By default the relevance sorting is applied<br>One of: relevance, -relevance, price, -price, distance, -distance, rating, -rating, stars, -stars |
| `price_min` <br><span class="optional">OPTIONAL</span> | Filter. Return only hotels where the cheaper price is at least price_min (included). Cannot be used together with price_buckets |
| `price_max` <br><span class="optional">OPTIONAL</span> | Filter. Return only hotels where the cheaper price is at most price_max (included). Cannot be used together with price_buckets |
| `price_buckets` <br><span class="optional">OPTIONAL</span> | OR filter. Return only hotels with offers inside the specified buckets. Cannot be used together with price_min/price_max |
| `district` <br><span class="optional">OPTIONAL</span> | OR filter. Return only results where a district matches |
| `stars` <br><span class="optional">OPTIONAL</span> | OR filter. Return only results where a star category matches. The values must be TravelAPI ids |
| `city` <br><span class="optional">OPTIONAL</span> | OR filter. When the search is done for an entity that contains different cities, this filter is available. Returns only results where the cities match. The values must be TravelAPI entity ids |
| `chain` <br><span class="optional">OPTIONAL</span> | OR filter. Return only results where a hotel chains matches. The values must be TravelAPI ids |
| `amenities` <br><span class="optional">OPTIONAL</span> | AND filter. Return only results where all amenities match. The values must be TravelAPI ids |
| `cancellation` <br><span class="optional">OPTIONAL</span> | OR filter. Return only results where a cancellation policies matches. Options are:<br>free_cancellation, non_refundable, refundable, special_conditions |
| `meal_plan` <br><span class="optional">OPTIONAL</span> | OR filter. Return only results where a meal plan matches. Options are:<br>room_only, breakfast_included, half_board, full_board, all_inclusive |
| `property_type` <br><span class="optional">OPTIONAL</span> | OR filter. Return only results where an accommodation type matches. The values must be TravelAPI ids |
| `hotel_name` <br><span class="optional">OPTIONAL</span> | Filter. Return only results where hotel name matches |
| `limit` <br><span class="optional">OPTIONAL</span> | Number of results to retrieve<br>between 1-100, default: 100 |
| `offset` <br><span class="optional">OPTIONAL</span> | How many results to skip from the first position. Useful for paginating<br>default: 0 |
| `partners_per_hotel` <br><span class="optional">OPTIONAL</span> | Maximum numbers of partners to retrieve per each hotel. Note that 0 means all the available partners. Map only supports 1 partner per hotel<br>default: 1 |
| `enhanced` <br><span class="optional">OPTIONAL</span> | This parameter allows you to add additional content to the default response. The available options are:<br>filters: Returns extra object in the response including the filters like stars, district, city, etc.<br>price_slider: Return the price_slider.<br>query_location: Returns the location (higher level entities according to the searched entity) and map boundary (the coordinates of the search area).<br>translations: Returns a dictionary with all literals and their corresponding translations using the request locale. |
| `bbox` <br><span class="optional">OPTIONAL</span> | Bounding Box coordinates in which to look for hotels as bbox=left,bottom,right,top<br>Example: -4.051,50.478,1.853,52.909 |

**Note**: The OR and AND filters allow multiple values coma separated. For example: *&amenities=Lift,Bar*

### Response

> Example response:

```json
{
  "correlation_id": "d93ddb4d-c97c-4979-9627-e188e02c8409",
  "meta": {
    "status": "COMPLETED",
    "total": 5500,
    "total_available": 4092,
    "completion_percentage": 100,
    "offers": 67275,
    "hotels_filtered": 0
  },
  "count": 15,
  "results": {
    "filters": {
      "district": [
        {
          "id": "27562177",
          "min_price": 45,
          "max_price": null,
          "count": 94
        },
        ...
      ],
      "chain": [
        {
          "id": "Holiday Inn",
          "min_price": 74,
          "max_price": null,
          "count": 74
        },
        ...
      ],
      "cancellation": [
        {
          "id": "free_cancellation",
          "min_price": 36,
          "max_price": null,
          "count": 2207
        },
        ...
      ],
      "city": [
        {
          "id": "27544008",
          "min_price": 32,
          "max_price": null,
          "count": 856
        },
        ...
      ],
      "amenities": [
        {
          "id": "WifiService",
          "min_price": 32,
          "max_price": null,
          "count": 3327
        },
        ...
      ],
      "price_buckets": [
        {
          "id": "PR_BK_0",
          "min_price": null,
          "max_price": 80,
          "count": 130
        },
        ...
      ],
      "stars": [
        {
          "id": "4",
          "min_price": 58,
          "max_price": null,
          "count": 1220
        },
        ...
      ],
      "meal_plan": [
        {
          "id": "room_only",
          "min_price": 32,
          "max_price": null,
          "count": 2060
        },
        ...
      ],
      "property_type": [
        {
          "id": "Hotel",
          "min_price": 32,
          "max_price": null,
          "count": 3486
        },
        ...
      ]
    },
    "map_boundary": {
      "n_e_lng": 1.72864,
      "s_w_lng": -2.04675,
      "s_w_lat": 50.63341,
      "n_e_lat": 52.7619
    },
    "hotel_pivot": null,
    "hotels": [
      {
        "reviews_count": 284,
        "coordinates": [
          1.2961,
          51.12328
        ],
        "hotel_id": "46997257",
        "images": [
          {
            "provider": "h_dp",
            "gallery": "http://d3ba47lalua02r.cloudfront.net/available/50049482/mca.jpg",
            "thumbnail": "http://d3ba47lalua02r.cloudfront.net/available/50049482/mt.jpg"
          }
        ],
        "name": "The West Bank Guest House",
        "offers": [
          {
            "price_gbp": 58,
            "price": 58,
            "deeplink": "www.skyscanner.net/hotel_deeplink/4.0/UK/en-GB/GBP/h_xp/46997257/2017-04-30/2017-05-02/hotel/hotel/hotels?guests=1&ticket_price=58&rooms_left=1&appVersion=2.0&q_datetime_utc=2017-04-25T13%3A37%3A37&rooms=1&deeplink_ids=eu-west-1.prod_ae42baa45b08402e0a109287d1780528&request_id=b745fa26-f166-478f-b52c-2fcee3f413fe&appName=web&legacy_provider_id=1&max_price=132.0",
            "closed_user_groups": null
          }
        ],
        "stars": "4",
        "rating": {
          "value": 7.7,
          "desc": "rating_good"
        }
      },
      ...
    ],
    "location": [
      {
        "name": "United Kingdom",
        "entity_id": "29475375",
        "entity_type": "Nation"
      }
    ]
  },
  "translations": {
    "CUG_create_account_to_unlock_deals_msg": "Create an account to unlock exclusive deals",
    "CUG_deal": "DEAL",
    ...
  }
}
```

*RESPONSE PARAMETERS*

| Element | Detail |
| ------- | ------ |
| `correlation_id` | An identifier of the request |
| `meta` | Contains metadata regarding the search cycle such as it's status |
| `count` | Number of hotels |
| `results` | An object containing the hotels and the enhancers if requested |
| `translations` | Only with the `translations` enhanced. Dictionary with all literals that can be translated |

### Location Request

This endpoint gives back hotels with prices too with map specific features but instead from an entity, around specific coordinates.

Provides the search by current location functionality.

*API endpoint*

`GET /v1/prices/map/location/{lon,lat}`

```shell
GET "https://www.skyscanner.net/g/hotels/v1/prices/map/location/{lon,lat}
  ?market={market}&locale={locale}&checkin_date={checkin_date}&checkout_date={checkout_date}
  &currency={currency}&adults={adults}&rooms={rooms}&images={images}&image_resolution={resolution}
  &image_type={type}&boost_official_partners={boost}&sort={sort_method}&limit={limit}&offset={offset}
  &partners_per_hotel={num_partners}&enhanced={enhanced}&bbox={left,bottom,right,top}"
```

*TRY IT OUT*

[![Run in Postman](https://run.pstmn.io/button.svg)](https://app.getpostman.com/run-collection/8c06f7a93120a724de16)

*HEADER VALUES*

| Header | Value |
| --- | --- |
| `apikey` <br><span class="required">REQUIRED</span> | This header is required to be on every single request any client does (it could also be accepted via query parameter) |
| `x-user-agent` <br><span class="required">REQUIRED</span> | Indicates which is the device and the platform related to the client. The format for that header is `device;B2B`, where:<br>Device is:<br>`T` for tablet<br>`D` for desktop<br>`M` for mobile<br>`N` if you are not able to detect the device type |

*URI PARAMETERS*

| Parameter | Description |
| --------- | ------- |
| `location` <br><span class="required">REQUIRED</span> | Location to search hotels near it. Following the format: lon,lat |
| `version` <br><span class="required">REQUIRED</span> | API version |

*QUERY PARAMETERS*

| Parameter | Description |
| --------- | ------- |
| `market` <br><span class="required">REQUIRED</span> | Matching [A-Z]{2} |
| `locale` <br><span class="required">REQUIRED</span> | Matching [a-z]{2}-[A-Z]{2} |
| `currency` <br><span class="required">REQUIRED</span> | Currency code |
| `checkin_date` <br><span class="required">REQUIRED</span> | YYYY-MM-DD |
| `checkout_date` <br><span class="required">REQUIRED</span> | YYYY-MM-DD |
| `rooms` <br><span class="required">REQUIRED</span> | Number of rooms<br>default: 1 |
| `adults` <br><span class="required">REQUIRED</span> | Number of adults<br>default: 2 |
| `apikey` <br><span class="required">REQUIRED</span> | This parameter is required to be on every single request any client does |
| `images` <br><span class="optional">OPTIONAL</span> | Maximum number of images to retrieve per each hotel<br>between 1-30, default: 3 |
| `image_resolution` <br><span class="optional">OPTIONAL</span> | Resolution options<br>high or low, default: high |
| `image_type` <br><span class="optional">OPTIONAL</span> | The format of the images<br>thumbnail or gallery |
| `boost_official_partners` <br><span class="optional">OPTIONAL</span> | Indicates whether prices from official partners must be shown in the first place [1] or not [0]<br>default: 0 |
| `sort` <br><span class="optional">OPTIONAL</span> | Sort by a given attribute. By default the relevance sorting is applied<br>One of: relevance, -relevance, price, -price, distance, -distance, rating, -rating, stars, -stars |
| `price_min` <br><span class="optional">OPTIONAL</span> | Filter. Return only hotels where the cheaper price is at least price_min (included). Cannot be used together with price_buckets |
| `price_max` <br><span class="optional">OPTIONAL</span> | Filter. Return only hotels where the cheaper price is at most price_max (included). Cannot be used together with price_buckets |
| `price_buckets` <br><span class="optional">OPTIONAL</span> | OR filter. Return only hotels with offers inside the specified buckets. Cannot be used together with price_min/price_max |
| `district` <br><span class="optional">OPTIONAL</span> | OR filter. Return only results where a district matches |
| `stars` <br><span class="optional">OPTIONAL</span> | OR filter. Return only results where a star category matches. The values must be TravelAPI ids |
| `city` <br><span class="optional">OPTIONAL</span> | OR filter. When the search is done for an entity that contains different cities, this filter is available. Returns only results where the cities match. The values must be TravelAPI entity ids |
| `chain` <br><span class="optional">OPTIONAL</span> | OR filter. Return only results where a hotel chains matches. The values must be TravelAPI ids |
| `amenities` <br><span class="optional">OPTIONAL</span> | AND filter. Return only results where all amenities match. The values must be TravelAPI ids |
| `cancellation` <br><span class="optional">OPTIONAL</span> | OR filter. Return only results where a cancellation policies matches. Options are:<br>free_cancellation, non_refundable, refundable, special_conditions |
| `meal_plan` <br><span class="optional">OPTIONAL</span> | OR filter. Return only results where a meal plan matches. Options are:<br>room_only, breakfast_included, half_board, full_board, all_inclusive |
| `property_type` <br><span class="optional">OPTIONAL</span> | OR filter. Return only results where an accommodation type matches. The values must be TravelAPI ids |
| `hotel_name` <br><span class="optional">OPTIONAL</span> | Filter. Return only results where hotel name matches |
| `limit` <br><span class="optional">OPTIONAL</span> | Number of results to retrieve<br>between 1-100, default: 100 |
| `offset` <br><span class="optional">OPTIONAL</span> | How many results to skip from the first position. Useful for paginating<br>default: 0 |
| `partners_per_hotel` <br><span class="optional">OPTIONAL</span> | Maximum numbers of partners to retrieve per each hotel. Note that 0 means all the available partners. Map only supports 1 partner per hotel<br>default: 1 |
| `enhanced` <br><span class="optional">OPTIONAL</span> | This parameter allows you to add additional content to the default response. The available options are:<br>filters: Returns extra object in the response including the filters like stars, district, city, etc.<br>price_slider: Return the price_slider.<br>query_location: Returns the location (higher level entities according to the searched entity) and map boundary (the coordinates of the search area).<br>translations: Returns a dictionary with all literals and their corresponding translations using the request locale. |
| `bbox` <br><span class="optional">OPTIONAL</span> | Bounding Box coordinates in which to look for hotels as bbox=left,bottom,right,top<br>Example: -4.051,50.478,1.853,52.909 |

**Note**: The OR and AND filters allow multiple values coma separated. For example: *&amenities=Lift,Bar*

### Response

> The response is the same as the search map entity one

*RESPONSE PARAMETERS*

| Element | Detail |
| ------- | ------ |
| `correlation_id` | An identifier of the request |
| `meta` | Contains metadata regarding the search cycle such as it's status |
| `count` | Number of hotels |
| `results` | An object containing the hotels and the enhancers if requested |
| `translations` | Only with the `translations` enhanced. Dictionary with all literals that can be translated |

## Hotel Prices

### Request

Given a hotel, this endpoint will give back the hotel with all the information and live prices. To reuse the prices already fetched by previous calls to the search endpoint the parameter *entity_id* must be filled with the same entity id.
Otherwise, the system will start fetching prices from the beginning for this specific hotel.
Is a regular practice following the user flow first of all search for prices using the search prices endpoint and then retrieve more specific information - perhaps the detailed reviews - about one of the hotels using the hotel prices endpoint.

*API endpoint*

B2B partner please use v1 endpoint

`GET /v1/prices/hotel/{hotel_id}`

V3 is a new endpoint which supports dbook booking and cug overriding.

`GET /v3/prices/hotel/{hotel_id}`

```shell
GET "https://www.skyscanner.net/g/hotels/v1/prices/hotel/{hotel_id}
  ?entity_id=27539733&market={market}&locale={locale}&checkin_date={checkin_date}&checkout_date={checkout_date}
  &currency={currency}&adults={adults}&rooms={rooms}&images={images}&image_resolution={resolution}
  &image_type={type}&boost_official_partners={boost}&partners_per_hotel={num_partners}"
```

*TRY IT OUT*

[![Run in Postman](https://run.pstmn.io/button.svg)](https://app.getpostman.com/run-collection/235d1617d92d7467ed1b)

*HEADER VALUES*

| Header | Value |
| --- | --- |
| `apikey` <br><span class="required">REQUIRED</span> | This header is required to be on every single request any client does (it could also be accepted via query parameter) |
| `x-user-agent` <br><span class="required">REQUIRED</span> | Indicates which is the device and the platform related to the client. The format for that header is `device;B2B`, where:<br>Device is:<br>`T` for tablet<br>`D` for desktop<br>`M` for mobile<br>`N` if you are not able to detect the device type |

*URI PARAMETERS*

| Parameter | Description |
| --------- | ------- |
| `hotel_id` <br><span class="required">REQUIRED</span> | Hotel to search prices for |
| `version` <br><span class="required">REQUIRED</span> | API version |

*QUERY PARAMETERS*

| Parameter | Description |
| --------- | ------- |
| `market` <br><span class="required">REQUIRED</span> | Matching [A-Z]{2} |
| `locale` <br><span class="required">REQUIRED</span> | Matching [a-z]{2}-[A-Z]{2} |
| `currency` <br><span class="required">REQUIRED</span> | Currency code |
| `checkin_date` <br><span class="required">REQUIRED</span> | YYYY-MM-DD |
| `checkout_date` <br><span class="required">REQUIRED</span> | YYYY-MM-DD |
| `rooms` <br><span class="required">REQUIRED</span> | Number of rooms<br>default: 1 |
| `adults` <br><span class="required">REQUIRED</span> | Number of adults<br>default: 2 |
| `apikey` <br><span class="required">REQUIRED</span> | This parameter is required to be on every single request any client does |
| `images` <br><span class="optional">OPTIONAL</span> | Maximum number of images to retrieve for each hotel<br>between 1-30, default: 1 |
| `image_resolution` <br><span class="optional">OPTIONAL</span> | Resolution options<br>high or low, default: high |
| `image_type` <br><span class="optional">OPTIONAL</span> | The format of the images<br>thumbnail or gallery or dynamic |
| `boost_official_partners` <br><span class="optional">OPTIONAL</span> | Indicates whether prices from official partners must be shown in the first place [1] or not [0]<br>default: 0 |
| `partners_per_hotel` <br><span class="optional">OPTIONAL</span> | Maximum numbers of partners to retrieve per each hotel. Note that 0 means all the available partners<br>default: 3 |
| `enhanced` <br><span class="optional">OPTIONAL</span> | This parameter allows you to add additional content to the default response. The available options are:<br>location: Returns the higher level entities according to the search entity.<br>translations: Returns a dictionary with all literals and their corresponding translations using the request locale. |
| `entity_id` <br><span class="optional">OPTIONAL</span> | This field should be present when this endpoint has been called when the user has already looked for prices in an upper entity containing the hotel in order to reuse the cached prices.<br>For example: A user searches for prices in Paris (the service stores Paris prices). And then, the user opens a hotel details page. In this case, the request to the service must have the entity_id param fulfilled with the Paris entity_id in order to reuse the prices.|
| `index` <br><span class="optional">OPTIONAL</span> | Mark the times of the same requests sent to bellboy, start from 1, default: 0 |
| `t_version` <br><span class="optional">OPTIONAL</span> | (B2B partner needn't set the value) Used for ABTesting, default is '' |
| `app_name` <br><span class="optional">OPTIONAL</span> | (B2B partner needn't set the value) This parameter allows you to set the app name, default is '' |
| `appVersion` <br><span class="optional">OPTIONAL</span> | (B2B partner needn't set the value) This parameter allows you to set the app version, default is '' |
| `search_id` <br><span class="optional">OPTIONAL</span> | (B2B partner needn't set the value) Elasticsearch ID, the value can be got from search response or first request response, default is '' |
| `cug_segments` <br><span class="optional">OPTIONAL</span> | (B2B partner needn't set the value) Only v3 supports, it allows you to add special cug segments for user. Options are:<br>mobile, logged_in, business, apps, flight_booked |
| `ignore_cache` <br><span class="optional">OPTIONAL</span> | (B2B partner needn't set the value) This parameter allows you to bypass Elasticsearch and Redis cache. Options are:<br>0: use cache, 1: bypass cache, default: 0 |

### Response

> Example response:

```json
{
    "meta": {
        "completion_percentage": 100,
        "search_id": "ca7a935824954024c5228394530677d66ecb7d5b24973a4d8afda9b911c4fb0f",
        "status": "COMPLETED",
        "offers": 14,
        "request_id": "39bb7709-2707-4ad5-8b74-7193810224fe"
    },
    "translations": {
        "CUG_create_account_to_unlock_deals_msg": "Créez un compte pour avoir accès à des offres exclusives",
        "CUG_deal": "OFFRE",
        ...
    },
    "results": {
        "partners": [
            {
                "is_dbook": false,
                "website_id": "h_98",
                "is_official": true,
                "name": "Travelanium",
                "logo": "www.skyscanner.fr/images/websites/220x80/h_98.png",
                "partner_type": "CRS"
            },
            ...
        ],
        "location": [
            {
                "entity_type": "District",
                "name": "Estación de Gran Vía",
                "entity_id": "27562647"
            },
            ...
        ],
        "hotel": {
            "chain_id": "90718893",
            "checkin_time": "14:00",
            "district": "27562647",
            "name_en": "Hotel Madrid Gran Via 25 Managed By Melia",
            "description": "https://dmf5e20brgddt.cloudfront.net/547b_2533_fr-FR_b2b",
            "reviews_count": 3011,
            "group_name": [
                "Meliá"
            ],
            "dbook_partners": [],
            "images": [
                {
                    "thumbnail": "https://d2xf5gjipzd8cd.cloudfront.net/available/353312696/mt.jpg",
                    "provider": "h_ct",
                    "category": "Bedroom",
                    "dynamic": "https://d2xf5gjipzd8cd.cloudfront.net/available/353312696/353312696_WxH.jpg",
                    "gallery": "https://d2xf5gjipzd8cd.cloudfront.net/available/353312696/mca.jpg"
                },
                ...
            ],
            "property_type": "Hotel",
            "offers": [
                {
                    "closed_user_groups": null,
                    "available": null,
                    "room_type": [
                        "double_room"
                    ],
                    "deeplink": "www.skyscanner.fr/hotel_deeplink/4.0/FR/fr-FR/EUR/h_me/46942019/2019-06-18/2019-06-19/hotel/hotel/hotels?guests=1&rooms=1&legacy_provider_id=1751086970&request_id=39bb7709-2707-4ad5-8b74-7193810224fe&q_datetime_utc=2019-06-12T12%3A02%3A15&appName=mobileweb&appVersion=2.0&ticket_price=166&deeplink_data=eyJ1cmwiOiAiaHR0cHM6Ly9tbS5tZWxpYS5jb20vZHluY2xpY2svbWVsaWEtY29tLz9ldGYtcHVibGlzaGVyPXNreXNjYW5uZXImZXRmLW5hbWU9bWV0YXNlYXJjaF9za3lzY2FubmVyX0ZSLXNreXNjYW5uZXImZXRmLXByZHJlZj0yODE5JmVzZWctbmFtZT1OTyZlc2VnLWl0ZW09Tk8mZXRmLW1lZGlhcGxhbj1GUi1JbmZsdWVuY2VyJmV1cmw9aHR0cDovL3d3dy5tZWxpYS5jb20vblJlc2VydmF0aW9ucy9qc3AvQ19SYXRlcy5qc3A%2FaWRQYXJ0bmVyPVNLWVNDQU5ORVJfRlImY29kaWdvSG90ZWw9MjgxOSZub2NoZXM9MSZpZExhbmc9ZnImZGlhPTE4Jm1lcz0wNiZhbmlvPTIwMTkmaGFiaXRhY2lvbmVzPTEmYWR1bHRzUm9vbTE9MSZjaGlsZHJlblJvb20xPTAmSWRQcm09U0tZU0NBTk5FUiZkaXZpc2FQcmVzZW50YWNpb249JnV0bV9zb3VyY2U9c2t5c2Nhbm5lciZ1dG1fbWVkaXVtPW1ldGFzZWFyY2gmdXRtX2NhbXBhaWduPXNreXNjYW5uZXJfRlImdXRtX2NvbnRlbnQ9MjgxOSZtYXJrZXQ9RlIiLCAiZmllbGRzIjogeyJzaWduYXR1cmUiOiAiYjBkZTZkNTFjMzk3YWRiZGEwMjlhOThhMGMxYWU4ZTcifX0%3D&max_price=205.0&channel=website",
                    "dbook_link": null,
                    "partner_id": "h_me",
                    "price": 166,
                    "is_official": true,
                    "price_gbp": 148,
                    "meal_plan": "breakfast_not_included",
                    "strike_through": null,
                    "cancellation": "non_refundable",
                    "cancellation_text": "Si vous annulez ou modifiez Annuler ou Modifier ou vous ne vous présentez pas 100 PCT vous sera débité en frais d'annulation"
                },
                ...
            ],
            "total_rooms": 175,
            "name": "Hotel Madrid Gran Vía 25, Managed by Meliá",
            "stars": "3",
            "amenities": [
                "Bar",
                "FrontDesk24hService",
                "Restaurant",
                ...
            ],
            "chain": "Meliã",
            "address": {
                "street_address": "Gran Via 25",
                "adm1": "Communauté de Madrid",
                "postcode": "28013",
                "district": "Estación de Gran Vía",
                "city": "Madrid",
                "nation": "Espagne"
            },
            "city": "27544850",
            "group_id": [
                "90719217"
            ],
            "checkout_time": "12:00",
            "hotel_id": "46942019",
            "official_website": "h_me",
            "rich_media": null,
            "rating": {
                "value": 8.1,
                "desc": "rating_very_good"
            },
            "reviews": {
                "badges": [
                    {
                        "badge_type": "hotel_type",
                        "text": "Très bon hôtel en ville",
                        "subtext": "Top 11% en ville"
                    },
                    ...
                ],
                "categories": [
                    {
                        "score": 95,
                        "entries": [
                            "Très bien situé",
                            "Emplacement parfait",
                            "Situation géographique excellente",
                            "Bonne situation"
                        ],
                        "id": "14",
                        "name": "Site"
                    },
                    ...
                ],
                "guest_types": [
                    {
                        "perc": 62,
                        "value": "couple",
                        "score": 86
                    },
                    ...
                ],
                "count": 3011,
                "summary": "Très bon hôtel pour une escapade citadine. Parfait pour le tourisme et proche des boutiques."
            },
            "coordinates": [
                -3.70228,
                40.42003
            ],
            "policies": "https://dmf5e20brgddt.cloudfront.net/a27b_2533_fr-FR_policies_b2b"
        },
        "price_includes": [
            "vat",
            "other_taxes"
        ]
    }
}
```

*RESPONSE PARAMETERS*

| Element | Detail |
| ------- | ------ |
| `meta` | Contains metadata regarding the search cycle such as it's status |
| `results` | An object containing the hotel and the enhancers if requested |
| `translations` | Only with the `translations` enhanced. Dictionary with all literals that can be translated |


## Hotels Prices

### Request

Given multiple hotels (maximum 50), this endpoint will give back the hotels with all the information and live prices.

*API endpoint*

`GET /v2/prices/hotel/{hotel_ids}`


```shell
GET "https://www.skyscanner.net/g/hbe-bellboy/v2/prices/hotel/{hotel_ids}
  ?market={market}&locale={locale}&checkin_date={checkin_date}&checkout_date={checkout_date}
  &currency={currency}&adults={adults}&rooms={rooms}&images={images}&image_resolution={resolution}
  &image_type={type}&boost_official_partners={boost}&partners_per_hotel={num_partners}"
```

*TRY IT OUT*

[![Run in Postman](https://run.pstmn.io/button.svg)](https://app.getpostman.com/run-collection/235d1617d92d7467ed1b)

*HEADER VALUES*

| Header | Value |
| --- | --- |
| `apikey` <br><span class="required">REQUIRED</span> | This header is required to be on every single request any client does (it could also be accepted via query parameter) |
| `x-user-agent` <br><span class="required">REQUIRED</span> | Indicates which is the device and the platform related to the client. The format for that header is `device;B2B`, where:<br>Device is:<br>`T` for tablet<br>`D` for desktop<br>`M` for mobile<br>`N` if you are not able to detect the device type |

*URI PARAMETERS*

| Parameter | Description |
| --------- | ------- |
| `hotel_ids` <br><span class="required">REQUIRED</span> | Hotels to search prices for, using ',' to join the hotels|
| `version` <br><span class="required">REQUIRED</span> | API version |

*QUERY PARAMETERS*

| Parameter | Description |
| --------- | ------- |
| `market` <br><span class="required">REQUIRED</span> | Matching [A-Z]{2} |
| `locale` <br><span class="required">REQUIRED</span> | Matching [a-z]{2}-[A-Z]{2} |
| `currency` <br><span class="required">REQUIRED</span> | Currency code |
| `checkin_date` <br><span class="required">REQUIRED</span> | YYYY-MM-DD |
| `checkout_date` <br><span class="required">REQUIRED</span> | YYYY-MM-DD |
| `rooms` <br><span class="required">REQUIRED</span> | Number of rooms<br>default: 1 |
| `adults` <br><span class="required">REQUIRED</span> | Number of adults<br>default: 2 |
| `apikey` <br><span class="required">REQUIRED</span> | This parameter is required to be on every single request any client does |
| `images` <br><span class="optional">OPTIONAL</span> | Maximum number of images to retrieve per each hotel<br>between 1-30, default: 1 |
| `image_resolution` <br><span class="optional">OPTIONAL</span> | Resolution options<br>high or low, default: high |
| `image_type` <br><span class="optional">OPTIONAL</span> | The format of the images<br>thumbnail or gallery or dynamic |
| `boost_official_partners` <br><span class="optional">OPTIONAL</span> | Indicates whether prices from official partners must be shown in the first place [1] or not [0]<br>default: 0 |
| `partners_per_hotel` <br><span class="optional">OPTIONAL</span> | Maximum numbers of partners to retrieve per each hotel. Note that 0 means all the available partners<br>default: 3 |
| `enhanced` <br><span class="optional">OPTIONAL</span> | This parameter allows you to add additional content to the default response. The available options are:<br>location: Returns the higher level entities according to the search entity.<br>translations: Returns a dictionary with all literals and their corresponding translations using the request locale. |
| `app_name` <br><span class="optional">OPTIONAL</span> | (B2B partner needn't set the value) This parameter allows you to set the app name, default is '' |
| `appVersion` <br><span class="optional">OPTIONAL</span> | (B2B partner needn't set the value) This parameter allows you to set the app version, default is '' |

### Response

> Example response:

```json
{
    "results": {
        "partners": [
            {
                "logo": "www.skyscanner.net/images/websites/220x80/d_ct.png",
                "name": "Trip.com",
                "is_official": false,
                "partner_type": "OTA",
                "website_id": "d_ct",
                "is_dbook": true
            },
            ...
        ],
        "hotels": [
            {
                "group_name": [
                    "Meliá"
                ],
                "amenities": [
                    "Laundry",
                    "Parking",
                    ...
                ],
                "name": "Hotel Madrid Gran Via 25 Managed By Melia",
                "images": [
                    {
                        "provider": "h_ct",
                        "dynamic": "https://d2xf5gjipzd8cd.cloudfront.net/available/353312696/353312696_WxH.jpg",
                        "thumbnail": "https://d2xf5gjipzd8cd.cloudfront.net/available/353312696/mt.jpg",
                        "category": "Bedroom",
                        "gallery": "https://d2xf5gjipzd8cd.cloudfront.net/available/353312696/mca.jpg"
                    },
                    ...
                ],
                "rich_media": null,
                "location": [
                    {
                        "entity_id": "27562647",
                        "name": "Gran Vía",
                        "entity_type": "District"
                    },
                    ...
                ],
                "rating": {
                    "desc": "rating_very_good",
                    "value": 8.1
                },
                "offers": [
                    {
                        "cancellation_text": null,
                        "meal_plan": null,
                        "partner_id": "d_ct",
                        "deeplink": "www.skyscanner.net/None&max_price=199.0&channel=website",
                        "available": null,
                        "is_official": false,
                        "room_type": [
                            "generic_room"
                        ],
                        "price": 128,
                        "price_gbp": 128,
                        "strike_through": null,
                        "closed_user_groups": null,
                        "cancellation": null,
                        "dbook_link": "www.skyscanner.net/hotels/book/46942019/d_ct?adults=1&rooms=1&checkin=2019-06-18&checkout=2019-06-19&requestId=6431b3f0-09b8-4d8b-9808-0bc551f9725c&priceCurrency=GBP&appId=hate-squad&priceAmount=128"
                    },
                    ...
                ],
                "city": "27544850",
                "reviews_count": 3022,
                "reviews": {
                    "categories": [
                        {
                            "entries": [
                                "Great location",
                                "Fantastic position",
                                "Wonderfully located",
                                "Perfect for shopping"
                            ],
                            "name": "Location",
                            "score": 95,
                            "id": "14"
                        },
                        ...
                    ],
                    "guest_types": [
                        {
                            "perc": 65,
                            "value": "couple",
                            "score": 79
                        },
                        ...
                    ],
                    "count": 3022,
                    "badges": [
                        {
                            "badge_type": "hotel_type",
                            "subtext": "Top 11% in city",
                            "text": "Great city hotel"
                        },
                        ...
                    ],
                    "summary": "Very good city hotel. Good for sightseeing and located near shopping areas."
                },
                "policies": "https://dmf5e20brgddt.cloudfront.net/7657_2533_en-GB_policies_b2b",
                "hotel_id": "46942019",
                "chain_id": "90718893",
                "chain": "Meliã",
                "total_rooms": 175,
                "name_en": "Hotel Madrid Gran Via 25 Managed By Melia",
                "checkin_time": "14:00",
                "group_id": [
                    "90719217"
                ],
                "property_type": "Hotel",
                "checkout_time": "12:00",
                "description": "https://dmf5e20brgddt.cloudfront.net/e289_2533_en-GB_b2b",
                "district": "27562647",
                "stars": "3",
                "coordinates": [
                    -3.70228,
                    40.42003
                ],
                "address": {
                    "nation": "Spain",
                    "adm1": "Community of Madrid",
                    "city": "Madrid",
                    "district": "Gran Vía",
                    "street_address": "Gran Via 25",
                    "postcode": "28013"
                }
            },
            ...
        ],
        "price_includes": [
            "vat",
            "other_taxes"
        ]
    },
    "translations": {
        "CUG_create_account_to_unlock_deals_msg": "Create an account to unlock exclusive deals",
        "CUG_deal": "DEAL",
        ...
    },
    "meta": {
        "status": "COMPLETED",
        "completion_percentage": 100,
        "search_id": "dd30d77810d91ae4ca062378c31d09c9658e7fec85330fcd6b515b55b6c73d4b",
        "offers": 62,
        "request_id": "6431b3f0-09b8-4d8b-9808-0bc551f9725c"
    }
}
```

*RESPONSE PARAMETERS*

| Element | Detail |
| ------- | ------ |
| `meta` | Contains metadata regarding the search cycle such as it's status |
| `results` | An object containing the hotel and the enhancers if requested |
| `translations` | Only with the `translations` enhanced. Dictionary with all literals that can be translated |
