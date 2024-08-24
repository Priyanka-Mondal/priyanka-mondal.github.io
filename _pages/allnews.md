---
layout: archive
title: ""
permalink: allnews/
author_profile: true
---

<!-- Custom Styles for All News Page -->
<style>
  /* Style for the main container */
  .news-container {
    max-width: 1500px; /* Wider layout for a spacious feel */
    margin: 0 auto; /* Center the container */
    padding: 40px; /* Padding for spacing */
    background-color: #f4f4f4; /* Light grey background for contrast */
    border-radius: 15px; /* Rounded corners for a modern look */
    box-shadow: 0 6px 12px rgba(0, 0, 0, 0.1); /* Subtle shadow for depth */
  }

  /* Style for the headings */
  .news-container h2 {
    font-size: 36px; /* Larger font size for emphasis */
    font-weight: bold; /* Bold font for the heading */
    text-align: center; /* Center-align the heading */
    margin-bottom: 30px; /* Space below the heading */
    background: linear-gradient(to right, #8e44ad, #1e90ff); /* Gradient text color */
    -webkit-background-clip: text; /* Clip the background to text */
    color: transparent; /* Transparent text to show gradient */
    text-transform: uppercase; /* Uppercase text for distinction */
    letter-spacing: 2px; /* Spacing between letters for a more open look */
  }

  /* Style for the news list */

  .news-container li {
    font-size: 18px; /* Font size for news items */
    margin-bottom: 10px; /* Space below each news item */
    padding: 10px; /* Padding for space */
    background-color: #ffffff; /* White background for news items */
    border-left: 6px solid #8e44ad; /* Colored border on the left */
    border-radius: 5px; /* Rounded corners for a softer look */
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.05); /* Subtle shadow for depth */
    transition: transform 0.2s ease, box-shadow 0.2s ease; /* Smooth transition for hover effect */
  }

  .news-container li:hover {
    transform: translateY(-3px); /* Slight lift effect on hover */
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1); /* Enhanced shadow on hover */
  }

  .news-container ul {
    list-style-type: none; /* Removes the bullets */
    padding-left: 0; /* Removes the default padding */
    margin: 0; /* Removes any margin */
  }



  /* Style for the back link */
  .back-link {
    display: block; /* Make it a block element */
    text-align: center; /* Center-align the text */
    margin-top: 30px; /* Space above the back link */
    font-size: 18px; /* Font size for the link */
    color: #1e90ff; /* Blue color for the link */
    text-decoration: none; /* Remove underline */
    font-weight: bold; /* Bold text for emphasis */
  }

  .back-link:hover {
    text-decoration: underline; /* Underline on hover */
  }

</style>

<!-- Main Container -->
<div class="news-container">
  <h2>News</h2>
  <ul>
    {% assign allnews = site.data.allnews.main %}
    {% for news in allnews %}
      <li>
        {{ news.date }} - 
        {% if news.link %}
          <a href="{{ news.link }}" target="_blank">{{ news.title }}</a>
        {% else %}
          {{ news.title }}
        {% endif %}
      </li>
    {% endfor %}
  </ul>

  <a href="https://priyanka-mondal.github.io/" class="back-link">&lt;&lt; Back</a>
</div>

