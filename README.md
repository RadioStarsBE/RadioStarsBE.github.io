# RadioStarsBE.github.io
Radio Stars Website Maintenance

## Contact ##
<a href="mailto:{{ 'example@example.com' | encode_email }}" title="Contact me">Contact me</a>

## Info ##
<div id="SiteJSON" style="white-space: pre; font-family: monospace; background:#f0f0f0; padding:1em; border-radius:5px;"></div>  
<br />
<div id="GitHubJSON" style="white-space: pre; font-family: monospace; background:#f0f0f0; padding:1em; border-radius:5px;"></div>  
<script>  
  // <!-- JSON "raw" injecté par Liquid dans une variable JS -->
  var data = {{ site | jsonify }};
  // <!-- Formatter et injecter dans le div -->
  document.getElementById('SiteJSON').textContent = JSON.stringify(data, null, 2);  
  // <!-- JSON "raw" injecté par Liquid dans une variable JS -->
  var data = {{ site.github | jsonify }};
  // <!-- Formatter et injecter dans le div -->
  document.getElementById('GitHubJSON').textContent = JSON.stringify(data, null, 2);  
</script>
