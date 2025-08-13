# RadioStarsBE.github.io
Radio Stars Website Maintenance

## Contact ##
<a href="mailto:{{ 'example@example.com' | encode_email }}" title="Contact me">Contact me</a>

## Info ##

{% for post in site.posts %}
  <P>Title : {{ post.title | xml_escape }}<br />
  <div>Link : <a href="{{ site.url }}{{ site.baseurl }}{{ post.url }}">{{ site.url }}{{ site.baseurl }}{{ post.url }}</a></div>
  <div>ID : {{ site.url }}{{ site.baseurl }}{{ post.id }}</dic>
  <div>Update : {{ post.date | date_to_xmlschema }}</div>
  <div>summary : {{ post.excerpt | xml_escape }}</div></P>
{% endfor %}

<div id="GitHubJSON" style="white-space: pre; font-family: monospace; background:#f0f0f0; padding:1em; border-radius:5px;"></div>  
<script>  
  // <!-- JSON "raw" injecté par Liquid dans une variable JS -->
  var data = {{ site.github | jsonify }};

  // <!-- Formatter et injecter dans le div -->
  document.getElementById('GitHubJSON').textContent = JSON.stringify(data, null, 2);  
</script>
