---
title: "Research Page"
output: html_document
---

<style>
  /* Styling for the tabs container */
  .tabs {
    margin-bottom: 20px;
    display: flex; /* Use flex layout to align the buttons */
    border: 2px solid #ccc; /* Add border around the entire tabs container */
    border-radius: 5px; /* Optional rounded corners */
    height: 50px; /* Set the height of the container */
  }

  /* Styling for the tab buttons */
  .tab-button {
    font-size: 18px; /* Increase the font size */
    flex-grow: 1; /* Make the buttons take up equal space */
    text-align: center; /* Center the text in the button */
    padding: 10px 0; /* Adjust padding to lower the button height */
    background-color: #f0f0f0; /* Light grey background */
    border-right: 1px solid #ccc; /* Border between the buttons */
    cursor: pointer;
    transition: background-color 0.3s ease, color 0.3s ease; /* Smooth transition */
    color: black; /* Default text color for unselected tab */
  }

  /* Remove border for the last button */
  .tab-button:last-child {
    border-right: none;
  }

  /* Active tab button (selected state) */
  .tab-button.active {
    background-color: black; /* Black background for the active tab */
    color: white; /* White text on active tab */
    border-color: #333; /* Darker border when active */
  }

  /* Hover effect for the buttons */
  .tab-button:hover {
    background-color: #e0e0e0; /* Light grey when hovered */
  }

  /* Content area styling */
  .tab-content {
    display: none;
  }

  /* Show the active tab content */
  .tab-content.active {
    display: block;
  }

  /* Placeholder content for tabs */
  .placeholder-content {
    font-style: italic;
    color: #888;
  }
</style>

## Research

<div class="tabs">
  <button class="tab-button active" onclick="showTab('articles')">Peer-Reviewed Articles</button>
  <button class="tab-button" onclick="showTab('books')">Books</button>
  <button class="tab-button" onclick="showTab('conferences')">Conferences</button>
  <button class="tab-button" onclick="showTab('projects')">Projects</button>
</div>

<!-- Peer-Reviewed Articles Section -->
<div id="articles" class="tab-content active">
  <h3>Peer-Reviewed Articles († Corresponding author)</h3>
  
  <p><strong>First-Author:</strong></p>
  <ul>
    <li><strong>Jiang, S.</strong>, Meng, Y., & Chen, B.† (2024). The impact of emotional states on bilingual language control in cued and voluntary switching contexts. <i>Journal of Memory and Language, 137</i>(19), 104527. <a href="https://doi.org/10.1016/j.jml.2024.104527">https://doi.org/10.1016/j.jml.2024.104527</a></li>
    <li><strong>Jiang, S.</strong>, Ma, L., & Chen, B.† (2024). The role of cognitive control in bilingual language comprehension: An event-related potential study of dense code-switching sentences. <i>Bilingualism: Language and Cognition, 27</i>(1), 137–153. <a href="https://doi.org/10.1017/S1366728923000494">https://doi.org/10.1017/S1366728923000494</a></li>
    <li><strong>Jiang, S.</strong>, Ma, L., & Chen, B.† (2023). Dynamic engagement of cognitive control in intra-sentential code-switching during comprehension. <i>Bilingualism: Language and Cognition, 26</i>(1), 62–77. <a href="https://doi.org/10.1017/S1366728922000323">https://doi.org/10.1017/S1366728922000323</a></li>
    <li><strong>Jiang, S.</strong>, & Lu, S.† (2021). Applications of eye movement boundary paradigm to lexical processing research. <i>Chinese Language in the World, 5</i>, 1-15. (in Chinese)</li>
    <li><strong>Jiang, S.</strong>, Lu, S.†, & Wang, S. (2020). The processing of Chinese adhesive constructions in sentence reading: Evidence from word segmentation task. <i>Journal of Chinese Language Education, 18</i>(2), 1-21. (in Chinese)</li>
  </ul>

  <p><strong>Corresponding-Author:</strong></p>
  <ul>
    <li>Yang, S., <strong>Jiang, S.</strong>†, Jiang, M.†, & Guo, Q. (2024). Lexical pathway from L2 to L1 activation in intermediate proficient bilinguals: behavioral and ERP evidence. <i>Frontiers in Human Neuroscience, 18</i>(June), 1-13. <a href="https://doi.org/10.3389/fnhum.2024.1270377">https://doi.org/10.3389/fnhum.2024.1270377</a></li>
  </ul>

  <p><strong>Other:</strong></p>
  <ul>
    <li>Lu, Z., Lu, S.†, & <strong>Jiang, S.</strong> (2019). The typological effect of the processing of N de V. <i>Chinese Language Learning, 3</i>, 78-86. (in Chinese)</li>
  </ul>
</div>

<!-- Books Section -->
<div id="books" class="tab-content">
  <h3>Books</h3>
  
  <p>VanPatten, B., Keating G. D., & Wulff, S. (Eds.). (2021). <i>Theories in Second Language Acquisition: An Introduction.</i> (Lu, S., & <strong>Jiang, S.</strong>, Trans.). Beijing: China Commerce and Trade Press. (Original work published 2020).</p>
</div>

<!-- Conferences Section -->
<div id="conferences" class="tab-content">
  <h3>Conferences</h3>
  <p class="placeholder-content">Coming soon.</p>
</div>

<!-- Projects Section -->
<div id="projects" class="tab-content">
  <h3>Projects</h3>
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

  // Initialize to show the first tab by default
  document.getElementsByClassName("tab-button")[0].click();
</script>
