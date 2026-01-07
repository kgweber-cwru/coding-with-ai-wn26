# Programming with Generative AI - Technical Workshop Series

A six-week hands-on workshop for learning to build applications with Large Language Models using Python and the OpenAI API.

## Overview

This workshop series teaches participants with basic Python skills how to programmatically interact with LLMs, building progressively from simple API calls to conversational agents with retrieval-augmented generation (RAG).

## Prerequisites

- Basic Python programming skills (variables, functions, loops, data structures)
- Ability to install Python packages using pip
- Familiarity with running Python scripts and Jupyter notebooks
- An OpenAI API account with a valid API key
- Estimated API costs: $5-10 for the entire course

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

### 4. Set Up Your API Key

1. Copy the example environment file:
   ```bash
   cp .env.example .env
   ```

2. Edit `.env` and add your OpenAI API key:
   ```
   OPENAI_API_KEY=sk-your-actual-key-here
   ```

3. **Important**: Never commit your `.env` file to version control!

### 5. Get Your OpenAI API Key

1. Go to [platform.openai.com](https://platform.openai.com)
2. Sign up or log in
3. Navigate to API Keys section
4. Create a new secret key
5. Copy it to your `.env` file immediately (you won't be able to see it again)
6. Add a small amount of credit ($5-10 is plenty for this course)

### 6. Launch Jupyter

```bash
jupyter notebook
```

Your browser should open automatically. Navigate to the week you're working on!

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
5. **Monitor costs**: Check your OpenAI usage dashboard regularly
6. **Save your work**: Make copies of notebooks before experimenting heavily

## Cost Management

To keep costs low:
- Use `gpt-4o-mini` for most exercises (significantly cheaper than GPT-4)
- Set `max_tokens` limits in your API calls
- Start with small test datasets
- Monitor your usage at [platform.openai.com/usage](https://platform.openai.com/usage)

## Troubleshooting

### "Module not found" errors
```bash
pip install -r requirements.txt
```

### API key not working
- Check that your `.env` file is in the root directory
- Verify the key starts with `sk-`
- Make sure you've added billing information to your OpenAI account

### Jupyter not starting
```bash
pip install --upgrade jupyter notebook
```

## Resources

- [OpenAI API Documentation](https://platform.openai.com/docs)
- [OpenAI Cookbook](https://github.com/openai/openai-cookbook)
- [Python dotenv Documentation](https://pypi.org/project/python-dotenv/)

## Getting Help

- During sessions: Ask the instructor
- Between sessions: Review the notebooks and try the examples
- Check the OpenAI documentation for API details

## License

Educational materials for CWRU School of Medicine workshop series.
