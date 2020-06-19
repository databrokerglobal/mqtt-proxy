# MQTT AUTH API

### `POST $AUTH_URL/connect`
#### Request
```json
{ "Uuid": "",
  "Username" : "",
  "Password" : "",
  "ClientIdentifier" : "",
}
```
#### Response 200
```json
{
  "Username" : "Override",
  "Password" : "Override",
  "ClientIdentifier" : "Override",
}
```
#### Response Error
The mqtt connection is aborted...

### `POST $AUTH_URL/subscribe`
#### Request
```json
 { "Uuid": "",
   "Username" : "",
   "Password" : "",
   "ClientIdentifier" : "",
   "Topic" : ""
}
```
#### Response
```json
{
   "Topic" : "Override"
}
```
#### Response Error
The subscription is cleanly rejected

### `$AUTH_URL/publish`, `$AUTH_URL/receive`
#### Request
```json
{ "Uuid": "",
   "Username" : "",
   "Password" : "",
   "ClientIdentifier" : "",
   "Topic" : "",
   "Payload": ""
}
```
#### Response
```json
{
   "Topic" : "Override",
   "Payload": "Override"
}
```
#### Response Error
The connection is is aborted (No MQTT Protocol way)
