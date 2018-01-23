---
layout: default
img: 
caption: Word vectors    
title: Homework 3 - Vector Semantics
active_tab: homework
release_date: 2018-01-24
due_date: 2018-01-31T11:00:00EST
attribution: Daphne Ippolito and Anne Cocos developed this homework assignment for UPenn's CIS 530 class in Spring 2018.
---


<!-- Check whether the assignment is up to date -->
{% capture this_year %}{{'now' | date: '%Y'}}{% endcapture %}
{% capture due_year %}{{page.due_date | date: '%Y'}}{% endcapture %}
{% if this_year != due_year %} 
<div class="alert alert-danger">
Warning: this assignment is out of date.  It may still need to be updated for this year's class.  Check with your instructor before you start working on this assignment.
</div>
{% endif %}
<!-- End of check whether the assignment is up to date -->

<div class="alert alert-info">
This assignment is due before {{ page.due_date | date: "%I:%M%p" }} on {{ page.due_date | date: "%A, %B %-d, %Y" }}.
</div>

Vector Semantics <span class="text-muted">: Assignment 3</span>
=============================================================

In this assignment you will implement many of the things you learned in chapter [15](https://web.stanford.edu/~jurafsky/slp3/15.pdf) of the textbook. If you haven't read it yet, now would be a good time to do that.

We will provide a small corpus of Shakespeare plays, which you will use to create a term-document matrix, a term-frequency matrix, and all of the derivations described in the textbook. Ultimately, your goal is to use the resulting vectors to measure play similarity and word similarity. All (or almost all) of the code you write will be direct implementations of concepts and equations described in chapter [15](https://web.stanford.edu/~jurafsky/slp3/15.pdf).

<div class="alert alert-info" markdown="1">
Here are the materials that you should download for this assignment:
* Some python code
* Data
</div>

Your Tasks
======================
All of the following are function stubs in the python code. You just need to fill them out.

Create matrices:
* fill out `create_term_document_matrix`
* fill out `create_term_context_matrix`
* fill out `create_PPMI_matrix`
* fill out `compute_tf_idf_matrix`

Compute similarities:
* fill out `compute_cosine_similarity`
* fill out `compute_jaccard_similarity`
* fill out `compute_dice_similarity`

Do some ranking:
* fill out `rank_plays`
* fill out `rank_words`

In the ranking tasks, play with different vector representations, and different similarity functions. Does one combination appear to work better than another? Do any interesting patterns emerge? Include this discussion in your writeup.


(Optional) Fun
=======================
So you've built some machinery that can measure similarity between words and documents. We gave you a Shakespeare corpus, but you can use any body of text you like. For example, check out [Project Gutenberg](https://www.gutenberg.org/) for public domain texts. The sky's the limit on what you can do, but here are some ideas:

* *Novel recommender system*. Maybe you enjoyed reading _Sense and Sensibility_ and _War and Peace_. Can you suggest some similar novels? Or maybe you need some variety in your consumption. Find novels that are really different.
* *Other languages*. Do these techniques work in other languages? Project Gutenberg has texts in a variety of languages. Maybe you could use this to measure language similarity?

Extra credit for playing around?


## Deliverables 
<div class="alert alert-warning" markdown="1">
Here are the deliverables that you will need to submit:
* writeup.pdf
* code (.zip). It should be written in Python 3.
</div>

## Recommended readings
* Jurafsky and Martin, chapter [15](https://web.stanford.edu/~jurafsky/slp3/15.pdf)