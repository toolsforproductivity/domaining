---
layout: default
title: Available Domains Listing
---


## [<< Back to Tool][tool-link-ref]
{:.no_toc}

### [View the Results][keyword-techniques-result]
{:.no_toc}

* Table Of Contents
{:toc}

# Listing available domains with price

Here, we organize the various domains available with pricing for 
[keywords-techniques strategy][jamie-lewis-lists].
As available in the [results][keyword-techniques-result] page, the
possibilities are generated as per the keywords and techniques provided.
In this section, we list the available domains obtained.

## How to Use

The results obtained from the registrar, say [Godaddy][godaddy-bulk-search] are saved to the file

```
_data/enhancements/enhancements/keywords-and-techniques/available.csv
```
and the result is rendered below

### Result

<table>
<th>name</th><th>Price (USD)</th>
{%- for result in site.data.enhancements.keywords-and-techniques.available -%}
<tr>
	<td>{{ result.name  }}</td>
	<td style="text-align:right">
	{%- assign price_array = result.price | split: "." -%}
	{%- assign arr_len =  price_array | size -%}
	{% if  arr_len > 1 %}
		{{ result.price }}
	{%- else -%}	
		{{ result.price | append: ".00" }}		
	{% endif %}
	</td>
</tr>
{% endfor %}
</table>


[godaddy-bulk-search]: https://www.godaddy.com/en-in/domains/bulk-domain-search
[jamie-lewis-lists]: {{ site.baseurl }}{% link pages/jamie-lewis-overview.md %}#how-to-find-10-domain-and-sell-them-for- "Click to see the internal summary by Jamie Lewis"
[tool-link-ref]: {{ site.baseurl }}{% link strategies/keywords-and-techniques/tool.md %}
[keyword-techniques-result]: {{ site.baseurl }}{% link strategies/keywords-and-techniques/result.md %}

<hr />
### [View the Results][keyword-techniques-result]

## [<< Back to Tool][tool-link-ref]
{:.no_toc}
