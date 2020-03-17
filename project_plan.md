# Project Plan v2

* Table of Contents
  * [Overview](#overview--arabic-learner-corpus-considerations)
  * [Data](#data)
  * [Analysis](#analysis)
  * [Presentation](#presentation)

## Overview: Arabic Learner Corpus Considerations
Turns out finding a corpus of written Levantine Arabic was way harder than anticipated, let alone
one that had any part-of-speech tagging already done. In my search for a usable corpus, I came
across the ["Arabic Learner Corpus"](https://www.arabiclearnercorpus.com/) which is freely 
downloadable for non-commercial use under a Creative Commons license. The curators of the
corpus note its potential usefulness in Second Language Acquisition (SLA) research, but
given the disparities in sample sizes and curious decision to lump together L1 Arabic
learners of Standard Arabic with non-L1 Arabic learners of Standard Arabic, I've
decided to take a closer look at these groups and see how useful or viable it really is.

## Data
The Arabic Learner Corpus contains XML files with rich metadata about the learner who
each data item was obtained from, including their age, gender identity, nationality,
L1 or non-L1 Arabic speaker status, and more. I plan to focus particularly on L1
and national origin for my analysis of these data, and plan to include a column
that will contain the general language family to which each learner's L1 belongs (the
current markdown only contains the specific language itself, but I think a more general
idea of the family would be useful as well). Metadata is also given for the genre of text
that the learner was producing (narrative or descriptive) as well as the general setting
(year, country, city) in which it was produced.

Sourcing has been accomplished thanks to the ready availability of the dataset from its
source above, but cleaning will likely be necessary to remove punctuation from the text
samples. I'm predicting difficulties here because I can't imagine NLTK's built-in tokenizer
can handle Arabic, so I'll probably have to find another option; the original `README` file
from the corpus notes the average text length, but I'd like to see if I reach the same conclusion
post-processing. In total, I plan to use all 1,585 files that this corpus contains, which
should be 282,732 words total. Thankfully, because these are XML files, the overall size should
still be relatively manageable in terms of computational processing load, and I'll likely be able
to upload the full dataset to GitHub, pending licensing clearance.

The biggest challenges will likely be 1) importing the data and reading from the XML format into
a `pandas DataFrame` object, and 2) handling text in a non-Roman script that is written from 
right-to-left.

## Analysis
Once I'm able to get the texts entered into a `DataFrame`, I plan to do some statistical tests
using various explanatory variables (L1, L1 family, nationality, etc.) to see how the learners
are patterning both within their own group and in comparison to other groups. Specifically, I am
very curious to see if the L1-Arabic Standard Arabic learner group is normally distributed or not.
It will also be important to consider the varying sample sizes for each group, as the number of 
L1 Arabic learners far outnumbers any other L1 group. The end goal, in essence, is to try and get
a sense of just how useful this corpus really is as a resource for research in SLA. As a rough 
"hypothesis," I am skeptical of the usefulness of this corpus to broader applications
beyond being a solid resource for people interested in acquisition of a prestige form of a language
(Standard Arabic) by both L1 members of that language's colloquiual variety and non-L1 learners from
other language backgrounds.

I would also be interested in training a classifier on data from the
L1 Arabic vs. Non-L1 Arabic group to see if it is capable of distinguishing between the two. While 
research in SLA holds that it is not a best practice to compare learners to native speakers
as a way of assessing proficiency or growth (but rather to compare them to other L2 learners), this
will nonetheless be a good way to get some practice in with building a simple yet (hopefully) effective
classifier.

## Presentation
All things considered, I'm imagining that this project will largely make use of the types of visualizations
that we've already been working with, particularly scatter plots, boxplots, and linear models of variance/dispersion.
It would be interesting to use the geographic data that's available through the XML format, but it's not one of my
priorities at the moment.


# ~Project Plan v1~
## ~~Overview~~
~~In vernacular Arabic, particularly the variety spoken in the Greater Syria/"Levant" region
(Syria, Lebanon, Jordan, Palestine, and partially Iraq), the "active participle" structure
is widely used to convey verbal meaning in the present progressive and habitual present.
Despite its prominence as a structural element of spoken Arabic, there remains little
research on its distribution or even much attention paid to its existence. The aim
of this project is to examine the distribution of active participle lexemes in
spoken Arabic, particularly regarding their distribution. Particular attention
will be paid to whether semantic characteristics of a given root meaning
play a role on when active participles are used to express verbal meanings
as opposed to more standard ideas of a "verb" in Arabic.~~

~~Ideally, an annotated corpus of spoken Arabic will be used for the purposes
of this project. Barring that, I plan on exploring ways that I could rely on
the structural characteristics of active participles to code them myself based
on data gathered from publicly-scrapable resources like Twitter and Reddit.~~