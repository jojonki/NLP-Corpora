# NLP Corpora


This is a list of NLP corpora. You can report a new corpus at the Issues page.

- 🤖🤖 Machine-to-Machine conversations which were synthetically generated.
- 👦🧒 Human-to-Human conversations. (including dialogs by crowd workers such as Mechanical Turk).
- 👦🤖 Human-to-Machine (dialog systems) conversations.
- 📝 Written dialogs, utterance is not assumed.
- 🗣 Spoken dialogs, also containing assuming to speak (generally written dialogs by crowd workers). 
- 🧙‍ The data was collected using a [Wizard-of-Oz](https://en.wikipedia.org/wiki/Wizard_of_Oz_experiment) scheme.


### Dialog (Task-oriented)

- [Large-Scale Multi-Domain Belief Tracking with Knowledge Sharing, Cambridge, 2018](https://arxiv.org/pdf/1807.06517.pdf)👦👦🧙‍    
2480 single-domain dialogs and 7375 multi-domain dialogs (usually from 2 up to 5 domains).    
There are [Code](https://github.com/nmrksic/neural-belief-tracker) and [Corpus (will be available)](http://dialogue.mi.eng.cam.ac.uk/index.php/corpus/).   

- [The (6) dialog bAbI tasks, facebook, 2016.](https://research.fb.com/downloads/babi/) 👦🤖🗣		
The set of six tasks for testing e2e task-oriented dialogs systems for restaurant reservation. Task1-5 are synthetically generated data while Task6 is created from human-to-computer dialogs (DSTC2).		
For each task, there are 1000 dialogs for training, 1000 for development and 1000 for testing. 

	```:Task 6 example
	U: <SILENCE>	
	S: Hello , welcome to the Cambridge restaurant system? You can ask for restaurants by area , price range or food type . How may I help you?
	U: cheap restaurant that serves german food
	S: I'm sorry but there is no restaurant serving german food
	U: what about asian oriental foo
	S: You are looking for a german restaurant right?
	U: asian
	S: Let me confirm , You are looking for a restaurant in the cheap price range right?
	```

- [babi plus, Heriot-Watt, 2017.](https://arxiv.org/abs/1709.07840) 🤖🤖🗣    
Synthetically added disfluencies to the dialogs of bAbI-Task 1. And [their code](https://github.com/ishalyminov/memn2n) is also available.

	```:example
	sys: hello what can I help you with today?
	usr: I’d like to book a uhm yeah I’d like to book a
		 table in a expensive price range no sorry in a
		 cheap price range
	sys: I’m on it. Any preference on a type of cuisine?
	usr: with indian food no sorry with spanish food
	```

- [A New Multi-Turn, Multi-Domain, Task-Oriented Dialogue Dataset, Stanford, 2017.](https://nlp.stanford.edu/blog/a-new-multi-turn-multi-domain-task-oriented-dialogue-dataset/)👦👦🧙‍		
Three domains (weather/calendar/poi) dialogs of a car assistant.	
3,031 multi-turn dialogues are created in manner of Wizard-of-Oz.

	```:example
		DRIVER:	I need to find the time and parties attending my optometrist appointment. 
		CAR	:	I have 3 appointments scheduled, with Alex, your sister, and Jeff. Which are you referring to?
		DRIVER:	I want to know about the one that Alex is joining me at.
		CAR	:	That optometrist appointment is at 4 pm.
		DRIVER:	Thanks.
		CAR	:	No problem.
	```


- [Frames: A Corpus for Adding Memory to Goal-Oriented Dialogue Systems, Maluuba, 2017.](https://datasets.maluuba.com/Frames)👦👦🧙‍      
 A corpus of 1369 human-human dialogues with an average of 15 turns per dialog collected in Wizard-of-Oz.
 
	```:example
	User	I'd like to book a trip to boston from London on Saturday, August 13, 2016 for 8 adults. I have a tight budget of 1700.	Frame #1
	Act 1	inform(intent=book)	
	Act 2	inform(dst_city = boston, or_city = London, str_date = Saturday\, August 13\, 2016, n_adults = 8, budget = 1700)"	
	Wizard	"Hi...I checked a few options for you, and unfortunately, we do not currently have any trips that meet this criteria. Would you like to book an alternate travel option?"	Frame #1
	Act 1	no_result	
	Act 2	suggest(dst_city)	
	User	"Yes, how about going to Detroit from London on August 13, 2016 for 5 adults. For this trip, my budget would be 1900."	Frame #2
	Act 1	inform(dst_city = Detroit, n_adults = 5, budget = 1900, ref = [1{or_city = London, str = August 13\, 2016}])	
	Wizard	"I checked the availability for those dates and there were no trips available. Would you like to select some alternate dates?"	Frame #2
	Act 1	no_result(str_date, end_date)	
	Act 2	suggest(str_date, end_date)
	```


- [DSTC 1-6](https://www.microsoft.com/en-us/research/event/dialog-state-tracking-challenge/)👦🤖🗣	
  Dialog State Tracking Challenge is research community tasks. The link presents each DSTC task respectively.
  - DSTC1: Bus schedules.
  - DSTC2/3: Restaurant reservations.
  - DSTC4: Tourist information.
  - DSTC5: Tourist information, and privided in several languages.
  - DSTC6: It consists of 3 parallel tracks: End-to-End Goal Oriented Dialog Learning, End-to-End Conversation Modeling, and Dialogue Breakdown Detection.

### Dialog (Others)


- [Personalizing Dialogue Agents, facebook, 2018.](https://github.com/facebookresearch/ParlAI/tree/master/projects/personachat)👦🧒📝    
Two people dialogs, conditioned on personas.
This contains 164,356 utterances (10,981 dialogs).

	```example
	[PERSON 1:] Hi
	[PERSON 2:] Hello ! How are you today ?
	[PERSON 1:] I am good thank you , how are you.
	[PERSON 2:] Great, thanks ! My children and I were just about to watch Game of Thrones.
	[PERSON 1:] Nice ! How old are your children?
	[PERSON 2:] I have four that range in age from 10 to 21. You?
	[PERSON 1:] I do not have children at the moment.
	[PERSON 2:] That just means you get to keep all the popcorn for yourself.
	[PERSON 1:] And Cheetos at the moment!
	[PERSON 2:] Good choice. Do you watch Game of Thrones?
	[PERSON 1:] No, I do not have much time for TV.
	[PERSON 2:] I usually spend my time painting: but, I love the show.
	```
	
- [Edina: Building an Open Domain Socialbot with Self-dialogues, 2017.](https://github.com/jfainberg/self_dialogue_corpus)👦👦    
The data is collected by AMT in manner of _self-dialog_, and used in Alexa Prize 2017.
The workers created self-dialogs alone given a topic.
There are 24,283 self-dialogues, 3,653,313 words, across 141,945 turns, from 2,717 Workers.
	
	```example
	What is your absolute favorite movie?
	I think Beauty and the Beast is my favorite.
	The new one?
	No, the cartoon. Something about it just feels magical.
	It is my favorite Disney movie.
	What’s your favorite movie in general?
	I think my favorite is The Sound of Music.
	Really? Other than cartoons and stuff I can never get into musicals.
	I love musicals. I really liked Phantom of the Opera.
	```


- [DailyDialog: A Manually Labelled Multi-turn Dialogue Dataset, 2017.](http://yanran.li/dailydialog)👦🧒📝    
The dialogs are our daily communication way and cover various topics about our daily life. The dataset contains 13,118 multi-turn dialogs.    

	```:example
	A: I’m worried about something.
	B: What’s that?
	A: Well, I have to drive to school for a meeting this morning, 
	   and I’m going to end up getting stuck in rush-hour traffic.
	B: That’s annoying, but nothing to worry about.
	   Just breathe deeply when you feel yourself getting upset.
	```
	
- [The Ubuntu Dialogue Corpus, 2015.](https://github.com/rkadlec/ubuntu-ranking-dataset-creator)🧒🧒📝    
 Human to Human dialogs in Ubuntu boards.    
1 million multi-turn dialogues, with a total of over 7 million utterances and 100 million words. 

### Question Answering

- [SQuAD 2.0, 2018](https://rajpurkar.github.io/SQuAD-explorer/)📝     

	> SQuAD2.0 combines the 100,000 questions in SQuAD1.1 with over 50,000 new, unanswerable questions written adversarially by crowdworkers to look similar to answerable ones. 


### Translation

🚧

### Sentiment Analysis

🚧

## References
- [A Survey of Available Corpora for Building Data-Driven Dialogue Systems](https://breakend.github.io/DialogDatasets/)
- [Natural Language Processing Corpora, NLP for Hackers](https://nlpforhackers.io/corpora/)
