# valley-textanalysis

# Introduction: 
The Valley of the Shadow is a University of Virginia Library digital archive of primary 
sources, documenting the lives of people living in both Augusta County, Virginia, and Franklin 
County, Pennsylvania from before, during, and after the civil war. In particular, these 
documents include historical letters and diary entries that have been transcribed into digital 
format. To gather this data, I created a web-crawler to scrape  documents from the 
archive and convert each document into a properly formatted text file, each with some 
associated metadata. From there, the files were pushed through a pipeline to create library and 
document tables, and subsequent token and vocabulary tables with additional fields appended 
later on. Before diving into the research methods, I looked over the summary statistics of the 
data, and the term features of the corpus from these tables.

There are a total of 2,746 documents available on the site - I've limited the scope of this project
to only letter documents from Augusta and Franklin counties. The length of the letters is 
much shorter than that of a novel; the median total number of word tokens per document is 
402 tokens/doc. A little more than 90% of authors have 6 or fewer letters belonging to them, 
however, the other 10% make up around 60% of the total documents. There is also an 
imbalance of county labels with nearly 2/3s of the letters originating from Augusta, and the 
majority of documents were written on the eve/during the Civil War (1860-1865). 

With these features, I establish my OCHO model as follows: county, author, year, month, day, document, 
page, paragraph, sentence, and token. Finally, it should be noted that most documents have 
some amount of missing information (i.e. illegible words, unknown author/date, etc.), original 
spelling mistakes, and a modernized spelling version.
