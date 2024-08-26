---
layout: archive
title: ""
permalink: research/
author_profile: true
---

<!-- Custom Styles for Page -->
<style>
  /* Style for the page container */
  .publications-container {
    max-width: 1500px; /* Wide width for spacious layout */
    margin: 0 auto; /* Center the container */
    padding: 30px; /* Add padding for spacing */
    background-color: #f4f4f4; /* Light grey background for contrast */
    border-radius: 15px; /* Rounded corners for a modern look */
    box-shadow: 0 6px 12px rgba(0, 0, 0, 0.1); /* Slightly deeper shadow for emphasis */
  }

  /* Style for the headings */
  .publications-container h2 {
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
  .publications-container ul {
    list-style-type: none; /* Remove default list styling */
    padding: 0; /* Remove padding */
  }

  .publications-container li {
    font-size: 20px; /* Slightly larger font size for readability */
    margin-bottom: 20px; /* Space below each list item */
    padding: 20px; /* Add padding for space */
    background-color: #ffffff; /* White background for contrast */
    border-left: 6px solid #8e44ad; /* Thicker colored border on the left */
    border-radius: 10px; /* Rounded corners for a softer look */
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.05); /* Subtle shadow for depth */
    transition: transform 0.2s ease, box-shadow 0.2s ease; /* Smooth transition for hover effect */
  }

  .publications-container li:hover {
    transform: translateY(-5px); /* Slight lift effect on hover */
    box-shadow: 0 8px 16px rgba(0, 0, 0, 0.1); /* Enhanced shadow on hover */
  }

  /* Style for buttons */
  .publications-container button {
    background: linear-gradient(to right, #8e44ad, #e74c3c);
    border: none;
    color: white;
    padding: 8px 16px;
    text-align: center;
    text-decoration: none;
    display: inline-block;
    font-size: 14px;
    margin: 4px 2px;
    cursor: pointer;
    border-radius: 25px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    transition: background 0.3s ease, transform 0.3s ease;
  }

  .publications-container button:hover {
    transform: scale(1.05);
  }

  .publications-container a {
    color: #1e90ff; /* Link color to match the gradient */
    text-decoration: none; /* Remove underline from links */
    font-weight: bold; /* Bold links for emphasis */
  }

  .publications-container a:hover {
    text-decoration: underline; /* Underline links on hover for clarity */
  }

  /* Responsive design for mobile */
  @media (max-width: 600px) {
    .publications-container {
      max-width: 95%; /* Adjust container width for mobile */
    }

    .publications-container h2 {
      font-size: 28px; /* Smaller font size for mobile */
    }

    .publications-container li {
      font-size: 18px; /* Smaller font size for list items */
    }
  }
</style>

<!-- Main Container -->
<div class="publications-container">
  <h2>Peer-Reviewed Publications</h2>

  <ul>
    <li>
      <span style="font-size: 18px; font-weight: bold; color: #1e3a8a;">
        <a href="https://www.usenix.org/conference/usenixsecurity24/presentation/mondal" target="_blank">I/O-Efficient Dynamic Searchable Encryption meets Forward & Backward Privacy</a>
      </span><br>
      <span style="font-size: 16px; color: #333333;">**Priyanka Mondal**, Javad Ghareh Chamani, Ioannis Demertzis, and Dimitrios Papadopoulos</span><br>
      <i><font color="SlateBlue">Proceedings of the 33rd USENIX Security Symposium 2024 (<b>USENIX'24</b>)</font></i><br>
      <a href="https://www.usenix.org/system/files/usenixsecurity24-mondal.pdf" target="_blank">
        <button>PDF</button>
      </a>
      <a href="https://priyanka-mondal.github.io/BIBS/iodse.bib" download>
        <button style="background: linear-gradient(to right, #f1c40f, #e67e22);">BIB</button>
      </a>
      <a href="https://priyanka-mondal.github.io/PDFS/FinalUsenix2024.pptx" target="_blank">
        <button style="background: linear-gradient(to right, #2ecc71, #006400);">SLIDES</button>
      </a>
      <a href="https://github.com/yourusername/yourrepository/raw/main/your-video.mp4" target="_blank">
      <button style="background: linear-gradient(to right, #1e90ff, #4169e1);">VIDEO</button>
      </a>
    </li>

    <!-- Repeat similar structure for other publications -->
    
    <li>
      <span style="font-size: 18px; font-weight: bold; color: #1e3a8a;">
        <a href="https://content.iospress.com/articles/journal-of-computer-security/jcs230048" target="_blank">Flow-Limited Authorization for consensus, replication, and secret sharing</a>
      </span><br>
      <span style="font-size: 16px; color: #333333;">**Priyanka Mondal**, Maximilian Algehed, and Owen Arden</span><br>
      <i><font color="SlateBlue">Journal of Computer Security, 31st Volume (<b>JCS'23</b>)</font></i><br>
      <a href="https://priyanka-mondal.github.io/PDFS/FLAQRJCS.pdf" target="_blank">
        <button>PDF</button>
      </a>
      <a href="https://priyanka-mondal.github.io/BIBS/FLAQRJCS.bib" download>
        <button style="background: linear-gradient(to right, #f1c40f, #e67e22);">BIB</button>
      </a>
    </li>

  <!-- First Missing Entry -->
    <li>
    <span style="font-size: 18px; font-weight: bold; color: #1e3a8a;">
      <a href="https://ieeexplore.ieee.org/document/9919637" target="_blank">Applying consensus and replication securely with FLAQR</a>
    </span> (<b><font color="SlateBlue"><i>Distinguished Paper Award</i>🏆</font></b>)<br>
    <span style="font-size: 16px; color: #333333;">**Priyanka Mondal**, Maximilian Algehed, and Owen Arden</span><br>
    <i><font color="SlateBlue">Proceedings of the 35th IEEE Computer Security Foundations (<b>CSF'22</b>)</font></i><br>
    <a href="https://priyanka-mondal.github.io/PDFS/FLAQR_official.pdf" target="_blank">
      <button>PDF</button>
    </a>
    <a href="https://priyanka-mondal.github.io/BIBS/FLAQRCSF.bib" download>
      <button style="background: linear-gradient(to right, #f1c40f, #e67e22);">BIB</button>
    </a>
    </li>

  <!-- Second Missing Entry -->
    <li>
    <span style="font-size: 18px; font-weight: bold; color: #1e3a8a;">
      <a href="https://plas21.software.imdea.org" target="_blank">Applying consensus and replication securely with FLAQR</a>
    </span> (Precursor of <b>CSF'22</b> paper)<br>
    <span style="font-size: 16px; color: #333333;">**Priyanka Mondal**, Maximilian Algehed, and Owen Arden</span><br>
    <i><font color="SlateBlue">The 16th Workshop on Programming Languages and Analysis for Security (<b>PLAS'21</b>)</font></i><br>
    <a href="https://arxiv.org/abs/2205.04384" target="_blank" download>
      <button>PDF</button>
    </a>
    <a href="https://priyanka-mondal.github.io/BIBS/FLAQRPLAS.bib" download>
      <button style="background: linear-gradient(to right, #f1c40f, #e67e22);">BIB</button>
    </a>
    </li>

  <!-- Third Missing Entry -->
    <li>
    <span style="font-size: 18px; font-weight: bold; color: #1e3a8a;">
      <a href="https://dl.acm.org/doi/abs/10.1145/3357223.3365442" target="_blank">Vote them out: Detecting and eliminating byzantine peers</a>
    </span> (Extended abstract & Poster)<br>
    <span style="font-size: 16px; color: #333333;">Tuan Tran, **Priyanka Mondal**, Roy Shadmon, Manthan Mallikarjun, Peter Alvaro, and Owen Arden</span><br>
    <i><font color="SlateBlue">Proceedings of the 10th ACM Symposium on Cloud Computing (<b>SoCC'19</b>)</font></i><br>
    <a href="https://priyanka-mondal.github.io/PDFS/voteThemOut.pdf" target="_blank">
      <button>PDF</button>
    </a>
    <a href="https://priyanka-mondal.github.io/BIBS/voteThemOut.bib" download>
      <button style="background: linear-gradient(to right, #f1c40f, #e67e22);">BIB</button>
    </a>
    <a href="https://priyanka-mondal.github.io/PDFS/voteThemOut-poster.pdf" target="_blank">
      <button style="background: linear-gradient(to right, #2ecc71, #006400);">POSTER</button>
    </a>
    </li>



    <!-- Add other publications similarly -->

  </ul>

  <h2>Other Publications</h2>

  <ul>
    <li>
      <span style="font-size: 18px; font-weight: bold; color: #1e3a8a;">
        <a href="https://web.stevens.edu/csf2019/program.html" target="_blank">Flowstate: A Language for Secure Replicated Computation</a>
      </span> (Poster)<br>
      <span style="font-size: 16px; color: #333333;">**Priyanka Mondal** and Owen Arden</span><br>
      <i><font color="SlateBlue">32nd IEEE Computer Security Foundations (<b>CSF'19</b>)</font></i><br>
      <a href="https://priyanka-mondal.github.io/PDFS/CSF_2019_paper_6.pdf" target="_blank">
        <button>PDF</button>
      </a>
      <a href="https://priyanka-mondal.github.io/PDFS/Flowstate_Poster.pdf" target="_blank">
        <button style="background: linear-gradient(to right, #2ecc71, #006400);">POSTER</button>
      </a>
    </li>

    <li>
      <span style="font-size: 18px; font-weight: bold; color: #1e3a8a;">
        <a href="https://priyanka-mondal.github.io/PDFS/PriyankaMEThesis.pdf" target="_blank">Extended Atomicity Checking with Blame Assignment for Android Applications</a>
      </span><br>
      <span style="font-size: 16px; color: #333333;">**Priyanka Mondal**</span><br>
      <i><font color="SlateBlue">Thesis, Master of Engineering, Indian Institute of Science</font></i><br>
      <a href="https://priyanka-mondal.github.io/PDFS/PriyankaMEThesis.pdf" target="_blank">
        <button>PDF</button>
      </a>
      <a href="https://github.com/Priyanka-Mondal/AtomDroid" target="_blank">
        <button style="background: linear-gradient(to right, #1e90ff, #4169e1);">CODE</button>
      </a>
    </li>
  </ul>
</div>

<!-- Include script for copy function -->
<script>
function copyBib(name) {
    navigator.clipboard.writeText(name);
}
</script>

