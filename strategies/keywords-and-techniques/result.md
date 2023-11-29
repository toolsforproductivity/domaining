---
layout: default
title: Tool Results
---

## [<< Back to Tool][tool-link-ref]
{:.no_toc}


# By Category

Rendering the collection based on data provided at `_data/keywords-and-techniques/`

* Table Of Contents
{:toc}

{%- assign all_results = "nil" -%}
{% for data_hash in site.data.keywords-and-techniques %}
{% assign data = data_hash[1] %}
{% assign keywords = data.keywords %}
{% assign techniques = data.techniques %}

## {{ data.category }}

{%- if site.debugging -%}
### Keywords
<ul>
{% for x in keywords %}
  <li> {{ x }} </li>
{% endfor %}
</ul>

### Techniques
<ul>
{%- for x in techniques -%}
<li> {{ x }} </li>
{%- endfor -%}
</ul>
<hr />
### Result
{%- endif -%}

{%- assign first_iteration = true -%}
{%- assign results = "nil" -%}
{%- for keyword in keywords -%}
	{%- for technique in techniques -%}
		{%- assign currentValue = keyword | append: technique -%}
		{%- assign results = results | append: " " | append: currentValue -%}
		{%- assign all_results = all_results | append: " " | append: currentValue -%}			
	{%- endfor -%}
{%- endfor -%}

{%- assign res = results | split: " "  %}
{%- assign actual_res = res | slice: 1, res.size %}
{%- assign content = actual_res | join: "<br />" %}

<div style="align-self:center;max-width:351pt; max-height:91pt; overflow: scroll; border: 1.75px solid black; padding: 7px">
{{ content }}
</div>

{% endfor %}


{%- assign all_res = all_results | split: " " -%}
{%- assign all_content = all_res |slice: 1, all_res.size | join: "<br />" -%}

<br />
<hr />
# Across All Categories
<hr />
<br />
Collect all values from all categories in `_data/keyword-and-techniques`

<div style="align-self:center;max-width:315pt; max-height:195pt; overflow: scroll; border: 1.75px solid black; padding: 7px">
{{ all_content }}
</div>

<br />
<hr />
Next - [Listing Available Domains][available-domains-listing]
<br />

[tool-link-ref]: {{ site.baseurl }}{% link strategies/keywords-and-techniques/tool.md %}
<br />


[available-domains-listing]: {{ site.baseurl }}{% link strategies/keywords-and-techniques/enhancements/available.md %}


## [<< Back to Tool][tool-link-ref]
{:.no_toc}


