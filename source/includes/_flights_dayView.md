## Flights Day View supported parameters Schema

```
/flights/day-view
```

A schema definition for the flights day-view microsite supported parameters

| Abstract            | Extensible | Status       | Identifiable | Custom Properties | Additional Properties | Defined In                   |
| ------------------- | ---------- | ------------ | ------------ | ----------------- | --------------------- | ---------------------------- |
| Can be instantiated | No         | Experimental | No           | Forbidden         | Permitted             |  |

## Flights Day View supported parameters Properties

For more details, please see our [Examples](#examples) 

| Property                                            | Type       | Required     | Nullable | Default                                    | Defined by                                          |
| --------------------------------------------------- | ---------- | ------------ | -------- | ------------------------------------------ | --------------------------------------------------- |
| [adultsv2](#adultsv2)                               | `integer`  | **Required** | No       | `1`                                        | Flights Day View supported parameters (this schema) |
| [airlines](#airlines)                               | `string`   | Optional     | No       |                                            | Flights Day View supported parameters (this schema) |
| [alliances](#alliances)                             | `string`   | Optional     | No       |                                            | Flights Day View supported parameters (this schema) |
| [alternativedestinations](#alternativedestinations) | `string[]` | Optional     | No       |                                            | Flights Day View supported parameters (this schema) |
| [alternativeorigins](#alternativeorigins)           | `string[]` | Optional     | No       |                                            | Flights Day View supported parameters (this schema) |
| [cabinclass](#cabinclass)                           | `enum`     | **Required** | No       | `"economy"`                                | Flights Day View supported parameters (this schema) |
| [childrenv2](#childrenv2)                           | `string`   | Optional     | No       |                                            | Flights Day View supported parameters (this schema) |
| [currency](#currency)                               | `string`   | Optional     | No       |                                            | Flights Day View supported parameters (this schema) |
| [departure-times](#departure-times)                 | `string`   | Optional     | No       |                                            | Flights Day View supported parameters (this schema) |
| [destination](#destination)                         | `string`   | **Required** | No       |                                            | Flights Day View supported parameters (this schema) |
| [duration](#duration)                               | `integer`  | Optional     | No       |                                            | Flights Day View supported parameters (this schema) |
| [inboundDate](#inbounddate)                         | `string`   | Optional     | No       |                                            | Flights Day View supported parameters (this schema) |
| [inboundaltsenabled](#inboundaltsenabled)           | `boolean`  | Optional     | No       |                                            | Flights Day View supported parameters (this schema) |
| [infants](#infants)                                 | `integer`  | Optional     | No       |                                            | Flights Day View supported parameters (this schema) |
| [locale](#locale)                                   | `string`   | Optional     | No       |                                            | Flights Day View supported parameters (this schema) |
| [market](#market)                                   | `string`   | Optional     | No       |                                            | Flights Day View supported parameters (this schema) |
| [origin](#origin)                                   | `string`   | **Required** | No       |                                            | Flights Day View supported parameters (this schema) |
| [outboundDate](#outbounddate)                       | `string`   | **Required** | No       |                                            | Flights Day View supported parameters (this schema) |
| [outboundaltsenabled](#outboundaltsenabled)         | `boolean`  | Optional     | No       |                                            | Flights Day View supported parameters (this schema) |
| [preferDirects](#preferdirects)                     | `boolean`  | Optional     | No       |                                            | Flights Day View supported parameters (this schema) |
| [showDirectDays](#showdirectdays)                   | `boolean`  | Optional     | No       | `true`                                     | Flights Day View supported parameters (this schema) |
| [rtn](#rtn)                                         | `enum`     | Optional     | No       |                                            | Flights Day View supported parameters (this schema) |
| [sortby](#sortby)                                   | `enum`     | Optional     | No       |                                            | Flights Day View supported parameters (this schema) |
| `*`                                                 | any        | Additional   | Yes      | this schema _allows_ additional properties |

### adultsv2

Number of adult passengers. Adults have to be 16 years old or older.

`adultsv2`

- is **required**
- type: `integer`
- default: `1`
- defined in this schema

#### adultsv2 Type

`integer`

- minimum value: `1`

### airlines

List of comma separated IATA carrier codes to be passed to the dayview filters. For example: &airlines=AA,KL,LH. To
unselect airline from the filters, the code must be specified with exclamation mark. For example: &airlines=AA,!KL,!LH  
You can search for IATA airline codes at the IATA website [here](https://www.iata.org/publications/pages/code-search.aspx)

`airlines`

- is optional
- type: `string`
- defined in this schema

#### airlines Type

`string`

### alliances

Comma separated list of alliance names passed to the dayview filters. For example: &alliances=oneworld,Star%20Alliance

`alliances`

- is optional
- type: `string`
- defined in this schema

#### alliances Type

`string`

### alternativedestinations

An array of location codes which will be used as alternative destinations

`alternativedestinations`

- is optional
- type: `string[]`
- defined in this schema

#### alternativedestinations Type

Array type: `string[]`

All items must be of the type: `string`

### alternativeorigins

An array of location codes which will be used as alternative origins

`alternativeorigins`

- is optional
- type: `string[]`
- defined in this schema

#### alternativeorigins Type

Array type: `string[]`

All items must be of the type: `string`

### cabinclass

Cabin class for the flight, possible values are: economy, premiumeconomy, business and first

`cabinclass`

- is **required**
- type: `enum`
- default: `"economy"`
- defined in this schema

The value of this property **must** be equal to one of the [known values below](#cabinclass-known-values).

#### cabinclass Known Values

| Value            | Description |
| ---------------- | ----------- |
| `economy`        |             |
| `premiumeconomy` |             |
| `business`       |             |
| `first`          |             |

### childrenv2

Number of child passengers. The value must be in the format integer|integer.. where each number is the age of the child
passenger

`childrenv2`

- is optional
- type: `string`
- defined in this schema

#### childrenv2 Type

`string`

### currency

The desired currency for the page. Examples: GBP, EUR, USD  
Please try to avoid using `locale`, `market` and `currency`, as these values will be governed by Skyscanner market detection logic on the Skyscanner site. If you believe you need to use these, please discuss with your account manager.

The desired currency for the page. Examples: GBP, EUR, USD

`currency`

- is optional
- type: `string`
- defined in this schema

#### currency Type

`string`

### departure-times

Sets the dayview departure time filters in minutes. For example: &departure-times=00-90,30-990 (first leg departs
between 00 and 1:30 and second leg departs between 00:30 and 16:30).

`departure-times`

- is optional
- type: `string`
- defined in this schema

#### departure-times Type

`string`

### destination

Location code for the destination

`destination`

- is **required**
- type: `string`
- defined in this schema

#### destination Type

`string`

### duration

Sets the dayview duration filters in minutes. For example: &duration=1320 (22 hours)

`duration`

- is optional
- type: `integer`
- defined in this schema

#### duration Type

`integer`

### inboundDate

Inbound date in the format YYYY-MM-DD

`inboundDate`

- is optional
- type: `string`
- defined in this schema

#### inboundDate Type

`string`

### inboundaltsenabled

Including nearby airports as an inbound place

`inboundaltsenabled`

- is optional
- type: `boolean`
- defined in this schema

#### inboundaltsenabled Type

`boolean`

### infants

Number of infant passengers. An infant is 1 year old or younger.

`infants`

- is optional
- type: `integer`
- defined in this schema

#### infants Type

`integer`

### locale

The desired locale for the page. Examples: es-ES, en-GB, ru-RU  
Please try to avoid using `locale`, `market` and `currency`, as these values will be governed by Skyscanner market detection logic on the Skyscanner site. If you believe you need to use these, please discuss with your account manager.

`locale`

- is optional
- type: `string`
- defined in this schema

#### locale Type

`string`

### market

The market of the user. Examples: UK, US, ES
Please try to avoid using `locale`, `market` and `currency`, as these values will be governed by Skyscanner market detection logic on the Skyscanner site. If you believe you need to use these, please discuss with your account manager.

`market`

- is optional
- type: `string`
- defined in this schema

#### market Type

`string`

### origin

Location code for the origin

`origin`

- is **required**
- type: `string`
- defined in this schema

#### origin Type

`string`

### outboundDate

Outbound date in the format YYYY-MM-DD

`outboundDate`

- is **required**
- type: `string`
- defined in this schema

#### outboundDate Type

`string`

### outboundaltsenabled

Including nearby airports as an outbound place

`outboundaltsenabled`

- is optional
- type: `boolean`
- defined in this schema

#### outboundaltsenabled Type

`boolean`

### preferDirects

Will search only for direct flights if the value is true

`preferDirects`

- is optional
- type: `boolean`
- defined in this schema

#### preferDirects Type

`boolean`

### showDirectDays

Controls the visibility of the day view screen, which presents the user with options for different dates with direct flights, when there are no direct flights for the currently selected dates.

`showDirectDays`

- is optional
- type: `boolean`
- defined in this schema

#### showDirectDays Type

`boolean`

### rtn

Trip type: 0 if oneway or 1 if return or multicity trip

`rtn`

- is optional
- type: `enum`
- defined in this schema

The value of this property **must** be equal to one of the [known values below](#rtn-known-values).

#### rtn Known Values

| Value | Description |
| ----- | ----------- |
| `0`   |             |
| `1`   |             |

### sortby

Sets the sorting order for the results. Possible values are: best, cheapest and fastest.

`sortby`

- is optional
- type: `enum`
- defined in this schema

The value of this property **must** be equal to one of the [known values below](#sortby-known-values).

#### sortby Known Values

| Value      | Description |
| ---------- | ----------- |
| `best`     |             |
| `cheapest` |             |
| `fastest`  |             |
