# Smart-Search-tool

I developed a smart search tool that allows users to easily find relevant free courses on Analytics Vidhya's platform. Here's a summary of my approach:

1. **Data Collection**: I started by scraping the course titles and other relevant details (such as course links and images) from Analytics Vidhya using BeautifulSoup.

2. **Model Selection**: Initially, I tried using the Groq API for generating embeddings and conducting searches, but it didn't provide the desired accuracy. I switched to using a pre-trained BERT model (bert-base-uncased) to generate embeddings for both user queries and course titles.

3. **Relevance Matching**: To match the user's query with the most relevant courses, I computed the cosine similarity between the query embedding and the embeddings of course titles. This allowed me to rank the courses based on their relevance to the query.

4. **Real-Time Autocomplete**: I implemented a real-time autocomplete feature that suggests the top 3 courses as the user types, improving the search experience through string matching.

5. **Gradio Interface**: I built a clean and user-friendly interface using Gradio, which dynamically displays relevant course details (like titles, images, links, and relevance scores) to users.

6. **Deployment on Hugging Face Spaces**: Finally, I deployed the tool on Hugging Face Spaces for public access and customized the interface with CSS to ensure a visually appealing and responsive design.

Bert model: https://huggingface.co/spaces/vishalranjan105/SmartSearchTool
