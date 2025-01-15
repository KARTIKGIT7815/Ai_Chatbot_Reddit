AI Reddit Bot
This project is a Reddit bot that automatically generates and posts AI-driven content to a specified subreddit every day. Using Groq's AI model and the LangChain framework, the bot generates creative content and posts it on Reddit via the PRAW API.

Features
Automated Content Generation: Generates AI-driven content using Groq's language model and LangChain.
Reddit Integration: Posts the generated content to a specified subreddit using the Reddit API (PRAW).
Scheduled Posting: Posts daily at a specific time, fully automating the content-sharing process.
Customizable: Modify the content generation prompt and posting schedule to suit your needs.
Requirements
Before running the bot, you need the following libraries:

praw: Reddit API client
requests: HTTP requests library
schedule: For scheduling tasks
langchain: Framework for working with language models
langchain-groq: Groq AI integration for LangChain
To install the required libraries, run the following command: pip install praw requests schedule langchain langchain-groq
Setup
Reddit API Credentials:

Create a Reddit API application here and get your client_id, client_secret, user_agent, username, and password.
Replace the placeholder values in the code with your credentials.
Groq API Key:

Obtain your API key from Groq.
Replace the placeholder API key in the code with your actual API key.
Subreddit Name:

Change 'test' in the reddit.subreddit('test') line to the actual name of the subreddit you want the bot to post to.
Usage

The bot will:
Authenticate with Reddit.
Generate content using the Groq model through LangChain.
Post the content to the specified subreddit.
Customizing the Content
The content generation prompt can be customized in the generate_content() function. For example, change this line:
input_text = 'Give a caption for a hill station'

Modify the input text to generate different types of content.

Scheduling
The bot posts daily at the time specified in this line:
schedule.every().day.at("16:09").do(post_to_reddit)

Example Output
A typical post made by the bot will look like:

Title: AI Daily Post
Body: "A scenic hill station offering picturesque views of the mountains and tranquil surroundings."

Troubleshooting
RedditAPIException (SUBREDDIT_NOEXIST): Ensure the subreddit name exists and is accessible.
Groq API Connection Issues: Check that your API key is correct and that the Groq API is functioning.
