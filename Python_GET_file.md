### Get a file usng requests

This is the  equivalent of 

curl -X GET -u "username:password" "https://example.com/v1/restapi/service"

The request can be sensitive to compicated passwords with extr charaters so a credentials object is used

~~~

import requests

from base64 import b64encode

credentials = b64encode(b"username:passw%rd")

r=requests.get("https://example.com/v1/restapi/service", headers={
  "Authorization": "Basic " + credentials.decode("utf-8")
})
print(r.json())

~~~
