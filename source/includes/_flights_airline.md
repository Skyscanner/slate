## Flights Airline contents Schema

```
/flights/flights-airline
```

A schema definition for the flights airline microsite supported query parameters

| Abstract            | Extensible | Status       | Identifiable | Custom Properties | Additional Properties | Defined In                                 |
| ------------------- | ---------- | ------------ | ------------ | ----------------- | --------------------- | ------------------------------------------ |
| Can be instantiated | No         | Experimental | No           | Forbidden         | Permitted             |  |

## Flights Airline contents Properties

| Property                    | Type     | Required     | Nullable | Defined by                                 |
| --------------------------- | -------- | ------------ | -------- | ------------------------------------------ |
| [airlineCode](#airlinecode) | `string` | **Required** | No       | Flights Airline contents (this schema)     |
| [airlineName](#airlinename) | `string` | Optional     | No       | Flights Airline contents (this schema)     |
| [currency](#currency)       | `string` | Optional     | No       | Flights Airline contents (this schema)     |
| [locale](#locale)           | `string` | Optional     | No       | Flights Airline contents (this schema)     |
| [market](#market)           | `string` | Optional     | No       | Flights Airline contents (this schema)     |
| `*`                         | any      | Additional   | Yes      | this schema _allows_ additional properties |

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

The desired currency for the page.

`currency`

- is optional
- type: `string`
- defined in this schema

#### currency Type

`string`

### locale

The desired locale for the page.

`locale`

- is optional
- type: `string`
- defined in this schema

#### locale Type

`string`

### market

The market of the user.

`market`

- is optional
- type: `string`
- defined in this schema

#### market Type

`string`
