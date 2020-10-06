# What is Natural Language Processing (NLP)?  
Natural Language Processing is a field that covers computer understanding and ma­nip­u­la­tion of human language. In simple terms, it means that making the computers understand the human native languages.  
# What is Natural Language Toolkit (NLTK)?  
This is a massively feature rich toolkit which can be used to perform NLP related functions and operations. Python is the platform used to build this library. The syntax of this toolkit is relatively simple and easy to learn as well.  
The following list contains other widely used tools for Natural Language Processing.  
1. Apache Lucene and Solr
2. Apache OpenNLP
3. GATE
4. Stanford’s Core NLP Suite
# How to install NLTK?  
Python is a must to be installed prior to the installation of NLTK. The following command can be used to install Python if you are on Linux or Mac.  
> sudo apt-get install python3  
If you are a windows user, you can use this link to download Python from the official website.  
Installation of NLTK to the workstation can be done using the following command. Bash or cmd.exe can be used to execute it.  
> pip install nltk
It is recommended that all components from NLTK is downloaded. This includes some sample text collections as well. Type the following text in a file and run it using python.  
''' import nltk    
nltk.download() '''  
This will pop a user interface which contains all the packages. Select them and click download.  
![image](https://miro.medium.com/max/581/1*Ey870pKTMadpGq0dS-yGJw.png)  
## How to run NLTK source files?  
This is done in the same way which python files are executed. Just save the source code with a “.py” extension. Then go into the directory of the files and execute “python <file_name>.py” from a cmd.exe or Bash.  
# What is a tokenizer?  
A tokenizer is a NLP function which can break a certain item into sub items (if possible) according to a set of given rules. For example, sentence tokenizers are used to break a collection of text into sentences while word tokenizers are used to break down text collections into words.  
In the following example, A collection of sentences are broken down into individual sentences.  
''' from nltk.tokenize import sent_tokenize  
sample_text = “Far far away, behind the word mountains, far from the countries Vokalia and Consonantia, there live the blind texts. Separated they live in Bookmarksgrove right at the coast of the Semantics, a large language ocean. A small river named Duden flows by their place and supplies it with the necessary regelialia. It is a paradisematic country, in which roasted parts of sentences fly into your mouth. ”  
tokenized_sentences = sent_tokenize(sample_text)
print(tokenized_sentences) '''
![image](https://miro.medium.com/max/638/1*8K5RRgfZYt5yP-L3wzBfhg.png)
The output is as below.  
The example presented below is shows a collection of sentences broken down into words.  
''' from nltk.tokenize import word_tokenize
sample_text = “Far far away, behind the word mountains, far from the countries Vokalia and Consonantia, there live the blind texts. Separated they live in Bookmarksgrove right at the coast of the Semantics, a large language ocean. A small river named Duden flows by their place and supplies it with the necessary regelialia. It is a paradisematic country, in which roasted parts of sentences fly into your mouth. ”
tokenized_words = word_tokenize(sample_text)
print(tokenized_words) '''
![image](https://miro.medium.com/max/640/1*xzYcIOhnVCd1k1uBT7xhnw.png)  
The corresponding output for the operation is as below.  
# What are stopwords?  
Stopwords are words which do not carry much meaning to the analysis of text. These words are used only to fill the gap between words.  
NLTK has a number of stopwords listed under the “nltk.corpus”. The language of required stopwords must be defined prior to using the tool.  
The following code lists all the stopwords in the english language.  
''' from nltk.corpus import stopwords
stop_words = set(stopwords.words(‘english’))
print(stop_words) '''  
And the output is as below.  
![image](https://miro.medium.com/max/639/1*fmgVQR4IO7rzi42ofkJovQ.png)  
It is common practice that removal of these words are done prior to analyzing the text.  
#What is Part of Speech (POS) tagging?  
This is classifying words into parts of speech of an assigned language. For example a certain word can be a noun or a verb or something else. This feature is very powerful and is massively helpful for further analysis.  
The following example code snippet outputs the POS tags of the sample text which was used throughout the blog post. The entire text is broken to sentences in the initial step. Every individual sentence is taken and tokenized into words. These words are finally fed into the parts of speech tagger.
''' import nltk  
from nltk.tokenize import sent_tokenize, word_tokenize  
sample_text = “Far far away, behind the word mountains, far from the countries Vokalia and Consonantia, there live the blind texts. Separated they live in Bookmarksgrove right at the coast of the Semantics, a large language ocean. A small river named Duden flows by their place and supplies it with the necessary regelialia. It is a paradisematic country, in which roasted parts of sentences fly into your mouth.”  
tokenized_sentences = sent_tokenize(sample_text)  
for sentence in tokenized_sentences :  
tokenized_words = word_tokenize(sentence)  
tagged_words = nltk.pos_tag(tokenized_words)  
print(tagged_words) '''
Execution of this outputs the following result.  
![image](https://miro.medium.com/max/643/1*WrA7eI5z35rnn_SWd6BOgA.png)  
Unlike the previous examples of tokenizers and stopwords, this outputs tuples. The first element of the tuple is the word while the second part is the POS tag. Some example of POS tags are listed below. You can access the full list by [!clicking here.](https://www.ling.upenn.edu/courses/Fall_2003/ling001/penn_treebank_pos.html)
![image](https://miro.medium.com/max/389/1*sReyvS29xlcibWrWbjygPw.png)
