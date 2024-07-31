---
title: More working with the DOM
description: 
date: 2024-07-18
tags:
  - JavaScript
  - DOM
  - HTML
  - CSS
---
<p>For our final session of the Bootcamp, we expanded on the core DOM concepts we'd learnt, building a simple webpage that filters images according to a set of radio buttons and an optional search input box.</p>
<p>As with our previous session, it was an exercise set in multiple stages, and this really helped me recognise the roles of differents functionalities within the code, especially having introduced a number of event listeners.</p>
<p>I also aimed to have each function perform only one action (more on this in a future post!).</p>

<div id="accordion">
    <!-- Part 1 -->
    <div class="card">
        <div class="card-header" id="headingOne">
            <h5 class="mb-0">
                <button class="btn" type="button" data-bs-toggle="collapse" data-bs-target="#collapse1" aria-expanded="false" aria-controls="collapseExample">
                    Part 1
                </button>
        </div>
    </div>
    <div class="collapse" id="collapse1">
        <div class="card card-body">
            <ul>
                <li>Pick 4 animals and get 4 pictures of each animal (16 total)</li>
                <li>Create a HTML page containing a search input, 4 buttons (one for each animal), 1 more button labelled “Show All”</li>
                <li>Give each button a class of “buttonFilter”</li>
                <li>Add 16 containers with the animal images randomly spread out. Add a class that represents the animal</li>
            </ul>
        </div>
    </div>
    <!-- Part 2 -->
    <div class="card">
        <div class="card-header" id="headingOne">
            <h5 class="mb-0">
                <button class="btn" type="button" data-bs-toggle="collapse" data-bs-target="#collapse2" aria-expanded="false" aria-controls="collapseExample">
                    Part 2
                </button>
        </div>
    </div>
    <div class="collapse" id="collapse2">
        <div class="card card-body">
        <ul>
            <li>Add a second class to each container that is called “imageFilter”.</li>
            <li>Add an attribute to each button animal =”tiger” (Show all, animal =”all”)</li>
            <li>Add a variable const button = document.querySelectorAll(".buttonFilter");</li>
            <li>const images = document.querySelectorAll(".imageFilter");</li>
        </ul>        
        </div>
    </div>
    <!-- Part 3 -->
    <div class="card">
        <div class="card-header" id="headingOne">
            <h5 class="mb-0">
                <button class="btn" type="button" data-bs-toggle="collapse" data-bs-target="#collapse3" aria-expanded="false" aria-controls="collapseExample">
                    Part 3
                </button>
        </div>
    </div>
    <div class="collapse" id="collapse3">
        <div class="card card-body">
            <ul>
                <li>Loop through each button in the button array.</li>
                <li>Add an event listener for each button that looks for a click event</li>
                <li>Grab the animal attribute with animal = this.getAttribute("animal");</li>
            </ul>            
        </div>
    </div>
    <!-- Part 4 -->
    <div class="card">
        <div class="card-header" id="headingOne">
            <h5 class="mb-0">
                <button class="btn" type="button" data-bs-toggle="collapse" data-bs-target="#collapse4" aria-expanded="false" aria-controls="collapseExample">
                    Part 4
                </button>
        </div>
    </div>
    <div class="collapse" id="collapse4">
        <div class="card card-body">
            <ul>
                <li>Loop through each item in the images array</li>
                <li>If animal = all change all of the containers to display:block</li>
                <li>If animal = “tiger” then if the container contains the class tiger display:block otherwise display:none</li>
            </ul>
        </div>
    </div>
    <!-- Part 5 -->
    <div class="card">
        <div class="card-header" id="headingOne">
            <h5 class="mb-0">
                <button class="btn" type="button" data-bs-toggle="collapse" data-bs-target="#collapse5" aria-expanded="false" aria-controls="collapseExample">
                    Part 5
                </button>
        </div>
    </div>
    <div class="collapse" id="collapse5">
        <div class="card card-body">
            <ul>
                <li>Add a keyup event to the search box</li>
                <li>The text entered should be used to filter based on the image alt attribute (or use the src attribute if you have no alts)</li>
                <li>The selected filter button should also be taken into account</li>
            </ul>
        </div>
    </div>
    <!-- Part 6 -->
    <div class="card">
      <div class="card-header" id="headingOne">
          <h5 class="mb-0">
              <button class="btn" type="button" data-bs-toggle="collapse" data-bs-target="#collapse6" aria-expanded="false" aria-controls="collapseExample">
                  Part 6
              </button>
      </div>
  </div>
  <div class="collapse" id="collapse6">
      <div class="card card-body">
          <ul>
            <li>Add CSS classes that show which filter is currently selected by adding a border to the clickable element.</li>
            <li>Add some helper text above the images that says something like “showing animals that match the search “{searchString}” and the filter {filter}</li>
          </ul>
      </div>
  </div>        
</div>
<br>
<h2>My submission:</h2>
<a href="https://codepen.io/hannahbooth/pen/qBzRKLE" target="_blank">https://codepen.io/hannahbooth/pen/qBzRKLE</a>
<br><br>
