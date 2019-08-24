# Final Report | Stage 7 | The final report
## A Neural QA Model for DBpedia
![Welcome](static/welcome.jpg)
Welcome to the final report of this year's GSoC period, If you are a newbie and want t oknow about the journey of this project do read it from the very begining else lets dive straight in. The whole work was added as a single pull request whose link is as follows: <span style="color:red"> Add link here. </span>

This page is divided into parts:

- Introduction
- Stage Wise Explaination 
    - Comparision between what was proposed and what was done.
    - New innovative ideas introduced in that stage and link to detailed information about that idea
    - Link to corresponding code and blog
    - What is left and what was discarded for being impractical.
- Future aspects of this project

If you just wanna have a look at the pristinely written and managed code please find it in the following link: [Github Repository: https://github.com/dbpedia/neural-qa/tree/working-gsoc-anand](https://github.com/dbpedia/neural-qa/tree/working-gsoc-anand)

The Meeting Documents that was maintained for the whole duration of GSoC can be accessed through: [Minutes of the Meeting](static/MOM/MOM.html)

We will try to keep it short and simple, lets begin.

<span align="center">![Begin](static/start.gif)</span>

## Introduction

With booming amount of information being continuously added to the internet, organising the facts becomes a very difficult task. Currently DBpedia hosts billions of such data points and corresponding relations in the RDF format.

Extracting data from such data sources requires a query to be made in SPARQL and the response to the query is a link that contains the information pertaining to the answer or the answer itself.

Accessing such data is difficult for a lay user, who does not know how to write a query. This proposal tries to built upon a System :(​ https://github.com/AKSW/NSpM/tree/master ​) — which tries to make this humongous linked data available to a larger user base in their natural languages(now restricted to English) by improving, adding and amending upon the existing codebase.

>> The primary objective of the project was to be able to translate any natural language question to a valid SPARQL query.

## Stage Wise Explaination 

The whole project was divided into 7 stages according to the proposal submitted. The stage structure is maintained for the ease of grasping the movement of the project through the timeline:



### Stage 0 | Community bonding period (May 6 - 27, 2019)
Understand the the current code base in detail, ponder upon all possible improvements and discuss with the mentors.

- Get to know the mentors and the community: listen, communicate and learn. [<span style="color:green"> Done </span>]
- Learn about the intricacies of the coding practices followed by DBpedia, which include coding, community relations as well as version control practices. [<span style="color:green"> Done </span>]
- Go through research paper on the relevant field to come up with good strategies to handle the problems at hand. (Learn from what has already been done in this field). [<span style="color:green"> Done </span>]
- Understand the people you are working with, finalize all required channels of communication. [<span style="color:green"> Done </span>] 

## Coding period (May 27, 2019 - August 19, 2019)
### Stage 1 | Improvements (Based on current state of research): (May 27, 2019 - June 4, 2019) 
The first stage will mainly focus on fixing all issues in the code to create a proper playing ground for future research endeavour that the project intends to take.

- Fixing all the deprecated parts  of the code to ensure the usability of the code  [<span style="color:green"> Done </span>]
    - The issues that were fixed are:

        | Issues        | URL           | Fixed|
        | ------------- |:-------------:|------:|
        | Zero division error                               | [(https://github.com/dbpedia/neural-qa/issues/8) ](https://github.com/dbpedia/neural-qa/issues/8) |<span style="color:green"> Yes </span> |
        | Adding progress bar for loops in generator.py:    | [(https://github.com/dbpedia/neural-qa/issues/9)](https://github.com/dbpedia/neural-qa/issues/9)     |<span style="color:green"> Yes </span> |
        | Fix tensorflow warnings                           | [(https://github.com/dbpedia/neural-qa/issues/10)](https://github.com/dbpedia/neural-qa/issues/10)              | <span style="color:green"> Yes </span> |
        | Tensorflow version                                | [(https://github.com/dbpedia/neural-qa/issues/11)](https://github.com/dbpedia/neural-qa/issues/11)              | <span style="color:green"> Yes </span> |
        | Fix PIPELINE                                      | [(https://github.com/dbpedia/neural-qa/issues/12)](https://github.com/dbpedia/neural-qa/issues/12)              | <span style="color:green"> Yes </span> |
- Improve the readme to ensure better understanding of the project to new developers and yourself.  [<span style="color:green"> Done </span>]
    - Readme fixes: [https://github.com/AKSW/NSpM/pull/21]
- Use accuracy measures other than BLEU like F-score (Do initial setup for all of them)  [<span style="color:orange"> Completed in stage 3  </span>]
    - BLEU is implemented as part of the NMT model.
    - F1 Score was implemented using GERBIL (Micro-F1 was used for all the tests)
        - As part of establishing a system for using GERBIL the following projects had to be setup:

            | Issues        | URL           |
            | ------------- |:-------------:|
            |GERBIL|[https://github.com/dice-group/gerbil](https://github.com/dice-group/gerbil)|
            |Django WebApp|[https://github.com/panchbhai1969/gerbil-client-django-webapp](https://github.com/panchbhai1969/gerbil-client-django-webapp)|

        - Both contain instructions to run the repository.
    - The blog to the corresponding coding stage is: [https://anandpanchbhai.com/A-Neural-QA-Model-for-DBpedia/WeekSeven](https://anandpanchbhai.com/A-Neural-QA-Model-for-DBpedia/WeekSeven)
- Setting up a way to evaluate the model against the QALD benchmark.  [<span style="color:green"> Done </span>]
    - GERBIL setup [<span style="color:green"> Done </span>]

### Stage 2 | Where do we stand today?  (June 5, 2019 - June 10, 2019)
This stage will shed a light on where we stand and forge a concrete path this project will take. (as according to Aman’s blog, extensive work couldn't be done in compositionality for complex QA because of the time constraints of the project).
- Test the existing model on compositionality for complex QA.   [<span style="color:green"> Done </span>]
    - Test were run on the following templates: [https://github.com/dbpedia/neural-qa/blob/master/data/GS-v3.csv](https://github.com/dbpedia/neural-qa/blob/master/data/GS-v3.csv) 
- Accessing the performance of the model in the previous point.  [<span style="color:green"> Done </span>]
    - The BLUE score on the test split reached ~95.
- Evaluate and adjust the model to gain maximum performance.  [<span style="color:green"> Done </span>]
- Discuss the shortcomings and discuss what to do next, also involving the ideas suggested in the previous section. [<span style="color:green"> Done </span>]

### Stage 3 | Generalised question making framework for compositionality (June 10, 2019 - June 23, 2019)
- Generating domain independent templates to minimize burden on the end user for both complex and simple QA. (As per the discussion in the previous stage ) [<span style="color:green"> Done </span>]
    - It was a rather complicated task, it is elaborately written as one of my post: [https://anandpanchbhai.com/A-Neural-QA-Model-for-DBpedia/WeekSix](https://anandpanchbhai.com/A-Neural-QA-Model-for-DBpedia/WeekSix)

### Stage 4 | Let's make it all natural (June 28, 2019 - July 5, 2019)

Making questions more natural, it was a rather interesting question. I used a mechanism similar to page rank used by google.

- The major idealogy used was: 
>> Hypothesis: Relevance of template can be determined by the popularity of the corresponding answers.
- Popularity can be loosely related to the number of page views and the page view values were extracted from SubjectiveEye3D paper. 
- Again the detailed information of the methodology can be found at: [https://anandpanchbhai.com/A-Neural-QA-Model-for-DBpedia/WeekSeven](https://anandpanchbhai.com/A-Neural-QA-Model-for-DBpedia/WeekSeven)


## Evaluation 1: June 24 - 28, 2019 

### Stage 5 | Finishing Question Making (July 6, 2019 - July 21, 2019)
This stage will be the last stage that tries to address the problems  related to template generation for simple and complex QA.

- Current complex QA model doesn’t understand when to add a new variable in the query, need to devise a method to make it more aware. Discuss and fInd a way to handle these points in the model. (Some of my ideas were mentioned in the previous section ) [<span style="color:red"> Not Done </span>]
- Discuss the results and devise plans for the future steps. 


## Evaluation 2: July 22 - 26, 2019 	


### Stage 6 | The Grid Search (July 27, 2019 - August 10, 2019)
Evaluating the performance of the model by tweaking the attributes for the NMT model to give maximum performance using the training dataset generated in the previous stages. 
- Grid Search [<span style="color:green"> Done </span>] 
    -The corresponding chart is as follows: [Grid Search](static/GridSearch/GridSearch.html)
    - The best results were obtained were:
        - BLEU = ~93
        - Accuracy = 60
    - Details results can be found in the blog: [https://anandpanchbhai.com/A-Neural-QA-Model-for-DBpedia/WeekFifteen.html](https://anandpanchbhai.com/A-Neural-QA-Model-for-DBpedia/WeekFifteen.html)
- Discussion with the mentors. [<span style="color:green"> Done </span>]
- Code cleanup (BUFFER) [<span style="color:orange"> Completed in stage 7 </span>]

### Stage 7 (August 11, 2019 - August 18, 2019)
- Code cleanup  (BUFFER) [<span style="color:green"> Done </span>]

## Students Submit Code and Final Evaluations: August 19 - 26, 2019


## Future aspects of this project
- The mentors and I decided to continue to work on the project for a few more months to get enough results to publish a paper.
- The major aim being able to show the efficancy of current nmt models in translating compositionality based questions to proper SPARQL query. 



### [Index Page](https://anandpanchbhai.com/A-Neural-QA-Model-for-DBpedia/)

