# llm-python

A set of instructional materials, code samples and Python scripts featuring LLMs (GPT etc) through interfaces like llamaindex, langchain, Chroma (Chromadb), Pinecone etc. Mainly used to store reference code for my LangChain tutorials on YouTube.

<!-- <img src="assets/youtube.png" width="50%" alt="LangChain youtube tutorials" /> -->

![LangChain youtube tutorials](assets/llmseries.png)

Learn LangChain from my YouTube channel (~8 hours of LLM hands-on building tutorials); Each lesson is accompanied by the corresponding code in this repo and is designed to be self-contained -- while still focused on some key concepts in LLM (large language model) development and tooling.

Feel free to pick and choose your starting point based on your learning goals:

| Part | LLM Tutorial                                                                         | Link                                                          | Video Duration |
| ---- | ------------------------------------------------------------------------------------ | ------------------------------------------------------------- | -------------- |
| 1    | OpenAI tutorial and video walkthrough                                                | [Tutorial Video](https://youtu.be/skw-togjY7Q)                | 26:56          |
| 2    | LangChain + OpenAI tutorial: Building a Q&A system w/ own text data                  | [Tutorial Video](https://youtu.be/DYOU_Z0hAwo)                | 20:00          |
| 3    | LangChain + OpenAI to chat w/ (query) own Database / CSV                             | [Tutorial Video](https://youtu.be/Fz0WJWzfNPI)                | 19:30          |
| 4    | LangChain + HuggingFace's Inference API (no OpenAI credits required!)                | [Tutorial Video](https://youtu.be/dD_xNmePdd0)                | 24:36          |
| 5    | Understanding Embeddings in LLMs                                                     | [Tutorial Video](https://youtu.be/6uyBc0jm1xQ)                | 29:22          |
| 6    | Query any website with LLamaIndex + GPT3 (ft. Chromadb, Trafilatura)                 | [Tutorial Video](https://youtu.be/6K1lyyzpxtk)                | 11:11          |
| 7    | Locally-hosted, offline LLM w/LlamaIndex + OPT (open source, instruction-tuning LLM) | [Tutorial Video](https://youtu.be/qAvHs6UNb2k)                | 32:27          |
| 8    | Building an AI Language Tutor: Pinecone + LlamaIndex + GPT-3 + BeautifulSoup         | [Tutorial Video](https://youtu.be/k8G1EDZgF1E)                | 51:08          |
| 9    | Building a queryable journal 💬 w/ OpenAI, markdown & LlamaIndex 🦙                  | [Tutorial Video](https://youtu.be/OzDhJOR5IfQ)                | 40:29          |
| 10   | Making a Sci-Fi game w/ Cohere LLM + Stability.ai: Generative AI tutorial            | [Tutorial Video](https://youtu.be/uR93yTNGtP4)                | 1:02:20        |
| 11   | GPT builds entire party invitation app from prompt (ft. SMOL Developer)              | [Tutorial Video](https://www.youtube.com/watch?v=Ll_VIsIjuFg) | 41:33          |
| 12   | A language for LLM prompt design: Guidance                                           | [Tutorial Video](https://youtu.be/k4Ejc3bLQiU)                | 43:15          |
| 13   | You should use LangChain's Caching!                                                  | [Tutorial Video](https://youtu.be/Uk_SJSnQRU8)                | 25:37          |
| 14   | Build Chat AI apps with Steamlit + LangChain                                         | [Tutorial Video](https://youtu.be/7QR6hXx_Nms)                | 32:11          |

The full lesson playlist can be found [here](https://www.youtube.com/playlist?list=PLXsFtK46HZxUQERRbOmuGoqbMD-KWLkOS).

## Update: Feb 5th 2025

I've pushed 4 new scripts to the repo, 15_sql.py to 18_chroma.py, which are intended to be used as code reference to this public course:

- [Building search engines in the age of AI](https://sectors.app/bulletin/ai-search)

Additionally, I'm now also hosting example code in this repo for the following [Generative AI Series](https://docs.sectors.app/recipes/generative-ai-python/01-background) by Sectors.

1. [Generative AI for Finance](https://docs.sectors.app/recipes/generative-ai-python/01-background): An overview of designing Generative AI systems for the finance industry and the motivation for retrieval-augmented generation (RAG) systems.

2. [Tool-Use Retrieval Augmented Generation (RAG)](https://docs.sectors.app/recipes/generative-ai-python/02-tool-use): Practical guide to building RAG systems leveraging on information retrieval tools (known as "tool-use" or "function-calling" in LLM)

3. [Structured Output from AIs](https://docs.sectors.app/recipes/generative-ai-python/03-structured-output): From using Generative AI to extract from unstructured data or perform actions like database queries, API calls, JSON parsing and more, we need schema and structure in the AI's output.

4. [Tool-use ReAct Agents w/ Streaming](https://docs.sectors.app/recipes/generative-ai-python/04-conversational): Updated for LangChain v0.3.2, we explore streaming, LCEL expressions and ReAct agents following the most up-to-date practices for creating conversational AI agents.

5. [Conversational Memory AI Agents](https://docs.sectors.app/recipes/generative-ai-python/05-memory-ai): Updated for LangChain v0.2.3, we dive into Creating AI Agents with Conversational Memory

Both of these series are public and free to access. The code in this repo is intended to be used as a reference for these courses.

### Quick Start

1. Clone this repo
2. Install requirements: `pip install -r requirements.txt`
3. Some sample data are provided to you in the `news` foldeer, but you can use your own data by replacing the content (or adding to it) with your own text files.
4. Create a `.env` file which contains your OpenAI API key. You can get one from [here](https://beta.openai.com/). `HUGGINGFACEHUB_API_TOKEN` and `PINECONE_API_KEY` are optional, but they are used in some of the lessons.
   - [Lesson 10](./11_worldbuilding.py) uses Cohere and Stability AI, both of which offers a free tier (no credit card required). You can add the respective keys as `COHERE_API_KEY` and `STABILITY_API_KEY` in the `.env` file.

The `.env` file should look like this:

```
OPENAI_API_KEY=your_api_key_here

# optionals (not required for most of the series)
HUGGINGFACEHUB_API_TOKEN=your_api_token_here
PINECONE_API_KEY=your_api_key_here
```

HuggingFace and Pinecone are optional but is recommended if you want to use the Inference API and explore those models outside of the OpenAI ecosystem. This is demonstrated in Part 3 of the tutorial series. 5. Run the examples in any order you want. For example, `python 6_team.py` will run the website Q&A example, which uses GPT-3 to answer questions about a company and the team of people working at Supertype.ai. Watch the corresponding video to follow along each of the examples.

### Dependencies

> 💡 Thanks to the work of @VanillaMacchiato, this project is updated as of **2023-06-30** to use the latest version of LlamaIndex (0.6.31) and LangChain (0.0.209). Installing the dependencies should be as simple as `pip install -r requirements.txt`. If you encounter any issues, please let me know.
>
> If you're watching the LLM video tutorials, they may have very minor differences (typically 1-2 lines of code that needs to be changed) from the code in this repo since these videos have been released with the respective versions at the time of recording (LlamaIndex 0.5.7 and LangChain 0.0.157). Please refer to the code in this repo for the latest version of the code.

I will try to keep this repo up to date with the latest version of the libraries, but if you encounter any issues, please: (1) raise a discussion through Issues or (2) volunteer a PR to update the code.

NOTE: `triton` package is supported only for the **x86_64** architecture. If you have problems with installing it, see the [triton compatibility guide](https://github.com/openai/triton?tab=readme-ov-file#compatibility). Specifically, errors like `ERROR: Could not find a version that satisfies the requirement triton (from versions: none)
ERROR: No matching distribution found for triton`.
`uname -p` should give you the processor's name.

### Mentorship and Support

I run a mentorship program under [Supertype Fellowship](https://fellowship.supertype.ai). The program is self-paced and free, with a community of other learners and practitioners around the world (English-speaking). You can optionally book a 1-on-1 session with my team of mentors to help you through video tutoring and code reviews.

### License

MIT © [Supertype](https://supertype.ai) 2024
