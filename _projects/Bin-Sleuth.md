---
layout: default
title:  "Meaningful Analysis of Malicious Binaries"
date:   2025-04-24
categories: [Python, Binary Ninja, Web Dev, Reverse Engineering, School Projects]
tags: [Python, Binary Analysis, Binary Ninja, Malware Analysis]
---

# In-Depth Analysis of Malware Using Django

This webapp is my third and final project for a Binary Program Analysis class. Going into this project, my goal was to build off of my previous project, CAPA-Match-Binja, increase the level of analysis, and present it to the user in a meaningful way. This is my first solo web-development project, so I know there are issues in the server handling.

<div class="hacker-nav-container">
  <style>
    /* These styles will only affect elements within .hacker-nav-container */
    .hacker-nav {
      display: flex;
      flex-wrap: wrap; /* Allows items to wrap onto a new line if needed */
      list-style: none;
      padding: 0;
      margin: 0;
    }

    .hacker-nav li {
      display: inline-block;
      margin-right: 15px;
      margin-bottom: 30px;
    }

    .hacker-nav li a {
      text-decoration: none;
      font-family: "Courier New", Courier, monospace;
      color: #b5e853;
      background-color: #151515;
      padding: 10px 20px;
      border: 2px solid #b5e853;
      border-radius: 3px;
      transition: all 0.3s ease;
    }

    .hacker-nav li a:hover {
      color: #151515;
      background-color: #b5e853;
    }
  </style>
  <ul class="hacker-nav">
    <li><a href="/mimikatz_sample">Sample Mimikatz Analysis</a></li>
  </ul>
</div>

## Current Functionality

### File-Level Information

1. Header Info
2. CAPA Matches
3. Section Entropy
4. Strings
5. Virus Total Score

### Function Level Information

1. Per-Function CAPA Matches
2. Disassembly
3. High Level Intermediate Language

## CORE DEPENDANCIES

Bin-Sleuth is heavily relient on Binary Ninja.  
A Paid Commercial Binary Ninja License is Required to run headless.

Additional python packages located in requirements.txt

## Sample Outputs

### CoreUtils-ls
![image](https://github.com/user-attachments/assets/6b72b7d9-fa8c-4c91-989f-152a45a5a804)

![image](https://github.com/user-attachments/assets/799c91da-abf2-4323-aa7d-a20d4e7e7aef)

### Mimikatz
![image](https://github.com/user-attachments/assets/abf2e3f4-8e52-4dc5-b6f7-cbdcb3c80599)

![image](https://github.com/user-attachments/assets/67632317-16ff-4498-b59b-a20cdf1464e8)
