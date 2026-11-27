# Day 2 – Advanced AI Chatbot with Conversation Memory

## Objective

The objective of Day 2 is to enhance the Sweet Crumbs Home Bakery chatbot by adding menu price calculation, function logging, conversation history, and error handling using Python and Groq.

## 1. Technologies Used

- Python
- Google Colab
- Groq API
- GPT-OSS-20B
- JSON
- OpenAI-compatible Chat Completions API

## 2. Task Description

Developed an interactive AI-powered chatbot for Sweet Crumbs Home Bakery.

The chatbot provides bakery information, answers customer queries, and maintains conversation history during the chat session.

## 3. Features Implemented

### 1. Bakery Menu

Created a Python dictionary containing bakery items and their prices.

| Item | Price |
|---|---:|
| Plum Cake | ₹500 |
| Chocolate Cake | ₹650 |
| Cupcake | ₹80 |

### 2. Price Calculation Function

Implemented a `get_price()` function to calculate the total price based on the selected item and quantity.

Example:

- Item: Cupcake
- Quantity: 6
- Total Price: ₹480

### 3. Decorator and Logging

Implemented a `log_call` decorator using Python's `functools` module.

It records the function name, arguments, and returned result whenever the decorated function is executed.

### 4. Conversation Memory

Implemented a `history` list to store system instructions, user messages, and chatbot responses.

This allows the chatbot to use previous messages as context during the conversation.

### 5. Error Handling

Implemented exception handling for:

- `RateLimitError`: Handles API rate-limit errors.
- `APIConnectionError`: Handles API connection problems.

The chatbot displays suitable messages instead of terminating immediately when these errors occur.

### 6. Interactive Chatbot

Implemented a continuous `while` loop to interact with customers.

The conversation continues until the user enters `bye`, `exit`, or `quit`.

## 4. Model Configuration

- Model: `openai/gpt-oss-20b`
- Temperature: `0.3`
- API Provider: Groq

## 5. How to Run

1. Open the notebook in Google Colab.
2. Install the required Groq package.
3. Add `GROQ_API_KEY` to Google Colab Secrets.
4. Import the required libraries.
5. Initialize the Groq client.
6. Execute the remaining cells in order.
7. Test the price calculation function.
8. Start the chatbot and ask bakery-related questions.

## 6. Learning Outcomes

- Learned how to use Python decorators.
- Understood how to use `functools.wraps`.
- Learned how to calculate product prices using Python functions.
- Understood how conversation history works in AI chatbots.
- Learned how to handle API errors using exception handling.
- Explored the OpenAI-compatible Chat Completions API through Groq.
- Built an interactive chatbot with conversation context.

## Conclusion

Successfully enhanced the Sweet Crumbs Home Bakery chatbot with price calculation, function logging, conversation memory, and error handling using Python and Groq.
