# Week Eight and Nine | Stage 4 | Hard Week, Slow performance gains

## TL;DR

Pretty sloppy weeks! Here are the tasks I was supposed to accomplish this week:

- A new test was suggested by one of the Mentors whuch was making sure to have some composition template exclusively in the test:
  - train will contain A, B
  - test will contain AoB
  - Her A and B represent ontology entities (*Done*)
- Improve the performance on this test (*In progress*)
- Report on experiments done. (*Done*)
- Add TLDR(To Long Didn’t Read) section to the blogs. (*In progress*)
- Improve and adapt whenever required. (*In progress*)
- Complete Blogs (*Not Done*)

### Suggestions after meeting

- Introduce proper alignment information to the model. This might fix the `<unk>` problem. As used in this paper: [https://arxiv.org/pdf/1806.10478.pdf](https://arxiv.org/pdf/1806.10478.pdf)
- Example:
  - it means to literally append lines to the `train.{en,sparql}` files with labels and resources, respectively. the result was faster convergence, so reaching a certain BLEU score in less time. an example could be:

```SPARQL  
train.en
--------
what is the capital of Germany?
...
germany
united states
japan
```

```SPARQL
train.sparql
------------
select var_s where br_open dbr_Germany dbo_capital var_s br_close
...
dbr_Germany
dbr_United_States
dbr_Japan
```

- Try embeddings
- One is to use a word embedding model which supports OOV words, such as fastText
- Another is to train your own corpus also including Wikipedia
- Add more examples to allow the model to learn so that the prediction increases.

### This Week Work

- Try more experiments, understand, evolve and proceed.

## End TL;DR

### [Index Page](https://anandpanchbhai.com/A-Neural-QA-Model-for-DBpedia/)









