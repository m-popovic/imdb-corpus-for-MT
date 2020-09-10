# IMDB Corpus for Machine Translation

This data set is compiled from the publicly available "Large Movie Review Dataset" (http://ai.stanford.edu/~amaas/data/sentiment)
which contains 50,000 IMDb user movie reviews in English. 
The original data set is mainly intended for sentiment analysis research, so each review is associated with its binary 
sentiment polarity label "positive" or "negative". Negative reviews have a score <=4 out of 10, positive reviews have 
a score >=7 out of 10 and the reviews with more neutral ratings are not included. The overall distribution of labels is
balanced, namely 25,000 positive and 25,000 negative reviews. 
In the entire collection, no more than 30 reviews are allowed for any particular movie.

For our experiments, namely building a machine translation system for translating IMDb reviews from English into Serbian and Croatian, 
we kept 200 reviews (100 positive and 100 negative) containing about 2,500 sentences for testing purposes, and used the 
remaining 49,800 reviews (about 500,000 sentences) for training. 
Human translation of the test set into Serbian and Croatian, which is necessary for fast automatic evaluation of MT output, is currently 
in progress, and at the time of our first experiment (in April 2019) Serbian reference translations were available for 
33 test reviews (17 negative and 16 positive) containing 485 sentences (208 negative and 277 positive). The same set was translated into Croatian in July 2020 and added here.
These test sets are available here (**imdb.{positive,negative}.test.apr19.{en,sr,hr}**), and we will be adding more segments 
as soon as more translations are available.

For the sake of completness we also added the training set (**imdb.train.en.tgz**) into this repository 
(IMPORTANT NOTE: not a parallel data set! available only in English! We used back (forward) translation in our MT experiments)

If you use this data set, please cite our Balto-Slavic NLP Workshop paper (2019) which introduces its usage for 
Machine Translation of IMDB reviews from English into Serbian:

@InProceedings{imdb-mt2019,
  author    = {Pintu Lohar and Maja Popovi\'{c} and Andy Way},
  title     = {{Building English-to-Serbian Machine Translation System for IMDb Movie Reviews}},
  booktitle = {Proceedings of the 7th Workshop on Balto-Slavic Natural Language Processing (BSNLP 2019)},
  month     = {August},
  year      = {2019},
  address   = {Florence, Italy},
}


as well as the ACL 2011 paper which introduces the original corpus:

@InProceedings{maas2011,
  author    = {Maas, Andrew L.  and  Daly, Raymond E.  and  Pham, Peter T.  and  Huang, Dan  and  Ng, Andrew Y. and  Potts, Christopher},
  title     = {{Learning Word Vectors for Sentiment Analysis}},
  booktitle = {Proceedings of the 49th Annual Meeting of the Association for Computational Linguistics: Human 
  Language Technologies (ACL-HLT 2011)},
  month     = {June},
  year      = {2011},
  address   = {Portland, Oregon, USA},
  pages     = {142--150},
}

