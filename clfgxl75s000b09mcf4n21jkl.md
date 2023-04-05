---
title: "How to Encode and Decode Base64 using JavaScript"
seoTitle: "How to Encode and Decode Base64 using JavaScript"
seoDescription: "In this article, you will learn about Base64 and how it works to convert binary data, regular strings, and lots more into ASCII text."
datePublished: Wed Mar 15 2023 14:37:25 GMT+0000 (Coordinated Universal Time)
cuid: clfgxl75s000b09mcf4n21jkl
slug: how-to-encode-and-decode-base64-using-javascript
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/oXlXu2qukGE/upload/397d6c27d44329681a928cc49a514d4f.jpeg
tags: javascript, html, html5, base64

---

In this article, you will learn about Base64 and how it works to convert binary data, regular [strings](/), and lots more into ASCII text.

## **What is Base64?**

%%[postads] 

[Base64](https://en.wikipedia.org/wiki/Base64) is a group of binary-to-text encoding schemes representing binary data in ASCII string format. It is commonly used to encode data that needs to be stored or transmitted in a way that cannot be directly represented as text.

Base64 encoding works by mapping binary data to 64 characters from the <mark>ASCII character set</mark>. The 64 characters used in Base64 encoding are: `A-Z`, `a-z`, `0-9`, `+`, and `/`.

Base64 decoding is the <mark>reverse process of encoding</mark>. It takes a Base64 encoded string and maps each character back to its 6-bit binary representation. The resulting binary data is a reconstruction of the original binary data encoded to Base64.

%%[postads] 

## **How to Encode and Decode HTML Base64 using JavaScript**

To encode and decode in JavaScript, you will use the `btoa()` and `atob()` JavaScript functions that are available and supported by modern web browsers.

These JavaScript helper functions are named after old Unix commands for converting <mark>binary to ASCII</mark> (<s>btoa</s>) and <mark>ASCII to binary</mark> (<s>atob</s>).

You can encode a string to base64 in JavaScript using the `btoa()` function and decode a base64 string using `atob()` function. For example, if you have a string stored in a variable, as seen below, you can first encode it to Base64:

```javascript
let myString = "Welcome to HackPig520's Blog!";
let encodedValue = btoa(myString);
console.log(encodedValue); // => V2VsY29tZSB0byBIYWNrUGlnNTIwJ3MgQmxvZyE=
```

You can also decode the `encodedValue` back to its original form using the `atob()` function. This function takes the encoded value and decodes it from **Base64**:

```js
let myString = "Welcome to HackPig520's Blog!";
let encodedValue = btoa(myString);
let decodedValue = atob(encodedValue);
console.log(decodedValue); // Welcome to HackPig520's Blog!
```

You now know how to encode and decode **Base64** in **JavaScript**.

Thanks for reading!