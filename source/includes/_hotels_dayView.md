## Hotels Day View supported parameters Schema

```
/hotels/day-view
```

A schema definition for the hotels day-view microsite supported parameters

| Abstract            | Extensible | Status       | Identifiable | Custom Properties | Additional Properties | Defined In                   |
| ------------------- | ---------- | ------------ | ------------ | ----------------- | --------------------- | ---------------------------- |
| Can be instantiated | No         | Experimental | No           | Forbidden         | Permitted             |  |

## Hotels Day View supported parameters Properties

| Property                | Type      | Required     | Nullable | Default                                    | Defined by                                         |
| ----------------------- | --------- | ------------ | -------- | ------------------------------------------ | -------------------------------------------------- |
| [adults](#adults)       | `integer` | Optional     | No       | `2`                                        | Hotels Day View supported parameters (this schema) |
| [checkin](#checkin)     | `string`  | Optional     | No       |                                            | Hotels Day View supported parameters (this schema) |
| [checkout](#checkout)   | `string`  | Optional     | No       |                                            | Hotels Day View supported parameters (this schema) |
| [currency](#currency)   | `string`  | Optional     | No       |                                            | Hotels Day View supported parameters (this schema) |
| [entity_id](#entity_id) | `string`  | **Required** | No       |                                            | Hotels Day View supported parameters (this schema) |
| [locale](#locale)       | `string`  | Optional     | No       |                                            | Hotels Day View supported parameters (this schema) |
| [market](#market)       | `string`  | Optional     | No       |                                            | Hotels Day View supported parameters (this schema) |
| [rooms](#rooms)         | `integer` | Optional     | No       | `1`                                        | Hotels Day View supported parameters (this schema) |
| [sort](#sort)           | `enum`    | Optional     | No       |                                            | Hotels Day View supported parameters (this schema) |
| `*`                     | any       | Additional   | Yes      | this schema _allows_ additional properties |

### adults

Number of adults. Adults number should be greater than or equal to the rooms number.

`adults`

- is optional
- type: `integer`
- default: `2`
- defined in this schema

#### adults Type

`integer`

- minimum value: `1`

### checkin

Checkin date in the format YYYY-MM-DD

`checkin`

- is optional
- type: `string`
- defined in this schema

#### checkin Type

`string`

### checkout

Checkout date in the format YYYY-MM-DD

`checkout`

- is optional
- type: `string`
- defined in this schema

#### checkout Type

`string`

### currency

The desired currency for the page. Examples: GBP, EUR, USD

`currency`

- is optional
- type: `string`
- defined in this schema

#### currency Type

`string`

### entity_id

The id of the geo location for which the search will be performed.

`entity_id`

- is **required**
- type: `string`
- defined in this schema

#### entity_id Type

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

### rooms

Number of rooms. Rooms number should be less than or equal to the adults number.

`rooms`

- is optional
- type: `integer`
- default: `1`
- defined in this schema

#### rooms Type

`integer`

- minimum value: `1`

### sort

Defines the order in which search results will appear. Options are: price, -price, distance, -rating, stars, -stars.

`sort`

- is optional
- type: `enum`
- defined in this schema

The value of this property **must** be equal to one of the [known values below](#sort-known-values).

#### sort Known Values

| Value      | Description |
| ---------- | ----------- |
| `price`    |             |
| `-price`   |             |
| `distance` |             |
| `-rating`  |             |
| `stars`    |             |
| `-stars`   |             |
