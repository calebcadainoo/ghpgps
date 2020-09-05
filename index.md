## GhanaPostGPS Public API
<hr>
### API Details
<hr>
<b>End Point URL:</b> https://ghpgps.herokuapp.com<br>
<b>Method:</b> POST<br>
<b>Parameters:</b> address (GhanaPostGPS Address)<br>
<b>Content-Type:</b> application/x-www-form-urlencoded<br>
<hr>
<hr><br><br>

<hr>
### Donations
<hr>
Please donate to keep this project running.<br>
<p>
  <a target="_blank" href="https://dashboard.flutterwave.com/donate/cejpesniqs3f">
      <img src="https://image.flaticon.com/icons/svg/3090/3090757.svg" style="width: 20px; height: auto;" alt="donate">
  </a>
</p>
<hr><br>


### Sample Codes
<b>Address:</b> AK-484-9321 or AK4849321<br><br>

<hr>
### C-Sharp
<hr>
Code:

```
var client = new RestClient("https://ghpgps.herokuapp.com");
client.Timeout = -1;
var request = new RestRequest(Method.POST);
request.AddHeader("Content-Type", "application/x-www-form-urlencoded");
request.AddParameter("address", "AK-484-9321");
IRestResponse response = client.Execute(request);
Console.WriteLine(response.Content);
```
<hr><br>

<hr>
### cURL
<hr>
Code:
```
curl --location --request POST 'https://ghpgps.herokuapp.com' \
--header 'Content-Type: application/x-www-form-urlencoded' \
--data-urlencode 'address=AK-484-9321'
```
<hr><br>

<hr>
### Go
<hr>
Code:
```
package main

import (
  "fmt"
  "strings"
  "net/http"
  "io/ioutil"
)

func main() {

  url := "https://ghpgps.herokuapp.com"
  method := "POST"

  payload := strings.NewReader("address=AK-484-9321")

  client := &http.Client {
  }
  req, err := http.NewRequest(method, url, payload)

  if err != nil {
    fmt.Println(err)
  }
  req.Header.Add("Content-Type", "application/x-www-form-urlencoded")

  res, err := client.Do(req)
  defer res.Body.Close()
  body, err := ioutil.ReadAll(res.Body)

  fmt.Println(string(body))
}
```
<hr><br>

<hr>
### Javscript
<hr>
Code:
```
var myHeaders = new Headers();
myHeaders.append("Content-Type", "application/x-www-form-urlencoded");

var urlencoded = new URLSearchParams();
urlencoded.append("address", "AK-484-9321");

var requestOptions = {
  method: 'POST',
  headers: myHeaders,
  body: urlencoded,
  redirect: 'follow'
};

fetch("https://ghpgps.herokuapp.com", requestOptions)
  .then(response => response.text())
  .then(result => console.log(result))
  .catch(error => console.log('error', error));
```
<hr><br>


<hr>
### NodeJS
<hr>
Code:
```
var request = require('request');
var options = {
  'method': 'POST',
  'url': 'https://ghpgps.herokuapp.com',
  'headers': {
    'Content-Type': 'application/x-www-form-urlencoded'
  },
  form: {
    'address': 'AK-484-9321'
  }
};
request(options, function (error, response) {
  if (error) throw new Error(error);
  console.log(response.body);
});
```
<hr><br>

<hr>
### PHP
<hr>
Code:
```
<?php

$curl = curl_init();

curl_setopt_array($curl, array(
  CURLOPT_URL => "https://ghpgps.herokuapp.com",
  CURLOPT_RETURNTRANSFER => true,
  CURLOPT_ENCODING => "",
  CURLOPT_MAXREDIRS => 10,
  CURLOPT_TIMEOUT => 0,
  CURLOPT_FOLLOWLOCATION => true,
  CURLOPT_HTTP_VERSION => CURL_HTTP_VERSION_1_1,
  CURLOPT_CUSTOMREQUEST => "POST",
  CURLOPT_POSTFIELDS => "address=AK-484-9321",
  CURLOPT_HTTPHEADER => array(
    "Content-Type: application/x-www-form-urlencoded"
  ),
));

$response = curl_exec($curl);

curl_close($curl);
echo $response;
```
<hr><br>

<hr>
### Python
<hr>
Code:
```
import requests

url = "https://ghpgps.herokuapp.com"

payload = 'address=AK-484-9321'
headers = {
  'Content-Type': 'application/x-www-form-urlencoded'
}

response = requests.request("POST", url, headers=headers, data = payload)

print(response.text.encode('utf8'))
```
<hr><br>

<hr>
### Swift
<hr>
Code:
```
import Foundation

var semaphore = DispatchSemaphore (value: 0)

let parameters = "address=AK-484-9321"
let postData =  parameters.data(using: .utf8)

var request = URLRequest(url: URL(string: "https://ghpgps.herokuapp.com")!,timeoutInterval: Double.infinity)
request.addValue("application/x-www-form-urlencoded", forHTTPHeaderField: "Content-Type")

request.httpMethod = "POST"
request.httpBody = postData

let task = URLSession.shared.dataTask(with: request) { data, response, error in 
  guard let data = data else {
    print(String(describing: error))
    return
  }
  print(String(data: data, encoding: .utf8)!)
  semaphore.signal()
}

task.resume()
semaphore.wait()
```
<hr><br>

<hr>
### Java
<hr>
Code:
```
OkHttpClient client = new OkHttpClient().newBuilder()
  .build();
MediaType mediaType = MediaType.parse("application/x-www-form-urlencoded");
RequestBody body = RequestBody.create(mediaType, "address=AK-484-9321");
Request request = new Request.Builder()
  .url("https://ghpgps.herokuapp.com")
  .method("POST", body)
  .addHeader("Content-Type", "application/x-www-form-urlencoded")
  .build();
Response response = client.newCall(request).execute();
```
<hr><br>

<hr>
### PowerShell
<hr>
Code:
```
$headers = New-Object "System.Collections.Generic.Dictionary[[String],[String]]"
$headers.Add("Content-Type", "application/x-www-form-urlencoded")

$body = "address=AK-484-9321"

$response = Invoke-RestMethod 'https://ghpgps.herokuapp.com' -Method 'POST' -Headers $headers -Body $body
$response | ConvertTo-Json
```
<hr><br>

<hr><hr>
#### Output/Response:
<hr>
1. Address found
```
{
    "data": {
        "Table": [
            {
                "Area": "NEW KAGYASI",
                "CenterLatitude": 6.650080145273592,
                "CenterLongitude": -1.648700346667856,
                "District": "Kumasi",
                "EastLat": 6.65005768739201,
                "EastLong": -1.6486780409076,
                "GPSName": "AK4849321",
                "NorthLat": 6.65010262239948,
                "NorthLong": -1.6487229566718,
                "PostCode": "AK484",
                "Region": "Ashanti",
                "SouthLat": 6.65005768739201,
                "SouthLong": -1.6487229566718,
                "Street": "Kumasi, Ashanti, GHA",
                "WestLat": 6.65010262239948,
                "WestLong": -1.6486780409076
            }
        ]
    },
    "found": true
}
```

2. Address not found
```
{
    "data": {
        "Table": null
    },
    "found": false
}
```
