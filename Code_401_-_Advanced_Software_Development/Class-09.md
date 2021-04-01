# Class 09

## references
https://dev.to/dangolant/things-i-brushed-up-on-this-week-the-http-request-lifecycle-

https://www.baeldung.com/java-http-request

## High level HTTP request

TCP - Transmission Control Protocol

Step 1: Local Processing 

1. browser extracts the "scheme" or protocol. 
1. browswer looks through its own cache of recent URLs the OS cache of queries, routers cache and DNS cache for the IP address

Step 2. Resolve an IP

1. if cache search fails, browser sends a DNS request. 
1. request searches for the target DNS server. 
1. server looks for the address 
1. request is now in the cache and client has an IP address

Step 3. Establish a Connection

1. reciever reorders the recieved packet back to its original order
1. three way handshake between the server, client, third party, and back to the server
1. full duplex connection

Step 4. Send an HTTP Request

1. HTTP request made of request line, header, and a body. 
1. TCP magic sequence number ensures the client recieves the whole request. 
1. server generates an HTTP response
1. Server response to the request 

Step 5. Tearing down and cleaning up

1. Response is fully delivered, four way handshake ends the TCP connection
1. browswer begins processing what it recieved


## Java HTTP Request

Built in Java class - HttpUrlConnection

Step 1. Creating a request

openConnection() method of the URL class
````
URL url = new URL("http://example.com");
HttpURLConnection con = (HttpURLConnection) url.openConnection();
con.setRequestMethod("GET");
````
Step 2. Adding Request Parameters 

set the doOutput property to true, then write a string of the for param1=value¶m2=value to the OutputStream of the HttpUrlConnection instance:

```` 
Map<String, String> parameters = new HashMap<>();
parameters.put("param1", "val");

con.setDoOutput(true);
DataOutputStream out = new DataOutputStream(con.getOutputStream());
out.writeBytes(ParameterStringBuilder.getParamsString(parameters));
out.flush();
out.close();
````
Step 3. Setting Request Headers

setRequestProperty() method 
getHeaderField() method

Step 4. Configuring Timeouts

setConnectTimeout() and setReadTimeout() methods

Step 5. Handling Cookies

CookieManager HttpCookie

Step 6. Handling Redirects

setInstanceFollowRedirects() 

Step 7. Reading the Response

getResponseCode(), connect(), getInputStream() or getOutputStream() methods

Step 8. Reading the Response on Failed Requests

HttpUrlConnection.getErrorStream()

Step 9. Building the Full Response

getFullResponse() or StringBuilder instance.