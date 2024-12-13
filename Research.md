---
title: "Research Page"
output: html_document
---

<style>
  /* Styling for the tabs container */
  .tabs {
    margin-bottom: 20px;
    display: flex; /* Use flex layout to align the buttons */
    border-radius: 10px; /* Rounded corners for the entire container */
    height: 40px; /* Lower the height of the container */
    overflow: hidden; /* Hide overflow to keep the design neat */
  }

  /* Styling for the tab buttons */
  .tab-button {
    font-size: 14px; /* Smaller font size */
    flex-grow: 1; /* Make the buttons take up equal space */
    text-align: center; /* Center the text in the button */
    padding: 8px 0; /* Reduce padding to make the buttons shorter */
    background-color: #ffffff; /* White background */
    border: 1px solid #ddd; /* Subtle border */
    border-right: none; /* Remove right border */
    color: #333; /* Dark text color */
    cursor: pointer;
    transition: all 0.3s ease; /* Smooth transition for all states */
    text-transform: capitalize; /* Capitalize only the first letter */
    font-weight: 500; /* Medium font weight */
  }

  /* Remove the right border for the last button */
  .tab-button:last-child {
    border-right: none;
  }

  /* Hover effect for the buttons */
  .tab-button:hover {
    background-color: #f4f4f4; /* Light grey background on hover */
    border-color: #bbb; /* Slightly darker border on hover */
    color: #000; /* Dark text color on hover */
  }

  /* Active tab button (selected state) */
  .tab-button.active {
    background-color: black; /* Black background for active tab */
    color: white; /* White text for the active tab */
    border-color: black; /* Black border for active tab */
    border-width: 2px; /* Slightly thicker border to highlight active tab */
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1); /* Light shadow for active tab */
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
  <button class="tab-button active" onclick="showTab('articles')">Peer-reviewed articles</button>
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
    <li><strong>Jiang, S.</strong>, & Lu, S.† (2021). Applications of eye movement boundary paradigm to lexical processing research. <i>Chinese Language in the World, 5</i>, 1-15. (in Chinese)<span style="font-size: smaller;">《句子阅读中汉语粘着构式的加工：来自词汇分割任务的证据》</span></li>
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
