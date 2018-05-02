# teaching-XHR

### Basic concept of how Internet works
- What is a server?
  - Serves/sends data to client 
  - Usually remote server when connected to the internet
- What is a client?
  - Our browser from either our laptop, desktop, smart phone
- Client & Server Model
  1. When you type faceboook.com into your browser
  2. A request goes out to the Facebook's remote server
  3. Facebook's remote server takes in that request
  4. Facebook interprets the code and responds back to the client
  5. The client receives the response with an html file and displays it on the page

### What is an API
- Everytime a request a is made by the client, you are interacting with the remote server's API
- API stands for Application Programming Interface
- Web tool to access data or services. 
- A software company releases its API to the public so that other software developers can design products that are powered by its service.
- Software to software interface, appications talk to applications without the client noticing. 
  - Movie ticket example
    - When you buy ticket through website, an API request is made to a remote application(stripe, paypal) to verify and process your credit card information
    - This is all behind the scenes that the client does not know about
![diagram 1](http://sahilsk.github.io/images/api-client.png)
![Diagram 2](http://diy-visualpedia.s3.amazonaws.com/API-diagram-02.png)
- There are tons of API's from big and small companies where they offer data or services
- We will be using XHR to make request to api endpoint
- Endpoints are url's that have data in JSON format
- JSON - Javascript Object Notation 
  - Formatted for easy readbility
  - We can use this data for our web application

### Why use API's?
- You can make amazing applications that use data from other applications 
- Data is already made for you, you hit those API's to get the data and manipulate it for your application 

### Live-Code making GET request to SWAPI 
- Show SWAPI and uri endpoints that returns json data
- Show Reddit api that returns json data
- We will be getting the name "Luke Skywalker" from API
- Instantiate a new XHR object
```js 
var oReq = new XMLHttpRequest();
```
- Declare a function to be used as the event listener.
```js
function reqListener () {
  console.log(this.responseText);
}
```
- Attach the event listener to an event
``` js
oReq.addEventListener("load", reqListener);
```
- Set the destination and send the request!
``` js
oReq.open("GET", "http://www.google.com");
oReq.send();
```
- The code 
```js 
function reqListener () {
  console.log(this.responseText);
}

var oReq = new XMLHttpRequest();
oReq.addEventListener("load", reqListener);
oReq.open("GET", "http://www.google.com");
oReq.send();
```

### Resources
[DevLeague Slides](http://devleague.slides.com/devleague/xhr#/4/2)

[MDN Docks](https://developer.mozilla.org/en-US/docs/Web/API/XMLHttpRequest/Using_XMLHttpRequest)


