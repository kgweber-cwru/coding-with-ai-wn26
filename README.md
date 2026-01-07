# Programming with Generative AI - Technical Workshop Series

A six-week hands-on workshop for learning to build applications with Large Language Models using Python and the Google Vertex AI API (Gemini).

## Overview

This workshop series teaches participants with basic Python skills how to programmatically interact with LLMs, building progressively from simple API calls to conversational agents with retrieval-augmented generation (RAG).

## Prerequisites

- Basic Python programming skills (variables, functions, loops, data structures)
- Ability to install Python packages using pip
- Familiarity with running Python scripts and Jupyter notebooks
- A Google Cloud Project with Vertex AI API enabled
- Google Cloud SDK (`gcloud`) installed and authenticated
- Estimated costs: Low (using Gemini 1.5 Flash) or Free Tier eligible

## Setup Instructions

### 1. Clone or Download this Repository

```bash
cd /path/to/your/projects
# (or download and extract the ZIP file)
```

### 2. Create a Virtual Environment (Recommended)

```bash
# Create virtual environment
python -m venv venv

# Activate it
# On macOS/Linux:
source venv/bin/activate
# On Windows:
venv\Scripts\activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Authenticate with Google Cloud

1. Ensure you have the `gcloud` CLI installed.
2. Login to your Google Cloud account:
   ```bash
   gcloud auth login
   ```
3. Set your project ID:
   ```bash
   gcloud config set project YOUR_PROJECT_ID
   ```
4. Configure Application Default Credentials (ADC) for the notebooks to use:
   ```bash
   gcloud auth application-default login
   ```


### 6. Launch Jupyter

```bash
jupyter notebook
```

Your browser should open automatically. Navigate to the week you're working on!

## Run on Google Colab

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

## Tips for Success

1. **Read before the session**: Review the concepts notebook before each weekly meeting
2. **Experiment**: Modify the example code and see what happens
3. **Complete assignments**: The weekly assignments build on each other
4. **Ask questions**: Use the discussion time during sessions
5. **Monitor costs**: Check your Google Cloud billing dashboard regularly
6. **Save your work**: Make copies of notebooks before experimenting heavily

## Cost Management

To keep costs low:
- Use `gemini-1.5-flash` for most exercises (significantly cheaper than Pro models)
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

- During sessions: Ask the instructor
- Between sessions: Review the notebooks and try the examples
- Check the Google Cloud documentation for API details

## License

Educational materials for CWRU School of Medicine workshop series.
