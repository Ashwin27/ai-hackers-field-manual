# AI Hackers' Field Manual
[[Toolbox]](#toolbox) [[Patterns]](#patterns) [[Models]](#models) <!--[[Prompt]](#prompt) [[Infra products]](#infra) [[Research]](#research) --> [[More Resources]](#resources)

The AI hackers community has been moving at neck breaking pace and often one can feel lost and overwhelmed with ever-increasing number of new tools. Focusing on clarity and brevity, this guide is created to help you get started hacking and serve as a springboard for further explorations! 

This is a community effort; please open PRs to add information! 

## Toolbox <a name="toolbox"></a>
Common tools you will come across as you explore projects built in the community. Some of these tools and frameworks may not be specific to LLM use cases, but have become the default choice of the community. Feel free to use other tools you like but it's good to generally know these. 

- [Flask](https://flask.palletsprojects.com/en/2.1.x/) - A lightweight web framework for Python. Since Python is the language of AI, you might as well use a web framework in Python. Another common option is [FastAPI](https://fastapi.tiangolo.com/).
- [Next.js](https://nextjs.org/docs) - A popular Javascript framework, often used with Vercel. 
- [Vercel](https://vercel.com) - A cloud platform specialized in hosting Next.js apps. 
- [Tailwindcss](https://tailwindcss.com/docs) - A utility-first CSS framework, which means you will define styling directly with pre-built css classes. 
- [Pinecone](https://www.pinecone.io/docs) - A vector database for AI applications. This is commonly used to store embeddings of data and enable similarity based search (More on this in Q&A bots). Alternatively, you can also use [Supabase](https://supabase.com/), [Milvus](https://milvus.io/), [Faiss](https://github.com/facebookresearch/faiss), [Chroma](https://www.trychroma.com/) and [Weaviate](https://weaviate.io/) and others.
- [LlamaIndex](https://github.com/jerryjliu/llama_index) - A library that provides an interface between LLMs and external data by handling data connectors, building indices and querying (eg. including managing prompt token size, etc.)
- [LangChain](https://github.com/hwchase17/langchain) - A library that helps you build LLM based complex action chains and agents. 
- [OpenAI API](https://platform.openai.com/docs/api-reference) - Currently the state of the art models. Commonly used APIs include:
  - Whisper - Audio to text. This is also open-sourced, so you can run your own service. 
  - Embedding - Generate high dimensional representation based on text and can be used for semantic search. 
  - Text completions and chat completions - The API behind ChatGPT. Multiple models exist. gpt-4 is the state of art, but general use cases can be done on gpt-3.5-turbo (cheaper and faster).
  - DALLE - Text to image. 

## Application Patterns and Examples <a name="patterns"></a>
Common pattners used in applications. Each pattern will include walk-throughs, community projects, and a super barebone implementation example for learning and clarity. More complex examples will be added over time. 
### AutoGPT Agent From Scratch
This is a pattern popularized by AutoGPT & BabyAGI projects. With this pattern, an agent is given a set of tools and is tasked to complete a goal. In each step, the agent uses LLM to iteratively decide which tool to use and solves the problem. 

Inspired by [LLM Agents](https://github.com/mpaepper/llm_agents/tree/main/llm_agents), here's is a built-from-scratch version in less than [150 lines of ruby](examples/llm_agents/llm_agents.rb) that implements a Thought, Action, Observation, Thought loop agent with access to Google Search and Ruby REPL. 

### ChatGPT Plugin
OpenAI actually has very detailed [documentation](https://platform.openai.com/docs/plugins/introduction) on how to setup a plugin. Here's an [example](examples/plugin/app.py) app. 

Some tips:
- It was bit tricky to install localhost plugin in ChatGPT. Make sure you are setting CORS correctly and explicitly setting a port number. For some reason, the default port number didn't work for me. 
- You can use chatgpt to write the manifest files for you. Just give it an example and describe the input and output. It will generate the manifest file scafolidng for you.
- Regarding prompts in the manifest, start with something simple and build on it. You don't need to overthink it in V1. 

### Semantic Search and Q&A Bots
🚧 Under Construction

## Current State of Models + Training <a name="models"></a>
🚧 Under Construction

<!-- ## Prompt engineering, techniques and templates <a name="prompt"></a>
🚧 Under Construction

## AI infra products and platforms <a name="infra"></a>
🚧 Under Construction

## Research + Papers <a name="research"></a>
🚧 Under Construction -->

## More Resources <a name="resources"></a>
🚧 Under Construction
