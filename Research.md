---
title: ""
output: html_document
---

I am broadly interested in how language interacts with cognition and emotion, particularly through the lens of 
<span class="tooltip"><b>bilingual language control</b>
  <span class="tooltiptext">For bilinguals, both languages are often active simultaneously, even when only one is required. This process could lead to frequent unintended cross-language intrusions, but such errors are rare in spontaneous speech and the laboratory. Therefore, a bilingual language control mechanism is proposed to allow bilinguals to select which language to use at a given moment and in a given context. This control mechanism also enables bilinguals to switch flexibly between languages during the same conversation.</span>
</span>.

<style>
  .tooltip {
    position: relative;
    display: inline-block;
    cursor: pointer;
    border-bottom: 1px dotted black; /* Adds a dotted underline */
  }

  .tooltip .tooltiptext {
    visibility: hidden;
    width: 400px; /* Adjust the width of the tooltip */
    background-color: #6c757d;
    color: #fff;
    text-align: center;
    border-radius: 5px;
    padding: 15px;
    position: fixed; /* Change position to fixed for centering */
    z-index: 9999;
    top: 50%; /* Position at the vertical center of the page */
    left: 50%; /* Position at the horizontal center of the page */
    transform: translate(-50%, -50%); /* Adjust the tooltip to be exactly centered */
    opacity: 0;
    transition: opacity 0.3s ease-in-out;
  }

  .tooltip:hover .tooltiptext {
    visibility: visible;
    opacity: 1;
  }

  /* Style for highlighted reference */
  .highlight {
    border: 2px solid #ff0000; /* Red border */
    padding: 10px;
    background-color: #ffe6e6; /* Light red background */
  }

  /* Smooth scroll behavior */
  html {
    scroll-behavior: smooth;
  }

  /* Tab Styles */
  .tabs {
    margin-bottom: 20px;
    display: flex; /* Use flex layout to align the buttons */
    border-radius: 10px; /* Rounded corners for the ent*
