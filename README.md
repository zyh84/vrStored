# vrStored
A version controlled key-value store with a HTTP API. 
API able to :
Accept a key(string) and value(some json blob/string) and store them. If an existing key is sent, the value should be updated
Accept a key and return the corresponding latest value
When given a key AND a timestamp, return whatever the value of the key at the time was.

Method: POST
Endpoint: /vrStored
Body: JSON: {key : value1}
Time: Current Time (Date.now)

Method: GET
Endpoint: /vrStored
Response: ALL Data in the Database

Method: GET
Endpoint: /vrStored/mykey
Response: value1 (latest value)

Method: GET
Endpoint: /vrStored/mykey?time=1482309257
Response: the value at that timepoint
