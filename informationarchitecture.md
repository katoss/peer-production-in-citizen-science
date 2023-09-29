---
layout: page
title: Information Architecture
---
<p class="message">This guide is based on my experiences developing a knowledge management system with the personal science community. For more details, please see Chapter 4 of my <a href="">thesis</a><span><i> (thesis currently under review, link will be posted soon)</i></span>.</p>

<h2>Designing Information Architectures Using the “Card Sorting” Method</h2>

<a href="https://www.nngroup.com/articles/card-sorting-definition/">Card sorting</a> is a method from user experience research, that can help you to create the information architecture (i.e. the navigation menu) of a website, that fits with your users' expectations. This is especially useful if you have a lot of pages on your website.

On this page I <b>share the methods</b> I used to improve the information architecture for the <a href="{{ '/designthinking' | absolute_url }}">Personal Science Wiki</a>. There are commercial websites that offer these functionalities, but they usually have high subscription costs, but I used and developed free or low-cost tools, so that card sorting was also possible on a budget.

## Preparation
There are some things that need to be prepared beforehand:
* <b>Which method to use</b> (e.g., there is <a href="https://www.usability.gov/how-to-and-tools/methods/card-sorting.html">'open' and 'closed'</a> cardsorting. I used open cardsorting)
* <a href="https://blog.optimalworkshop.com/moderated-vs-online-card-sorting-best-friends/">Moderated or unmoderated</a> card sorting? Moderated card sorting is more informative, but take more time.
* <b>Which tools to use</b> (see data collection and data analysis below)
* <b>How many participants</b>, and who? It depends on the analysis method, time restrictions, target group
* Choosing a selection of <b>website titles to put on your cards</b>. They should be representative of the content. I also added some edge cases that were particularly interesting to me because they did not fit well into the current system
* Do you need <b>ethics approval</b>? If you do your research in an academic context, you might need to get in touch with your institutional review board before conducting your study. This process can take several months, so it is important to consider it!
* <b>Invite participants</b> and schedule sessions

## Data collection
* If you do <b>in-person sessions</b>, you can run card sorting with paper post-its (and then entering the data in a spreadsheet manually, in case you want to do quantitative analysis). 
* For <b>online sessions</b>, there are many different online tools. Free multi-purpose tools like Trello or Miro can be used for data collection, but you will also have to enter the data manually in spreadsheets for quantitative analysis. I used the tool <a href="https://kardsort.com/">kardSort</a>, which is dedicated to card sorting tasks, and lets you export the data as a .csv file. It is free for up to 10 cards. For bigger projects, a one-time payment of 25 Euros is due. 
* I did moderated online sessions, and ran the studies with Google Meet, asking the participants to share their screen and to share their thoughts out loud. I <b>recorded the sessions</b> with the recording function of Google Meet, and had them automatically transcribed with <a href="https://tactiq.io/">tactiq</a> (Attention: the transcription was an good help for me, but it needed a lot of manual correction).
* For a more detailed <b>study protocol</b>, you can check Chapter 4.2.2 of my thesis, and the ethics approval documents in the <a href="https://zenodo.org/record/8250059">supplementary materials</a> of my thesis (which includes the study protocol).

<figure>
  <img src="https://raw.githubusercontent.com/katoss/peer-production-in-citizen-science/main/assets/img/kardsort-screenshot.png" width="auto"/>
  <figcaption>
    Figure 1. A screenshot of the kardSort interface during a card sorting task. The left column (“Cards”) contains all cards that have not yet been sorted. All other columns are categories created and filled by the participant.

  </figcaption>
</figure>

## Data analysis
You can analyse card sorting tasks qualitatively and/or quantitatively. Both methods have advantages and disadvantages, and a combination will give you the most detailed insights. 

### Qualitative analysis
* This means you analyze the comments of your participants, and "eyeball" the categories they created, which cards they put together, and which cards they struggled with (See this paper for a useful guide on how to do qualitative analysis)
* You can take notes during or after the session, or record the session and analyze/take notes afterwards, trying to find interesting patterns.

### Quantative analysis
* This means you use statistical methods, like hierarchical cluster analysis, to determine information architecture that represents the average of all candidates.
* Many commercial tools have these functions integrated, but are quite costly.
* There is free software, notably Casolysis and SynCaps (they are also linked on the kardSort website). They do their job, but the downside is that they are windows-only, closed source, and no more maintained.
* If you know how to use Python, you can use the <a href="https://cardsort.readthedocs.io/en/latest/">Python package "cardsort"</a> that I developed for this purpose. It is free and open source, and can perform some basic standard analyses (distance matrix calculation based on hierarchical cluster analysis, dendrogram visualization, and extraction of user-generated cluster labels). Feel free to use and share it, and to give feedback if you like!

<figure>
  <img src="https://raw.githubusercontent.com/katoss/peer-production-in-citizen-science/main/assets/img/dendrogram.png" width="auto"/>
  <figcaption>
    Figure 2. Dendrogram visualizing the results of hierarchical cluster analysis of the card sorting outputs of all 20 participants (created with 'cardsort' python package). The different colors represent clusters of cards. 
  </figcaption>
</figure>

## Learning from the data
Both learning from the comments of the participants, as well as visualizations from quantitative analysis can help you inform your future information architecture. Which cards were often put together? Which labels did users give these clusters of cards? Is there a hierarchy (most tools don't allow hierarchies, but participants might have commented on it)? Are there maybe different mental models of information architectures that co-exist (maybe new users have other needs than frequent users)? Card sorting (unfortunately) cannot create the information architecture for you, but it can help you take informed decisions when developing it, oriented at your users needs, so they find what they are looking for.

## References
### Tools I used
* <a href="https://kardsort.com/">kardSort</a> (for data collection)
* <a href="https://cardsort.readthedocs.io/en/latest/">cardsort python package (for data analysis)</a>
* <a href="https://tactiq.io/">tactiq</a> (for transcription)
* Google Meet (for sessions and recordings)
### Further reading on card sorting method
* Donna Spencer. Card Sorting - Designing Usable Categories (https://rosenfeldmedia.com/books/card-sorting/)
* Otherwise, resources like Nielsen Norman Group and usability.gov have lots of material online!