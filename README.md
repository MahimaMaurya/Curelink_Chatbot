# Chatbot for Meal Picture Queries
## Project Description
This project involves developing a python program to automatically respond to patient queries about meal pictures sent via WhatsApp.
The core functionality of the project is to generate accurate and context-aware responses to meal pictures submitted by patients. The system uses Large Language Model i.e. **gemini-1.5-flash** to analyze the meal images, compare them against the prescribed diet charts, and generate actionable advice based on the patient’s medical profile and chat history.

## Performance of the Model
1. Generated_Response = Ideal_Response
<img width="1063" alt="Screenshot 2024-08-25 at 12 51 06" src="https://github.com/user-attachments/assets/13e4fe0d-10c7-4787-8072-05297d13a35f">
Above pictures implies that our model perfectly aligned with the expected ideal_response.

2. Ideal_response doesn't match with user_query

<img width="1067" alt="Screenshot 2024-08-25 at 12 45 04" src="https://github.com/user-attachments/assets/95cef345-ab2a-4d2d-a369-5651fd20719e">
   
3. Generated_Response > Ideal_Response
<img width="1007" alt="Screenshot 2024-08-25 at 12 51 59" src="https://github.com/user-attachments/assets/a96a09f0-799e-41af-8c86-edc6c432493d">

## Scenario when model underperformed
1. When user send the image at wrong time and tells the timing in caption
   In this case, our model doesn't consider it by following diet_chart
   <img width="795" alt="Screenshot 2024-08-25 at 13 17 04" src="https://github.com/user-attachments/assets/983143d6-0084-46bc-bca3-84fcbcbd109d">

## Noteworthy Points
-To reduce cost and time incur in LLM's, most of the work which could be handled directly by json is done using python function. Model could be made better usi pro version which allow more tokens and context awareness.
-As the project focuses on only meal picture query but the json contains some simple text query their modle limilitation can be observed.
-It made in keeping in mind that user uploads in real time situation but if their's ambiguity in time then the model may malfunction.

