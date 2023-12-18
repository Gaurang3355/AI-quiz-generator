# AI-quiz-generator
AI quiz generator using python, streamlit and openai api.

Documentation

Overview
This Streamlit application is a dynamic quiz generator using OpenAI's GPT-3 model to create 
questions and answers on specified topics. Users can select a topic, the number of questions, and 
then take the quiz. The application records responses and calculates scores.



Implementation Details

1. Importing Libraries and Initializing OpenAI Client
• Streamlit (streamlit): For web app features.
• OpenAI (openai): For generating quiz questions.
• os: To manage environment variables.
The OpenAI client requires an API key for requests.

2. Session State Initialization
Function initialize_session_state sets up variables like quiz, current_question, player_score, 
user_answers, and quiz_finished.

3. Generating the Quiz
generate_quiz requests multiple-choice questions from OpenAI's API, taking topic and 
num_questions as inputs, returning question dictionaries.

4. Displaying Questions
display_question shows each question with options, also tracking selected answers for scoring.

5. Main Quiz Application (aimcq)
Encapsulates quiz logic, including topic input, question generation, navigation, scoring, and displaying 
final scores and correct answers.



User Guide

Starting the Quiz
1. Enter Quiz Topic: Specify the quiz topic.
2. Set Number of Questions: Choose up to 10 questions.
3. Generate Quiz: Click 'Generate Quiz' to create the quiz.

Taking the Quiz
1. Answer Questions: Select answers from provided options.
2. Navigate Through Questions: Use 'Save and Next' to proceed.

Completing the Quiz
1. View Score: Your score appears at the end.
2. Review Answers: Shows your answers alongside the correct ones.

Additional Notes
• An active internet connection and a valid OpenAI API key are needed.
• Streamlit's session state maintains data across app interactions.
• Designed for educational and entertainment purposes.



Installation and Setup

1. Setting Up the Environment
• Install Python: Ensure Python is installed.
• Install Streamlit and OpenAI: Use pip install streamlit and pip install openai.

2. Setting Up the OpenAI API Key
• Obtain an API key from OpenAI's website.
• Store it securely in an environment variable or insert it directly in the code.

3. Creating the Python Script
• Save the provided code in aimcq.py.

4. Running the Application
• Navigate to the script's directory and run streamlit run aimcq.py.

5. Interacting with the Quiz Application
• Follow the steps in the User Guide section.



Known Issues and Solutions

Identified Issues
• Logic Error in Front-End: The application sometimes fails to generate correct answers and 
display scores accurately (I was not able to fix these issues due to time constraint).

Proposed Solutions
• Code Review and Testing: Conduct a thorough review of the front-end logic, particularly the 
functions handling question generation and score calculation.
• Consult Documentation: Review OpenAI and Streamlit documentation for any updates or 
best practices that might affect functionality.
