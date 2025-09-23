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

<details>
  <summary><b>Click for help with "API Endpoints" questions</b></summary>
  
  ```bash
  // Filter by main ingredient
  
  www.themealdb.com/api/json/v1/1/filter.php?i=chicken_breast

  // Change words after "i=" for different ingredient filters
  //NOTE: spaces wont work, so use and underscore instead

  www.themealdb.com/api/json/v1/1/filter.php?i=egg
  www.themealdb.com/api/json/v1/1/filter.php?i=banana
  www.themealdb.com/api/json/v1/1/filter.php?i=brown_sugar
  ```

</details>

<img src="images\1-chicken-breast.png" style="width:180px;" alt="image description">

## API Problem-Solving
API documentation is sometimes incomplete or inaccurate, requiring you to investigate other parts of the website, examine different endpoints, and experiment to uncover the solution you need.

Locate the endpoint for meal details by id - you'll notice that the id shown is a series of numbers, as are all the IDs, but there is no further detail into what the IDs in the documentation.

1. Test the example meal ID endpoint in your browser
2. Try random IDs in the URL and see what happens
3. Explore other endpoints in the documentation and see if you can find out more about the meal IDs
4. Explore other pages on the Meal Database website and see if you can find out more about the IDs (hint: pay attention to the URL in the address bar on different pages)
5. Find the meal ID API endpoint for pancakes

<details>
  <summary><b>Click for help with "API Problem-Solving" questions</b></summary>
  
  ```bash
  //meal id endpoint and example

  www.themealdb.com/api/json/v1/1/lookup.php?i=52772
  ```
Several endpoints will return JSON with a field called idMeal, this is the same id that can be used in the query for the meal by id endpoint. For example, the following API call shows the JSON result for the "list by first letter" endpoint:

<img src="images\1-id-json-example.png" style="width:70%;" alt="image description">
 
 You can also find ids by browsing recipes on the the website pages. You can see the the meal id is in the URL for each recipe.

 <img src="images\1-id-webpage-example.png" style="width:70%;" alt="image description">

 NOTE: Neither of these examples are consistent for all APIs. They are good examples of exploring an application to discover things about a specific API.
</details>

<img src="images\1-pancakes.png" style="width:180px;" alt="image description">

## Reading JSON
Identify what the column headers would be in a table from the JSON data in the response of the following API calls:
1. [https://www.themealdb.com/api/json/v1/1/filter.php?c=Seafood](https://www.themealdb.com/api/json/v1/1/filter.php?c=Seafood)
2. [https://www.themealdb.com/api/json/v1/1/list.php?c=list](https://www.themealdb.com/api/json/v1/1/list.php?c=list)
3. [https://www.themealdb.com/api/json/v1/1/search.php?f=a](https://www.themealdb.com/api/json/v1/1/search.php?f=a)

<details>
  <summary><b>Click for help & answers</b></summary>
Identify what the column headers would be in a table from the JSON data in the response of the following API calls:

1. strMeal, strMealThumb, idMeal

<img src="images\1-json-headers.png" style="width:100%;" alt="image description">

2. strCategory

<img src="images\1-json-headers2.png" style="width:50%;" alt="image description">

3. 'idMeal', 'strMeal', 'strMealAlternate', 'strCategory', 'strArea', 'strInstructions', 'strMealThumb', 'strTags', 'strYoutube', 'strIngredient1', 'strIngredient2', 'strIngredient3', 'strIngredient4', 'strIngredient5', 'strIngredient6', 'strIngredient7', 'strIngredient8', 'strIngredient9', 'strIngredient10', 'strIngredient11', 'strIngredient12', 'strIngredient13', 'strIngredient14', 'strIngredient15', 'strIngredient16', 'strIngredient17', 'strIngredient18', 'strIngredient19', 'strIngredient20', 'strMeasure1', 'strMeasure2', 'strMeasure3', 'strMeasure4', 'strMeasure5', 'strMeasure6', 'strMeasure7', 'strMeasure8', 'strMeasure9', 'strMeasure10', 'strMeasure11', 'strMeasure12', 'strMeasure13', 'strMeasure14', 'strMeasure15', 'strMeasure16', 'strMeasure17', 'strMeasure18', 'strMeasure19', 'strMeasure20', 'strSource', 'strImageSource', 'strCreativeCommonsConfirmed', 'dateModified'

<img src="images\1-json-headers3.png" style="width:70%;" alt="image description">

</details>

<br>

Find the following values in the JSON output of the API Call [https://www.themealdb.com/api/json/v1/1/search.php?s=pie](https://www.themealdb.com/api/json/v1/1/search.php?s=pie)

1. What is the Category for Fish Pie?
2. What is the first ingredient listed for Sugar Pie?
3. What are the tags listed for Mince Pies?

<details>
  <summary><b>Click for help & answers</b></summary>

    1. What is the Category for Fish Pie?
        answer: Seafood

<img src="images\1-read-json.png" style="width:50%;" alt="image description">

    2. What is the first ingredient listed for Sugar Pie?
        answer: Brown Sugar

<img src="images\1-read-json2.png" style="width:70%;" alt="image description">

    3. What are the tags listed for Mince Pies?
        answer: Christmas

<img src="images\1-read-json3.png" style="width:50%;" alt="image description">

</details>

<img src="images\1-pie.png" style="width:180px;" alt="image description">



[NEXT STEP: APIs in the Browser](2-api-extras-quiz.html){: .btn .btn-blue }