# LuckData-tiktok-api-free
LuckData Tiktok API is the easiest way to scrape TikTok social network. 
Building a custom social scraping solution can be expensive and time-consuming. 
Tiktok API will do everything for you, just call the desired API endpoint to scrape the user's homepage information.

# How to get a free LuckData tiktok API key
Register for a Luckdata account and apply for the tiktok API. Luckdata will grant 100 free points for one month, which can be used with a limit of one request per second. If you need higher points and more request capacity, a paid version is required. Alternatively, you can wait for the next month to receive another 100 free points for use.

# GET User Info Code Snippets
Code examples include python, Java, go, etc.

## python
<pre>import requests

headers = {
    'X-Luckdata-Api-Key': 'your key'
}

json_data={}

response = requests.get(
    'https://luckdata.io/api/tiktok-api/get_get_user_info?username=huaweimobile&sec_user_id=',
    headers=headers,
    
)
print(response.json())</pre>
## java
<pre>import java.io.IOException;
import java.net.URI;
import java.net.http.HttpClient;
import java.net.http.HttpRequest;
import java.net.http.HttpResponse;

HttpClient client = HttpClient.newHttpClient();

HttpRequest request = HttpRequest.newBuilder()
    .uri(URI.create("https://luckdata.io/api/tiktok-api/get_get_user_info?username=huaweimobile&sec_user_id="))
    .GET()
    
    .setHeader("X-Luckdata-Api-Key", "your key")
    .build();

HttpResponse response = client.send(request, HttpResponse.BodyHandlers.ofString());</pre>
## go
<pre>package main

import (
  "fmt"
  "io"
  "log"
  "net/http"
  "strings"
)

func main() {
  client := &http.Client{}
  var data = nil
  req, err := http.NewRequest("GET", "https://luckdata.io/api/tiktok-api/get_get_user_info?username=huaweimobile&sec_user_id=", data)
  if err != nil {
    log.Fatal(err)
  }
  
  req.Header.Set("X-Luckdata-Api-Key", "your key")
  resp, err := client.Do(req)
  if err != nil {
    log.Fatal(err)
  }
  defer resp.Body.Close()
  bodyText, err := io.ReadAll(resp.Body)
  if err != nil {
    log.Fatal(err)
  }
  fmt.Printf("%s\n", bodyText)
}</pre>
##  shell
<pre> curl -X GET "https://luckdata.io/api/tiktok-api/get_get_user_info?username=huaweimobile&sec_user_id="  -H "X-Luckdata-Api-Key":"your key" </pre>
## C#
<pre>using System.Net.Http;
using System.Net.Http.Headers;

HttpClient client = new HttpClient();

HttpRequestMessage request = new HttpRequestMessage(HttpMethod.get, "https://luckdata.io/api/tiktok-api/get_get_user_info?username=huaweimobile&sec_user_id=");


request.Headers.Add("X-Luckdata-Api-Key", "your key");

request.Content = new StringContent("");
request.Content.Headers.ContentType = new MediaTypeHeaderValue("application/json");

HttpResponseMessage response = await client.SendAsync(request);
response.EnsureSuccessStatusCode();
string responseBody = await response.Content.ReadAsStringAsync();
JavaScript
fetch('https://luckdata.io/api/tiktok-api/get_get_user_info?username=huaweimobile&sec_user_id=', {
    method: 'GET',
    headers: {
        'X-Luckdata-Api-Key': 'your key'
    }
})</pre>
# MORE
For more information about LuckData Tiktok API, please click:<a href="https://luckdata.io/marketplace/detail/tiktok-api">LuckData-tiktok-api</a>
