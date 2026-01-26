# Programming with Generative AI - Technical Workshop Series

A six-week hands-on workshop for learning to build applications with Large Language Models using Python and the Google Vertex AI API (Gemini).

Principally designed to be run on Google Colab, but with the ability to run locally as well.

## Overview

This workshop series teaches participants with basic Python skills how to programmatically interact with LLMs, building progressively from simple API calls to conversational agents with retrieval-augmented generation (RAG).

## Prerequisites

- Basic Python programming skills (variables, functions, classes, loops, data structures)
- Ability to install Python packages using pip
- Familiarity with running Python scripts and Jupyter notebooks
- A Google Cloud Project with Vertex AI API enabled
- Google Cloud SDK (`gcloud`) installed and authenticated
- Estimated costs: Low (using Gemini 1.5 Flash) or Free Tier eligible



## Run on Google Colab

### Set up your environment and GCP world according to instructions in the [Week 0 Setup Guide](week-0/STUDENT-SETUP-GUIDE.md)

Generally speaking, once you're set up:

If you'd like to run these notebooks in Google Colab, use the "Open In Colab" badge at the top of each notebook or open directly:

- Click the badge to launch the notebook in Colab.
- On first run, Colab will prompt you to install dependencies. Approve installation.
- Authenticate with Google: the notebook will call `google.colab.auth.authenticate_user()` and then you can enter your Google Cloud Project ID when prompted.

Notes:
- These notebooks install `google-genai` and `google-auth` on Colab and set the `GOOGLE_CLOUD_PROJECT` environment variable when you provide it.
- If you prefer, set `GOOGLE_CLOUD_PROJECT` in your Colab environment or use Application Default Credentials.

## Workshop Structure

Each week contains:
- **`concepts.ipynb`**: Main lesson notebook with explanations and examples
- **`assignment.ipynb`**: Scaffolded assignment for independent work

### Week 1: Understanding LLMs and API Basics
- How LLMs work (tokens, prediction, probability)
- Setting up and making your first API calls
- Understanding API parameters

### Week 2: Building Conversations
- Message history and conversation structure
- System prompts and roles
- Managing context

### Week 3: Programmatic Prompt Engineering
- Structured prompts and templates
- Dynamic prompt construction
- Output parsing and validation

### Week 4: Introduction to RAG - Concepts and Embeddings
- What is RAG and why use it?
- Understanding embeddings
- Semantic similarity search

### Week 5: Building Simple RAG Systems
- Document chunking strategies
- Retrieval and context injection
- Complete RAG pipeline

### Week 6: Best Practices and Integration
- Error handling and reliability
- Cost management
- Real-world application design
- 
### Bonus Content
- Using Gradio to put a simple UI onto your work - a worked example

## Tips for Success

1. **Be ready with the Week_0 material** complete so you're ready to go
1. **Read before the session**: Review the concepts notebook before each weekly meeting
2. **Experiment**: Modify the example code and see what happens
3. **Complete assignments**: The weekly assignments build on each other
4. **Ask questions**: Use the discussion time during sessions
5. **Monitor costs**: Check your Google Cloud billing dashboard regularly
6. **Save your work**: Make copies of notebooks before experimenting heavily

## Cost Management

To keep costs low:
- Use `gemini-2.5-flash-lite` for most exercises (significantly cheaper than Pro models)
- Set `max_output_tokens` limits in your API calls
- Start with small test datasets
- Monitor your usage at [console.cloud.google.com/billing](https://console.cloud.google.com/billing)

## Troubleshooting

### "Module not found" errors
```bash
pip install -r requirements.txt
```

### Authentication errors
- Ensure you have run `gcloud auth application-default login`
- Verify your Google Cloud Project has the Vertex AI API enabled

### Jupyter not starting
```bash
pip install --upgrade jupyter notebook
```

## Resources

- [Google GenAI SDK Documentation](https://github.com/googleapis/python-genai)
- [Gemini API Documentation](https://ai.google.dev/gemini-api/docs)
- [Python dotenv Documentation](https://pypi.org/project/python-dotenv/)

## Getting Help

- During sessions: Ask the instructor (Kate Weber)
- Between sessions: Review the notebooks and try the examples: contact Kate for help
- Check the Google Cloud documentation for API details

## License

Educational materials for CWRU School of Medicine workshop series.
 
## Troubleshooting: Colab and GitHub 404s

- Colab does not read local `.env` files. In Colab, use the PROJECT_ID prompt at the top of the notebook or set the environment variable in a cell:

   ```python
   import os
   os.environ['GOOGLE_CLOUD_PROJECT'] = 'your-project-id'
   ```

- If you see a `404 Not Found` when opening via the "Open in Colab" badge, the badge may point to a branch or path that doesn't contain the notebook. Fix options:
   - Push the notebooks to the branch referenced by the badge (commonly `main`).
   - Or update the badge URL to the repository branch that contains the notebooks.

- If Colab prompts for GitHub access or fails to load: sign in to Colab and authorize GitHub, then retry using the badge or use `File → Open notebook → GitHub` and search the repo.

- Workarounds: if issues persist, use `File → Save a copy in Drive` from the Colab error view or open the notebook directly from GitHub and copy into Colab.

- Transient errors: GitHub API rate limits or transient failures can cause temporary 404s — wait a minute and retry if everything else looks correct.
