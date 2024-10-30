# Generative-AI-Powered-QA-Chatbot-Model_With_GPT_4o_and_Ollama
This project demonstrates the creation of a Q&A chatbot application using Streamlit, OpenAI's API, LangChain, and Ollama. The chatbot can interact with users and respond to their queries using different language models like GPT-4, GPT-4 Turbo, Mistral, Llama3.1, and Gemma2:2b. It allows users to switch between OpenAI and Ollama models and customize their preferences, such as temperature and maximum token length, to control the chatbot's response style and verbosity.

The application provides a user-friendly interface with Streamlit, enabling easy interaction and configuration of model parameters.

## Features
1. Interactive UI: Built using Streamlit for a user-friendly experience.
2. Model Flexibility: Supports various language models from OpenAI and Ollama.
3. Customizable Settings: Allows users to adjust parameters like temperature, maximum tokens, and API keys.
4. Dual Mode: Switch between OpenAI and Ollama models based on user preference.
5. Environment Variable Management: Uses .env file for storing sensitive information securely.

## Steps Involved in the Project
1. Environment Setup:
Install necessary libraries mentioned in the requirements.txt file.
Create a .env file to store environment variables securely, such as LANGCHAIN_API_KEY.

2. Langsmith Tracking Configuration:
Set up environment variables for Langsmith API key and project tracking using os.environ.
This allows tracking of the model's performance and response data.

3. Prompt Template Creation:
Define a prompt template using ChatPromptTemplate from LangChain for consistent interaction with the model.
Set the system message to instruct the model to behave as a helpful assistant and dynamically receive user input queries.

4. Response Generation Functions:
Implement two functions, generate_response and generate_response2, to handle different engines (Ollama and OpenAI).
The functions utilize LangChain's chaining mechanism to parse user input through the prompt template and the selected model, returning the generated response.
5. Streamlit Interface Design:
Use Streamlit to create a web-based interface.
Add a title and a sidebar for model settings, including API key input, model selection, temperature, and max tokens.

6. Dynamic User Interaction:
Capture user input through a text box.
Based on user selections (OpenAI or Ollama models), call the appropriate response generation function.
Display the generated response on the main interface.

7. Conditional Logic for Model Handling:
Use conditional checks to handle different models and input scenarios.
Ensure the appropriate function is called based on user input and selected model, providing flexibility between OpenAI and Ollama.

8. Error Handling and User Feedback:
Implement error handling to ensure all required inputs are provided.
Display messages to guide users to input necessary information if missing.
