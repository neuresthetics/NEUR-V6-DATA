# NEUR-V6-DATA
V6 Rendition of Neuresthetics Theory

# Project Overview

This repository contains scripts and data files related to aggregating lists of historical geniuses from various AI-generated sources and additional JSON files for definitions and belief system evaluations.

## Files Description

- **aggregateGeniiListsByFreq.py**: A Python script that processes multiple CSV files containing lists of geniuses (from sources like Grok, Gemini, DeepSeek, and GPT). It normalizes names, groups entries, resolves duplicates using fuzzy matching, aggregates frequencies, determines primary fields, sorts the results by frequency (descending) and name (ascending), and outputs a refined CSV file named 'geniiAggregateSortFreq.csv'. The script handles up to 500 entries, ensuring no more than that in the final list.

- **geniiGrok.csv**: A CSV file listing names and fields of notable geniuses, generated or compiled by Grok AI. It includes historical figures across domains like mathematics, physics, philosophy, literature, and more, with some entries truncated in the provided document.

- **geniiGemini.csv**: A CSV file similar to geniiGrok.csv, but sourced from Gemini AI. It contains names and fields of geniuses, covering polymaths, scientists, philosophers, artists, and others, with some duplicated or truncated entries noted.

- **geniiDeepSeek.csv**: A CSV file from DeepSeek AI, listing geniuses with their names and fields. It spans a wide range including polymaths, scientists, philosophers, artists, and extends into social sciences and anthropology, with significant truncation in the document.

- **geniiGPT.csv**: A CSV file from GPT AI, containing names (often hyphenated) and fields of geniuses. It covers physicists, mathematicians, philosophers, economists, activists, politicians, artists, musicians, and more, focusing on impactful figures.

- **geniusDefinition.json**: A JSON file providing a detailed definition of "genius," including etymology, operational criteria for identification (emphasizing achievement over IQ), exclusion criteria, distinctions from related concepts, historical context, and guidelines for CSV compilation (e.g., targeting >=300 unique entries, duplicate handling).

- **beliefCoherence.json**: A JSON file evaluating various belief systems (e.g., Atheism, Secular Humanism, Rationalism, up to Falun Gong) on criteria like logical self-consistency, resolution of paradoxes, empirical compatibility, evidence vs. revelation, and predictive success. Each entry includes scores, notes, and overall reasoning, ranking systems from high (e.g., Atheism at 50) to low coherence.