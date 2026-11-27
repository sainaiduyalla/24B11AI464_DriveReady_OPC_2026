# Day 3 – LangChain Chatbot, Conversation Memory, Testing and Agents

## 1. Objective

The objective of Day 3 is to develop an AI-powered chatbot using LangChain and Groq. This task focuses on prompt templates, conversation memory, automated testing using CSV files, and creating a basic LangChain agent.

## 2. Technologies Used

- Python
- Google Colab
- Groq API
- LangChain
- LangChain Groq
- GPT-OSS-20B
- CSV

## 3. Task 1: Setup and LLM Initialization

Installed the required LangChain packages and initialized the Groq LLM using `ChatGroq`.

**Model Configuration:**
- Model: `openai/gpt-oss-20b`
- Temperature: `0.3`

## 4. Task 2: Chatbot Using LangChain

Created a Sweet Crumbs Home Bakery chatbot using LangChain components.

**Components Used:**
- `ChatPromptTemplate`: Defines the chatbot's system and user prompts.
- `MessagesPlaceholder`: Passes conversation history into the prompt.
- `StrOutputParser`: Converts the LLM response into a string.
- `chain`: Connects the prompt, LLM, and output parser.

**Chatbot Features:**
- Provides bakery menu and pricing information.
- Answers questions about eggless cakes.
- Informs customers about the 24-hour order notice.
- Responds in English or Telugu based on the customer's language.
- Follows predefined instructions.

## 5. Task 3: Conversation Memory

Implemented conversation memory using a Python list named `history`.

The chatbot stores previous user messages and AI responses and passes them into subsequent requests.

**Example:**

Customer: Hi, I'm Ravi. Do you make eggless cakes?

Customer: What's my name?

The chatbot uses the previous conversation to identify the customer's name.

Note: This memory works during the current Python session.

## 6. Task 4: Automated Testing Using CSV

Created a `tests.csv` file containing 10 different test questions and their expected keywords.

Implemented a `run_tests()` function using Python's CSV module.

**Working:**
1. Read test questions from `tests.csv`.
2. Send each question to the LangChain chain.
3. Check whether the expected keyword appears in the chatbot response.
4. Display PASS or FAIL for each test.
5. Calculate the total number and percentage of passed tests.

## 7. Task 5: LangChain Agent

Explored the `create_agent()` function from LangChain.

Created a basic LangChain agent using the existing LLM and system prompt.

The agent currently uses an empty tools list (`tools=[]`). Additional tools can be integrated in future tasks.

## 8. Learning Outcomes

- Learned how to use LangChain prompt templates.
- Understood the purpose of MessagesPlaceholder.
- Learned how to use StrOutputParser.
- Implemented conversation memory using Python lists.
- Created automated chatbot tests using CSV files.
- Learned how to check chatbot responses using expected keywords.
- Explored the basic creation of LangChain agents.

## 9. How to Run

1. Open the notebook in Google Colab.
2. Install the required packages.
3. Add `GROQ_API_KEY` to Google Colab Secrets.
4. Initialize the Groq LLM.
5. Define the system prompt and LangChain chain.
6. Implement conversation memory.
7. Create `tests.csv` using the `%%writefile` command.
8. Run the automated testing function.
9. Create and test the LangChain agent.

## Conclusion

Successfully developed a Sweet Crumbs Home Bakery chatbot using LangChain and Groq, implemented conversation memory, performed automated testing with 10 CSV test cases, and explored the creation of a basic LangChain agent.
