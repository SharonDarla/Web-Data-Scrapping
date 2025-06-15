# Web-Data-Scrapping
# Introduction: 
This project involves scraping articles from a list of URLs, performing text analysis on the extracted content, and generating an Excel file with various calculated metrics and individual text files for each article.

# Project Description: 
The main goal of this project is to automate the process of extracting article content from provided URLs and analyzing it based on several text analysis metrics, including sentiment scores, readability indices, word counts, and more. The results are then compiled into a structured Excel file for easy review and further analysis.

# Features
	• Scrapes article title and content from a list of URLs.
	• Saves extracted articles as individual text files.
	• Calculates sentiment scores (Positive, Negative, Polarity, Subjectivity).
	• Calculates readability metrics (Average Sentence Length, Percentage of Complex Words, Fog Index).
	• Calculates word-related metrics (Complex Word Count, Word Count, Syllable per Word, Average Word Length).
	• Calculates Personal Pronoun count.
	• Generates an Excel file containing all calculated metrics and hyperlinks to the original articles.
 
# Project Setup:
1. Input Data:
	- We need an Excel file containing a list of URLs and their corresponding IDs. The file should have at least two columns: 'URL_ID' and 'URL'.
	- Place the input Excel file (e.g., Input.xlsx) in a directory accessible by the script (or update the input_file variable in the script to point to its location).
	- Next we need zip files containing stopwords and a master dictionary with positive and negative words. Update the stop_words_zip, master_dict_zip, and the file paths for positive and negative words in the script to point to the locations of your files.

2. Running the Script:
	* Make sure you have all the required libraries installed (as mentioned in the Setup section).
	* Ensure the necessary NLTK data ('punkt' and 'punkt_tab') is downloaded.
	* Update the file paths in the script to point to your input Excel file, stop words directory, and positive/negative words files.
Execute the Python script. The script will iterate through the URLs, scrape the content, perform analysis, and generate the output files.

# Output:

The script will generate the following outputs:
3. Individual Article Text Files: For each URL in the input, a text file will be created in the same directory as the script, named after the 'URL_ID' from the input file. These files will contain the scraped article title and content.
4. Output Data Structure.xlsx: An Excel file will be created containing a table with the following columns for each analyzed article:
	- URL_ID: The ID of the article.
	- URL: The original URL of the article (with hyperlink).
	- POSITIVE SCORE: The calculated positive sentiment score.
	- NEGATIVE SCORE: The calculated negative sentiment score.
	- POLARITY SCORE: The calculated polarity score.
	- SUBJECTIVITY SCORE: The calculated subjectivity score.
	- AVG SENTENCE LENGTH: The average number of words per sentence.
	- PERCENTAGE OF COMPLEX WORDS: The percentage of complex words in the article.
	- FOG INDEX: The calculated Fog Index.
	- AVG NUMBER OF WORDS PER SENTENCE: Same as AVG SENTENCE LENGTH.
	- COMPLEX WORD COUNT: The total count of complex words.
	- WORD COUNT: The total count of words.
	- SYLLABLE PER WORD: The average number of syllables per word.
	- PERSONAL PRONOUNS: The count of personal pronouns.
	- AVG WORD LENGTH: The average number of characters per word.


# Libraries Used:
	• pandas: For data manipulation and analysis. 
	• requests: For making HTTP requests to scrape web pages. 
	• Beautiful Soup: For parsing HTML and XML documents. 
	• textstat: For calculating readability statistics. 
	• NLTK (Natural Language Toolkit): For natural language processing tasks like tokenization and stop word removal. 
	• XlsxWriter: For creating Excel files with formatting and features like hyperlinks. 
	• openpyxl: (Used indirectly by pandas for reading/writing Excel files) For reading and writing Excel 2007+ files. 
	• Matplotlib: (Used for visualizations) For creating static, interactive, and animated visualizations in Python. 
	• Seaborn: (Used for visualizations) For making statistical graphics in Python. 


