---
layout: archive
title: ""
permalink: teaching/
author_profile: true
---

<!-- Custom Styles for Page -->
<style>
  /* Style for the page container */
  .teaching-container {
    max-width: 1500px; /* Increase the width to 1500px for more space */
    margin: 0 auto; /* Center the container */
    padding: 20px; /* Add some padding */
    background-color: #f9f9f9; /* Light grey background for contrast */
    border-radius: 10px; /* Rounded corners for a softer look */
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1); /* Subtle shadow for depth */
  }

  /* Style for the heading */
  .teaching-container h2 {
    font-size: 32px; /* Larger font size for emphasis */
    font-weight: bold; /* Bold font for the heading */
    color: #1e3a8a; /* Dark blue color for the heading */
    text-align: center; /* Center-align the heading */
    margin-bottom: 30px; /* Space below the heading */
    background: linear-gradient(to right, #8e44ad, #1e90ff); /* Gradient text color */
    -webkit-background-clip: text; /* Clip the background to text */
    color: transparent; /* Transparent text to show gradient */
  }

  /* Style for the course list */
  .teaching-container ul {
    list-style-type: none; /* Remove default list styling */
    padding: 0; /* Remove padding */
  }

  .teaching-container li {
    font-size: 18px; /* Font size for course list */
    margin-bottom: 20px; /* Space below each list item */
    padding: 15px; /* Add padding for space */
    background-color: #ffffff; /* White background for contrast */
    border-left: 5px solid #8e44ad; /* Colored border on the left */
    border-radius: 5px; /* Rounded corners for a softer look */
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.05); /* Subtle shadow for depth */
    transition: transform 0.2s ease, box-shadow 0.2s ease; /* Smooth transition for hover effect */
  }
  .teaching-container li:hover {
    transform: translateY(-5px); /* Slight lift effect on hover */
    box-shadow: 0 8px 16px rgba(0, 0, 0, 0.1); /* Enhanced shadow on hover */
  }

  /* Style for course details */
  .teaching-container li p {
    margin: 5px 0; /* Margin for spacing between lines */
    line-height: 1.6; /* Increase line height for readability */
  }

  /* Style for professor and description text */
  .teaching-container .professor, .teaching-container .description {
    font-style: italic; /* Italicize for differentiation */
    color: #666666; /* Grey color for a softer look */
  }
  .teaching-container .gradient {
    font-weight: bold;
    background: linear-gradient(to right, #8e44ad, #1e90ff); /* Gradient colors */
    -webkit-background-clip: text; /* Clips the gradient to the text */
    -webkit-text-fill-color: transparent; /* Makes the text transparent to show the gradient */
    background-clip: text; /* Standard property for other browsers */
    color: transparent; /* Makes the text transparent to show the gradient */
 }

  /* Responsive design for mobile */
  @media (max-width: 600px) {
    .teaching-container {
      max-width: 95%; /* Adjust container width for mobile */
    }

    .teaching-container h2 {
      font-size: 28px; /* Smaller font size for mobile */
    }

    .teaching-container li {
      font-size: 16px; /* Smaller font size for list items */
    }
  }
</style>

<!-- Main Container -->
<div class="teaching-container">
  <h2>Courses Taught at University of California, Santa Cruz</h2>

  {% assign allclasses = site.data.teaching.main | where:'render', 'true' %}

  <ul>
    {% for class in allclasses %}
    <li>
      <span class="gradient">{{ class.course }} - {{ class.name }}</span> - {{ class.quarter }}, {{ class.designation }}<br>
      <span class="professor">With Prof. {{ class.prof | newline_to_br }}</span><br>
      <span class="description">{{ class.description | newline_to_br }}</span>
    </li>
    {% endfor %}
  </ul>
</div>

