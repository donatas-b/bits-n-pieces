RestSharp is a wrapper around HttpClient that allows you to do the following:

 - Add default parameters of any kind (not just headers) to the client, once
 - Add parameters of any kind to each request (query, URL segment, form, attachment, serialized body, header) in a straightforward way
 - Serialize the payload to JSON or XML if necessary
 - Set the correct content headers (content type, disposition, length, etc.)
 - Handle the remote endpoint response
 - Deserialize the response from JSON or XML if necessary


// Creates a client with default options to call a given base URL  
``var client = new RestClient("https://localhost:5000");``

// Creates a client using the options object
```
var options = new RestClientOptions("https://localhost:5000") {
    MaxTimeout = 1000
};
var client = new RestClient(options);
```
// resource is the sub-path of the client base path
```
var request = new RestRequest(resource); 
```

// override default GET
```
var request = new RestRequest(resource, Method.Post);
```


//add header
```
AddHeader(string name, string value);
AddHeader<T>(string name, T value);           // value will be converted to string
AddOrUpdateHeader(string name, string value); // replaces the header if it already exists

var request = new RestRequest("/path").AddHeader("X-Key", someKey);
```

//default client headers
```
client.AddDefaultHeader(string name, string value);
```

// add cookie
```
request.AddCookie("foo", "bar");
```

//add body
 - `AddJsonBody` for JSON payloads
 - `AddXmlBody` for XML payloads
 - `AddStringBody` for pre-serialized payloads

```
var param = new MyClass { IntData = 1, StringData = "test123" };
request.AddJsonBody(param);
```


//make a call
```
public async Task<RestResponse> ExecuteAsync(
    RestRequest request, 
    CancellationToken cancellationToken = default
)
```
