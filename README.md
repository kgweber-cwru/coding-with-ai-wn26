# Programming with Generative AI - Technical Workshop Series

A six-week hands-on workshop for learning to build applications with Large Language Models using Python and the Google Vertex AI API (Gemini).

Principally designed to be run on Google Colab, but with the ability to run locally as well.

## Overview

This workshop series teaches participants with basic Python skills how to programmatically interact with LLMs, building progressively from simple API calls to conversational agents with retrieval-augmented generation (RAG).

> Before Week 1: finish the Week 0 setup. Follow the guide and run the verification notebook so you are ready to code on day one.
> - Setup guide: [week-0/STUDENT-SETUP-GUIDE.md](week-0/STUDENT-SETUP-GUIDE.md)
> - Verification notebook (with Colab badge): [week-0/setup_verification.ipynb](week-0/setup_verification.ipynb)

## Prerequisites

- Basic Python programming skills (variables, functions, classes, loops, data structures)
- Ability to install Python packages using pip
- Familiarity with running Python scripts and Jupyter notebooks
- A Google Cloud Project with Vertex AI API enabled (see Week 0 guide for step-by-step)
- Redeemed Google Cloud educational credits and linked billing account (Week 0 guide)
- Project ID on hand for notebooks; Google Cloud SDK (`gcloud`) installed if running locally
- Estimated costs: Low (using `gemini-2.5-flash-lite`) or Free Tier eligible

## Run on Google Colab

### Set up your environment and GCP world according to instructions in the [Week 0 Setup Guide](week-0/STUDENT-SETUP-GUIDE.md)

Mini-checklist for Colab users (mirrors the Week 0 verification notebook):

- Open the notebook via its "Open in Colab" badge.
- File → Save a copy in Drive so you have your own editable copy.
- Run the first cell to install/auth; when prompted, authenticate and enter your Project ID.
- Run the Gemini test call at the end of the notebook; confirm you see a model response.

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

### Bonus Content
- Using Gradio to put a simple UI onto your work - a worked example

## Tips for Success

1. **Be ready with the Week 0 material** complete so you're ready to go
2. **Read before the session**: Review the concepts notebook before each weekly meeting
3. **Experiment**: Modify the example code and see what happens
4. **Complete assignments**: The weekly assignments build on each other
5. **Ask questions**: Use the discussion time during sessions
6. **Monitor costs**: Check your Google Cloud billing dashboard regularly
7. **Save your work**: Make copies of notebooks before experimenting heavily

### Quick verification (Week 0)

- Drive mounted and writable (saw the `cwru-setup-test.txt` message)
- Dependencies installed (`google-genai`, `google-auth` installed in Colab)
- Project ID set in the session
- Vertex AI API enabled in your project
- Gemini test call returned a response (no 403/permission errors)

If any of these fail, rerun [week-0/setup_verification.ipynb](week-0/setup_verification.ipynb) and follow the prompts.

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

### Week 0 setup hiccups
- Re-run the Week 0 verification notebook to pinpoint failures (auth, Project ID, API enablement, billing/credits)
- Double-check the Week 0 guide steps for enabling Vertex AI and redeeming credits

### Jupyter not starting
```bash
pip install --upgrade jupyter notebook
```

## Resources

- [Google GenAI SDK Documentation](https://github.com/googleapis/python-genai)
- [Gemini API Documentation](https://ai.google.dev/gemini-api/docs)
- [Python dotenv Documentation](https://pypi.org/project/python-dotenv/)
- Week 0 verification notebook: [week-0/setup_verification.ipynb](week-0/setup_verification.ipynb)
- Week 0 setup guide: [week-0/STUDENT-SETUP-GUIDE.md](week-0/STUDENT-SETUP-GUIDE.md)

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
