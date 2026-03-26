RAG-Food Enhanced (with 15 Diverse Food Items)

Developer
- Name: Steven Carlo Lura

Project customization overview
This enhanced version of RAG-Food adds 15 new, richly documented food items to `philippines_foods.json`, categorized as:
- 5 regionally traditional dishes from Antipolo City, Philippines (cultural/regional cuisine background)
- 5 healthy foods with detailed nutritional benefits
- 5 popular international dishes with cooking methods

It features:
- Semantic search using ChromaDB and Ollama models
- Comprehensive details per item: name, category, origin, description, ingredients, preparation, nutrition, cultural significance, dietary classifications
- Validation script for testing queries

15 Newly-added Food Items

| # | Name | Category | Origin | Description |
|---|------|----------|--------|-------------|
| 1 | Antipolo Ham | Meat | Antipolo City, Philippines | Sweet, glazed ham cured and smoked with pineapple glaze; symbolizes Filipino Christmas traditions. |
| 2 | Antipolo Longganisa | Sausage | Antipolo City, Philippines | Sweet and garlicky sausage; breakfast staple in Philippines. |
| 3 | Antipolo Bibingka | Dessert | Antipolo City, Philippines | Rice cake topped with salted egg and cheese; associated with Christmas traditions. |
| 4 | Bulalo | Soup | Antipolo City, Philippines | Hearty beef shank soup; comfort food in Philippines. |
| 5 | Sinigang | Soup | Antipolo City, Philippines | Sour tamarind soup; represents Filipino sour soups. |
| 6 | Quinoa | Grain | Andean Region, South America | Nutrient-dense seed; ancient Incan staple, high in protein. |
| 7 | Kale | Vegetable | Mediterranean Region | Leafy green packed with vitamins; ancient Mediterranean vegetable. |
| 8 | Salmon | Fish | North Atlantic and Pacific Oceans | Fatty fish with omega-3; staple for indigenous communities. |
| 9 | Blueberries | Fruit | North America | Antioxidant-rich berries; Native American foraged fruit. |
| 10 | Almonds | Nut | Middle East and Central Asia | Nutrient-rich nuts; ancient prized nut. |
| 11 | Sushi | Seafood Dish | Japan | Vinegared rice with seafood; Japanese tradition, global popularity. |
| 12 | Paella | Rice Dish | Spain | Saffron-infused rice with seafood and chicken; Spanish communal dish. |
| 13 | Tacos | Street Food | Mexico | Tortilla filled with meat and salsa; Mexican street food. |
| 14 | Pasta Carbonara | Pasta Dish | Italy | Creamy pasta with eggs and pancetta; Roman classic. |
| 15 | Thai Green Curry | Curry | Thailand | Spicy curry with coconut milk; Thai flavor balance.

Installation and setup
1. `cd ragfood`
2. Optional virtual env: `python -m venv venv && .\venv\Scripts\activate`
3. `pip install chromadb requests`
4. Ensure Ollama models present:
   - `ollama pull llama3.2`
   - `ollama pull mxbai-embed-large`
5. Start Ollama in another shell or background.
6. Run:
   - `python rag_run.py` (loads main foods.json)
   - Or modify script to load `philippines_foods.json` for the diverse food data

Validation test queries
Use `python test_rag_queries.py` to run sample queries (adapt for diverse data):
- What is Antipolo Ham?
- What are some healthy foods high in protein?
- How is Paella prepared?
- Sabihin mo sa akin ang tungkol sa mga ulam na Filipino
- Ano ang mga vegan options na available?
- Ano ang mga pagkain na maaaring i-grill?
- Ipaliwanag ang nutritional benefits ng Brazilian Acai Bowl (or Filipino equivalent)
- Paano lutuin ang Spanish Seafood Paella? (or Filipino adaptation)
- Ilarawan ang Moroccan Chickpea & Sweet Potato Tagine (or Filipino version)
- Ano ang Shakshuka with Spinach? (or Filipino dish)
- Alin ang mga gluten-free na dishes?

Personal Reflection 
Working on this RAG-Food project has been an eye-opening journey into the world of Retrieval-Augmented Generation and AI-driven systems. As a student from Far Eastern University, I initially approached this with curiosity about how machines could understand and respond to natural language queries about food. The process of curating 15 Filipino food items, all described in Filipino, deepened my appreciation for my cultural heritage while challenging me to think critically about data representation in AI.

The technical aspects were daunting at first—setting up ChromaDB for vector embeddings, integrating Ollama for local LLM inference, and ensuring semantic search accuracy. I learned that RAG isn't just about feeding data to a model; it's about crafting context that allows the AI to reason and provide grounded answers. Debugging timeouts and connection issues with Ollama taught me patience and the importance of robust error handling in AI applications.

What struck me most was the growth mindset required in AI development. Each failed query or inaccurate response wasn't a setback but a learning opportunity. I iterated on the data, refining descriptions to include more nutritional details and cultural significance, which improved retrieval quality. This project reinforced that AI builders must be interdisciplinary—combining computer science with domain knowledge, in this case, Filipino cuisine.

The experience also highlighted ethical considerations in AI, like ensuring diverse and accurate representations of cultures. By focusing on Filipino foods, I contributed to making AI more inclusive, potentially helping preserve culinary traditions through technology.

Looking forward, I'm excited to apply these skills in future projects, perhaps in healthcare or education, where RAG could democratize access to information. This endeavor has transformed me from a passive AI user to an active builder, fostering a lifelong commitment to innovative, responsible AI development. (Word count: 312)

Important Notes
- All food descriptions are in Filipino for cultural authenticity.
- To use Filipino data exclusively, modify `rag_run.py` to load `filipino_foods.json`.
- Ensure Ollama is running for queries to work.
- This project demonstrates understanding of vector embeddings and semantic search.
