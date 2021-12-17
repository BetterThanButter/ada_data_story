# AAAF Adventure
To check the posted verison visit:
`https://betterthanbutter.github.io/ada_data_story/`

## Executive summary
TODO 

## Introduction
Working with a text data could be very insightfull since the text data includes people ideas and thoughts. Unlike pictures and tabular data, text gives an opportunity to understand what is in people minds. The following project and ideas are based on the quotes dataset - Quotebank: A Corpus of Quotations from a Decade of News. This is a corpus of 178M quotations. The content was  extracted from 162 million English news articles published between 2008 and 2020. 

## Data overview

Since it is a news articles, especially in English it would be some features we should take into account. First of all, we decided to identify "sparsity" of the data. 

### AAAF Tips & Tricks
The idea is to somehow drop the tale of the data. Tale is a set of quotes which would be difficult to use to get any insights. In order to clean the data, we assume that each quote is a intersection of idea and a speaker. Then we would like to get rid of "tale" people or "tale" ideas - the set of people and topics with a low number of data points. The goal of this step is to reduce the data sample and to clean the data out of noize.

### Preliminary data analysis 
Initially our idea was to identify trends in social media, that is why we chose N topics and then filter the quotes with the tags. 
Tags was choosen randomly:

`"brexit","drugs","sexism","immigration","islam","ebola","pandemy","terrorism","home violence","meat consumption","vegetarian","feminism","harassment","darknet", "fraud","privacy","climate change","global warming","carbon emission","mental disease", "mental health","burn out",
"burnout"`.

After filering the quotes with these tags we obtain: 

{% include initial_analysis/overall_quotes_distribution.html %}

As a next step we decided to take a look into dataset trough the time. We plotted some of tags occurence trough the time:

{% include initial_analysis/tags_occurence_timeline.html %}

Let's take a more detailed look on this data. On the current step we can already observe some intersting insights about the data we have:

1. For all topics we have a dramatic decrease of quotes occcurence during June 2010 and also for January, March, June and November 2016. **As we have quite big set of tags and significant number of quotes we could conclude that it could be a problem of dataset.** It is important to take into account such a details for the future analysis.
2. Besides the issues with a couple of periods, the dataset provides as a very clear and reasonable data. For example we observe very high occurence of the `financial crisis` at the end of 2008 and in the beginning of 2020. These dates correspond to big financial cirsis at USA and COVID pandemy start resepctively.
3. The second interesting example is `brexit` tag that literally does not exist before the 2016 and afer shows a disruptive growth to one of the most popular.

### Data Enrichment
Previously we descibed the concept that each point in the dataset is a pair of the idea and the person who was quoted. Of course, there are a lot of the quotes without any sense, but in this case we could treat them as "idea-empty" phrases. In order to get more insights about the data we merged on of the data subsets ('climate-change') with a **WikiData API**. As a result we obtain personal data for the persons linked with the quote. In some cases several persons are associated with the quote, in such cases we use majority vote if possible or randomly in equivalent cases. 
### Identifying biases
As we know, the dataset was collected by parsing the data the news articles in English. It meanse that our dataset could be presentative only for the English-speakers part of the world. Our hypothesis is that big part of the content would be produced by USA and UK. In order to check thi bias we plot the quotes distribution by countries for `climate change` for 2008.

{% include initial_analysis/countries_distribution_climate_change_2008.html %}


As we can see, USA dominates in the dataset. Since the `climate change' is a very popular topic and we have also checked the distribution for other years we could be sure that **USA is presented the best in the dataset**

Moving further we decided to check the geographical data more precisely. We ploted the distribution of the States where people work or in case their work place in empty on WikiData we used place of birth. Inside-US geogaphical distribution is concentrated in Distric of Columbia - there Washington is located.


{% include initial_analysis/states_distribution_climate_change_2008.html %}

Washington is a heart of American democracy - there all senators and other politicians are doing their job. 

## Project Idea
Honestly speaking, the final idea of our project was born in the working process. Meeting different insights and constraints of the data, USA and especially Washington was evaluated as a place with high concentration of quotes. As we all know it's a city with a highest density of politicians. 

Politics is an essential part of many USA citizens and even not-USA people. That is why we have a lot of data from Washington and USA. In our analysis we would take into account USA Senat members from 2008 to 2020. Senat members are always eleceted from their native state and we expect them to talk about the native state problems and challenges. We collected data for around 200 senators here:
`https://docs.google.com/spreadsheets/d/1Viwlaz--L4lrQ-uO6yTGSvXYHHxTXi4JFCW6ar2_j10/edit?usp=sharing`
 
Based on the insights about the data and several assumptions we decided to move forward with a research in this area. More precisely we are going to evaluate different parties, states and senators activity. Also we are going to check how several topics are discussed by different states. This analysis would allow us to understand the activiy and biases of different state representative.  

## Basic analysis towards the Idea
Important to mention that we exclude `'Barack Obama', 'Donald Trump' and 'Joe Biden`' from data since when they was elected the number of quotes dramatically changed.
### Most talkative speakers
We ploted top 30 popular senators in the dataset:
{% include main_analysis/most_talkative_senators.html %}

As we can see both parties are well represented. Eventually, Bernie Sanders, being one of the independent senators generates so many quotes.  
### Parties representation
But what about parties in general? Democratic and Republican are opposite players in USA Senat. We discovered year-by-year total activity of both parties:
{% include main_analysis/parties_representation.html %}

It's clear from the data that from 2008 to the 2014 there is a clear advantage of Democratic party over the Republic one. Actually it is a Barack Obama president time, that period was very good for Democratic party, all important roles in the Senat was occupied by the Blue party.

### State activity
The next step in our analysis is to understand states activity. As an initial step we would like to check overall states activity as a number of quotes of Senators who represent the state.
{% include main_analysis/quotes_number_distrib_by_states.html %}


{% include main_analysis/quotes_number_distrib_by_states_education.html %}
{% include main_analysis/quotes_number_distrib_by_states_justice.html %}
{% include main_analysis/quotes_number_distrib_by_states_taxes.html %}
{% include main_analysis/quotes_number_distrib_by_states_weapons.html %}



**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)


Moving forward with our analysis we decided to look in details on the `climate change` topic. We build the subset for the next steps including the next three topics: `"climate change", "carbon emission", "global warming"` as all of these topics are related to the `climate change`. 



### An approach to the project
### Try to find trends and then check the correlations

## Data Processing
### 


## Initial Analysis of the dataset
### asdasd
#### 


## Hypothesis List

## Combining with external data























You can use the [editor on GitHub](https://github.com/BetterThanButter/ada_data_story/edit/gh-pages/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

<table>
    <tr>
        <td>Foo</td>
    </tr>
</table>



- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [Basic writing and formatting syntax](https://docs.github.com/en/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/BetterThanButter/ada_data_story/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.

{% include testing_slider.html %}
