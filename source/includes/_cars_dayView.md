## Carhire Day View supported query parameters Schema

```
/cars/day-view
```

A schema definition for the carhire day-view microsite supported query parameters

| Abstract            | Extensible | Status       | Identifiable | Custom Properties | Additional Properties | Defined In                   |
| ------------------- | ---------- | ------------ | ------------ | ----------------- | --------------------- | ---------------------------- |
| Can be instantiated | No         | Experimental | No           | Forbidden         | Permitted             |  |

## Carhire Day View supported query parameters Properties

| Property                      | Type      | Required     | Nullable | Defined by                                                |
| ----------------------------- | --------- | ------------ | -------- | --------------------------------------------------------- |
| [currency](#currency)         | `string`  | Optional     | No       | Carhire Day View supported query parameters (this schema) |
| [driverAge](#driverage)       | `integer` | **Required** | No       | Carhire Day View supported query parameters (this schema) |
| [dropoffPlace](#dropoffplace) | `string`  | Optional     | No       | Carhire Day View supported query parameters (this schema) |
| [dropoffTime](#dropofftime)   | `string`  | **Required** | No       | Carhire Day View supported query parameters (this schema) |
| [locale](#locale)             | `string`  | Optional     | No       | Carhire Day View supported query parameters (this schema) |
| [market](#market)             | `string`  | Optional     | No       | Carhire Day View supported query parameters (this schema) |
| [pickupPlace](#pickupplace)   | `string`  | **Required** | No       | Carhire Day View supported query parameters (this schema) |
| [pickupTime](#pickuptime)     | `string`  | **Required** | No       | Carhire Day View supported query parameters (this schema) |
| `*`                           | any       | Additional   | Yes      | this schema _allows_ additional properties                |

### currency

The desired currency for the page

`currency`

- is optional
- type: `string`
- defined in this schema

#### currency Type

`string`

### driverAge

Driver age between 18 and 99

`driverAge`

- is **required**
- type: `integer`
- defined in this schema

#### driverAge Type

`integer`

### dropoffPlace

Pick up IATA code / hotel or city entity id

`dropoffPlace`

- is optional
- type: `string`
- defined in this schema

#### dropoffPlace Type

`string`

### dropoffTime

Drop Off Datetime in ISO 8601 standard. I.e YYYY-MM-DDTHH:MM

`dropoffTime`

- is **required**
- type: `string`
- defined in this schema

#### dropoffTime Type

`string`

### locale

The desired locale for the page

`locale`

- is optional
- type: `string`
- defined in this schema

#### locale Type

`string`

### market

The market of the user

`market`

- is optional
- type: `string`
- defined in this schema

#### market Type

`string`

### pickupPlace

Pick up IATA code / hotel or city entity id

`pickupPlace`

- is **required**
- type: `string`
- defined in this schema

#### pickupPlace Type

`string`

### pickupTime

Pick Up Datetime in ISO 8601 standard. I.e YYYY-MM-DDTHH:MM

`pickupTime`

- is **required**
- type: `string`
- defined in this schema

#### pickupTime Type

`string`
