## Hotel Details supported query parameters Schema

```
/hotels/hotel-details
```

A schema definition for the hotel details microsite supported query parameters

| Abstract            | Extensible | Status       | Identifiable | Custom Properties | Additional Properties | Defined In                             |
| ------------------- | ---------- | ------------ | ------------ | ----------------- | --------------------- | -------------------------------------- |
| Can be instantiated | No         | Experimental | No           | Forbidden         | Permitted             | [hotelDetails.json](hotelDetails.json) |

## Hotel Details supported query parameters Properties

| Property              | Type      | Required     | Nullable | Defined by                                             |
| --------------------- | --------- | ------------ | -------- | ------------------------------------------------------ |
| [adults](#adults)     | `integer` | Optional     | No       | Hotel Details supported query parameters (this schema) |
| [checkin](#checkin)   | `string`  | Optional     | No       | Hotel Details supported query parameters (this schema) |
| [checkout](#checkout) | `string`  | Optional     | No       | Hotel Details supported query parameters (this schema) |
| [currency](#currency) | `string`  | Optional     | No       | Hotel Details supported query parameters (this schema) |
| [hotelId](#hotelid)   | `string`  | **Required** | No       | Hotel Details supported query parameters (this schema) |
| [locale](#locale)     | `string`  | Optional     | No       | Hotel Details supported query parameters (this schema) |
| [market](#market)     | `string`  | Optional     | No       | Hotel Details supported query parameters (this schema) |
| [rooms](#rooms)       | `integer` | Optional     | No       | Hotel Details supported query parameters (this schema) |
| `*`                   | any       | Additional   | Yes      | this schema _allows_ additional properties             |

### adults

Number of adults

`adults`

- is optional
- type: `integer`
- defined in this schema

#### adults Type

`integer`

### checkin

Date in the format YYYY-MM-DD

`checkin`

- is optional
- type: `string`
- defined in this schema

#### checkin Type

`string`

### checkout

Date in the format YYYY-MM-DD

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

### hotelId

The entity id of the hotel.

`hotelId`

- is **required**
- type: `string`
- defined in this schema

#### hotelId Type

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

Number of rooms

`rooms`

- is optional
- type: `integer`
- defined in this schema

#### rooms Type

`integer`
