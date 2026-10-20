# Tornado Text Analysis

Web Mining and Applied NLP | Project 01 | Beth Spornitz

## Overview

This project analyzes the vocabulary used in Wikipedia's article about tornadoes. The goal is to identify frequently used terms and explore how basic text cleaning affects the results.

## Data Source

The data comes from the [Wikipedia Tornado article](https://en.wikipedia.org/wiki/Tornado).

The Python script retrieves the article's HTML and extracts its text for analysis.

## Tools and Methods

- Python and Requests to retrieve the web page.
- BeautifulSoup to extract text from HTML.
- Text cleaning to convert words to lowercase, remove punctuation, and filter selected common words and Wikipedia reference terms.
- Polars to calculate word frequencies.
- Matplotlib and WordCloud to visualize the results.

## Results

The original tornado analysis contained 15,744 raw words and 9,706 cleaned words.

After adding a custom stop-word filter, 9,032 words remained.

The most frequent words included:

| Word | Frequency |
|---|---:|
| tornado | 324 |
| tornadoes | 224 |
| weather | 88 |
| national | 57 |
| storm | 57 |
| cloud | 55 |
| radar | 35 |
| damage | 34 |

### Tornado Word Frequency Chart

![Tornado Word Frequency Chart](images/tornado_word_frequency.png)

### Tornado Word Cloud

![Tornado Word Cloud](images/tornado_word_cloud.png)

The script completed successfully.

## Interpretation

The most frequent words reflect the article's focus on tornadoes and severe weather. Terms such as storm, cloud, radar, and damage are relevant to understanding tornado characteristics and impacts.

Removing common words and reference terms made the results easier to interpret. However, some unrelated terms and publication years still appear in the analysis.  I would need to refine further to make sure they were all removed.

## Limitations

This analysis uses only one Wikipedia article, so the results cannot represent all tornado-related information.

The text also includes Wikipedia navigation and references, which can affect word frequencies. The stop-word filter removes some of this noise but does not eliminate it completely.

Word frequency also measures how often terms appear in the article, not how frequently actual weather events occur.

## Next Steps

Future improvements could include analyzing multiple severe weather articles and removing references more precisely.

## Project Links

- [GitHub Repository](https://github.com/BethSpornitz/nlp-01-severe-weather)
- [Python Analysis Script](https://github.com/BethSpornitz/nlp-01-severe-weather/blob/main/src/nlp/web_words.py)
- [Wikipedia Data Source](https://en.wikipedia.org/wiki/Tornado)

## Project Resources

- [Project Instructions](project-instructions.md)
- [Glossary](glossary.md)
- [Professional Python Guide](https://denisecase.github.io/pro-analytics-02/)
