---
layout: default
title: Tool for Keywords Techniques Strategy
jamie_lewis_two_list_godaddy: cXW2IYRhAxI
---

## [<< Back to Index]({{ site.baseurl }}{% link index.markdown %})
{:.no_toc}

* Table of Contents
{:toc}


# Keywords Techniques Tool

## Objective

To help in building the lists as per this [approach][jamie-lewis-lists] across categories.
It is a slight improvement on the approach suggested in the video with the added option
of organizing by categories. For each category (industry / sector / niche),
use relevant keywords and techniques.

## How It Works - Core Strategy

Steps to make it work (locally or on server)
+ Install [jekyll][jekyll] and run the server. Locally, the command would be

	```
	bundle exec jekyll serve
	```

+ Modify the data file(s) at `_data/keywords-and-techniques/`
  + See this [tutorial for yaml](https://idratherbewriting.com/documentation-theme-jekyll/mydoc_yaml_tutorial.html)
  + An example file is at `_data/keywords-and-techniques/category_1.yml` as below

```
category: category_1
keywords:
  - keyword1
  - keyword2
techniques:
  - technique1
  - technique2
  - technique3
```
+ Add a file for each category that you need as above.

+ View the output (a single web page) - [here][keyword-techniques-result]

+ Go to [GoDaddy Bulk Search][godaddy-bulk-search], search 
names from [the web page][keyword-techniques-result] to check availability.

[godaddy-bulk-search]: https://www.godaddy.com/en-in/domains/bulk-domain-search

## Enhancements

Check the [details][keyword-techniques-strategy] for a detailed explanation of the
strategy with advantages and limitations.
Let's look now at the helper tools for the various enhancements described 
in the above section. They are as listed below

+ Organize and list [available domains][available-domains-listing] with pricing

[jamie-lewis-lists]: {{ site.baseurl }}{% link pages/jamie-lewis-overview.md %}#how-to-find-10-domain-and-sell-them-for- "Click to see the internal summary by Jamie Lewis"
[keyword-techniques-strategy]: {{ site.baseurl }}{% link strategies/keywords-and-techniques/details.md %}
[keyword-techniques-result]: {{ site.baseurl }}{% link strategies/keywords-and-techniques/result.md %}
[available-domains-listing]: {{ site.baseurl }}{% link strategies/keywords-and-techniques/enhancements/available.md %}
[jekyll]: https://jekyllrb.com/

<hr />
### [View the Strategy][keyword-techniques-strategy]
{:.no_toc}

## [<< Back to Index]({{ site.baseurl }}{% link index.markdown %})
{:.no_toc}
