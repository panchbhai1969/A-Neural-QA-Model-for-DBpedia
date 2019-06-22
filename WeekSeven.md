# WeekSeven | Stage 3 | Looking Beyond: making questions more human

This came out to be an interesting week with me diving in deep, in thought of what method to use to tackle the problem that arised in the previous meeting, which was:

>> The question seem to be useful but, they are at time nonsensical and grammatically incorrect. Thus they donot represnt real questions that the end system will encounter.

So, it was time to get back to analysing what could be done!, lets first bring all ideas that came up in the meeting together:

![Analysis](static/analysis.gif)

Some of the suggestions given by the mentors in the previous meeting were:

- Using Pre-Trained embeddings (Not very clear)
- Knowledge graph tokens
- Try classifying the natural language questions(english questions here) as natural and non-natural
- Google API to look for trends
- Manual Grammer correction
- Automated Grammer correction (Some mentors disagreed)

I also remember thar the previous developer's proposal had some mechanism through which he was trying to get the importance of the entities, When I read his proposal again. I came across these points which seemed useful:

- Property with no training examples(more learning opportunity)
- Rank based using: [http://atzori.webofcode.org/projects/rankProperties/](http://atzori.webofcode.org/projects/rankProperties/) - When I tried to make use of it. It seemed very difficult to use. The links to supporting research papers were not present too.
- Preventing using duplicate properties
- The class which has maximum number of example entries in DBpedia will be more important to be trained (because quantitatively and intuitively it holds maximum information that can be queried)
- Certain pruning stratergies.

The most important of all were some links posted by Tommaso Soru in slack:
>> this is a list of KGE approaches: https://gist.github.com/mommi84/07f7c044fa18aaaa7b5133230207d8d4

>> this is a pre-trained embedding model for DBpedia 2016-04: https://zenodo.org/record/1320038#.XQfS4XvTV25

Though i was not able to download the accompanying dataset in the second one, the supporting paper was really useful. 


