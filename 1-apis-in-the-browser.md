---
layout: default
title: 1 APIs in the Browser
nav_order: 2
parent: Workshop Activities
---
# Trying APIs in the Browser
You'll use a broswer to explore API enpoints (URL). A browser is a great starting point because it doesn’t require any coding knowledge. You can simply paste an API URL into the address bar, hit Enter, and see the raw data. 

Using APIs in borwsers automoatically uses the GET method, so you wont need to worry about specifying what method you're using.

## API Endpoints
1. Go to [The Meal Database API documentation](https://www.themealdb.com/api.php) and read all the available endpoints
2. Find the endpoint that allows you to filter recipes by main ingredient
3. Try the "Filter by main ingredient" end point in your browsers address bar
    * Use the example from the documentation
    * Try 3 more ingredients of your choice and see what happens. What happens when there are no recipes with the ingedient you set?
    * Add the name of some of recipes that come up into the [Recipe Endpoints Whiteboard](https://www.canva.com/design/DAGzXJAhQ_Q/KrDhketfmSFb9-bA7rbvmA/view?utm_content=DAGzXJAhQ_Q&utm_campaign=designshare&utm_medium=link2&utm_source=uniquelinks&utlId=h93ee196ecf)

<img src="images\1-chicken-breast.png" style="width:180px;" alt="image description">

## API Problem-Solving
API documentation is sometimes incomplete or inaccurate, requiring you to investigate other parts of the website, examine different endpoints, and experiment to uncover the solution you need.

Locate the endpoint for meal details by id - you'll notice that the id shown is a series of numbers, as are all the IDs, but there is no further detail into what the IDs in the documentation.

1. Test the example meal ID endpoint in your browser
2. Try random IDs in the URL and see what happens
3. Explore other endpoints in the documentation and see if you can find out more about the meal IDs
4. Explore other pages on the Meal Database website and see if you can find out more about the IDs (hint: pay attention to the URL in the address bar on different pages)
5. Find the meal ID API endpoint for pancakes

<img src="images\1-pancakes.png" style="width:180px;" alt="image description">

## Reading JSON
Identify what the column headers would be in a table from the JSON data in the response of the following API calls:
1. [https://www.themealdb.com/api/json/v1/1/filter.php?c=Seafood](https://www.themealdb.com/api/json/v1/1/filter.php?c=Seafood)
2. [https://www.themealdb.com/api/json/v1/1/list.php?c=list](https://www.themealdb.com/api/json/v1/1/list.php?c=list)
3. [https://www.themealdb.com/api/json/v1/1/search.php?f=a](https://www.themealdb.com/api/json/v1/1/search.php?f=a)

Find the following values in the JSON output of the API Call [https://www.themealdb.com/api/json/v1/1/search.php?s=pie](https://www.themealdb.com/api/json/v1/1/search.php?s=pie)
1. What is the Category for Fish Pie?
2. What is the first ingredient listed for Sugar Pie?
3. What are the tags listed for Mince Pies?

<img src="images\1-pie.png" style="width:180px;" alt="image description">

[NEXT STEP: APIs in the Browser](2-api-extras-quiz.html){: .btn .btn-blue }