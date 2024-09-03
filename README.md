# OpenAI
[**OpenAI API**](https://platform.openai.com/docs/overview) (A backend for [**ChatGPT**](https://chatgpt.com/) application)

1. Create an [**OpenAI**](https://openai.com/) account.
2. Create an [**API key**](https://platform.openai.com/api-keys) to access the OpenAI API.


```python
import os
from openai import OpenAI
from secret_key import OPENAI_API_KEY

client = OpenAI(api_key=OPENAI_API_KEY)

chat_completion = client.chat.completions.create(
    model="gpt-3.5-turbo",
    messages=[
        {
            "role": "user",
            "content": "Explain Data Science",
        }
    ]
)

print(chat_completion.choices[0].message)
```

- **OpenAI API** is a powerful tool that allows developers to interact with OpenAI's LLMs, such as GPT-3 and GPT-4.
- These models can generate human-quality text, translate languages, write creative content, and answer your questions informally.

**How it works?**
1. **API Key:** An OpenAI API key to access the API. This key can be obtained from the OpenAI platform after creating an account.
2. **API Requests:** You send HTTP requests to the OpenAI API endpoint, specifying the model you want to use and the prompt or input text.
3. **API Responses:** The API returns a JSON response containing the generated text or other relevant data.

**Example:**
Using the OpenAI API to generate a summary of a given text:

```python
import openai
from secret_key import OPENAI_API_KEY

openai.api_key = OPENAI_API_KEY

prompt = "Enter the text"

response = openai.Completion.create(
    engine="text-davinci-003",
    prompt="Summarize the following text:\n" + prompt,
    max_tokens=100,
    n=1,
    stop=None,
    temperature=0.5,
)

print(response.choices[0].text)
```

**Explanation of parameters:**
1. **engine:** The specific language model to use (e.g., "text-davinci-003").
2. **prompt:** The text you want the model to process.
3. **max_tokens:** The maximum number of tokens to generate in the response.
4. **n:** The number of generated responses.
5. **stop:** A list of strings that, if encountered in the generated text, will cause the generation to stop.
6. **temperature:** Controls the randomness of the generation. Higher values make the output more creative, while lower values make it concise.

**Common use cases for OpenAI API:**
1. **Natural Language Processing (NLP) Tasks:** Text summarization, machine translation, question answering, and text generation.
2. **Content Creation:** Writing articles, stories, scripts, and code.
3. **Customer Service:** Chatbots and virtual assistants.
4. **Research:** Exploring the capabilities and limitations of large language models.
