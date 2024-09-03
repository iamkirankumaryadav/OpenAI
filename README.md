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
