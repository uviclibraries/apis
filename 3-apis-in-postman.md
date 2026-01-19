---
layout: default
title: 3 APIs in Postman
nav_order: 2
parent: Workshop Activities
---

# APIs in Postman

[Postman](https://www.postman.com/) is a GUI (graphical user interface) which allows users to test and explore APIs at a high level. No programing necessary. We will by querying the [*City of Vancouver Open Data Portal* API](https://opendata.vancouver.ca/api/explore/v2.1/console) which is a database that shares public City oof Vancouver datasets.

## Make a Postman account

Postman has a free version and is online. Simply create an account at [Postman.com](https://www.postman.com/).

## Getting started

Let's start our first project
1. From the home page select **Get Started**

    <br><img src="images\3-1-get-started.png" style="width:70%;" alt="image description"><br>

2. In the top left hand corner select **New**

    <br><img src="images\3-3-new-project.png" style="width:70%;" alt="image description"><br>

3. Remember that we are working with REST APIs which use HTTP (over the web). Select **HTTP** for the type of project.

    <br><img src="images\3-2-http-project.png" style="width:70%;" alt="image description"><br>


## Reading the Documnetation

Go to the documentation for [*City of Vancouver Open Data Portal* API](https://opendata.vancouver.ca/api/explore/v2.1/console). This is a typical layout for API documentation - keep in mind that some API documentation is different and can be challenging to work off of. In this documentation You'll find the name of the server in the desctiption at the top:

<br><img src="images\3-4-server-url.png" style="width:70%;" alt="image description"><br>

<br>Below the description is the list of available paths:

<br><img src="images\3-5-query-paths.png" style="width:70%;" alt="image description"><br>  

<br>If you click on one of the paths, you'll see the parameters you can use with it:

<br><img src="images\3-6-query-facet-options.png" style="width:70%;" alt="image description"><br> 

<details>
<summary><b>Click for a reminder of the parts of a query string</b></summary> <br>

<div style="background-color:black"> 
<span style="color:orange">{SERVER}</span><span style="color:#73d98e">{PATH}</span><span style="color:yellow">{PARAMERTERS}</span> <br><br>

<span style="color:orange">opendata.vancouver.ca/api/explore/v2.1</span><span style="color:#73d98e">/catalog/datasets</span><span style="color:yellow">?limit=10
</span>

</div>

</details>

## Making an API Call in Postman

It's time to test out some API calls using Postman.

1. Combine the server URL with the path to query catalog datasets and send it using a GET Method in Postman.

    <details>
    <summary><b>Click for help making the call</b></summary><br>

    <br><img src="images\3-7-combine-to-create-call.png" style="width:90%;" alt="image description"><br>

    </details><br>

2. Scan the Body of the response and identify some of the variable names and values. Ensure your response code is 200 OK.

    <details>
    <summary><b>Click for help navigating the response</b></summary><br>

    examples of variable names in the response: 
    - visibility
    - dataset_id
    - dataset_uid
    - features
    - attachments
    - etc.

    <br><img src="images\3-8-view-response-body-json.png" style="width:90%;" alt="image description"><br>

    </details>

## More Advanced API Calls

Let's try a call using one of the query parameters. The "refine" parameter is the same as using a facet if you were using the GUI (graphical user interface) to look-up datasets. Most of the time you cna use the GUI (if there is one) to figure out API calls

Apply a facet in the [GUI version of City of Vancouver Open Data Portal](https://opendata.vancouver.ca/explore/). For example, select the theme "Food and Housing". You can use the resulting URL to help build your parameter for the API call.

<br><img src="images\3-10-filter-in-search-tool.png" style="width:90%;" alt="image description"><br> 

Hint 1: the formatting is not exactly the same. Be sure to read the formatting in the API documentation closely.  

Hint 2: one way to check that it's correct is compare the number and name of datasets returned. If they match, you probably did it right.

<br><img src="images\3-9-refine-param.png" style="width:90%;" alt="image description"><br>    

<details>
<summary><b>Click for help writing the refine parameter</b></summary><br>

When you select the theme "Food and Housing" the resulting URL is: 

https://opendata.vancouver.ca/explore/?disjunctive.features&disjunctive.theme&disjunctive.keyword&disjunctive.data-owner&disjunctive.data-team&sort=modified&==<mark>refine.theme=Food+and+housing==</mark>

This indicates that the facet is called "theme" and the value should have plus (+) signs between the words.

Translating this to the API format will become:

https://opendata.vancouver.ca/api/explore/v2.1/catalog/datasets<mark>?refine=theme:Food+and+housing</mark>

</details>

## Extra

Read the documentation and try at lease one other path or parameter of your choice.

**Congrats! You've completed the workshop.**

[NEXT STEP: Additional Resources](additional-resources.md){: .btn .btn-blue }