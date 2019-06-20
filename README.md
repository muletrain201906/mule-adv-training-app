# Contents

## Environments

**Set env variable to either env=dev, or env=prod**

env=dev is set in mule-app.properties for use in Anypoint Studio

## Ports

In the environment specific property files different HTTP ports are set.

env: 9020
prod: 9030

**example call: http://localhost:9020/flights-reservations**

## Flights Application

/flights-reservations (env=dev)
/flights (env=prod)

**Return collection of flights**

/flights-reservations/{ID} (env=dev)
/flights/{ID} (env=prod)

**Returns individual flight (results are cached)**

## Object Store

/store?key=abc&value=xyz
**Store key/value pair in Object Store**

/retrieve
**Retrieve all key/value pairs from Object Store**

/retrieve?key=abc
**Retrieve key/value pair specified by key from Object Store**

## Idempotent Filter

/idempotent?value=test
**Store the unique identifier from the value parameter, returns initial OUTPUT!
Subsequent request with the same parameter are filtered, no OUTPUT**

