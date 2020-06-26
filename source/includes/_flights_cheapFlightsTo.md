## Cheap Flights To supported parameters Schema

```
/flights/cheap-flights-to
```

A schema definition for the cheap flights to microsite supported parameters

| Abstract            | Extensible | Status       | Identifiable | Custom Properties | Additional Properties | Defined In                                 |
| ------------------- | ---------- | ------------ | ------------ | ----------------- | --------------------- | ------------------------------------------ |
| Can be instantiated | No         | Experimental | No           | Forbidden         | Permitted             | [cheapFlightsTo.json](cheapFlightsTo.json) |

## Cheap Flights To supported parameters Properties

| Property                    | Type     | Required     | Nullable | Defined by                                          |
| --------------------------- | -------- | ------------ | -------- | --------------------------------------------------- |
| [currency](#currency)       | `string` | Optional     | No       | Cheap Flights To supported parameters (this schema) |
| [destination](#destination) | `string` | **Required** | No       | Cheap Flights To supported parameters (this schema) |
| [locale](#locale)           | `string` | Optional     | No       | Cheap Flights To supported parameters (this schema) |
| [market](#market)           | `string` | Optional     | No       | Cheap Flights To supported parameters (this schema) |
| `*`                         | any      | Additional   | Yes      | this schema _allows_ additional properties          |

### currency

The desired currency for the page. Examples: GBP, EUR, USD

`currency`

- is optional
- type: `string`
- defined in this schema

#### currency Type

`string`

### destination

Location code for the destination

`destination`

- is **required**
- type: `string`
- defined in this schema

#### destination Type

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
