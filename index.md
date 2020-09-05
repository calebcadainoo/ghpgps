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

### Sample Codes
<b>Address:</b> AK-484-9321<br><br>

<hr>
### C-Sharp
<hr>
```
var client = new RestClient("https://ghpgps.herokuapp.com");
client.Timeout = -1;
var request = new RestRequest(Method.POST);
request.AddHeader("Content-Type", "application/x-www-form-urlencoded");
request.AddParameter("address", "AK-484-9321");
IRestResponse response = client.Execute(request);
Console.WriteLine(response.Content);
```