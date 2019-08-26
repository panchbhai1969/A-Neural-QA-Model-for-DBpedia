# The training week | The Results

## TL;DR
[Eukaryotes] : Using pre-trained embeddings for DBpedia (Biased graph walks: https://zenodo.org/record/1320038#.XT8CeHUzbEG) for SPARQL embeddings and English: pre trained embeddings using the models already trained by me with the following configuration:  
- Layer:2 
- Size: 128
- Without attention
- Drop-out: 0.2
- Dataset: 10% test | 10% dev | 80% train
- BLEU: 97.69 and accuracy: 89.75

The performance reached was:
- BLEU: 93 units
- Accuracy: 63 units

Best results were reached at 15000 iterations, 

Interestingly the train set had a hard time to reach good performance. The performance dipped after 45,000 iterations to 85 BLEU and 25% accuracy. May be overfitting. The mentors too agreed that this decrease might be the case of overfitting.

![Eyukaryotes: Test BLEU graph](static/eukaryotes-test-bleu.png)

Two directions were suggested by the mentors in the last meeting:
- One was to continue using the RDF2Vec embedding and record all the results thus ending the GSoC project there
- Second being to explore the area of fasttext for training the embeddings.

Looking at the time constraints it is not possible to look into something new and finish all the while maintaining quality. The work will be hasty and not upto the mark.
- Each experiment approximately took:
    - Institute server: ~ 1 day 20 hours
    - GCP: ~4 hours
     
### Tests on the Person data

New tests were done on the person dataset. The following results were found:(attention: attention scaled luong)
<span align="centre">![table](static/table.png)</span>

## TL:DR ends

<span align="centre">![table](static/person_results.png)</span>


### [Index Page](https://anandpanchbhai.com/A-Neural-QA-Model-for-DBpedia/)
