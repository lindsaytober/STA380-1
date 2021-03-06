Flights at ABIA
===============

There comes a time in a person's life when he or she has to travel to a
place that is too far to reach by car, and there is no choice but to
resort to air travel. Unfortunately, air travel comes with a litany of
issues, some of which include overpriced food, long security lines, and
crying babies. Among all of the possible issues associated with air
travel, a delayed flight may be the most frustrating for customers.
Fortunately, by using flight data from all flights that either landed at
or departed from Austin-Bergstrom International Airport (APIA), we could
pick flights that have the least probability of getting delayed.

This analysis will address the following three questions that relate to
choosing flights that have the least likelihood of getting delayed:

-   What are the best times of the year and week to book air travel?
-   Which airlines have the most delays?
-   How does your destination impact the answers to the first 2
    questions?

For analysis purposes, we will assume any departure delay greater than
10 minutes to be a delayed flight regardless of what percentile this
number may be bucketed to. Even if 10 minutes is considered below
average for a flight during the Christmas season, a delay of 10 minutes
is still infuriating for the customer.

### Best Times to Travel (on Average)

To begin, let's understand the general trends of delayed flights. The
chart below shows how the time of year impacts the number of delayed
flights.

<img src="STA380_HW2_Yuan_Tober_files/figure-markdown_strict/delay_by_month_chart-1.png" style="display: block; margin: auto;" />

<table>
<thead>
<tr class="header">
<th align="left"></th>
<th align="right">% Flights Delayed during Month</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left">1</td>
<td align="right">18.7</td>
</tr>
<tr class="even">
<td align="left">2</td>
<td align="right">21.2</td>
</tr>
<tr class="odd">
<td align="left">3</td>
<td align="right">24.6</td>
</tr>
<tr class="even">
<td align="left">4</td>
<td align="right">17.2</td>
</tr>
<tr class="odd">
<td align="left">5</td>
<td align="right">20.5</td>
</tr>
<tr class="even">
<td align="left">6</td>
<td align="right">21.7</td>
</tr>
<tr class="odd">
<td align="left">7</td>
<td align="right">18.0</td>
</tr>
<tr class="even">
<td align="left">8</td>
<td align="right">18.4</td>
</tr>
<tr class="odd">
<td align="left">9</td>
<td align="right">11.0</td>
</tr>
<tr class="even">
<td align="left">10</td>
<td align="right">12.3</td>
</tr>
<tr class="odd">
<td align="left">11</td>
<td align="right">13.6</td>
</tr>
<tr class="even">
<td align="left">12</td>
<td align="right">25.4</td>
</tr>
</tbody>
</table>

<img src="STA380_HW2_Yuan_Tober_files/figure-markdown_strict/dealy_by_weekday_chart-1.png" style="display: block; margin: auto;" />

<table>
<thead>
<tr class="header">
<th align="left"></th>
<th align="right">% Flights Delayed by Day</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left">1</td>
<td align="right">19.1</td>
</tr>
<tr class="even">
<td align="left">2</td>
<td align="right">17.3</td>
</tr>
<tr class="odd">
<td align="left">3</td>
<td align="right">16.2</td>
</tr>
<tr class="even">
<td align="left">4</td>
<td align="right">20.6</td>
</tr>
<tr class="odd">
<td align="left">5</td>
<td align="right">22.4</td>
</tr>
<tr class="even">
<td align="left">6</td>
<td align="right">16.4</td>
</tr>
<tr class="odd">
<td align="left">7</td>
<td align="right">18.4</td>
</tr>
</tbody>
</table>

According to both of these charts, the month and day with the lowest
percentage of delayed flights is October and Saturday, respectively.
However, these percentages aggregate all destinations and airlines
together.

### Airlines to Avoid

Next, let's look at which airlines have the highest percentage of
delayed flights.

<img src="STA380_HW2_Yuan_Tober_files/figure-markdown_strict/delay_by_airline_chart-1.png" style="display: block; margin: auto;" />

<font size="0.5">\*\*\*US Airways data only available from
January-September 2008. October-December data is combined with American
Airlines due to a merger.</font>

The two worst airlines for delays are Atlantic Southeast Airlines and
Comair. In addition to those two, the percentage of flights with
departure delays in 2008 from seven different airlines exceeded 20%.

However, airlines don't have flights to every city and may specialize in
certain regions. For example, in 2008, Southwest Airlines did not have
any flights to New York City from Austin. If there are multiple airlines
that fly to a city, how can a customer know which airline to take? And
if that city has multiple airports, which airport should he or she
choose?

### Tale of Cities with Two Airports: Choosing the Best Airlines and Months to Travel

While customers usually have limited flexibility on travel dates, times,
and destinations, they often have most control over flight options when
traveling to a city with multiple airports (e.g., Dallas/Ft. Worth
metroplex is serviced by both DFW and Dallas Love Field).

Suppose customer 'Mary' has extended holiday time and is planning to
visit three cities, each of which has two major airports (New York City,
Dallas, and Chicago). Mary will be flying out of Austin and is looking
to minimize the chance of getting a delay for each of her trips. To
support her decision on when and how to fly to each city, she has three
questions:

-   For what months should Mary book her flights?
-   For each city, which airport should she fly to ?
-   Which airlines should she choose?

Charts of % departure delays, by month and airline, for each city she
plans to visit are shown below.

<center>
<h5>
% Flights to NYC with &gt;10 min Departure Delay by Airline
</h5>
</center>
<img src="STA380_HW2_Yuan_Tober_files/figure-markdown_strict/NYC plot-1.png" style="display: block; margin: auto;" />

<center>
<h5>
% Flights to DAL with &gt;10 min Departure Delay by Airline
</h5>
</center>
<img src="STA380_HW2_Yuan_Tober_files/figure-markdown_strict/Dallas plot-1.png" style="display: block; margin: auto;" />

<center>
<h5>
% Flights to Chicago with &gt;10 min Departure Delay by Airline
</h5>
</center>
<img src="STA380_HW2_Yuan_Tober_files/figure-markdown_strict/CHI plot-1.png" style="display: block; margin: auto;" />

According to these 3 groups of charts, September and October appear to
be the best times to fly, which is consistent with what the very first
chart of this analysis showed. However, the best airlines for each city
vary. Below is a sample itinerary that Mary could use:

<table>
<caption>Sample Itinerary</caption>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left">Airline and Airport</th>
<th align="left">Month</th>
<th align="left">Day of Week</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left">New York City</td>
<td align="left">JetBlue Airways JFK</td>
<td align="left">October</td>
<td align="left">Wednesday</td>
</tr>
<tr class="even">
<td align="left">Dallas</td>
<td align="left">American Airlines DFW</td>
<td align="left">November</td>
<td align="left">Tuesday</td>
</tr>
<tr class="odd">
<td align="left">Chicago</td>
<td align="left">Southwest Airlines MDW</td>
<td align="left">September</td>
<td align="left">Wednesday</td>
</tr>
</tbody>
</table>

Segmenting data to match the scope of the problem is extremely
important. In this case, the problem is figuring out which airlines to
take to cities that have 2 airports. For example, although Southwest
Airlines had the second-highest percentage of delayed flights when
including all of its destinations, its flights to Midway Airport in
Chicago are relatively punctual between June and September. However,
because this analysis only contains data fron 2008, one-off events such
as storms or emergencies may skew the data. Regardless of this
limitation, the general trends seem to be consistent: flights during the
holidays experience the most delays, and flights during the middle of
the week have the least delays. Beyond this, generalizations are
slightly harder to make.

Author Attribution
==================

Author attribution is one of the many applications of text analysis.
Given a group of documents by various authors, how accurately can we
predict the authorship of an out-of-sample document? Reuters, a
well-known news source, is a prime subject for conducting author
attribution analysis.

### Preparing the Data

The Reuters C50 corpus contains articles written by 50 different
authors, where each author has 50 'training' articles and 50 'testing'
articles. The training articles were used to build a Document Term
Matrix for predicting author attribution of the 50 testing articles.
This required some transformation of the data in pre-processing (e.g.,
changing case to all lowercase; removing numbers, punctuation, and
excess white-space; and eliminating 'stop words' that are common enough
in the English language to remove valuable insight for author
attribution) to allow for effective text analysis.

Given the training and testing data sets are two separate corpuses,
aligning the terms used in their Document Term Matrices to ensure
matching dimensions is critical to accurately modeling author
attribution. Establishing a single 'umbrella' term list for the two
corpuses requred a couple of assumptions. First, new terms existing in
articles from the testing data set (i.e., terms present in the testing
articles that are not present in the training articles) would not have
any weight indicators to assist in attributing the articles to a given
author, so these 'new' terms were excluded from the umbrella term list.
Second, terms present in the training articles that were not present in
the testing articles were kept in the umbrella term list as they were
used in building the model on the training data (e.g., for Naive Bayes,
the weight matrix is constructed using the bag of words model, which
required usage of all words to accurately build weights). This resulted
in approximately 10,000 irrelevant words for the test data set, but it
ensured that the weights of the common words were accurate for a given
document and author.

### Model Summary

Two models were selected to predict author attribution of the testing
articles: (1) Principal Component Multinomial Logistic Regression and
(2) Naive Bayes.

#### Model 1: Principal Component Multinomial Logistic Regression

Conducting Principal Compenent Analysis (PCA) on the training articles
provided contexts, or loadings, to apply to the Document Term Matrix.
Given each of the 50 authors had 50 articles included in the training
set, PCA resulted in 2,500 principal components to capture variance
across the 2,500 documents within the training corpus. With limitations
on computational power, the first 100 principal components were selected
for running multinomial logistic regression. This subset of 100
principal components accounted for 45% of the variance and still took a
significant time to process.

A multinomial logistic regression model was trained to predict authors
on the 100 principal components for all training articles, then applied
to the testing articles to predict author identities in the
out-of-sample data set. Multinomial logistic regression using PCA
resulted in a test accuracy of 65.46%.

#### Model 2: Naive Bayes

For Naive Bayes, the Document Term Matrix was used to create a training
table of multinomial probability vectors by author. Each multinomial
probability vector was calculated by aggregating the scores by term
across documents written by a given author, adding a smoothing factor
(1/2500) to ensure non-zero totals, and taking the respective
probability for that term against the author's full volume of terms. The
resulting multinomial probability vectors provide a 'bag of words'
situational probability of selecting that word at random from within the
host of articles written by that author.

Using the training table of multinomial probability vectors by author,
log probabilities for each article within the testing data set were
calculated under the Naive Bayes model. Whichever author resulted in the
highest sum of log probabilities was taken as the 'predicted' author.
The Naive Bayes model resulted in a test accuracy of 55.28%.

### Model Evaluation

Taken at face value, the Naive Bayes model outperformed the Principal
Component Multinomial Logistic Regression (PCR) model by almost 10%
(64.56% vs. 55.28%, respectively). However, model accuracy varied by
author:

<table>
<caption>Author Prediction Accuracy by Model</caption>
<thead>
<tr class="header">
<th align="left">Author</th>
<th align="left">NB Accuracy</th>
<th align="left">PCR Accuracy</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left">AaronPressman</td>
<td align="left">90.00 %</td>
<td align="left">88.57 %</td>
</tr>
<tr class="even">
<td align="left">AlanCrosby</td>
<td align="left">96.00 %</td>
<td align="left">75.00 %</td>
</tr>
<tr class="odd">
<td align="left">AlexanderSmith</td>
<td align="left">43.90 %</td>
<td align="left">58.73 %</td>
</tr>
<tr class="even">
<td align="left">BenjaminKangLim</td>
<td align="left">44.83 %</td>
<td align="left">38.24 %</td>
</tr>
<tr class="odd">
<td align="left">BernardHickey</td>
<td align="left">78.95 %</td>
<td align="left">65.52 %</td>
</tr>
<tr class="even">
<td align="left">BradDorfman</td>
<td align="left">61.76 %</td>
<td align="left">69.84 %</td>
</tr>
<tr class="odd">
<td align="left">DarrenSchuettler</td>
<td align="left">52.38 %</td>
<td align="left">46.88 %</td>
</tr>
<tr class="even">
<td align="left">DavidLawder</td>
<td align="left">34.62 %</td>
<td align="left">27.27 %</td>
</tr>
<tr class="odd">
<td align="left">EdnaFernandes</td>
<td align="left">89.29 %</td>
<td align="left">70.97 %</td>
</tr>
<tr class="even">
<td align="left">EricAuchard</td>
<td align="left">44.62 %</td>
<td align="left">67.27 %</td>
</tr>
<tr class="odd">
<td align="left">FumikoFujisaki</td>
<td align="left">98.00 %</td>
<td align="left">95.74 %</td>
</tr>
<tr class="even">
<td align="left">GrahamEarnshaw</td>
<td align="left">70.91 %</td>
<td align="left">85.37 %</td>
</tr>
<tr class="odd">
<td align="left">HeatherScoffield</td>
<td align="left">32.79 %</td>
<td align="left">34.62 %</td>
</tr>
<tr class="even">
<td align="left">JanLopatka</td>
<td align="left">58.33 %</td>
<td align="left">57.50 %</td>
</tr>
<tr class="odd">
<td align="left">JaneMacartney</td>
<td align="left">17.19 %</td>
<td align="left">26.44 %</td>
</tr>
<tr class="even">
<td align="left">JimGilchrist</td>
<td align="left">86.21 %</td>
<td align="left">89.09 %</td>
</tr>
<tr class="odd">
<td align="left">JoWinterbottom</td>
<td align="left">86.96 %</td>
<td align="left">91.67 %</td>
</tr>
<tr class="even">
<td align="left">JoeOrtiz</td>
<td align="left">50.68 %</td>
<td align="left">70.18 %</td>
</tr>
<tr class="odd">
<td align="left">JohnMastrini</td>
<td align="left">46.34 %</td>
<td align="left">45.21 %</td>
</tr>
<tr class="even">
<td align="left">JonathanBirt</td>
<td align="left">80.39 %</td>
<td align="left">72.86 %</td>
</tr>
<tr class="odd">
<td align="left">KarlPenhaul</td>
<td align="left">90.91 %</td>
<td align="left">83.87 %</td>
</tr>
<tr class="even">
<td align="left">KeithWeir</td>
<td align="left">69.70 %</td>
<td align="left">65.62 %</td>
</tr>
<tr class="odd">
<td align="left">KevinDrawbaugh</td>
<td align="left">62.50 %</td>
<td align="left">68.89 %</td>
</tr>
<tr class="even">
<td align="left">KevinMorrison</td>
<td align="left">60.42 %</td>
<td align="left">53.73 %</td>
</tr>
<tr class="odd">
<td align="left">KirstinRidley</td>
<td align="left">80.49 %</td>
<td align="left">74.07 %</td>
</tr>
<tr class="even">
<td align="left">KouroshKarimkhany</td>
<td align="left">91.49 %</td>
<td align="left">86.79 %</td>
</tr>
<tr class="odd">
<td align="left">LydiaZajc</td>
<td align="left">91.89 %</td>
<td align="left">77.27 %</td>
</tr>
<tr class="even">
<td align="left">LynneO'Donnell</td>
<td align="left">90.91 %</td>
<td align="left">81.82 %</td>
</tr>
<tr class="odd">
<td align="left">LynnleyBrowning</td>
<td align="left">87.72 %</td>
<td align="left">89.13 %</td>
</tr>
<tr class="even">
<td align="left">MarcelMichelson</td>
<td align="left">69.57 %</td>
<td align="left">78.95 %</td>
</tr>
<tr class="odd">
<td align="left">MarkBendeich</td>
<td align="left">72.34 %</td>
<td align="left">71.88 %</td>
</tr>
<tr class="even">
<td align="left">MartinWolk</td>
<td align="left">91.18 %</td>
<td align="left">65.38 %</td>
</tr>
<tr class="odd">
<td align="left">MatthewBunce</td>
<td align="left">97.78 %</td>
<td align="left">91.30 %</td>
</tr>
<tr class="even">
<td align="left">MichaelConnor</td>
<td align="left">84.62 %</td>
<td align="left">81.58 %</td>
</tr>
<tr class="odd">
<td align="left">MureDickie</td>
<td align="left">33.33 %</td>
<td align="left">40.82 %</td>
</tr>
<tr class="even">
<td align="left">NickLouth</td>
<td align="left">80.39 %</td>
<td align="left">85.00 %</td>
</tr>
<tr class="odd">
<td align="left">PatriciaCommins</td>
<td align="left">73.47 %</td>
<td align="left">70.83 %</td>
</tr>
<tr class="even">
<td align="left">PeterHumphrey</td>
<td align="left">44.58 %</td>
<td align="left">52.94 %</td>
</tr>
<tr class="odd">
<td align="left">PierreTran</td>
<td align="left">64.71 %</td>
<td align="left">61.54 %</td>
</tr>
<tr class="even">
<td align="left">RobinSidel</td>
<td align="left">88.10 %</td>
<td align="left">78.33 %</td>
</tr>
<tr class="odd">
<td align="left">RogerFillion</td>
<td align="left">90.91 %</td>
<td align="left">85.37 %</td>
</tr>
<tr class="even">
<td align="left">SamuelPerry</td>
<td align="left">64.15 %</td>
<td align="left">54.90 %</td>
</tr>
<tr class="odd">
<td align="left">SarahDavison</td>
<td align="left">44.44 %</td>
<td align="left">69.70 %</td>
</tr>
<tr class="even">
<td align="left">ScottHillis</td>
<td align="left">16.90 %</td>
<td align="left">21.74 %</td>
</tr>
<tr class="odd">
<td align="left">SimonCowell</td>
<td align="left">60.00 %</td>
<td align="left">51.79 %</td>
</tr>
<tr class="even">
<td align="left">TanEeLyn</td>
<td align="left">39.02 %</td>
<td align="left">38.18 %</td>
</tr>
<tr class="odd">
<td align="left">TheresePoletti</td>
<td align="left">67.27 %</td>
<td align="left">86.96 %</td>
</tr>
<tr class="even">
<td align="left">TimFarrand</td>
<td align="left">69.09 %</td>
<td align="left">65.71 %</td>
</tr>
<tr class="odd">
<td align="left">ToddNissen</td>
<td align="left">37.74 %</td>
<td align="left">29.63 %</td>
</tr>
<tr class="even">
<td align="left">WilliamKazer</td>
<td align="left">39.58 %</td>
<td align="left">48.78 %</td>
</tr>
</tbody>
</table>

As the chart shows, Naive Bayes showed the most benefit over PCR for
author Martin Wolk, with a test accuracy of 91.18% for NB and 65.39% for
PCR. On the flip side, PCR performed best over Naive Bayes for author
Sarah Davison, with a test accuracy of 69.70% for PCR and 44.44% for NB.
Aside from the biggest gaps in accuracy between the models, the chart
comparing model accuracy reveals that some authors had high success on
both models (e.g., Aaron Pressman, Fumiko Fujisaki) or low success on
both models (e.g., David Lawder, Jane Macartney). What might be driving
these issues?

We can start to assess this question by looking at the plot of authors
against the top two Principal Components:
<img src="STA380_HW2_Yuan_Tober_files/figure-markdown_strict/PCR_plot-1.png" style="display: block; margin: auto;" />

Authors 38 (Peter Humphrey) and 46 (Tan EeLyn) stand out as two authors
that are closer together in the plane of P1 x P2 but further away from
most of the other authors. Going back to the summary table, we see that
Tan EeLyn (author 46) had test accuracies of 39.02% for NB and 38.18%
for PCR. Given the close distance to 38, we can check the portion of
errors where test articles for author 46 were incorrectly attributed to
author 38. Out of 30 incorrect attributions for author 46, 15 documents
(or 50.00%) were attributed to author 38.

How does this interaction play out within the Naive Bayes model? For
Naive Bayes, 55.88% of the incorrect attributions for author 46 were to
author 38. Similar to the closer loadings of PC1 and PC2 under the PCR
model, we can confirm whether authors 46 and 38 have similar weights for
the Naive Bayes model. This is done easily by comparing the top 10 terms
from both of authors' multinomial probability vectors:

<table>
<caption>Top 10 Terms of Multinomial Probability Vector</caption>
<thead>
<tr class="header">
<th align="left">Author 46 (Tan EeLyn)</th>
<th align="left">Authors 38 (Peter Humphrey)</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left">beijing</td>
<td align="left">beijing</td>
</tr>
<tr class="even">
<td align="left">british</td>
<td align="left">british</td>
</tr>
<tr class="odd">
<td align="left">china</td>
<td align="left">china</td>
</tr>
<tr class="even">
<td align="left">chinas</td>
<td align="left">chinese</td>
</tr>
<tr class="odd">
<td align="left">chinese</td>
<td align="left">hong</td>
</tr>
<tr class="even">
<td align="left">hong</td>
<td align="left">kong</td>
</tr>
<tr class="odd">
<td align="left">kong</td>
<td align="left">kongs</td>
</tr>
<tr class="even">
<td align="left">kongs</td>
<td align="left">legislature</td>
</tr>
<tr class="odd">
<td align="left">legislature</td>
<td align="left">people</td>
</tr>
<tr class="even">
<td align="left">tungchan</td>
<td align="left">tungchan</td>
</tr>
</tbody>
</table>

Both lists of terms are very similar, which may explain why many of the
test articles for author 46 are attributed to author 38. Take, for
example, test article \#2261, which had the following term frequencies:

<table>
<caption>Top 10 Terms by Frequency for Test Article #2261</caption>
<thead>
<tr class="header">
<th align="left"></th>
<th align="right">Frequency in Document</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left">hong</td>
<td align="right">16</td>
</tr>
<tr class="even">
<td align="left">kong</td>
<td align="right">14</td>
</tr>
<tr class="odd">
<td align="left">legislature</td>
<td align="right">9</td>
</tr>
<tr class="even">
<td align="left">july</td>
<td align="right">6</td>
</tr>
<tr class="odd">
<td align="left">abode</td>
<td align="right">5</td>
</tr>
<tr class="even">
<td align="left">beijing</td>
<td align="right">5</td>
</tr>
<tr class="odd">
<td align="left">handover</td>
<td align="right">5</td>
</tr>
<tr class="even">
<td align="left">provisional</td>
<td align="right">5</td>
</tr>
<tr class="odd">
<td align="left">china</td>
<td align="right">4</td>
</tr>
<tr class="even">
<td align="left">june</td>
<td align="right">4</td>
</tr>
</tbody>
</table>

Many of these terms appear in the top 10 lists for authors 46 and 38. In
addition, the higher frequency of legislature in test article \#2261 may
have been one of the key drivers for attributing that document to author
46 instead of 38, as 'legislature' has a higher relative multinomial
probability for author 46.

While both models significantly improved the chances of correctly
attributing the author - up to 64.56% for NB and 55.28% for PCR from
1/50, or 2% at random - Naive Bayes did have a slightly higher test
accuracy. In addition, the results of the Naive Bayes model were easier
to interpret, given the 'bag of words' probabilities by term are more
intuitive than the contextual representation of Principal Components. As
such, we prefer to use the Naive Bayes model for author attribution.
Given there were only 50 articles from each author in the training data
set, we believe that the Naive Bayes model could be significantly
improved by including additional training articles to further
differentiate multinomial probability vectors between different authors.

</br>

Practice with Association Rule Mining
=====================================

Applying association rule mining to market baskets is a helpful method
to understand and predict market basket associations. For example,
pretend that 'Paul' is marketing director of a local grocery store. Paul
is interested in understanding the purchasing habits of the store's
customers to inform the new layout management is rolling out in the next
month. Specifically:

-   Which items should be located to the front of the store?
-   Which items should be grouped together (i.e., which items are
    customers more likely to buy together)?

These questions can be addressed using association rule mining, which
helps to predict additional items within a customer's basket
(consequents) given an initial set of market basket items (antecedents).

Taking transactional data on grocery purchases, we can run an 'apriori'
algorithm to give Paul the information he needs. To focus in on key
relationships, we will set thresholds as follows:

-   Support threshold &gt; 1%, to include only antecedents that show up
    in over 1% of all baskets (casting a wide net)
-   Confidence threshold &gt; 10%, to include only antecedents that have
    the associated consequents over 10% of the time
-   Max predictor items = 3, to include only antecedents with 3 or less
    items, as there is not sufficient shelf space to group a higher
    number of items

### Subset 1: Frequent Purchases

After running the algorithm, the first thing we notice is that eight
items have no antecedents:

<table>
<caption>Market Basket Rules with No Antecedents</caption>
<thead>
<tr class="header">
<th align="left">Rules</th>
<th align="right">Support</th>
<th align="right">Confidence</th>
<th align="right">Lift</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left">{} =&gt; {bottled water}</td>
<td align="right">0.1105236</td>
<td align="right">0.1105236</td>
<td align="right">1</td>
</tr>
<tr class="even">
<td align="left">{} =&gt; {tropical fruit}</td>
<td align="right">0.1049314</td>
<td align="right">0.1049314</td>
<td align="right">1</td>
</tr>
<tr class="odd">
<td align="left">{} =&gt; {root vegetables}</td>
<td align="right">0.1089985</td>
<td align="right">0.1089985</td>
<td align="right">1</td>
</tr>
<tr class="even">
<td align="left">{} =&gt; {soda}</td>
<td align="right">0.1743772</td>
<td align="right">0.1743772</td>
<td align="right">1</td>
</tr>
<tr class="odd">
<td align="left">{} =&gt; {yogurt}</td>
<td align="right">0.1395018</td>
<td align="right">0.1395018</td>
<td align="right">1</td>
</tr>
<tr class="even">
<td align="left">{} =&gt; {rolls/buns}</td>
<td align="right">0.1839349</td>
<td align="right">0.1839349</td>
<td align="right">1</td>
</tr>
<tr class="odd">
<td align="left">{} =&gt; {other vegetables}</td>
<td align="right">0.1934926</td>
<td align="right">0.1934926</td>
<td align="right">1</td>
</tr>
<tr class="even">
<td align="left">{} =&gt; {whole milk}</td>
<td align="right">0.2555160</td>
<td align="right">0.2555160</td>
<td align="right">1</td>
</tr>
</tbody>
</table>

These eight items are purchased on a fairly regular basis, so Paul
should recommend that management place these items in easy to find
places (e.g., eye level for refrigerated items) and put them towards the
front of the store to the extent possible.

### Subset 2: Strong Indicators

To address Paul's second question, we can focus on associations where
antecedents imply consequents with a lift greater than or equal to 2,
meaning that customers are at least twice as likely to buy the
consequent goods with the antecedent goods in their basket, and 50%
confidence, meaning that at least half of the customers with the
antecedent goods have the consequent goods in their baskets:

<table>
<caption>Market Basket Rules with Lift &gt;= 2 &amp; Confidence &gt;= 0.5</caption>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left">Rules</th>
<th align="right">Support</th>
<th align="right">Confidence</th>
<th align="right">Lift</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left">340</td>
<td align="left">{curd,yogurt} =&gt; {whole milk}</td>
<td align="right">0.0100661</td>
<td align="right">0.5823529</td>
<td align="right">2.279125</td>
</tr>
<tr class="even">
<td align="left">346</td>
<td align="left">{butter,other vegetables} =&gt; {whole milk}</td>
<td align="right">0.0114896</td>
<td align="right">0.5736041</td>
<td align="right">2.244885</td>
</tr>
<tr class="odd">
<td align="left">349</td>
<td align="left">{domestic eggs,other vegetables} =&gt; {whole milk}</td>
<td align="right">0.0123030</td>
<td align="right">0.5525114</td>
<td align="right">2.162336</td>
</tr>
<tr class="even">
<td align="left">358</td>
<td align="left">{whipped/sour cream,yogurt} =&gt; {whole milk}</td>
<td align="right">0.0108795</td>
<td align="right">0.5245098</td>
<td align="right">2.052747</td>
</tr>
<tr class="odd">
<td align="left">364</td>
<td align="left">{other vegetables,pip fruit} =&gt; {whole milk}</td>
<td align="right">0.0135231</td>
<td align="right">0.5175097</td>
<td align="right">2.025351</td>
</tr>
<tr class="even">
<td align="left">370</td>
<td align="left">{citrus fruit,root vegetables} =&gt; {other vegetables}</td>
<td align="right">0.0103711</td>
<td align="right">0.5862069</td>
<td align="right">3.029608</td>
</tr>
<tr class="odd">
<td align="left">385</td>
<td align="left">{root vegetables,tropical fruit} =&gt; {other vegetables}</td>
<td align="right">0.0123030</td>
<td align="right">0.5845411</td>
<td align="right">3.020999</td>
</tr>
<tr class="even">
<td align="left">388</td>
<td align="left">{root vegetables,tropical fruit} =&gt; {whole milk}</td>
<td align="right">0.0119980</td>
<td align="right">0.5700483</td>
<td align="right">2.230969</td>
</tr>
<tr class="odd">
<td align="left">394</td>
<td align="left">{tropical fruit,yogurt} =&gt; {whole milk}</td>
<td align="right">0.0151500</td>
<td align="right">0.5173611</td>
<td align="right">2.024770</td>
</tr>
<tr class="even">
<td align="left">403</td>
<td align="left">{root vegetables,yogurt} =&gt; {other vegetables}</td>
<td align="right">0.0129131</td>
<td align="right">0.5000000</td>
<td align="right">2.584078</td>
</tr>
<tr class="odd">
<td align="left">406</td>
<td align="left">{root vegetables,yogurt} =&gt; {whole milk}</td>
<td align="right">0.0145399</td>
<td align="right">0.5629921</td>
<td align="right">2.203354</td>
</tr>
<tr class="even">
<td align="left">409</td>
<td align="left">{rolls/buns,root vegetables} =&gt; {other vegetables}</td>
<td align="right">0.0122013</td>
<td align="right">0.5020921</td>
<td align="right">2.594890</td>
</tr>
<tr class="odd">
<td align="left">412</td>
<td align="left">{rolls/buns,root vegetables} =&gt; {whole milk}</td>
<td align="right">0.0127097</td>
<td align="right">0.5230126</td>
<td align="right">2.046888</td>
</tr>
<tr class="even">
<td align="left">430</td>
<td align="left">{other vegetables,yogurt} =&gt; {whole milk}</td>
<td align="right">0.0222674</td>
<td align="right">0.5128806</td>
<td align="right">2.007235</td>
</tr>
</tbody>
</table>

The primary insight from this information is that a number of different
items are good indicators that a customer will buy whole milk, though
most of the antecedents are either dairy or produce products. This is
likely because of the high percentage of baskets that included whole
milk (25%). Regardless, these indicators may still warrant a suggestion
to put the dairy products near produce.

### Subset 3: Stronger Indicators with More Frequent Purchases

However, some of these rules do not have very high support levels. We
can view a different segment that has at least 3% support, meaning that
the antecedent goods are in at least 3% of the baskets, lowering lift to
greater than or equal to 1.5 and confidence to greater than or equal to
0.3:

<table>
<caption>Market Basket Rules with Support &gt;= 0.03, Confidence &gt;= 0.3, &amp; Lift &gt;= 1.5</caption>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left">Rules</th>
<th align="right">Support</th>
<th align="right">Confidence</th>
<th align="right">Lift</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left">197</td>
<td align="left">{whipped/sour cream} =&gt; {whole milk}</td>
<td align="right">0.0322318</td>
<td align="right">0.4496454</td>
<td align="right">1.759754</td>
</tr>
<tr class="even">
<td align="left">216</td>
<td align="left">{pip fruit} =&gt; {whole milk}</td>
<td align="right">0.0300966</td>
<td align="right">0.3978495</td>
<td align="right">1.557043</td>
</tr>
<tr class="odd">
<td align="left">278</td>
<td align="left">{sausage} =&gt; {rolls/buns}</td>
<td align="right">0.0306050</td>
<td align="right">0.3257576</td>
<td align="right">1.771048</td>
</tr>
<tr class="even">
<td align="left">306</td>
<td align="left">{tropical fruit} =&gt; {other vegetables}</td>
<td align="right">0.0358922</td>
<td align="right">0.3420543</td>
<td align="right">1.767790</td>
</tr>
<tr class="odd">
<td align="left">308</td>
<td align="left">{tropical fruit} =&gt; {whole milk}</td>
<td align="right">0.0422979</td>
<td align="right">0.4031008</td>
<td align="right">1.577595</td>
</tr>
<tr class="even">
<td align="left">316</td>
<td align="left">{root vegetables} =&gt; {other vegetables}</td>
<td align="right">0.0473818</td>
<td align="right">0.4347015</td>
<td align="right">2.246605</td>
</tr>
<tr class="odd">
<td align="left">318</td>
<td align="left">{root vegetables} =&gt; {whole milk}</td>
<td align="right">0.0489070</td>
<td align="right">0.4486940</td>
<td align="right">1.756031</td>
</tr>
<tr class="even">
<td align="left">330</td>
<td align="left">{yogurt} =&gt; {other vegetables}</td>
<td align="right">0.0434164</td>
<td align="right">0.3112245</td>
<td align="right">1.608457</td>
</tr>
<tr class="odd">
<td align="left">332</td>
<td align="left">{yogurt} =&gt; {whole milk}</td>
<td align="right">0.0560244</td>
<td align="right">0.4016035</td>
<td align="right">1.571735</td>
</tr>
<tr class="even">
<td align="left">338</td>
<td align="left">{other vegetables} =&gt; {whole milk}</td>
<td align="right">0.0748348</td>
<td align="right">0.3867578</td>
<td align="right">1.513634</td>
</tr>
</tbody>
</table>

Whole milk is still a key item, further supporting the insights from the
first subset of rules. In addition, some new rules have surfaced given
the revised parameters, prompting the following potential
recommendations:

-   Put rolls/buns near saugages in refrigerated section to increase
    sales of these breakfast combos (related to rule \#278)
-   Put tropical fruit in a prime location to encourage purchasing of
    additional vegetables (related to rule \# 306)
-   Put root vegetables in a prime location to encourage purchasing of
    additional vegetables (related to rule \# 316)

### Subset 4: Highest Lift

One final subset might be to look at relationships with the largest lift
values, indicating antecedents that are most likely to increase the odds
of a consequent being in the same basket:

<table>
<caption>Market Basket Rules with 10 Highest Lift Values</caption>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left">Rules</th>
<th align="right">Support</th>
<th align="right">Confidence</th>
<th align="right">Lift</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left">342</td>
<td align="left">{whole milk,yogurt} =&gt; {curd}</td>
<td align="right">0.0100661</td>
<td align="right">0.1796733</td>
<td align="right">3.372304</td>
</tr>
<tr class="even">
<td align="left">371</td>
<td align="left">{citrus fruit,other vegetables} =&gt; {root vegetables}</td>
<td align="right">0.0103711</td>
<td align="right">0.3591549</td>
<td align="right">3.295046</td>
</tr>
<tr class="odd">
<td align="left">357</td>
<td align="left">{other vegetables,yogurt} =&gt; {whipped/sour cream}</td>
<td align="right">0.0101678</td>
<td align="right">0.2341920</td>
<td align="right">3.267062</td>
</tr>
<tr class="even">
<td align="left">386</td>
<td align="left">{other vegetables,tropical fruit} =&gt; {root vegetables}</td>
<td align="right">0.0123030</td>
<td align="right">0.3427762</td>
<td align="right">3.144780</td>
</tr>
<tr class="odd">
<td align="left">60</td>
<td align="left">{root vegetables} =&gt; {beef}</td>
<td align="right">0.0173869</td>
<td align="right">0.1595149</td>
<td align="right">3.040367</td>
</tr>
<tr class="even">
<td align="left">59</td>
<td align="left">{beef} =&gt; {root vegetables}</td>
<td align="right">0.0173869</td>
<td align="right">0.3313953</td>
<td align="right">3.040367</td>
</tr>
<tr class="odd">
<td align="left">370</td>
<td align="left">{citrus fruit,root vegetables} =&gt; {other vegetables}</td>
<td align="right">0.0103711</td>
<td align="right">0.5862069</td>
<td align="right">3.029608</td>
</tr>
<tr class="even">
<td align="left">385</td>
<td align="left">{root vegetables,tropical fruit} =&gt; {other vegetables}</td>
<td align="right">0.0123030</td>
<td align="right">0.5845411</td>
<td align="right">3.020999</td>
</tr>
<tr class="odd">
<td align="left">417</td>
<td align="left">{other vegetables,whole milk} =&gt; {root vegetables}</td>
<td align="right">0.0231825</td>
<td align="right">0.3097826</td>
<td align="right">2.842082</td>
</tr>
<tr class="even">
<td align="left">348</td>
<td align="left">{other vegetables,whole milk} =&gt; {butter}</td>
<td align="right">0.0114896</td>
<td align="right">0.1535326</td>
<td align="right">2.770630</td>
</tr>
</tbody>
</table>

This segment of rules with higher lift totals suggest a couple of
additional ideas for store layout:

-   Ensure curd is near the whole milk and yogurt (related to
    rule \#342)
-   Consider positioning some sour cream near vegetables and some near
    yogurt (related to rule \#357)
-   Promote 'meat and potatoes' (beef and root vegetable) pairings
    (related to rule \#60 and rule \#59)

### Conclusions

Overall, the discovered item sets make sense given the skew from items
that had strong representation across all market baskets (e.g., whole
milk, other vegetables). Additional market basket data could help to
improve confidence in some of the rules, if they hold true. As Paul
continues to collect market basket data, he should revise his
recommendations on product placement. If nothing else, this analysis
supports ensuring that the inventory of whole milk is stocked regularly
so that customers don't have to ask, 'Got Milk?'.

</br>
