---
layout: archive
title: ""
permalink: talks/
author_profile: true
---

<!-- Custom Styles for Page -->
<style>
  /* Style for the page container */
  .talks-container {
    max-width: 1500px; /* Wider width for more space */
    margin: 0 auto; /* Center the container */
    padding: 20px; /* Add some padding */
    background-color: #f9f9f9; /* Light grey background for contrast */
    border-radius: 10px; /* Rounded corners for a softer look */
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1); /* Subtle shadow for depth */
  }

  /* Style for the headings */
  .talks-container h2 {
    font-size: 32px; /* Larger font size for emphasis */
    font-weight: bold; /* Bold font for the heading */
    color: #1e3a8a; /* Dark blue color for the heading */
    text-align: center; /* Center-align the heading */
    margin-bottom: 30px; /* Space below the heading */
    background: linear-gradient(to right, #8e44ad, #1e90ff); /* Gradient text color */
    -webkit-background-clip: text; /* Clip the background to text */
    color: transparent; /* Transparent text to show gradient */
    text-transform: uppercase; /* Uppercase text for distinction */
  }

  /* Style for the talk list */
  .talks-container ul {
    list-style-type: none; /* Remove default list styling */
    padding: 0; /* Remove padding */
  }

  .talks-container li {
    font-size: 18px; /* Font size for talk list */
    margin-bottom: 20px; /* Space below each list item */
    padding: 15px; /* Add padding for space */
    background-color: #ffffff; /* White background for contrast */
    border-left: 5px solid #8e44ad; /* Colored border on the left */
    border-radius: 5px; /* Rounded corners for a softer look */
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.05); /* Subtle shadow for depth */
    transition: transform 0.2s ease, box-shadow 0.2s ease; /* Smooth transition for hover effect */
  }
  .talks-container li:hover {
    transform: translateY(-5px); /* Slight lift effect on hover */
    box-shadow: 0 8px 16px rgba(0, 0, 0, 0.1); /* Enhanced shadow on hover */
  }

  /* Style for talk details */
  .talks-container li p {
    margin: 5px 0; /* Margin for spacing between lines */
    line-height: 1.6; /* Increase line height for readability */
  }

  /* Style for venue text */
  .talks-container .venue {
    font-style: italic; /* Italicize for differentiation */
    color: #666666; /* Grey color for a softer look */
    display: block; /* Display block to force new line */
    margin-top: 5px; /* Add some space above the venue */
  }

  /* Responsive design for mobile */
  @media (max-width: 600px) {
    .talks-container {
      max-width: 95%; /* Adjust container width for mobile */
    }

    .talks-container h2 {
      font-size: 28px; /* Smaller font size for mobile */
    }

    .talks-container li {
      font-size: 16px; /* Smaller font size for list items */
    }
  }
</style>

<!-- Main Container -->
<div class="talks-container">
  <h2>Conference Talks</h2>
  {% assign alltalks = site.data.talks.main | where:'render', 'true' | where:'type', 'con' %}

  <ul>
    {% for talk in alltalks %}
    <li>
      <strong>{{ talk.conf }}</strong> - {{ talk.title }}<br>
      <span class="venue">{{ talk.venue }}</span>
    </li>
    {% endfor %}
  </ul>

  <h2>Seminar Talks</h2>
  {% assign alltalks = site.data.talks.main | where:'render', 'true' | where:'type', 'seminar' %}

  <ul>
    {% for talk in alltalks %}
    <li>
      <strong>{{ talk.conf }}</strong> - {{ talk.title }}<br>
      <span class="venue">{{ talk.venue }}</span>
    </li>
    {% endfor %}
  </ul>
</div>

