# Anatomy of Horror  
**Milestone 01 — 2025/10/24**  

The goal of this project is to explore **horror films as a cultural barometer**, reflecting collective anxieties across time, geography, and culture.  
By combining film metadata, language models, and visual analysis, this project seeks to uncover patterns linking the menaces that define horror to the contexts that produce them.

---

## Main Data Sources
- **TMDb API**: metadata for ~4,000 horror movies (1950–2024): titles, genres, countries, keywords, posters, etc.
- **LLM-generated labels**: manually defined "fear categories" and applied them using a natural language model.  
- **Relevant scholarship**: to inform the typology of fears and interpretation.

---

## Notes
The data is spread across different sources and formats. Basic merging and cleaning will involve steps like:  
- Handling missing or short plot overviews (<150 chars).  
- Parsing and normalizing country and genre fields.  
- Extracting LLM-generated fear categories from text responses.  
- Downloading and preprocessing poster images.  

---

## Project Directions

### **Option 1 — The Mapping of Fear**
**Questions:**  
- How have dominant fear types in horror changed across decades?  
- Do different countries tend to produce different types of horror?  
- Do fear themes correlate with titles, keywords, or other features (e.g., director gender)?  
- How accurate is the LLM classification compared to a smaller manual sample?

**Approach:**
- Use film metadata and text-based features (title, overview, keywords) to classify each movie into one of 11 fear categories.  
- Compare LLM-assigned labels to human-coded subsets for reliability testing.  
- Analyze how the relative share of each fear type changes across time, region, and potentially gender.  
- Optional focus: restrict the analysis to one country and contextualize findings with specific historical data (e.g., migration, conflict, or economic data).

---

### **Option 2 — The Aesthetics of Fear**
**Question:**  
Do visual trends in horror posters change over time?
Are there identifiable types of posters in the horror gender? Do they align with their thematic or production countries?

**Approach:**  
- Download and analyze poster images.  
- Extract visual features (color palettes, contrast, saturation, darkness, etc.)  
- Cluster films visually to detect recurring patterns, using both unsupervised and supervised methods.
- Examine potental clusters in relation to fear categories, decades, and countries.
