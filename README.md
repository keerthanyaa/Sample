# READ ME : 

## Introduction
RAG-Based Chatbot for Web content interaction simplifies data retrieval by scraping data from a given URL and converting it to structured JSON format. Additionally, it also extends to answering user questions based on the extracted data..

In this notebook, we will be looking at a sample code for execution of RAG based chatbot for webscraping.

This project utilizes Two agents , namely -

1. Scrapping agent - which is responsible to scrap data from the URL (provided as input) to save it as a JSON format file named - scrapped_data.json

2. Chatbot with memory Agent - which takes the information from the JSON format file to create a vector and saves (i.e upserts) the vector embedding in Pinecone (vector database). A chatbot with memory will be used based on which user can question upon the URL link uploaded

### Functionality overview
### Objective: Design and implement a set of intelligent agents that work together to

(1) scrape content from a specified website URL and save it in a structured format, and

(2) utilize the scraped data to answer user queries about the website content.

### Input:

Task 1: URL of the webpage.
Task 2: Any query regarding the scraped data.

### Output:

Task 1: JSON file with scraped data.
Task 2: Answer to questions regarding scrapped web page

## Approach
### PART 1 : SCRAPPING AGENT

1.1 Scrape data from the webpage (URL - input)  

1.2 Save the scrapped data in JSON format

____________________________________________________________________________________________________________
### PART 2 : CHATBOT WITH MEMORY AGENT

2.1 Retrieve JSON data and format it to string

2.2 Split the document to chunks (for creating and upserting embeddings)

2.3 Text Embedding using sentence transformer model

2.4 Upsert data to pinecone

2.5 Question & Answer Chatbot with memory


____________________________________________________________________________________________________________

## NOTE :

Ensure that the directory is been set up in the following way :

      |_ Web_Scraping
      
             |_ key (dir) 
            
                |_ openai.txt
                
                |_ pinecone.txt
                
            |_ Sample_web_scrapping.ipynb
            
            |_ ReadMe.txt
            
            |_ requirements.txt

Here, 

      Web_Scraping : is the working directory
      
      key          : is a folder consisting of two txt filed - 
      
                    openai.txt : paste your OpenAi API key (without enclosing in quote)
                    
                    pinecone.txt : paste your pinecone API key (without enclosing in quote)
                    
      Sample_web_scarpping.ipynb : the Jupyter Notebook file (To be run)
      
      ReadMe.md
      
      requirements.txt : consists of the necessary pip installations
      

      


