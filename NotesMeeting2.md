# Meeting 2: Notes

### Answering the questions put forward in the last meeting: 

>> ### What is my idea to handle the main issue of the project: Complex QA? 

The definition of complex QA defined in the previous meeting was

>> A composition B are there in the training dataset, C also exists in the dataset but is not related in any way with B. The final model should be able to generate B composition C when the need arises.

Compositionality is only one aspect of complex question and answer, and the given definition is restricted to only a few examples in terms of complexity. The proposal I  put forward tends to handle this issue by:

- Creating a bigger dataset of composite complex question and answer, as bigger dataset have been known to enhance the performance of the NsPM models.

- To create a bigger dataset I intend to follow the specific methods laid out in my proposal.

- While carrying out the literature survey I came across some important findings on which i would like to here the mentors comments (later part of this page). 
-----

### Work done this week:

- Understanding the code base. (Still working)
- Literature Survey.
- We will be using GERBIL for all testing purposes, I intend to create the script for converting the datsets we have to the format accepted by GERBIL and then let it calculate the scores.(By file upload mechanism)

## Literature Survey

While carrying out the literature survey I came across another definitions which are as follows:

>> Simple QA: those which can be answered using a SPARQL query with a single triple pattern.

>> Complex QA: Questions in which the intended SPARQL query does not consist of a single triple pattern.

Many queries are not simple: 
- Comparative
questions (e.g. "Was John Oliver born before Jon Stewart?"),  
- Boolean questions (e.g.
"Is Poland a part of Eurozone?")
- Questions involving fact aggregation (e.g. "Who
has won the most Grammy awards?")
- Logically composite question (e.g. "In
which university did both Christopher Manning and Sebastian Thrun teach?") 

These cannot be answered by a system restricted to simple questions.

Source: [LC-QuAD: A Corpus for Complex Question Answering over Knowledge Graphs](http://lc-quad.sda.tech/)

-----

### Data generation

- A very similar method to that used by Aman was used in the preparation of LCQuAD data set which comprises of 5000 samples. Example:

```json
{
        "_id": "1701", 
        "corrected_question": "Which architect of Marine Corps Air Station Kaneohe Bay was also tenant of New Sanno hotel /'", 
        "intermediary_question": "What is the <architect> of the <Marine Corps Air Station Kaneohe Bay> and <tenant> of the <New Sanno Hotel>", 
        "sparql_query": " SELECT DISTINCT ?uri WHERE { <http://dbpedia.org/resource/Marine_Corps_Air_Station_Kaneohe_Bay> <http://dbpedia.org/property/architect> ?uri. <http://dbpedia.org/resource/New_Sanno_Hotel> <http://dbpedia.org/ontology/tenant> ?uri} ", 
        "sparql_template_id": 16
    }
```

- The data generation methodology is very similar to Amans but natural language questions were made gramatically correct using human intervention.(By paraphrasing)

- The dataset is fairly big compared to other available datasets, we can replace the entities to increase the size of the dataset by many folds. One such application was: https://github.com/hobbit-project/QuestionAnsweringBenchmark

- You can find the paper here: [LC-QuAD: A Corpus for Complex Question Answering over Knowledge Graphs](http://lc-quad.sda.tech/)

- The main point here being that a carefully curated datset exists and we should take advantage of it.  

- The paper stated that the said dataset was to be later included in QALD8  but the size of the training datset was only 219 questions in QALD8.

---

### Checking out the previous competitors in QALD dataset:

>> WDAqua-core1: A Question Answering service for RDF
Knowledge Bases:

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
upb.de:80/. Their system is able to cope with comparatives and superlatives in
questions via hand-crafted rules.

## Conclusion

- The literature survey played a very important role in helping me understand the current state of research in this field.

- Data genertion has been done before, leveraging the work that has already been done will be beneficial.

- Going through the previous implementations, i also came across a point that training final model over DBpedia is a very computationally expensive task. Any addition of entities will cause the model to be modified accordingly.

- I would like to continue to explore the areas a bit more this weeks and come up with some ideas I have in mind without changing the current timeline.


### [Index Page](https://anandpanchbhai.com/A-Neural-QA-Model-for-DBpedia/)









