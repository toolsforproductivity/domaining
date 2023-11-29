---
layout: text
---
{% for data_hash in site.data.keywords-and-techniques %}
{% assign data = data_hash[1] %}
{% assign keywords = data.keywords %}
{% assign techniques = data.techniques %}

{%- assign first_iteration = true -%}
{%- assign results = "" -%}
{%- for keyword in keywords -%}
	{%- for technique in techniques -%}
		{%- assign currentValue = keyword | append: technique -%}
		{%- if first_iteration -%}
			{%- assign results = currentValue -%}
			{%- assign first_iteration = false -%}
		{%- else -%}
			{%- assign results = results | append: " " | append: currentValue -%}
		{%- endif -%}
	{%- endfor -%}
{%- endfor -%}

{%- assign res = results | split: " " %}
{%- assign content = res | join: "\n" %}

{%- for value in res -%}
	{%- assign idxMod = forloop.index | modulo: 3 -%}
	{{ value }} <br />
{%- endfor -%}
{%- endfor -%}


```
content
```
