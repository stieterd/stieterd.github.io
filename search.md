---
layout: page
title: Search
---
<!-- Html Elements for Search -->
<div id="search-container">
<input type="text" id="search-input" size="40" placeholder="search...">
<hr size="40">
<div style="margin: auto; width: 100%; padding: 10px;">
<ul id="results-container"></ul>
</div>
<hr size="40">
    
</div>

<!-- Script pointing to search-script.js -->
<script type="text/javascript" src="/assets/js/search-script.js"></script>

<!-- Configuration -->
<script>
SimpleJekyllSearch({
  searchInput: document.getElementById('search-input'),
  resultsContainer: document.getElementById('results-container'),
  json: '/search.json'
})
</script>