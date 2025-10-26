---
title: DataTone Blog Post – Alvin Kang
layout: default
---

# DataTone: Managing Ambiguity in Natural Language Interfaces for Data Visualization  
**By Bongshin Lee, Rubaiat Habib Kazi, Nathalie Henry Riche, Sheelagh Carpendale, and Steven M. Drucker (UIST 2015)**  
*Blog post by Alvin Kang*  

---

## Introduction  
As data becomes increasingly central to decision-making, there is a growing need for tools that allow a wider range of users to explore and visualize data, not just data scientists.  
Creating charts and dashboards, however, can be challenging for users who do not have technical expertise or knowledge of programming.  

DataTone addresses this problem by enabling users to type **natural language queries** to generate visualizations while effectively managing the **ambiguities of human language**.

---

## Background and Motivation  
Traditional visualization tools, including drag-and-drop interfaces like Tableau, require users to understand concepts such as axes, labels, and chart types. This learning curve can make visualization inaccessible to many users.  

DataTone was designed to make data visualization **as natural as conversation**. The authors recognized that:  
- People naturally think and communicate in **everyday language**, not formal syntax.  
- Ambiguity is inherent in language; for example, the term “region” could refer to a state, country, or sales territory.  

By treating ambiguity as part of the interaction rather than an error, DataTone reduces the cognitive barrier to data exploration.

**Additional context for readers:**  
- Understanding **traditional visualization workflows** helps appreciate the simplification offered by DataTone.  
- Basic knowledge of **natural language processing (NLP)** can clarify how queries are interpreted.  
- Recognizing that ambiguity is normal in human communication explains the necessity of **shared disambiguation**.

---

## Natural Language Interfaces for Visualization  
Natural Language Interfaces for Visualization (NLIVs) allow users to communicate with computers using ordinary language instead of code.  

Human language is **ambiguous and context-dependent**, which presents challenges for NLIVs. DataTone addresses these challenges by turning ambiguity into a **collaborative process**: the system interacts with the user to clarify intent and generate accurate visualizations.

**Example of ambiguity handling:**  
1. Query: “Show revenue and profit by region for last quarter.”  
2. Possible ambiguities:  
   - “Region” could refer to state, country, or sales territory.  
   - “Revenue and profit” could be represented as separate charts, combined bars, or line charts.  
3. DataTone presents clarification options via **disambiguation widgets**.  
4. User selection determines the final visualization.  

This process illustrates how DataTone manages ambiguity in a systematic manner.

---

## Compare and Contrast: Traditional Tools vs. DataTone  

| Feature | Traditional Tool | DataTone |
|---------|-----------------|----------|
| Input | Drag-and-drop, scripting | Natural language query |
| Ambiguity Handling | User must guess, trial-and-error | Interactive disambiguation |
| Learning Curve | Medium to high | Low, beginner-friendly |
| User Control | Limited | Shared control between user and system |
| Error Recovery | Manual correction | Interactive clarification widgets |

This comparison highlights the key advantages of DataTone over conventional visualization tools.

---

## Technical Architecture  
DataTone consists of several modular components:

- **Natural Language Parser:** Identifies attributes, metrics, and actions in queries.  
- **Ambiguity Detector:** Flags terms with multiple possible meanings.  
- **Mapping Engine:** Converts language components into visualization parameters.  
- **Disambiguation Interface:** Provides options for user clarification.  
- **Visualization Renderer:** Produces the final chart after clarification.

The pipeline can be summarized as:  
