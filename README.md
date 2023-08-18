# Dhipin
import requests

api_key = "YOUR_API_KEY"
url = "https://api.openai.com/v1/engines/davinci-codex/completions"

prompt = "Once upon a time in a"
response = requests.post(url, headers={"Authorization": f"Bearer {api_key}"}, json={"prompt": prompt, "max_tokens": 50})

generated_text = response.json()["choices"][0]["text"]
print(generated_text)
