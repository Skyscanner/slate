## Carhire Home page supported parameters Schema

```
/cars/home
```

A schema definition for the carhire home page microsite supported parameters

| Abstract            | Extensible | Status       | Identifiable | Custom Properties | Additional Properties | Defined In                     |
| ------------------- | ---------- | ------------ | ------------ | ----------------- | --------------------- | ------------------------------ |
| Can be instantiated | No         | Experimental | No           | Forbidden         | Permitted             | [carsHome.json](carsHome.json) |

## Carhire Home page supported parameters Properties

| Property              | Type     | Required   | Nullable | Defined by                                           |
| --------------------- | -------- | ---------- | -------- | ---------------------------------------------------- |
| [currency](#currency) | `string` | Optional   | No       | Carhire Home page supported parameters (this schema) |
| [locale](#locale)     | `string` | Optional   | No       | Carhire Home page supported parameters (this schema) |
| [market](#market)     | `string` | Optional   | No       | Carhire Home page supported parameters (this schema) |
| `*`                   | any      | Additional | Yes      | this schema _allows_ additional properties           |

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
