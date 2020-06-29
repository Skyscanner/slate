## Flights Airline supported parameters Schema

```
/flights/flights-airline
```

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
Please try to avoid using `locale`, `market` and `currency`, as these values will be governed by Skyscanner market detection logic on the Skyscanner site. If you believe you need to use these, please discuss with your account manager.

`currency`

- is optional
- type: `string`
- defined in this schema

#### currency Type

`string`

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
