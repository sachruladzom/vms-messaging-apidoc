# Config Profile
Memakai format JSON

## Record Greeting
Command: `RECGREETING`

jika `filename` <strong>kosong</strong> dan `active` <strong>false</strong>, <br>
maka file greeting di <strong>hapus</strong> 

### Request
Format: `JSON`

| Parameter | Type| value | Description |
| :--- | :--- | :--- | :--- |
| `command` | `string` |RECGREETING| initial leaving |
| `ip` | `int` |127.0.0.1| ip dari server ivr|
| `ivr_name` | `string` |SBY| nama ivr node |
| `number` | `string`| 0818123123 | info nomor penelepon |
| `filename` | `string`| personal_greeting_filename | personal greeting |
| `active` | `boolean`| `true`<br>`false`| aktifasi personal greeting |

#### Contoh Request
```javascript
{
  "command" : "RECGREETING",
  "ip" : "127.0.0.1",
  "ivr_name" : "SBY",
  "number"    : "0818123123",
  "filename" : "voice_greeting_filename",
  "active" : true
}
```

### Response
Format: `JSON`

| Parameter | Type| value | Description |
| :--- | :--- | :--- | :--- |
| `status` | `string` | `ok` <br> `error`| `ok` pemrosesan data berhasil<br> `error` pemrosesan data gagal |


#### Contoh Response
```javascript
{
  "status" : "ok",
}
```


## Change Language
Command: `CFGLANG`


### Request
Format: `JSON`

| Parameter | Type| value | Description |
| :--- | :--- | :--- | :--- |
| `command` | `string` |CFGLANG||
| `ip` | `int` |127.0.0.1| ip dari server ivr|
| `ivr_name` | `string` |SBY| nama ivr node |
| `number` | `string`| 0818123123 | info nomor penelepon |
| `language` | `string`| `ina`<br>`eng`| `ina` indonesia<br>`eng` english |

#### Contoh Request
```javascript
{
  "command" : "RECGREETING",
  "ip" : "127.0.0.1",
  "ivr_name" : "SBY",
  "number"    : "0818123123",
  "language" : "ina"
}
```

### Response
Format: `JSON`

| Parameter | Type| value | Description |
| :--- | :--- | :--- | :--- |
| `status` | `string` | `ok` <br> `error`| `ok` pemrosesan data berhasil<br> `error` pemrosesan data gagal |


#### Contoh Response
```javascript
{
  "status" : "ok",
}
```


## Service

service dibagi 2, leaving dan retrieve:

* [Skenario leaving](leaving.md) : `Leaving`
* [Skenarion Retrieve](retreive.md) : `Retrieve`