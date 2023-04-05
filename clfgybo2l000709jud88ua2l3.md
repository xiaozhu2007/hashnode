---
title: "How to Make an HTTP Request in JavaScript"
seoTitle: "How to Make an HTTP Request in JavaScript"
seoDescription: "When building applications, you will have to interact between the backend and frontend to get the data."
datePublished: Sun Mar 19 2023 14:58:00 GMT+0000 (Coordinated Universal Time)
cuid: clfgybo2l000709jud88ua2l3
slug: how-to-make-an-http-request-in-javascript
tags: js

---

## **How to Make a GET Request with the Fetch API**

The Fetch API is a built-in JavaScript method for retrieving resources and interacting with your backend server or an API endpoint. Fetch API is built-in and does not require installation into your project.

Fetch API accepts one mandatory argument: the API endpoint/URL. This method also accepts an **optional** argument, which is an optional object when making a GET request **because it is the default request**.

```js
  fetch(url, {
      method: "GET"
  })
```

Let’s create a GET request to get a response from the [HTTPBIN.ORG](https://httpbin.org/).

```js
fetch("http://httpbin.org/json")
  .then((response) => response.json())
  .then((json) => console.log(json));
```

This will return a single post which you can now store in a variable and use within your project.

> *Note: For other methods, such as* `POST` *and* `DELETE`*, you need to attach the method to the options array.*

%%[postads] 

## **How to Make a GET Request with** `XMLHttpRequest`

You can use the XMLHttpRequest object to interact with servers. This method can request data from a web server’s API endpoint/URL without doing a full page refresh.

> ***Note:*** *All modern browsers have a built-in* `XMLHttpRequest` *object to request data from a server.*

Let’s perform the same request with the `XMLHttpRequest` by creating a new `XMLHttpRequest` object. You will then open a connection by specifying the request type and endpoint (the URL of the server), then you'll send the request and finally, listen to the server’s response.

```js
const xhr = new XMLHttpRequest();
xhr.open("GET", "http://httpbin.org/json");
xhr.send();
xhr.responseType = "json";
xhr.onload = () => {
  if (xhr.readyState == 4 && xhr.status == 200) {
    console.log(xhr.response);
  } else {
    console.log(`Error: ${xhr.status}`);
  }
};
```

In the above code, a new XMLHttpRequest object is created and stored in a variable called `xhr`. You can now access all its objects using the variable, such as the `.open()` method, when you specify the request type (GET) and the endpoint/URL where you want to request data.

Another method you will use is `.send()`, which sends the request to the server. You can also specify the format in which the data will be returned using the `responseType` method. At this point, the GET request is sent, and all you have to do is listen to its response using the `onload` event listener.

If the client's state is done **(4),** and the status code is successful (**200)**, then the data will be logged to the console. Otherwise, an error message showing the error status will appear.

%%[postads] 

## Warming Up

You now know how to **make an HTTP request** in **JavaScript**.

Thanks for reading!