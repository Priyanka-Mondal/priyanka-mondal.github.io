---
layout: archive
title: ""
excerpt: "Home"
permalink: /
author_profile: true
---

<style>

  a {
    color: Blue;
    text-decoration: none !important;
    &:hover {
      text-decoration: underline  !important;
    }
}
</style>

 <!--link rel="stylesheet" href="https://priyanka-mondal.github.io/styles.css"-->
<h2> Hello there !! Welcome to my personal website. </h2>  

Currently, I am working towards my PhD at [University of California, Santa Cruz(UCSC)](https://www.ucsc.edu/about/){:target="_blank"}. I am advised by [Prof. Owen Arden](https://owenarden.github.io/home/){:target="_blank"} and [Prof. Ioannis Demertzis](https://idemertzis.com){:target="_blank"}. 
My research lies in the intersection of security in distributed systems, language-based security,
and applied cryptography. I also have experience with Encrypted search, Compiler Design, Program Analysis, Blockchain Technologies and Formal Verification techniques in [Coq](https://coq.inria.fr/){:target="_blank"}. I work closely with the people from [Language, Systems, and Data Lab (LSD)](https://lsd.ucsc.edu){:target="_blank"}, and [Security Research Lab (SRL)](https://srl-ucsc.github.io/seminar.html){:target="_blank"}. At UCSC, I am a member of [Women in Cyber Security](https://www.wicys.org){:target="_blank"} 
and [Women in Science and Engineering](https://wiseucsc.wixsite.com/wise){:target="_blank"}, 
advocating for diversity and excellence in science and technology. Before joining UCSC, I worked as a software engineer for the Networking & Cloud team at [Citrix R&D, Bangalore](https://www.citrix.com){:target="_blank"}, for two years. Prior to that, 
I acquired a masters degree from the esteemed [IISc, Bangalore](https://iisc.ac.in){:target="_blank"}, where I worked with [Prof. Aditya Kanade](https://www.linkedin.com/in/aditya-kanade-572113139/){:target="_blank"} in the [Software Engineering and Analysis Lab](https://www.iisc-seal.net){:target="_blank"}, developing an automated bug detection [tool](https://drive.google.com/file/d/0B0yDXlBaWkDwamZoRnZDYTZlNTg/view?usp=drive_link&resourcekey=0-arHXT1Dx5MEKqy6SfSSdKA){:target="_blank"} for Android applications. 
I am also a proud alumna of [IIEST, Shibpur](https://www.iiests.ac.in){:target="_blank"}, where I did my undergraduate studies; 
during this time, I had the opportunity to work as a summer intern at [Nomura Research Institute, Kolkata](https://www.nrifintech.com){:target="_blank"}.

Through my work, I strive to make Distributed Systems fault-tolerant, secure, and efficient. 
Feel free to connect with me as I explore the world of Distributed Systems.

<!-- more -->

## News
{% assign allnews = site.data.somenews.main | where:'render', 'true' %}
{% for news in allnews -%}
- {{ news.date }} - {{ news.title }}
{% endfor %}
[All news>>](https://priyanka-mondal.github.io/news/)
