---
layout: archive
title: ""
permalink: awards/
author_profile: true
---

<!-- Custom Styles for Page -->
<style>
  /* Style for the page container */
  .awards-container {
    max-width: 1500px; /* Wide width for spacious layout */
    margin: 0 auto; /* Center the container */
    padding: 30px; /* Add padding for spacing */
    background-color: #f4f4f4; /* Light grey background for contrast */
    border-radius: 15px; /* Rounded corners for a modern look */
    box-shadow: 0 6px 12px rgba(0, 0, 0, 0.1); /* Slightly deeper shadow for emphasis */
  }

  /* Style for the headings */
  .awards-container h2 {
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

  /* Style for the list items */
  .awards-container ul {
    list-style-type: none; /* Remove default list styling */
    padding: 0; /* Remove padding */
  }

  .awards-container li {
    font-size: 20px; /* Slightly larger font size for readability */
    margin-bottom: 20px; /* Space below each list item */
    padding: 20px; /* Add padding for space */
    background-color: #ffffff; /* White background for contrast */
    border-left: 6px solid #8e44ad; /* Thicker colored border on the left */
    border-radius: 10px; /* Rounded corners for a softer look */
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.05); /* Subtle shadow for depth */
    transition: transform 0.2s ease, box-shadow 0.2s ease; /* Smooth transition for hover effect */
  }

  .awards-container li:hover {
    transform: translateY(-5px); /* Slight lift effect on hover */
    box-shadow: 0 8px 16px rgba(0, 0, 0, 0.1); /* Enhanced shadow on hover */
  }

  /* Responsive design for mobile */
  @media (max-width: 600px) {
    .awards-container {
      max-width: 95%; /* Adjust container width for mobile */
    }

    .awards-container h2 {
      font-size: 28px; /* Smaller font size for mobile */
    }

    .awards-container li {
      font-size: 18px; /* Smaller font size for list items */
    }
  }
</style>

<!-- Main Container -->
<div class="awards-container">
  <h2>Awards</h2>
  <ul>
    {% for award in site.data.awards.awards %}
    <li>
      <p><strong>{{ award.title }}</strong>, {{ award.event }}{% if award.year %}, {{ award.year }}{% endif %}</p>
    </li>
    {% endfor %}
  </ul>

  <h2>Grants and Fellowships</h2>
  <ul>
    {% for grant in site.data.awards.grants %}
    <li>
      <p>
        <strong>{{ grant.title }}</strong> for {{ grant.event }}
        {% if grant.location %} ({{ grant.location }}){% endif %}
        {% if grant.year %}, {{ grant.year }}{% endif %}
        {% if grant.duration %} - {{ grant.duration }}{% endif %}
      </p>
    </li>
    {% endfor %}
  </ul>
</div>

