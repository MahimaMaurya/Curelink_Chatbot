# Chatbot for Meal Picture Queries

## Project Description

This project involves developing a Python program designed to automatically respond to patient queries regarding meal pictures sent via WhatsApp. The core functionality of the system includes:

- Image Analysis: Utilizing the Large Language Model **gemini-1.5-flash** to analyze meal images.
- Diet Comparison: Comparing images against prescribed diet charts.
- Contextual Advice: Generating actionable advice based on the patient's medical profile and chat history.

## Performance of the Model

1. Generated_Response = Ideal_Response

<img width="1063" alt="Screenshot 2024-08-25 at 12 51 06" src="https://github.com/user-attachments/assets/13e4fe0d-10c7-4787-8072-05297d13a35f">
The model aligns perfectly with the expected ideal response.

2. Ideal_response doesn't match with user_query
<img width="1067" alt="Screenshot 2024-08-25 at 12 45 04" src="https://github.com/user-attachments/assets/95cef345-ab2a-4d2d-a369-5651fd20719e">
The ideal response does not align with the user’s query; however, our generated response provides the correct output.
   
3. Generated_Response > Ideal_Response
<img width="1007" alt="Screenshot 2024-08-25 at 12 51 59" src="https://github.com/user-attachments/assets/a96a09f0-799e-41af-8c86-edc6c432493d">
Our model is generating responses that are significantly better compared to the ideal_response.

4. Scenario: When the user sends an image at the wrong time and indicates the timing in the caption. The model fails to consider the timing in the context of the diet chart.
<img width="795" alt="Screenshot 2024-08-25 at 13 17 04" src="https://github.com/user-attachments/assets/983143d6-0084-46bc-bca3-84fcbcbd109d">

## Noteworthy Points

- Cost and Efficiency: To reduce costs and time incurred with LLMs, tasks that can be handled directly by JSON are managed using Python functions.
- Model Limitations: As the assignment told to solely handle meal picture queries, it may show limitations when processing simple text queries in the JSON.
- Real-time Considerations: The system is designed for real-time user uploads. However, if there is ambiguity in timing, the model may malfunction.

## Future Improvements

- Pro Version: Upgrading to the pro version of the LLM could enhance the model's capabilities by allowing more tokens and improving context awareness.
- Handling Ambiguity: Addressing the issue of timing ambiguity by better context awareness to improve model accuracy and reliability.
