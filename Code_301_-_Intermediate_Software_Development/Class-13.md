# Class 13

## References 

- - Sending form data MDN Web Docs -
https://developer.mozilla.org/en-US/docs/Learn/Forms/Sending_and_retrieving_form_data

### Sending form data 
by MDN Web Docs

#### Client/server architecture

"a client (usually a web browser) sends a request to a server (most of the time a web server like Apache, Nginx, IIS, Tomcat, etc.), using the HTTP protocol. The server answers the request using the same protocol."

An HTTP request is a nice convenient way to have a user send information to the server

On the client side: defining how to send the data

- The form element formats how the data will be sent

- The "action" attribute defines where the data goes. - define the url of the page you want the user to be sent

- the "method" attribute 
    - defines HOW the data is sent
    - GET, POST
        - GET - asks server to send back a given resource data is appended to the URL
        - POST - browser talks to the server and asks for a response that takes into consideration the data in the body of the HTTP request
#### Viewing HTTP requests

1. Open the developer tools.
1. Select "Network"
1. Select "All"
1. Select "foo.com" in the "Name" tab
1. Select "Headers"

##### On the server side: retrieving the data

using express for node.js installed in your terminal and used to talk between the client and the server. 

- A special case: sending files

    - 'This attribute lets you specify the value of the Content-Type HTTP header included in the request generated when the form is submitted. This header is very important because it tells the server what kind of data is being sent. By default, its value is application/x-www-form-urlencoded. In human terms, this means: "This is form data that has been encoded into URL parameters."'

    - 'If you want to send files, you need to take three extra steps:

        - Set the method attribute to POST because file content can't be put inside URL parameters.
        - Set the value of enctype to multipart/form-data because the data will be split into multiple parts, one for each file plus one for the text data included in the form body (if text is also entered into the form).
        - Include one or more <input type="file"> controls to allow your users to select the file(s) that will be uploaded.
        "


