# AI engineering practice

My practice notebooks from Ed Donner's Agentic AI course, written while I learn to build with large language models. This is a learning log, so every notebook keeps the outputs from my real runs, mistakes included.

| Notebook | What I practised |
|---|---|
| [`day_3.ipynb`](day_3.ipynb) | Calling a local model through Ollama with the OpenAI client and a `messages` list |
| [`day_4.ipynb`](day_4.ipynb) | A raw HTTP request to Ollama with `requests`, then Groq's `gpt-oss-120b` with `reasoning_effort="low"` |
| [`judge.ipynb`](judge.ipynb) | Reading a judge's JSON verdict and turning a 1-based ranking back into list positions |
| [`day_5_judge.ipynb`](day_5_judge.ipynb) | One `get_client()` for Ollama, Groq and Gemini, the same probability question to three models, and an LLM judge that ranks their answers as JSON. One judge reply came back cut off, probably at `max_tokens`, so `json.loads` failed, and the error is left in |
| [`chatloop.ipynb`](chatloop.ipynb) | A terminal chat loop that keeps the whole conversation in `messages`, on Azure OpenAI `gpt-5-mini` |
| [`ollama_chatbot.ipynb`](ollama_chatbot.ipynb) | The same chat loop on a local `qwen2.5:3b` model |

## Running them

- Python 3.12, then `pip install -r requirements.txt`.
- Put your keys in a `.env` file next to the notebooks: `GROQ_API_KEY`, `GEMINI_API_KEY`, `AZURE_GPT_5_MINI_API_KEY` and `AZURE_ENDPOINT`. The `.gitignore` keeps it out of git.
- The local notebooks need [Ollama](https://ollama.com) running with `qwen2.5:3b-instruct-q4_0` and `llama3.2:3b-instruct-q4_0` pulled.

Short daily notes on what I learned are in my [til](https://github.com/Shubham-afk-del/til) repo.
