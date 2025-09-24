---
layout: page
title: "Teaching"
---

<div class="tabs">
  <button class="tab-button active" onclick="showTab('home')">Home</button>
  <button class="tab-button" onclick="showTab('research')">Research</button>
  <button class="tab-button" onclick="showTab('teaching')">Teaching</button>
  <button class="tab-button" onclick="showTab('projects')">Projects</button>
</div>

<!-- Teaching Section -->
<div id="teaching" class="tab-content active">
  <h2>Teaching Experience</h2>

  <p><strong>Instructor, College English, Shanghai University of Finance and Economics</strong><br>
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <strong>Feb 2025 - Jun 2025</strong></p>

  <p><strong>Teaching Assistant, Advanced Chinese Writing, Peking University</strong><br>
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <strong>Sep 2018 - Jan 2019</strong><br>
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Instructor: Haiyan Li</p>

  <p><strong>Lecturer, Harvard Beijing Academy (HBA)</strong><br>
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <strong>Jul 2016 - Aug 2016</strong></p>
</div>

<script>
  // JavaScript for switching between tabs
  function showTab(tabName) {
    var i, tabContents, tabButtons;
    tabContents = document.getElementsByClassName("tab-content");
    tabButtons = document.getElementsByClassName("tab-button");

    for (i = 0; i < tabContents.length; i++) {
      tabContents[i].classList.remove("active");
    }

    for (i = 0; i < tabButtons.length; i++) {
      tabButtons[i].classList.remove("active");
    }

    document.getElementById(tabName).classList.add("active");
    event.currentTarget.classList.add("active");
  }
</script>

<style>
  /* Tab button styling */
  .tabs {
    margin-bottom: 20px;
    display: flex;
    border-radius: 10px;
    height: 40px;
    overflow: hidden;
  }

  .tab-button {
    font-size: 14px;
    flex-grow: 1;
    text-align: center;
    padding: 8px 0;
    background-color: #ffffff;
    border: 1px solid #ddd;
    border-right: none;
    color: #333;
    cursor: pointer;
    transition: all 0.3s ease;
    text-transform: capitalize;
    font-weight: 500;
  }

  .tab-button:last-child {
    border-right: none;
  }

  .tab-button:hover {
    background-color: #f4f4f4;
    border-color: #bbb;
    color: #000;
  }

  .tab-button.active {
    background-color: black;
    color: white;
    border-color: black;
    border-width: 2px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  }

  .tab-content {
    display: none;
  }

  .tab-content.active {
    display: block;
  }
</style>

