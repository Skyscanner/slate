## Hotels Home View supported query parameters Schema

```
/hotels/home-view
```

A schema definition for the hotels home-view microsite supported query parameters.

| Abstract            | Extensible | Status       | Identifiable | Custom Properties | Additional Properties | Defined In                     |
| ------------------- | ---------- | ------------ | ------------ | ----------------- | --------------------- | ------------------------------ |
| Can be instantiated | No         | Experimental | No           | Forbidden         | Permitted             |  |

## Hotels Home View supported query parameters Properties

| Property                                      | Type      | Required   | Nullable | Defined by                                                |
| --------------------------------------------- | --------- | ---------- | -------- | --------------------------------------------------------- |
| [adults](#adults)                             | `integer` | Optional   | No       | Hotels Home View supported query parameters (this schema) |
| [checkin](#checkin)                           | `string`  | Optional   | No       | Hotels Home View supported query parameters (this schema) |
| [checkout](#checkout)                         | `string`  | Optional   | No       | Hotels Home View supported query parameters (this schema) |
| [currency](#currency)                         | `string`  | Optional   | No       | Hotels Home View supported query parameters (this schema) |
| [locale](#locale)                             | `string`  | Optional   | No       | Hotels Home View supported query parameters (this schema) |
| [market](#market)                             | `string`  | Optional   | No       | Hotels Home View supported query parameters (this schema) |
| [rooms](#rooms)                               | `integer` | Optional   | No       | Hotels Home View supported query parameters (this schema) |
| [skyscanner_node_code](#skyscanner_node_code) | `string`  | Optional   | No       | Hotels Home View supported query parameters (this schema) |
| `*`                                           | any       | Additional | Yes      | this schema _allows_ additional properties                |

### adults

Number of adults. Adults number should be greater than or equal to the rooms number.

`adults`

- is optional
- type: `integer`
- defined in this schema

#### adults Type

`integer`

### checkin

Checkin date in the formats: `YYYY-MM-DD`, `YYMMDD` or `YYYYMMDD`.

`checkin`

- is optional
- type: `string`
- defined in this schema

#### checkin Type

`string`

### checkout

Checkout date in the formats: `YYYY-MM-DD`, `YYMMDD` or `YYYYMMDD`.

`checkout`

- is optional
- type: `string`
- defined in this schema

#### checkout Type

`string`

### currency

The desired currency for the page

`currency`

- is optional
- type: `string`
- defined in this schema

#### currency Type

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

### rooms

Number of rooms. Rooms number should be less than or equal to the adults number.

`rooms`

- is optional
- type: `integer`
- defined in this schema

#### rooms Type

`integer`

### skyscanner_node_code

The IATA code of the destination.

`skyscanner_node_code`

- is optional
- type: `string`
- defined in this schema

#### skyscanner_node_code Type

`string`
