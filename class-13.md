# _Sending form data:_
- Once the form data has been validated on the client-side, it is okay to submit the form.
- The <form> element defines how the data will be sent. All of its attributes are designed to let you configure the request to be sent when a user hits a submit button. 
* The two most important attributes are action and method.
>+ The action attribute defines where the data gets sent. 
>> Its value must be a valid relative or absolute URL.
>>> If this attribute isn't provided, the data will be sent to the URL of the page containing the form the current page.
- The ***GET*** method is the method used by the browser to ask the server to send back a given resource: "Hey server, I want to get this resource." In this case, the browser sends an empty body. Because the body is empty, if a form is sent using this method the data sent to the server is appended to the URL
- The **POST** method is a little different. It's the method the browser uses to talk to the server when asking for a response that takes into account the data provided in the body of the HTTP request: "Hey server, take a look at this data and send me back an appropriate result." If a form is sent using this method, the data is appended to the body of the HTTP request.
- The POST method is a little different. It's the method the browser uses to talk to the server when asking for a response that takes into account the data provided in the body of the HTTP request: "Hey server, take a look at this data and send me back an appropriate result." If a form is sent using this method, the data is appended to the body of the HTTP request.
* Sending files with HTML forms is a special case. Files are binary data or considered as such whereas all other data is text data. Because HTTP is a text protocol, there are special requirements for handling binary data.
- sending form data is easy, but securing an application can be tricky. Just remember that a front-end developer is not the one who should define the security model of the data.It's possible to perform client-side form validation, but the server can't trust this validation because it has no way to truly know what has really happened on the client-side.


