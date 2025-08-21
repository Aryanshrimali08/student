---
layout: post
title: About
permalink: /about/
comments: true
---

## As a conversation Starter


<style>
    /* Style looks pretty compact, 
       - grid-container and grid-item are referenced the code 
    */
    .grid-container {
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(150px, 1fr)); /* Dynamic columns */
        gap: 10px;
    }
    .grid-item {
        text-align: center;
    }
    .grid-item img {
        width: 100%;
        height: 100px; /* Fixed height for uniformity */
        object-fit: contain; /* Ensure the image fits within the fixed height */
    }
    .grid-item p {
        margin: 5px 0; /* Add some margin for spacing */
    }

    .image-gallery {
        display: flex;
        flex-wrap: nowrap;
        overflow-x: auto;
        gap: 10px;
        }

    .image-gallery img {
        max-height: 150px;
        object-fit: cover;
        border-radius: 5px;
    }
</style>

<!-- This grid_container class is used by CSS styling and the id is used by JavaScript connection -->
<div class="grid-container" id="grid_container">
    <!-- content will be added here by JavaScript -->
</div>

<script>
    // 1. Make a connection to the HTML container defined in the HTML div
    var container = document.getElementById("grid_container"); // This container connects to the HTML div

    // 2. Define a JavaScript object for our http source and our data rows for the Living in the World grid
    var http_source = "https://upload.wikimedia.org/wikipedia/commons/";

    // 3a. Consider how to update style count for size of container
    // The grid-template-columns has been defined as dynamic with auto-fill and minmax

    // 3b. Build grid items inside of our container for each row of data
    for (const location of living_in_the_world) {
        // Create a "div" with "class grid-item" for each row
        var gridItem = document.createElement("div");
        gridItem.className = "grid-item";  // This class name connects the gridItem to the CSS style elements
        // Add "img" HTML tag for the flag
        var img = document.createElement("img");
        img.src = http_source + location.flag; // concatenate the source and flag
        img.alt = location.flag + " Flag"; // add alt text for accessibility

        // Add "p" HTML tag for the description
        var description = document.createElement("p");
        description.textContent = location.description; // extract the description

        // Add "p" HTML tag for the greeting
        var greeting = document.createElement("p");
        greeting.textContent = location.greeting;  // extract the greeting

        // Append img and p HTML tags to the grid item DIV
        gridItem.appendChild(img);
        gridItem.appendChild(description);
        gridItem.appendChild(greeting);

        // Append the grid item DIV to the container DIV
        container.appendChild(gridItem);
    }
</script>

### Interests and hobbies

My passions and interests keep me engaged and curious
<comment>
Gallery of pics, scroll to the right for more...
</comment>
<div class="image-gallery">
  <img src="{{site.baseurl}}/images/about/20250119_154433.jpg" alt="Image 1">
  <img src="{{site.baseurl}}/images/about/Night @ the museum Photo 1- Aryan Shrimali.jpg" alt="Image 2">
  <img src="{{site.baseurl}}/images/about/20230302_204336.jpg" alt="Image 3">
  <img src="{{site.baseurl}}/images/about/20240906_192706 (1).jpg" alt="Image 4">

### Culture and heritage

My identity as an Indian-American student defines who I am 

- I have lived in 6 unqiue cities thoughout my life since I was born in Rockville, Maryland. 
- I have 1 sibling who entered OVMS this year. I also have many aunts and uncles: 4 aunts on my dads side and 2 aunts and 2 uncles on my moms side. 
- Here are some of the pictures of my family

<comment>
Gallery of Pics, scroll to the right for more ...
</comment>
<div class="image-gallery">
  <img src="{{site.baseurl}}/images/about/IMG-20250702-WA0025.jpg" alt="Image 1">
  <img src="{{site.baseurl}}/images/about/IMG-20250717-WA0061.jpg" alt="Image 2">
  <img src="{{site.baseurl}}/images/about/IMG-20250302-WA0060.jpg" alt="Image 3">
  <img src="{{site.baseurl}}/images/about/IMG-20250302-WA0084.jpg" alt="Image 4">
</div>
