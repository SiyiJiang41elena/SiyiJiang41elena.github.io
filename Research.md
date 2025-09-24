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
</style>

My current research focuses on:<br /> 
(1) Bilingual language control in **emotional** and **social** contexts (Jiang, Meng, & Chen, <a href="#jiang2024">2024</a>).<br /> 
(2) The interconnection between bilingual language control and **cognitive control** (also known as executive function or executive control) (Jiang, Ma, & Chen, <a href="#jiang2023">2023</a>, <a href="#jiang2024">2024</a>).<br /> 

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
      Jiang, S., Meng, Y., & Chen, B.† (2024). The impact of emotional states on bilingual language control in cued and voluntary switching contexts. <i>Journal of Memory and Language, 137</i>(19), 104527. <a href="https://doi.org/10.1016/j.jml.2024.104527">https://doi.org/10.1016/j.jml.2024.104527</a>
    </li>
    <li id="jiang2023">
      Jiang, S., Ma, L., & Chen, B.† (2023). Dynamic engagement of cognitive control in intra-sentential code-switching during comprehension. <i>Bilingualism: Language and Cognition, 26</i>(1), 62–77. <a href="https://doi.org/10.1017/S1366728922000323">https://doi.org/10.1017/S1366728922000323</a>
    </li>
    <li id="jiang2021">
      Jiang, S., & Lu, S.† (2021). Applications of eye movement boundary paradigm to lexical processing research. <i>Chinese Language in the World, 5</i>, 1-15. (in Chinese)<span style="font-size: smaller;">《边界范式在阅读中词汇加工机制研究中的应用》</span>
    </li>
    <li id="jiang2020">
      Jiang, S., Lu, S.†, & Wang, S. (2020). The processing of Chinese adhesive constructions in sentence reading: Evidence from word segmentation task. <i>Journal of Chinese Language Education, 18</i>(2), 1-21. (in Chinese)<span style="font-size: smaller;">《汉语母语者与二语者粘合式结构的词切分研究》</span>
    </li>
    <li id="lu2019">
      Lu, Z., Lu, S.†, & Jiang, S. (2019). The typological effect of the processing of N de V. <i>Chinese Language Learning, 3</i>, 78-86. (in Chinese)<span style="font-size: smaller;">《”n的v“结构认知加工的类型学效应研究》</span>
    </li>
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

  // Add event listener to handle the citation click and highlight the corresponding reference
  document.querySelectorAll('a').forEach(link => {
    link.addEventListener('click', function(e) {
      // Prevent default link behavior
      e.preventDefault();

      // Remove highlight from all references
      document.querySelectorAll('li').forEach(reference => {
        reference.classList.remove('highlight');
      });

      // Add highlight to the clicked reference
      const targetReference = document.querySelector(this.getAttribute('href'));
      targetReference.classList.add('highlight');

      // Scroll to the reference
      targetReference.scrollIntoView({ behavior: "smooth" });
    });
  });
</script>
