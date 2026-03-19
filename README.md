This repository is automatically populated by automation scripts that retrieve, parse, and store data.

## api/dbd

This stores information pertaining to the game Dead By Daylight. As there is no official API or predictable source of promo codes,
it is intended to serve as a simple reference to historical promo code data by periodically scanning known sources. It is powered
by a Google App Script.

`codes.json` stores promo codes in a JSON object:
```js
{
  "active": Code[],
  "general": Code[],
  "expired": Code[]
}
```
- `active` are codes that are currently active and can be redeemed within the application
- `general` are codes that are not expected to expire, sometimes referred to as "evergreen" codes
- `expired` are codes that are no longer active

Codes are stored in the following structure:
```js
{
  "code": String,
  "rewards": String[]
}
```
- `code` is the text used to redeem the associated reward(s)
- `rewards` is a list describing what will be redeemed when claiming the code
