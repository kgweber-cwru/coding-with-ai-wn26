# Workshop Instructor Guide

## Pre-Workshop Setup

### Announcements (2 weeks before)
Send to participants:
- Link to OpenAI platform: https://platform.openai.com
- Instructions to create account and add $5-10 credit
- Link to Python installation guide
- Repository URL (if using Git)

### Week Before First Session
- Test all notebooks run without errors
- Verify .env.example is in repo
- Prepare example datasets if needed
- Set up shared communication channel (Slack, Teams, etc.)

## Week-by-Week Instructor Notes

### Week 1: LLM Basics and API
**Key Concepts:** Tokens, temperature, system messages, cost awareness
**Common Issues:**
- API key setup problems
- Environment variable confusion
- Token counting confusion

**Tips:**
- Walk through .env setup together
- Show OpenAI usage dashboard
- Emphasize starting with gpt-4o-mini

### Week 2: Conversations
**Key Concepts:** Message history, context management, system prompts
**Common Issues:**
- Forgetting to append assistant responses
- Context window confusion
- Memory/token costs growing

**Tips:**
- Demonstrate growing context visually
- Show history display method
- Discuss when to reset/summarize

### Week 3: Prompt Engineering
**Key Concepts:** Templates, few-shot learning, structured output
**Common Issues:**
- JSON parsing failures
- Missing template variables
- Few-shot examples not diverse enough

**Tips:**
- Test JSON extraction with edge cases
- Show validation/retry patterns
- Discuss example quality

### Week 4: Embeddings and RAG Concepts
**Key Concepts:** Vector similarity, semantic search, basic RAG
**Common Issues:**
- Confusion about what embeddings "mean"
- Similarity score interpretation
- Embedding API costs

**Tips:**
- Use visual examples of similarity
- Demonstrate with very similar/dissimilar texts
- Discuss dimensionality conceptually

### Week 5: Building RAG Systems
**Key Concepts:** Chunking strategies, metadata, retrieval quality
**Common Issues:**
- Chunk size selection
- Losing context in chunks
- Poor retrieval results

**Tips:**
- Show different chunking strategies
- Emphasize testing retrieval quality
- Discuss trade-offs

### Week 6: Best Practices
**Key Concepts:** Error handling, testing, cost optimization
**Common Issues:**
- Over-engineering too early
- Not enough real testing
- Forgetting production considerations

**Tips:**
- Share production war stories
- Discuss real failure modes
- Emphasize iterative improvement

## Troubleshooting Guide

### "Module not found" errors
```bash
pip install -r requirements.txt
```

### API key not working
1. Check .env file exists in root
2. Verify key starts with 'sk-'
3. Check OpenAI account has credit
4. Restart Jupyter kernel

### Jupyter won't start
```bash
pip install --upgrade jupyter notebook
jupyter notebook --generate-config
```

### Rate limit errors
- Slow down requests
- Check account tier
- Implement exponential backoff

### High costs
- Switch to gpt-4o-mini
- Reduce max_tokens
- Implement caching
- Show usage dashboard

## Pacing Suggestions

### 50-minute session structure:
- 0-5 min: Review previous week's assignment
- 5-25 min: Present new concepts with live coding
- 25-40 min: Hands-on experimentation
- 40-45 min: Introduce assignment
- 45-50 min: Q&A and wrap-up

### If running behind:
- Skip bonus content
- Assign extra reading
- Focus on core concepts
- Extend lab time

### If ahead of schedule:
- Deeper Q&A
- Show additional examples
- Discuss advanced topics
- Workshop troubleshooting

## Assignment Grading Rubric (if grading)

### Completeness (40%)
- All required elements present
- Code runs without errors
- Demonstrates understanding

### Quality (30%)
- Code is well-commented
- Follows best practices
- Handles edge cases

### Creativity (20%)
- Applied to real domain problem
- Thoughtful design decisions
- Goes beyond requirements

### Reflection (10%)
- Thoughtful answers
- Demonstrates learning
- Identifies improvements

## Additional Resources

### For Participants
- OpenAI Cookbook: https://github.com/openai/openai-cookbook
- OpenAI Documentation: https://platform.openai.com/docs
- Python dotenv docs: https://pypi.org/project/python-dotenv/

### For Instructors
- Keep examples updated with latest API
- Watch for model deprecations
- Monitor pricing changes
- Collect participant feedback

## Feedback Collection

### Mid-series check-in (Week 3)
- Pacing appropriate?
- Technical level right?
- Need more/less support?

### End of series
- What worked well?
- What should change?
- Would you recommend?
- Future topics of interest?

## Common Questions & Answers

**Q: Can I use Claude/Gemini instead of OpenAI?**
A: Yes, but you'll need to adapt the API calls. Core concepts remain the same.

**Q: Do I need to know machine learning?**
A: No! This workshop focuses on using LLMs, not building them.

**Q: Will this work with my own data?**
A: Yes! RAG weeks specifically cover working with your own documents.

**Q: How much will this cost?**
A: Typically $5-10 total using gpt-4o-mini for all assignments.

**Q: Can I use this for production?**
A: Week 6 covers production considerations, but further work needed for true production deployment.

## Contact

For questions or issues:
- During sessions: Ask immediately
- Between sessions: [Communication channel]
- Technical issues: [Support contact]
