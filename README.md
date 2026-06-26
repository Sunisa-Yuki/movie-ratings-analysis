# Movie Runtime vs. Ratings

Do longer movies get worse ratings? That was the idea we wanted to test. The 
common assumption is that audiences get bored with long films and rate them lower, 
while critics don't care as much. We checked if that's actually true.

## The Question

Are longer runtimes linked to lower audience ratings but not critic ratings? And 
does that change depending on the decade or the age rating of the film?

## The Data

We built a dataset of 1,713 movies from 1920 to 2021, pulling streaming titles from 
Netflix, Hulu, Amazon Prime, and Disney+. We matched those with IMDb scores (for 
audiences) and Rotten Tomatoes scores (for critics).

Most of the cleaning work was turning messy runtime text into real numbers and 
grouping inconsistent age ratings into simple buckets (G, PG, PG-13, R).

## What We Found

The opposite of what we expected. Longer movies actually score slightly *higher* 
with both audiences and critics, not lower.

The link is weak but it's there, and it's positive for both groups:

- Audiences (IMDb): r = 0.117, R² = 0.013
- Critics (Rotten Tomatoes): r = 0.199, R² = 0.040

So the "people hate long movies" idea doesn't really hold up. Both groups react to 
runtime in almost the same way. The decade the movie came out didn't change this, 
and age rating barely predicted anything either.

## Limitations

The data leans heavily toward newer titles (lots of post-2015 stuff), online ratings 
have self-selection bias, and some short-form content got mixed in with full features. 
So I'd take the results as a starting point, not the final word.

## Tools

Python, pandas, NumPy, Matplotlib, Seaborn, scikit-learn, Jupyter

## My Role

This was a group project. On the technical side, I worked on collecting the data, 
cleaning and merging the streaming platform datasets, and the exploratory data 
analysis (boxplots of ratings by age rating). I also wrote the project abstract.

I also took on some of the team coordination, helping organize meeting times and 
divide tasks evenly across the group. During the EDA checkpoint, for instance, I 
helped distribute the plotting work among teammates so everyone had a clear part.

## Notes

Originally built as a group final project for COGS 108 at UC San Diego. This is a 
public copy for my portfolio. Data files aren't included since the original repo 
blocked large files. The four numbered notebooks walk through the full project from 
data cleaning to final analysis.
