---
title: "Text Analysis President Bollinger's Commencement Speeches Part 1"
date: 2023-04-21
---
<p>For Advanced Analytic Techniques (GR5018), our second lab assignment had us carry out some analysis on texts of our choosing. Examples in class drew mostly from State of the Union addresses by US presidents, or other speeches by US politicians. I opted for something closer to home, and chose to look at the <a href="https://president.columbia.edu/content/speeches-archive">commencement addresses</a> of Columbia University’s president, Lee C. Bollinger. Bollinger will step down at the end of June 2023 after 21 years at the helm. My analysis was therefore on the incomplete “set” of addresses, but I do plan on revisiting after Commencement in a few weeks time. I also didn't carry out any topic modeling, which I would like to do. I can make some guesses about the topics that appear and reappear in his speeches; but it will be interesting to do the actual analysis.</p>
<p>I copied and pasted the text into an MSWord document and used the “Find and Replace” tool to clean up the text a bit before re-pasting into .txt files. I opted to use code to remove both stopwords (provided from the Natural Language Toolkit (NLTK) corpus) and punctuation.</p>

<p>We were asked to create a word cloud as part of the assignment, which I did using the WordCloud library.</p>
![word cloud](/docs/assets/bollinger_wordcloud.jpg)

<p>Then, I used the CountVectorizer method to obtain word frequencies. The output produced 5,166 columns representing the unique words found in his addresses. Bollinger is a distinguished scholar with deep and broad interests, which is reflected in his expansive vocabulary. I also looked at the correlation between his addresses. All values came in between 0.28 and 0.48, with the majority in the 0.3s. It appears Bollinger writes fairly original addresses every year. The most highly correlated addresses appear to be 2013 and 2015 (0.488097), and the least correlated addresses appear to be 2003 and 2020 (0.288031).</p>

<p>Next, I used the Textblob library to measure sentiment subjectivity and polarity. Textblob assigns a polarity score (between −1.0 and 1.0, where −1.0 is very negative and 1.0 is very positive) and a subjectivity score (between 0.0 and 1.0, where 0.0 is very objective and 1.0 is very subjective). From this analysis, we see that all of Bollinger's addresses have a polarity > 0.0, which makes sense, given that these are commencement addresses celebrating the accomplishments of our graduates. The addresses of 2007 and 2009 tie for highest polarity score of 1.0, and the address of 2020—the University's first-ever virtual commencement, 2 months after the <a href="https://www.nytimes.com/interactive/2022/nyregion/nyc-covid-timeline.html">arrival of Covid in New York</a>—has the lowest score of 0.14. The addresses of 2007 and 2009 also tie for the highest subjectivity score. The speech with the lowest subjectivity score is 2003, Bollinger's very first commencement address.</p>

<p>Finally, I conducted sentiment analysis across the entire length of each address, plotting the results as graphs. This first graph plots the first 19 addresses. The speech hitting the highest sentiment is 2013 (dark turquoise), and the lowest sentiment is 2017 (dark magenta).</p>
![sentiment progress plot 1](/docs/assets/bollinger_sentiment1.jpg)

<p>This next graph plots Bollinger’s longest and shortest addresses. The longest is from 2019 and celebrated what Bollinger called the ‘Centennial Class’ (The course Contemporary Civilization, considered the origins of the <a href="https://bulletin.columbia.edu/columbia-college/core-curriculum/">Core Curriculum</a>, was first established as an undergraduate requirement in 1919). The shortest address is the virtual address of 2020.</p>
![sentiment progress plot 2](/docs/assets/bollinger_sentiment2.jpg)
  
<p>This graph plots Bollinger's most volatile addresses.</p>
![sentiment progress plot 3](/docs/assets/bollinger_sentiment3.jpg)

<p>I am looking forward to taking a look at the complete “set.”</p>
<p>Next post: <a href="https://mf3321.github.io/2023/05/05/Democracy's-Data.html">Democracy's Data</a></p>
<p>Previous post: <a href="https://mf3321.github.io/2023/04/07/Escape-from-Model-Land.html">Escape From Model Land</a></p>
