# RadioStarsBE.github.io
Radio Stars Website Maintenance

## Info ##
<div id="jsonDisplay" style="white-space: pre; font-family: monospace; background:#f0f0f0; padding:1em; border-radius:5px;"></div>  

<script>  
  // <!-- JSON "raw" injecté par Liquid dans une variable JS -->
  var data = {{ site.github | jsonify }};
  
  // <!-- Formatter et injecter dans le div -->
  document.getElementById('jsonDisplay').textContent = JSON.stringify(data, null, 2);  
</script>
