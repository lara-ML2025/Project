# Anatomy of Horror  

The goal of this project is to explore horror films as a cultural barometer, reflecting collective anxieties across time, geography, and culture.
By combining film metadata, language models, and visual analysis, the project seeks to uncover patterns linking the menaces that define horror to the contexts that produce them.

---

## Main Data Sources
- TMDb API: metadata for 5,000 horror films released between 1950 and 2024 (titles, genres, countries, keywords, date of release, poster images).
- IMDb datasets: ratings and vote counts used to contextualize horror relative to other genres in the recent landscape.
- LLM-generated labels: a manually defined taxonomy of 11 fear categories applied to the dataset using a local large language model.
---

### Notes on Data Preparation
The data is spread across multiple sources and formats. Preparation involved steps such as:
- Merging IMDb and TMDb metadata.
- Handling missing or very short plot overviews.
- Parsing and normalizing fields like genre, decade, and country.
- Extracting and structuring LLM-generated fear labels from text responses.
- Downloading, resizing, and preprocessing poster images for visual analysis.
---

## Implemented Analyses

### Narrative Analysis — Mapping Fear

Questions:
- What are the dominant fear types in horror films?
- How does fear representation evolve across historical periods?

Approach:
- Classified each horror film into one of 11 manually defined fear categories using plot overviews and keyword metadata.
- Tested the LLM prompt on a smaller sample before applying it to the full corpus.
- Analyzed the distribution of fear categories across decades and compared long-run trends.

### Visual Analysis — The Aesthetics of Fear

Questions:
- Do horror posters exhibit recurring visual patterns?
- Do these visual patterns align with specific fear categories or historical periods?
- When do visual aesthetics diverge from narrative themes?

Approach:
- Downloaded and embedded poster images using CLIP (ViT-B/32).
- Reduced dimensionality with PCA and clustered posters using KMeans.
- Interpreted clusters manually and cross-referenced them with fear categories and decades.
- Applied TF-IDF to plot overviews within visual clusters as an additional interpretive validation.