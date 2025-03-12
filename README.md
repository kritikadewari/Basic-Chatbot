# Basic-Chatbot
1. Function: greet()
   This function runs once at the start.
   It displays a welcome message and tells the user how to exit the chatbot (by typing 'bye').

2. Function: get_user_input()   
   It prompts the user to type something (with "You: " as the prompt).
   Whatever the user types is converted to lowercase (so the bot can handle different cases easily).
   Returns the user's input to be processed by the chatbot.

3. Function: generate_response(user_input)
   This function processes the user input and decides how the bot should respond.
Inside this function:
  If the user types 'bye', the bot responds with 'Goodbye! Have a great day!', and the second item in the returned tuple is True, which tells the chatbot to exit.
  If the user types something with 'hello' or 'hi' anywhere in the message, the bot responds with 'Hello there! How can I help you?'.
  If the message contains 'how are you', the bot gives a response about how it's doing.
  If the message includes 'what is your name', the bot introduces itself.
  If the message includes 'help', the bot offers some guidance.
  Else, if none of these conditions match, it says: 'I'm not sure how to respond to that. Try asking something else!'

4.  Function: chatbot()
   This is the main controller of the chatbot.
   It first calls the greet() function to say hello.
   Then:
      It runs an infinite loop (while True:) to keep chatting.
      Every loop:
       It asks the user for input.
       It generates a response.
        It prints the chatbot's response.
        If should_exit is True (when the user says 'bye'), it breaks out of the loop and the chatbot stops running.
