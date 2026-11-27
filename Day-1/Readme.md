# Day 1 – AI Chatbot and Prompt Guard

## Objective
The objective of this task is to build a simple AI chatbot using Groq and LangChain and understand how Prompt Guard helps identify potentially malicious prompts.

## 1. Technologies Used
- Python
- Google Colab
- Groq API
- LangChain
- GPT-OSS-120B
- Llama Prompt Guard 2

## 2. Task 1: Sweet Crumbs Home Bakery Chatbot

### Description
Developed a simple AI chatbot for Sweet Crumbs Home Bakery using the Groq LLM through LangChain.

The chatbot provides information about bakery orders and follows predefined instructions.

### Features
- Provides polite responses to customer questions.
- Informs customers that orders require 24 hours' notice.
- Supports eggless cake options.
- Does not promise specific delivery times.
- Responds in under 60 words.

### Model Configuration
- Model: `openai/gpt-oss-120b`
- Temperature: `0`

### Working
1. Retrieve the Groq API key from Google Colab Secrets.
2. Initialize the LLM using `ChatGroq`.
3. Define a system prompt containing bakery information and chatbot rules.
4. Send the system prompt and user's question to the LLM.
5. Display the generated response.

## 3. Task 2: Prompt Guard

### Description
Used the Meta Llama Prompt Guard 2 model to understand how potentially malicious prompts and prompt injection attempts can be detected.

### Model Used
`meta-llama/llama-prompt-guard-2-22m`

### Example
The input prompt contains an instruction such as:

"Ignore your previous instructions."

This is an example of a prompt injection attempt.

### Working
1. Initialize the Groq client.
2. Select the Prompt Guard model.
3. Send a potentially malicious prompt.
4. Display the model's output.

### Purpose
Prompt Guard can help applications identify potentially malicious inputs before they reach the main chatbot model.

**Note:** The current code tests Prompt Guard separately. It does not yet integrate the detection result into the bakery chatbot or automatically block malicious prompts.

## 4. Learning Outcomes
- Understood how to connect Python applications with Groq.
- Learned how to initialize an LLM using LangChain.
- Understood the role of system prompts and user prompts.
- Built a basic AI chatbot for a bakery.
- Learned about prompt injection attacks.
- Explored how Prompt Guard can help detect malicious prompts.

## 5. How to Run
1. Open the notebook in Google Colab.
2. Install the required packages.
3. Add `GROQ_API_KEY` in Google Colab Secrets.
4. Run the chatbot code.
5. Test the chatbot with different bakery-related questions.
6. Run the Prompt Guard example separately.

## Conclusion
Successfully developed a basic AI-powered bakery chatbot using Groq and LangChain and explored Llama Prompt Guard 2 for detecting potentially malicious prompts.
