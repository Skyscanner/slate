## Carhire Home page supported query parameters Schema

```
/cars/home
```

A schema definition for the carhire home page microsite supported query parameters

| Abstract            | Extensible | Status       | Identifiable | Custom Properties | Additional Properties | Defined In                     |
| ------------------- | ---------- | ------------ | ------------ | ----------------- | --------------------- | ------------------------------ |
| Can be instantiated | No         | Experimental | No           | Forbidden         | Permitted             |                                |

## Carhire Home page supported query parameters Properties

| Property              | Type     | Required   | Nullable | Defined by                                                 |
| --------------------- | -------- | ---------- | -------- | ---------------------------------------------------------- |
| [currency](#currency) | `string` | Optional   | No       | Carhire Home page supported query parameters (this schema) |
| [locale](#locale)     | `string` | Optional   | No       | Carhire Home page supported query parameters (this schema) |
| [market](#market)     | `string` | Optional   | No       | Carhire Home page supported query parameters (this schema) |
| `*`                   | any      | Additional | Yes      | this schema _allows_ additional properties                 |

### currency

The desired currency for the carhire search results

`currency`

- is optional
- type: `string`
- defined in this schema

#### currency Type

`string`

### locale

The desired locale for the carhire search results

`locale`

- is optional
- type: `string`
- defined in this schema

#### locale Type

`string`

### market

The market for which the carhire search will be performed.

`market`

- is optional
- type: `string`
- defined in this schema

#### market Type

`string`
