---
layout: page
title: ""
---

<!-- Dropdown to select content -->
<select id="contentSelector" onchange="showContent()">
  <option value="articles">Peer-Reviewed Articles</option>
  <option value="books">Books</option>
</select>

<!-- Peer-Reviewed Articles Section -->
<div id="peerReviewedArticles">
  ## Peer-Reviewed Articles († Corresponding author)
  *First-Author:*
  - **Jiang, S.**, Meng, Y., & Chen, B.† (2024). The impact of emotional states on bilingual language control in cued and voluntary switching contexts. *Journal of Memory and Language, 137*(19), 104527. [https://doi.org/10.1016/j.jml.2024.104527](https://doi.org/10.1016/j.jml.2024.104527)<br> 
  - **Jiang, S.**, Ma, L., & Chen, B.† (2024). The role of cognitive control in bilingual language comprehension: An event-related potential study of dense code-switching sentences. *Bilingualism: Language and Cognition, 27*(1), 137–153. [https://doi.org/10.1017/S1366728923000494](https://doi.org/10.1017/S1366728923000494)<br> 
  - **Jiang, S.**, Ma, L., & Chen, B.† (2023). Dynamic engagement of cognitive control in intra-sentential code-switching during comprehension. *Bilingualism: Language and Cognition, 26*(1), 62–77. [https://doi.org/10.1017/S1366728922000323](https://doi.org/10.1017/S1366728922000323)<br> 
  - **Jiang, S.**, & Lu, S.† (2021). Applications of eye movement boundary paradigm to lexical processing research. *Chinese
  Language in the World, 5*, 1-15. (in Chinese)<br> 
  - **Jiang, S.**, Lu, S.†, & Wang, S. (2020). The processing of Chinese adhesive constructions in sentence reading: Evidence from word segmentation task. *Journal of Chinese Language Education, 18*(2), 1-21. (in Chinese)<br>

  *Corresponding-Author:*
  - Yang, S., **Jiang, S.**†, Jiang, M.†, & Guo, Q. (2024). Lexical pathway from L2 to L1 activation in intermediate proficient bilinguals: behavioral and ERP evidence. *Frontiers in Human Neuroscience, 18*(June), 1-13. [https://doi.org/10.3389/fnhum.2024.1270377](https://doi.org/10.3389/fnhum.2024.1270377)<br> 
</div>

<!-- Books Section -->
<div id="books" style="display:none;">
  ## Books
  VanPatten, B., Keating G. D., & Wulff, S. (Eds.). (2021). *Theories in Second Language Acquisition: An Introduction.* (Lu,
  S., & **Jiang, S.**, Trans.). Beijing: China Commerce and Trade Press. (Original work published 2020). 
</div>

<script>
  function showContent() {
    var selector = document.getElementById("contentSelector");
    var selectedValue = selector.value;
    
    // Hide both sections initially
    document.getElementById("peerReviewedArticles").style.display = "none";
    document.getElementById("books").style.display = "none";
    
    // Show the selected section
    if (selectedValue === "articles") {
      document.getElementById("peerReviewedArticles").style.display = "block";
    } else if (selectedValue === "books") {
      document.getElementById("books").style.display = "block";
    }
  }

  // Ensure the default content is visible on page load
  window.onload = function() {
    showContent();
  };
</script>
