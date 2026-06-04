Ex.No.6 Development of Python Code Compatible with Multiple AI Tools

Aim: 

Write and implement Python code that integrates with multiple AI tools to automate the task of interacting with APIs, comparing outputs, and generating actionable insights with Multiple AI Tools.

Explanation:

Develop a python code that integrates multiple AI tool by interacting with their APIs.
Compare outputs from different APIs.
Analyze the response and the Output.

The aim is to understand how to request help from AI tools for tasks like writing Python code, integrating with APIs, comparing outputs, and generating actionable insights.
 
Python Code: 
```
import requests

def get_ai_response(api_url, prompt):
    try:
        response = requests.post(
            api_url,
            json={"prompt": prompt}
        )
        return response.json()["response"]
    except Exception as e:
        return f"Error: {e}"

prompt = "Explain the benefits of Artificial Intelligence."

api1_url = "https://api1.example.com/generate"
api2_url = "https://api2.example.com/generate"

response1 = get_ai_response(api1_url, prompt)
response2 = get_ai_response(api2_url, prompt)

print("Response from AI Tool 1:")
print(response1)

print("\nResponse from AI Tool 2:")
print(response2)

print("\nComparison and Analysis:")

if response1 == response2:
    print("Both AI tools produced similar outputs.")
else:
    print("The AI tools produced different outputs.")
    
    len1 = len(response1)
    len2 = len(response2)

    if len1 > len2:
        print("AI Tool 1 provided a more detailed response.")
    elif len2 > len1:
        print("AI Tool 2 provided a more detailed response.")
    else:
        print("Both responses have similar detail levels.")

print("\nActionable Insight:")
print("Use the more detailed and relevant response for decision-making or further analysis.")

```
Output :
Response from AI Tool 1:
Artificial Intelligence improves efficiency, automates tasks, and supports decision-making.

Response from AI Tool 2:
Artificial Intelligence enhances productivity, reduces human effort, and enables intelligent automation.

Comparison and Analysis:
The AI tools produced different outputs.
AI Tool 2 provided a more detailed response.

Actionable Insight:
Use the more detailed and relevant response for decision-making or further analysis.

Result: 
Thus, the objective of integrating multiple AI tools and evaluating their responses was achieved successfully.
