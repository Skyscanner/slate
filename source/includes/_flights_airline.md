## Flights Airline supported parameters Schema

```
/flights/flights-airline
```

A schema definition for the flights airline microsite supported parameters

| Abstract            | Extensible | Status       | Identifiable | Custom Properties | Additional Properties | Defined In                                 |
| ------------------- | ---------- | ------------ | ------------ | ----------------- | --------------------- | ------------------------------------------ |
| Can be instantiated | No         | Experimental | No           | Forbidden         | Permitted             |  |

## Flights Airline supported parameters Properties

| Property                    | Type     | Required     | Nullable | Defined by                                         |
| --------------------------- | -------- | ------------ | -------- | -------------------------------------------------- |
| [airlineCode](#airlinecode) | `string` | **Required** | No       | Flights Airline supported parameters (this schema) |
| [airlineName](#airlinename) | `string` | Optional     | No       | Flights Airline supported parameters (this schema) |
| [currency](#currency)       | `string` | Optional     | No       | Flights Airline supported parameters (this schema) |
| [locale](#locale)           | `string` | Optional     | No       | Flights Airline supported parameters (this schema) |
| [market](#market)           | `string` | Optional     | No       | Flights Airline supported parameters (this schema) |
| `*`                         | any      | Additional   | Yes      | this schema _allows_ additional properties         |

### airlineCode

The airline code.

`airlineCode`

- is **required**
- type: `string`
- defined in this schema

#### airlineCode Type

`string`

### airlineName

The airline name.

`airlineName`

- is optional
- type: `string`
- defined in this schema

#### airlineName Type

`string`

### currency

The desired currency for the page. Examples: GBP, EUR, USD

`currency`

- is optional
- type: `string`
- defined in this schema

#### currency Type

`string`

### locale

The desired locale for the page. Examples: es-ES, en-GB, ru-RU

`locale`

- is optional
- type: `string`
- defined in this schema

#### locale Type

`string`

### market

The market of the user. Examples: UK, US, ES

`market`

- is optional
- type: `string`
- defined in this schema

#### market Type

`string`
