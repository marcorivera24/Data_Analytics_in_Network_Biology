# Data Analytics in Network Biology

This project was developed for the **Advanced Coding for Data Analytics** course at **Luiss Guido Carli**.  
The objective was to construct and analyze a **biomedical knowledge graph** using publicly available data from **Hetionet**, with a focus on discovering relationships between diseases, symptoms, genes, compounds, and side effects. :contentReference[oaicite:2]{index=2}

## Project Overview

Biological systems can be modeled as graphs, where:

- **Nodes** represent biological entities such as genes, diseases, compounds, symptoms, pathways, and side effects
- **Edges** represent relationships between those entities

In this project, the graph was built from two files:

- `nodes.tsv` → contains entity ID, name, and kind
- `edges.sif` → contains connections between entities and their edge types

The graph was created in Python using libraries such as **Pandas** and **NetworkX**, then saved for reuse in future analyses. :contentReference[oaicite:3]{index=3} :contentReference[oaicite:4]{index=4}

## Dataset

The project uses the **Hetionet biomedical knowledge graph**, a heterogeneous network containing multiple biological entity types and relationships.  
The dataset includes:

- Genes
- Diseases
- Symptoms
- Compounds
- Pathways
- Molecular functions
- Biological processes
- Cellular components
- Anatomy
- Pharmacologic classes
- Side effects :contentReference[oaicite:5]{index=5} :contentReference[oaicite:6]{index=6}

## Tools and Technologies

- **Python**
- **Pandas**
- **NetworkX**
- Data visualization libraries for charts and graph plots

## Project Tasks

### Task 1 — Constructing the Biomedical Knowledge Graph
- Loaded `nodes.tsv` and `edges.sif`
- Created a directed biomedical graph
- Added nodes with attributes and edges with metaedge labels
- Saved the graph to avoid rebuilding it every time :contentReference[oaicite:7]{index=7} :contentReference[oaicite:8]{index=8}

### Task 2 — Analyzing the Biomedical Knowledge Graph
The following analyses were performed:

1. Computed the total number of entities for each unique node kind  
2. Computed the total number of each unique edge type  
3. Computed the average in-degree and out-degree for each node type  
4. Computed the number of connections for each disease and identified the most connected diseases  
5. Extracted the **Disease–Symptom** subgraph and computed the average number of connections between diseases and symptoms  
6. Measured similarity between:
   - **Type 1 diabetes mellitus** and **Type 2 diabetes mellitus**
   - **Eye Pain** and **Blindness**
7. Built a small case study for an imaginary patient using the symptom **Hemoglobinuria**, exploring possible diseases, genes, treatments, and side effects. :contentReference[oaicite:9]{index=9} :contentReference[oaicite:10]{index=10}

## Key Results

Some of the main results from the analysis include:

- The biomedical graph contains a wide range of heterogeneous node types, with **genes** being the most frequent category
- The most common edge types include relationships such as:
  - gene participates in biological process
  - anatomy expresses gene
  - gene regulates gene
  - gene interacts with gene
- The **Disease–Symptom** subgraph contains **575 nodes** and **3900 edges**
- The total number of disease-symptom connections is **3357**
- The average number of symptom connections per disease is **24.50**
- The cosine similarity between:
  - **Type 1 diabetes mellitus** and **Type 2 diabetes mellitus** is **0.3145**
  - **Eye Pain** and **Blindness** is **0.5916**
- The most connected diseases in the graph include:
  - breast cancer
  - hematologic cancer
  - IgA glomerulonephritis
  - melanoma
  - rheumatoid arthritis :contentReference[oaicite:11]{index=11}

## Example Patient Analysis

To demonstrate how graph analysis can support biomedical reasoning, an imaginary patient with the symptom **Hemoglobinuria** was studied.

### Possible diseases:
- Anemia
- Malaria

### Example treatment insights:
- **Anemia**:
  - vitamin supplements
  - dietary adjustments
  - blood transfusions in specific cases

- **Malaria**:
  - Artemether
  - Quinine

### Example gene associations:
- **Malaria**: BIN1, DNPH1, THOC3, LRRN3
- **Anemia**: CHEK1, PRF1, IFNA2, NPPB

This case study shows how graph-based analysis can connect symptoms to diseases, genes, compounds, and side effects in a structured way. :contentReference[oaicite:12]{index=12}

## Visualizations

The project presentation includes:

- An overall biomedical graph visualization
- Bar charts for node-type and edge-type counts
- Degree analysis by node category


- Most connected diseases
- Disease–symptom subgraph visualization
- Similarity analysis between diseases and symptoms
- A final patient-centered graph exploration for Hemoglobinuria :contentReference[oaicite:13]{index=13}

  ## Link Presentation
  https://www.youtube.com/watch?v=GHodgL50AWs
  

