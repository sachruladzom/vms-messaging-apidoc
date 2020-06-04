# COMMAND PROMO
Memakai format JSON

## Get Promo
Command: `GETPROMO`

### Request
Format: `JSON`

| Parameter | Type| value | Description |
| :--- | :--- | :--- | :--- |
| `command` | `string` |GETPROMO| GET PROMO |
| `ip` | `int` |127.0.0.1| ip dari server ivr|
| `ivr_name` | `string` |SBY| nama ivr node |
| `number` | `string` | 0818123123 | a number |
| `promo` | `string` | `x`<br>`y` | `x` mengambil voice promo x<br> `y` mengambil voice promo y|

#### Contoh Request
```javascript
{
  "command" : "GETPROMO",
  "ip" : "127.0.0.1",
  "ivr_name" : "SBY",
  "number"    :  "0818123123",
  "promo" : "x"
}
```

### Responses
Format JSON
| Parameter | Type| Sample value | Description |
| :--- | :--- | :--- | :--- |
| `status` | `string` | `ok` <br> `error`| proses pengambilan data berhasil<br> `error` proses pengambilan data gagal |
| `voice` | `string` | promo_voice | filename voice promo

```javascript
{
	"status" : "ok",
	"voice" : "promo_voice_filename"
}
```

## Send Notifikasi Promo
Command: `SENDPROMO`

### Request
Format: `JSON`

| Parameter | Type| value | Description |
| :--- | :--- | :--- | :--- |
| `command` | `string` |SENDPROMO| send PROMO |
| `ip` | `int` |127.0.0.1| ip dari server ivr|
| `ivr_name` | `string` |SBY| nama ivr node |
| `number` | `string` | 0818123123 | a number |
| `promo` | `string` | `x`<br>`y` | `x` send sms promo x<br> `y` send sms promo y|

#### Contoh Request
```javascript
{
  "command" : "GETPROMO",
  "ip" : "127.0.0.1",
  "ivr_name" : "SBY",
  "number"    :  "0818123123",
  "promo" : "x"
}
```

### Responses
Format JSON
| Parameter | Type| Sample value | Description |
| :--- | :--- | :--- | :--- |
| `status` | `string` | `ok` <br> `error`| proses data berhasil<br> `error` proses data gagal |

```javascript
{
	"status" : "ok",
}
```

## Service

service dibagi 2, leaving dan retrieve:

* [Skenario leaving](leaving.md) : `Leaving`
* [Skenarion Retrieve](retreive.md) : `Retrieve`