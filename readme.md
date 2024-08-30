# 🦜 Langchain: Summarize Text from YouTube or Websites Using Groq Language Models

## Project Overview

This project is a Streamlit application designed to summarize text content from YouTube videos or websites. Utilizing the LangChain framework and the Groq `Gemma-7b-It` model, the application extracts and summarizes content from URLs provided by the user. The application is capable of processing YouTube video links or any other valid website URLs, making it a versatile tool for content summarization.

## Installation and Setup

### Step 1: Clone the Repository
Clone the repository to your local machine to access the project files:

```bash
git clone <repository-url>
cd <repository-directory>
```

### Step 2: Set Up a Virtual Environment
It's recommended to create a virtual environment to avoid conflicts between different Python projects:

``` bash
python -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`
```
### Step 3: Install Dependencies
Install the required Python packages listed in the requirements.txt file:

```bash
pip install -r requirements.txt
```

### Step 4: Configure Environment Variables
Ensure you have a .env file in the root directory of the project with the following content:
```bash 
GROQ_API_KEY=<your-groq-api-key>
```

This file will be used to securely load the Groq API key required for accessing the Gemma-7b-It model.

### Step 5: Add a .gitignore File
If it’s not already present, ensure you have a .gitignore file to exclude sensitive or unnecessary files from version control. A typical .gitignore might include:

```bash 
# Python
*.pyc
__pycache__/

# Virtual Environment
venv/

# Environment Variables
.env

# Jupyter Notebook
.ipynb_checkpoints/
```

## Usage
#### Running the Application
To start the Streamlit application, use the following command:

```bash
streamlit run app.py
```

## Using the Application

- `Set the API Key`: In the sidebar of the application, enter your Groq API key. This key is required to access the Groq model for text summarization.
Input the URL: Enter the URL of the YouTube video or website that you want to summarize. The URL can be a YouTube video link or any other valid website link.
- `Summarize the Content`: Click the "Summarize the content from YT or website" button to generate a summary of the content. The application will validate the URL and, if valid, extract the content and produce a summary.
- `View the Summary`: Once the summarization is complete, the summary will be displayed on the screen.
Handling Errors
If there are any issues, such as missing API keys or invalid URLs, the application will display an error message guiding you to correct the input.

## Project Components
- `Streamlit Interface`: Provides an interactive UI for user input and output display.
- `Groq Model`: Uses the Gemma-7b-It model from Groq for generating text summaries.
- `Prompt Template`: A custom prompt template is used to instruct the model on how to summarize the content.
- `Document Loaders`: Depending on the URL type, either YoutubeLoader or UnstructuredURLLoader is used to extract content.
- `Summarization Chain`: Combines the model and prompt template to create a summarization chain that processes and summarizes the content.

## Requirements
The project requires the following Python packages:

- `langchain`
- `python-dotenv`
- `validators==0.28.1`
- `youtube_transcript_api`
- `langchain_community`
- `unstructured`
- `pytube`
Install these dependencies using:

```bash
pip install -r requirements.txt
```

## Contribution
If you'd like to contribute to this project, please follow these steps:

- `Fork the Repository`: Create a copy of the repository under your GitHub account.
- `Create a New Branch`: Make changes in a new branch to keep the main branch stable.
- `Commit Your Changes`: Once your changes are complete, commit them with a clear message explaining what has been done.
- `Push to Your Branch`: Upload your branch to GitHub.
- `Submit a Pull Request`: Open a pull request to have your changes reviewed and, if approved, merged into the main project.

## License
This project is licensed under the MIT License. See the `LICENSE` file for more details.

