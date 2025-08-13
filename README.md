# RadioStarsBE.github.io
Radio Stars Website Maintenance

## Contact ##
[Contact me](mailto:{{ 'example@example.com' | encode_email }} "Contact me")

## Info ##

{% for post in site.posts %}
  Title : {{ post.title | xml_escape }}  
  Link : [{{ site.url }}{{ site.baseurl }}{{ post.url }}]({{ site.url }}{{ site.baseurl }}{{ post.url }})  
  ID : {{ site.url }}{{ site.baseurl }}{{ post.id }}  
  Update : {{ post.date | date_to_xmlschema }}  
  summary : {{ post.excerpt | xml_escape }}  
{% endfor %}

<div id="GitHubJSON" style="white-space: pre; font-family: monospace; background:#f0f0f0; padding:1em; border-radius:5px;"></div>  
<script>  
  // <!-- JSON "raw" injecté par Liquid dans une variable JS -->
  var data = {{ site.github | jsonify }};

  // <!-- Formatter et injecter dans le div -->
  document.getElementById('GitHubJSON').textContent = JSON.stringify(data, null, 2);  
</script>
