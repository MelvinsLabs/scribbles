
# API

## Versioning


## Authentication (AuthN)

API AuthN can be done by different mechanisms -
  * API Key
  * ClientId + ClientSecret
  * Mutual TLS

### API Key

  * In this mechanism, each Client is provided with an unique API Key.
  * This API Key is used to identity the Client as well.
  * API Key is a randomly generated GUID.
  * API Key is usually passed as a Request Header or as a Query Parameter, over HTTPS.
  * API Keys are saved at the server-side in a Hashed manner to prevent accidental exposure of all API Keys, in case the server database is compromised.
  * API Keys can be used for Rate Limiting.

### ClientId + ClientSecret

  * In this mechanism, each Client is tracked by a unique ClientId.
  * Each ClientId is tagged with a ClientSecret.
  * ClientId & ClientSecret is passed as a Basic Authorization Request Header, over HTTPS.
  * ClientId & ClientSecret is saved at the server-side in a Hashed manner to prevent accidental exposure of all API Keys, in case the server database is compromised.
  * ClientId can be used for Rate Limiting.
