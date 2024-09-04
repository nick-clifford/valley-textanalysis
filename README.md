# Manifest

__Provenance:__
	The following data files come from the Valley of the Shadow digital archive as part of the Virginia Center for Digital History at the University of Virginia. Valley of the Shadow makes the site freely available for non-commercial uses in research, teaching, scholarship, and private study. Site users are responsible for any uses they make of materials on the site. Textual data was scraped from the site and cleaned to produce the files.

__Location:__
	https://valley.lib.virginia.edu/VoS/usingvalley/valleyguide.html

__Description:__ 
	The archive includes primary sources that describe the lives of people living in Augusta County, VA, and Franklin County, Pennsylvania, before, during, and after the American Civil War. The data used for this project includes only the letters and diary passages from the archive.

__Format:__ 
	Each letter/diary was scraped from the site in HTML format, cleaned, and converted to .txt files. Meta-data for each document is located in the header of the file, labeling the date, author, and county of the document. The body of the document includes the historical text as well as any transcribed annotations made by historians. There are 2 copies of the data: One is the text of the letters in their original form, and the other is the modernized spelling of the text. 

# Introduction: 
The Valley of the Shadow is a University of Virginia Library digital archive of primary 
sources, documenting the lives of people living in both Augusta County, Virginia, and Franklin 
County, Pennsylvania from before, during, and after the Civil War. In particular, these 
documents include historical letters and diary entries that have been transcribed into digital 
format. To gather this data, I created a web-crawler to scrape  documents from the 
archive and convert each document into a properly formatted text file, each with some 
associated metadata. From there, the files were pushed through a pipeline to create library and 
document tables, and subsequent token and vocabulary tables with additional fields appended 
later on. Before diving into the research methods, I display the summary statistics of the 
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

# Analysis Performed
- Principal Component Analysis
- Word Embeddings
- Sentiment Analysis (Emotion throughout the War)
