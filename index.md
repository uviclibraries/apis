---
layout: default
title: Introduction 
nav_order: 1
---
**UPDATE PHOTO**
<img src="images\rest-api-logo.png" style="float:right;width:180px;" alt="image description">

# Using APIs to GET data

- Pre-workshop activities: 00 min 
- Introductory presentation: 45 min
- Hands-on activities: 30 min

## Why use REST APIs? 

[REST APIs](https://TOOL-URL-HERE.org/){:target="_blank"} are great for pulling data because they’re simple, flexible, and widely supported. They use standard web protocols (like HTTP), which means you can access data from almost any programming language (i.e. Python) or tool (i.e. Power BI). REST APIs let you request just the data you need, often in formats like JSON. Plus, they’re easy to integrate into automation workflows, dashboards, or data analysis pipelines.

This workshop uses a broswer to explore API enpoints (URL). Introducing REST APIs through a browser is a great starting point because it’s visual, immediate, and doesn’t require any coding knowledge. You can simply paste an API URL into the address bar, hit Enter, and see the raw data. This helps demystify how APIs work by showing that they’re just web addresses that return data instead of web pages.

## Some limitations of REST APIs:

1. **Rate Limits**  
   Many APIs restrict how often you can make requests, which can be a problem for large-scale or real-time data needs.

2. **Pagination Complexity**  
   APIs often return data in chunks (pages), requiring extra logic to loop through and collect all the data.

3. **Authentication Overhead**  
   Some APIs require complex authentication (like OAuth), which can be tricky for beginners to set up.

4. **Inconsistent Standards**  
   Not all REST APIs follow the same conventions, so learning one doesn’t guarantee you’ll understand another.

5. **Limited Query Capabilities**  
   Unlike databases, REST APIs may not support advanced filtering or sorting, requiring more work on the client side.

6. **Versioning Issues**  
   APIs can change over time, and if you're not using versioned endpoints, your integration might break unexpectedly.

## Using Postman or Python:

1. **More Control Over Requests**  
   Postman and Python let you customize headers, authentication, and body content—things you can’t easily do in a browser.

2. **Support for All HTTP Methods**  
   Browsers only support `GET` requests directly, but APIs often require `POST`, `PUT`, or `DELETE`, which tools like Postman and Python handle easily.

3. **Handling Authentication**  
   Many APIs require tokens or keys. Postman and Python make it easy to include these securely in your requests.

4. **Automation & Reusability**  
   With Python, you can write scripts to automate data pulls, loop through paginated results, and schedule tasks—none of which is possible in a browser.

5. **Better Response Handling**  
   Postman formats responses nicely for readability, and Python lets you parse and process data programmatically, which is essential for analysis or integration.

6. **Debugging & Testing**  
   Postman offers built-in tools to test and debug API calls, while Python gives you full control to log, retry, and handle errors.


## Learning objectives 

At the end of this workshop, you will be able to:

1. Identify the parts of an API request URL
2. Call a simple REST API request in a broswer
3. Write and edit a REST API url with a custom query
4. Read JSON data 
5. Know the general meaning behind the response codes starting with 2, 4, and 5
6. Define authentication, pagination, and response headers
 
 
[NEXT STEP: Pre-Workshop Activities](pre-workshop.html){: .btn .btn-blue }
