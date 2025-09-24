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

  .highlight {
    background-color: yellow;
    border: 2px solid #ff0000;
  }

  /* Smooth scroll behavior */
  html {
    scroll-behavior: smooth;
  }
</style>

My current research focuses on:<br /> 
(1) Bilingual language control in **emotional** and **social** contexts (Jiang, Meng, & Chen, 2024, JML).<br /> 
(2) The interconnection between bilingual language control and **cognitive control** (also known as executive function or executive control) (Jiang, Ma, & Chen, 2023, BLC; 2024, BLC).<br /> 

I mainly use electroencephalogram (EEG) and reaction time measures to investigate these topics. My work has been published in prestigious journals, such as <i>Journal of Memory and Language</i> and <i>Bilingualism: Language and Cognition</i>.


<div class="tabs">
  <button class="tab-button active" onclick="showTab('articles')">Articles</button>
  <button class="tab-button" onclick="showTab('books')">Books</button>
  <button class="tab-button" onclick="showTab('conferences')">Conferences</button>
  <button class="tab-button" onclick="showTab('projects')">Projects</button>
</div>

<!-- Articles Section -->
<div id="articles" class="tab-content active">
  (†) indicates the corresponding author
  <ul>
    <li id="jiang2024">
      Yang, S., <strong><span class="highlight-trigger">Jiang, S.</span></strong>†, Jiang, M.†, & Guo, Q. (2024). Lexical pathway from L2 to L1 activation in intermediate proficient bilinguals: behavioral and ERP evidence. <i>Frontiers in Human Neuroscience, 18</i>(June), 1-13. <a href="https://doi.org/10.3389/fnhum.2024.1270377">https://doi.org/10.3389/fnhum.2024.1270377</a>
    </li>
    <li id="jiang2024b">
      <strong><span class="highlight-trigger" data-target="#jiang2024b">Jiang, S.</span></strong>, Meng, Y., & Chen, B.† (2024). The impact of emotional states on bilingual language control in cued and voluntary switching contexts. <i>Journal of Memory and Language, 137</i>(19), 104527. <a href="https://doi.org/10.1016/j.jml.2024.104527">https://doi.org/10.1016/j.jml.2024.104527</a>
    </li>
    <li>
      <strong>Jiang, S.</strong>, Ma, L., & Chen, B.† (2024). The role of cognitive control in bilingual language comprehension: An event-related potential study of dense code-switching sentences. <i>Bilingualism: Language and Cognition, 27</i>(1), 137–153. <a href="https://doi.org/10.1017/S1366728923000494">https://doi.org/10.1017/S1366728923000494</a><span style="font-size: smaller;">    (Accepted with minor revision)</span>
    </li>
    <!-- other articles here -->
  </ul>
</div>

<!-- Books Section -->
<div id="books" class="tab-content">
  <ul>
    <li>VanPatten, B., Keating G. D., & Wulff, S. (Eds.). (2021). <i>Theories in Second Language Acquisition: An Introduction.</i> (Lu, S., & <strong>Jiang, S.</strong>, Trans.). Beijing: China Commerce and Trade Press. (Original work published 2020).</li>
  </ul>
</div>

<!-- Conferences Section -->
<div id="conferences" class="tab-content">
  <p class="placeholder-content">Coming soon.</p>
</div>

<!-- Projects Section -->
<div id="projects" class="tab-content">
  <p class="placeholder-content">Coming soon.</p>
</div>

<script>
  // JavaScript for switching between tabs
  function showTab(tabName) {
    var i, tabContents, tabButtons;
    tabContents = document.getElementsByClassName("tab-content");
    tabButtons = document.getElementsByClassName("tab-button");
    
    for (i = 0; i < tabContents.length; i++) {
      tabContents[i].style.display = "none";
    }
    
    for (i = 0; i < tabButtons.length; i++) {
      tabButtons[i].classList.remove("active");
    }
    
    document.getElementById(tabName).style.display = "block";
    event.currentTarget.classList.add("active");
  }

  // JavaScript for highlighting and scrolling to the clicked item
  document.querySelectorAll('.highlight-trigger').forEach(trigger => {
    trigger.addEventListener('click', function() {
      // Remove highlight from all items
      document.querySelectorAll('.highlight').forEach(item => {
        item.classList.remove('highlight');
      });
      
      // Highlight the clicked item
      var targetId = this.getAttribute('data-target');
      var targetItem = document.querySelector(targetId);
      targetItem.classList.add('highlight');
      
      // Scroll to the highlighted item
      targetItem.scrollIntoView({ behavior: 'smooth' });
    });
  });
  
  // Initialize to show the first tab by default
  document.getElementsByClassName("tab-button")[0].click();
</script>
