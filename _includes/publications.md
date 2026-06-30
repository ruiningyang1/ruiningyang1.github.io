<h2 id="publications" style="margin: 2px 0px -15px;">Publications</h2>

<div class="publications">
<ol class="bibliography">

{% for link in site.data.publications.main %}

<li>
<div class="pub-row">
  {% if link.image %}
  <div class="col-sm-3 abbr" style="position: relative;padding-right: 15px;padding-left: 15px;">
    <img src="{{ link.image }}" class="teaser img-fluid z-depth-1" style="width=100;height=40%">
    {% if link.conference_short %} 
    <abbr class="badge">{{ link.conference_short }}</abbr>
    {% endif %}
  </div>
  {% endif %}
  <div class="col-sm-9" style="position: relative;padding-right: 15px;padding-left: 20px;">
      <div class="title">{% if link.pdf %}<a href="{{ link.pdf }}">{{ link.title }}</a>{% else %}{{ link.title }}{% endif %}</div>
      <div class="author">{{ link.authors }}</div>
      <div class="periodical"><em>{{ link.conference }}</em>
      </div>
    <div class="links">
      {% if link.pdf %} 
      <a href="{{ link.pdf }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">PDF</a>
      {% endif %}
      {% if link.code %} 
      <a href="{{ link.code }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Code</a>
      {% endif %}
      {% if link.page %} 
      <a href="{{ link.page }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Project Page</a>
      {% endif %}
      {% if link.bibtex %} 
      <a href="{{ link.bibtex }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">BibTex</a>
      {% endif %}
      {% if link.bibtex_text %} 
      <a class="btn btn-sm z-depth-0 bibtex-toggle" role="button" style="font-size:12px;cursor:pointer;">Cite</a>
      {% endif %}
      {% if link.notes %} 
      <strong> <i style="color:#e74d3c">{{ link.notes }}</i></strong>
      {% endif %}
      {% if link.others %} 
      {{ link.others }}
      {% endif %}
    </div>
    {% if link.bibtex_text %}
    <div class="bibtex hidden"><pre>{{ link.bibtex_text }}</pre></div>
    {% endif %}
  </div>
</div>
</li>

{% endfor %}

</ol>
</div>

<style>
.publications ol.bibliography li .bibtex pre {
  background: var(--global-code-bg-color, #f5f5f5);
  border: 1px solid var(--global-text-color-light, #cccccc);
  border-radius: 6px;
  overflow-x: auto;
  white-space: pre;
  margin-top: 8px;
  margin-bottom: 0;
}
</style>

<script>
(function () {
  document.querySelectorAll('.bibtex-toggle').forEach(function (btn) {
    btn.addEventListener('click', function () {
      var li = btn.closest('li');
      if (!li) return;
      var box = li.querySelector('.bibtex.hidden');
      if (box) box.classList.toggle('open');
    });
  });
})();
</script>
