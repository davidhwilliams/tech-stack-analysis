# Web App Tech Stack Clustering and Trends Analysis

This project aims to cluster web apps based on their tech stack features to identify common patterns and outliers between frontend and backend web app frameworks.

### Tasks

- Represent tech stacks as feature vectors (e.g., one-hot encoding or embeddings for technologies).
- Apply clustering algorithms like K-Means, DBSCAN, or Hierarchical Clustering.
- Use dimensionality reduction techniques like PCA to visualize clusters.

### Outcome

- Clear grouping of tech stack clusters (e.g., modern stacks, legacy stacks, highly specialized stacks).
- Insights into which clusters are most associated with scalability, performance, or domain-specific success.

### Data Sources

- GitHub repositories via [GitHub API](https://docs.github.com/en/rest?apiVersion=2022-11-28)

---

## Prerequisites

Before you begin, ensure you have met the following requirements:

- Python 3.7 or higher
- Install dependencies from `requirements.txt` by running:

```bash
pip install -r requirements.txt
```

## Running the Jupyter Notebook

To interactively explore the data and train models, you can use the provided Jupyter notebook. Follow these steps:

```bash
# 1. Start Jupyter Notebook
jupyter notebook

# 2. Open the notebook
tech-stack-frameworks.ipynb
```

This notebook includes:

- Exploratory Data Analysis (EDA) on GitHub Repositories.
-

### Results

- Cluster Themes: Clusters were grouped by common library usage:
  - Frontend-heavy clusters: Dominated by libraries like React, Vue, and Angular.
  - Backend-heavy clusters: Included frameworks like Express, Koa, and Django.
  - Utility-heavy clusters: Featured general-purpose libraries like Lodash, Axios, and Moment.
- Cluster Insights:
  - Larger clusters represented general-purpose stacks, while smaller clusters indicated niche or domain-specific technologies (e.g., data visualization or 3D graphics).
  - Utility libraries like Axios and Lodash appeared across multiple clusters, reflecting their versatility.
- Shortcomings:
  - The clustering grouped libraries by similarity but didn’t explicitly uncover frontend-backend pairings as originally intended.

## Future Improvements

- Feature Engineering:

  - Incorporate co-occurrence metrics to explicitly capture relationships between frontend and backend libraries.
  - Use project metadata (e.g., size, stars, or domain) to add context to the clusters.

- Advanced Clustering Techniques:

  - Experiment with graph-based clustering to model relationships between libraries directly.
  - Explore hierarchical clustering for better interpretability.

- Expanded Dataset:

  - Include additional dependency file types, such as pom.xml for Java or requirements.txt for Python.
  - Use external datasets, like developer surveys or job postings, to validate and enrich the clustering analysis.

- Visualization Enhancements:

  - Develop interactive dashboards to explore clusters dynamically.
  - Use network graphs to visualize relationships between libraries.

- Iterative Refinement:
  - Iterate on preprocessing and clustering based on feedback to align the results more closely with the goal of identifying frontend-backend combinations.

## License

This project is licensed under the MIT License - see the LICENSE file for details.
