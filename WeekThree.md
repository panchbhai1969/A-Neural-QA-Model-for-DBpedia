# WeekThree | Literature Survey

It's the third week now, I have gone through a lions part of the existing codebase that I am going to work on for the next few months. 

While doing my older project, I learnt an important aspect of working on something new and that was to understand the bleeding edge of technology that pertains to your area of work. While creating the proposal I did go through a lot of papers but while solely working on the project I decided to dig a bit deeper.

### Work done this week:

- Understanding the code base. (mainly template-generation )
- We will be using GERBIL for all evaluation purposes, I intend to create the script for converting the datsets we have to the format accepted by GERBIL and then let it calculate the scores.(By file upload mechanism)
- Literature Survey.

---
## Literature Survey.

The first stop was to re-read the papers I already read that were part of this project:
 
- SPARQL as a Foreign Language: https://arxiv.org/abs/1708.07624
- Neural Machine Translation for Query Construction and Composition: https://arxiv.org/abs/1806.10478

These papers forma the very base of this project idea, and it was important to understand them properly before diving into the code.

---

Now there were 2 important aspect to the final goal of this project that I had decided to focus on:

- Perform experiments on compositionality for complex QA
- QALD benchmark

While searching for complex Q&A I found about the LCQuAD dataset:

## LCQuAD

- A very similar method to that used by Aman was used in the preparation of the LCQuAD dataset which comprises of 5000 samples. Example:

```json
{
        "_id": "1701", 
        "corrected_question": "Which architect of Marine Corps Air Station Kaneohe Bay was also tenant of New Sanno hotel /'", 
        "intermediary_question": "What is the <architect> of the <Marine Corps Air Station Kaneohe Bay> and <tenant> of the <New Sanno Hotel>", 
        "sparql_query": " SELECT DISTINCT ?uri WHERE { <http://dbpedia.org/resource/Marine_Corps_Air_Station_Kaneohe_Bay> <http://dbpedia.org/property/architect> ?uri. <http://dbpedia.org/resource/New_Sanno_Hotel> <http://dbpedia.org/ontology/tenant> ?uri} ", 
        "sparql_template_id": 16
    }
```

- The data generation methodology was very similar to Amans but natural language questions were made gramatically correct using human intervention.(By paraphrasing)

- The dataset was fairly big compared to other available datasets, we could replace the entities to increase the size of the dataset by many folds. One such application was: https://github.com/hobbit-project/QuestionAnsweringBenchmark

- You can find the paper here: [LC-QuAD: A Corpus for Complex Question Answering over Knowledge Graphs](http://lc-quad.sda.tech/)

- The paper stated that the said dataset was to be later included in QALD8  but the size of the training datset was only 219 questions in QALD8.

- The main point here being that a carefully curated datset exists and we should take advantage of it. For template generation. 

## QALD Benchmark

>> QALD is a series of evaluation campaigns on question answering over linked data. So far, it has been organized as an ESWC workshop and an ISWC workshop as well as a part of the Question Answering lab at CLEF.

### Checking out the previous competitors in QALD dataset:

>> WDAqua-core1: A Question Answering service for RDF
Knowledge Bases, brief workflow is given below:

- Query Expansion phase we first see to which possible concepts the consequent words in the question can refer to. 

- Query Construction phase, based on the distance of the different concepts in the graph, we construct all possible SPARQL queries. 

- Query Ranking phase, we rank the generated SPARQL
queries.

- Answer Decision. For this step some training data is needed. This phase consists of a model that decides, based on the features above, if the top-ranked SPARQL query is an answer or not.

---

### There were other approaches too, but most of them were rule based in nature.

- ganswer2 has participated outside the actual challenge this year as a
system without a paper submission in Task 1. Zou et al. use a graph-based
approach to generate a semantic query graph, which reduced the transformation
of natural language to SPARQL to a subgraph matching problem.

- TeBaQA by Peter Nancke et al. from Leipzig University in Germany is an
unpublished system which is based on learning SPARQL templates from past
benchmark challenges and filling them subsequently. The system is available at
http://139.18.2.39:8187/.


- Elon by Szabó Bence et al. from Paderborn University in Germany stems
from a student project and is available at http://qald-beta.cs.upb.de:443/.
It is based on an own dictionary and not yet published.


- QASystem by Lukas Blübaum and Nick Düsterhus is also a student project
from Paderborn University Germany and available at http://qald-beta.cs.
upb.de:80/.  Their system is able to cope with comparatives and superlatives in questions via hand-crafted rules.

## Conclusion

- The literature survey played a very important role in helping me understand the current state of research in this field.
- Data genertion has been done before, leveraging the work that has already been done will be beneficial. The qestions are good in terms of templates and can be used effectively.
- Going through the previous implementations, I also came across a point that training final model over DBpedia is a going to be a computationally expensive task. Any addition of entities will cause the model to be modified accordingly.
- GERBIL will be used for all evaluations.
- There was no task explicitly assigned to me this week so I resorted to the points I mentioned in my proposal and went ahead with the literature survey.
- I would like to continue to explore the areas a bit more the coming week and come up with some ideas  without changing the current timeline.



### [Index Page](https://anandpanchbhai.com/A-Neural-QA-Model-for-DBpedia/)







