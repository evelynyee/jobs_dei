# CS 329R Project - Fall 2025
Working title: *(Un)virtue signaling: AI/ML job postings in a post-DEI America*

Evelyn Yee

**Question:** How have US tech companies responded to the 2025 [anti-DEI executive orders (EOs)](https://civilrights.org/resource/anti-deia-eos), in regards to their public-facing AI/ML job postings?

**Significance:** The Trump administration has brandished "anti-woke" as a major political priority in public messaging and political actions, as seen in the volley of executive orders and the recent [AI Action Plan](https://www.ai.gov/action-plan). The most ubiquitous generative AI tools are primarily being developed by US-based companies (e.g., OpenAI, Google, Anthropic, Meta), American politics and beliefs may have a massive impact on the state of AI development, including the crucial question of who develops these models. If tech companies are changing their job postings to encourage less diversity, equity, and inclusion, this will create blocks for diverse candidates to apply and receive jobs in this space, limiting the perspectives involved in the development of this influential technology.

**Hypotheses:** More DEI; Less DEI; Same amount of DEI sentiment but less explicit language; No change at all
- **Null Hypothesis:** The language used in AI/ML job postings is the same, regarding DEI content, before and after the anti-DEI executive orders.
    - **Interpretation:** The EOs have not been effective at changing hiring practices in AI/ML roles.
- **My (prior) hypothesis** is that **DEI language has reduced in general**. Most companies have reduced/removed DEI sentiments completely from their job postings, but a **few companies have kept the sentiment** despite explicit wording changes.
    - **Interpretation:** The EOs have been effective to reduce outward DEI hiring presentation, but in certain DEI-motivated companies, they may not have changed the internal considerations.

**Data:** US AI/ML job postings before and after February 2025
- Before: https://www.kaggle.com/datasets/kanchana1990/ai-and-ml-job-listings-usa
    - 1K? rows, Latest dated June 2024.
- After: https://www.kaggle.com/datasets/ivankmk/thousand-ml-jobs-in-usa
    - 858 rows from March 2025 or later; 139 from February 2025 or earlier.

Pre-processing: text normalization (punctuation, case), tokenization/word splitting

**Methods:**
- Word frequency (average # of DEI words per posting)
    - Narrow vocabulary: "diversity", "diverse", "equity", "equitable", "inclusion", "inclusive"
    - Broad vocabulary: other words with highly correlated Word2Vec embeddings to the list above
- LLM grading: binary indication whether the post contains DEI-related content or not
    - validate a small random sample of LLM grades manually

**Extension**: Analyze trends across multiple sectors of job posts

General job posting datasets (all require paid access):
- [Revio - COSMOS](https://www.reveliolabs.com/job-postings-cosmos/)
- [Bright Data - LinkedIn/Indeed/Glassdoor](https://brightdata.com/products/datasets)
- [Techmap](https://aws.amazon.com/marketplace/pp/prodview-c4xjytslo7mqy#offers)


