# NLP Corpora


This is a list of NLP corpora. You can report a new corpus at the Issues page.

<!-- TOC depthFrom:1 depthTo:6 withLinks:1 updateOnSave:1 orderedList:0 -->

- [NLP Corpora](#nlp-corpora)
	- [Emoji Meanings](#emoji-meanings)
	- [Corpora](#corpora)
		- [Dialog (Task-oriented)](#dialog-task-oriented)
		- [Dialog (Others)](#dialog-others)
		- [Question Answering](#question-answering)
		- [Translation](#translation)
		- [Sentiment Analysis](#sentiment-analysis)
		- [Others](#others)
	- [References](#references)

<!-- /TOC -->

## Emoji Meanings
- 🤖🤖 Machine-to-Machine conversations which were synthetically generated.
- 👦🧒 Human-to-Human conversations. (including dialogs by crowd workers such as Mechanical Turk).
- 👦🤖 Human-to-Machine (dialog systems) conversations.
- 📝 Written texts, utterance is not assumed.
- 🗣 Spoken dialogs, also containing assuming to speak (generally written dialogs by crowd workers).
- 🧙‍ The data was collected using a [Wizard-of-Oz](https://en.wikipedia.org/wiki/Wizard_of_Oz_experiment) scheme.

## Corpora
### Dialog (Task-oriented)

- [Permuted Dialog bAbI tasks, IBM, EMNLP 2018.](https://github.com/IBM/permuted-bAbI-dialog-tasks)

	```
	28 <SILENCE>	what do you think of this option: resto_rome_expensive_french_8stars-1|what do you think of this option: resto_rome_expensive_french_8stars-2
	29 do you have something else	sure let me find an other option for you
	30 <SILENCE>	what do you think of this option: resto_rome_expensive_french_8stars-2
	31 do you have something else	sure let me find an other option for you
	32 <SILENCE>	what do you think of this option: resto_rome_expensive_french_1stars
	33 that looks great	great let me do the reservation
	```


- [MultiWOZ - A Large-Scale Multi-Domain Wizard-of-Oz Dataset for Task-Oriented Dialogue Modelling, EMNLP 2018.](https://arxiv.org/pdf/1807.06517.pdf)👦👦🧙‍    
2480 single-domain dialogs and 7375 multi-domain dialogs (usually from 2 up to 5 domains).    
This dataset is designed for Dialog State Tracking.
There are [Code](https://github.com/nmrksic/neural-belief-tracker) and [Corpus)](http://dialogue.mi.eng.cam.ac.uk/index.php/corpus/).   

	```
	3 domain(s): ['bus', 'hotel', 'train']
	Usr: I need to book a hotel in the east that has 4 stars.
	Sys: I can help you with that. What is your price range?
	Usr: That doesn't matter as long as it has free wifi and parking.
	Sys: If you'd like something cheap, I recommend the Allenbell. For something moderately priced, I would recommend the Warkworth House.
	Usr: Could you book the Wartworth for one night, 1 person?
	Sys: What day will you be staying?
	Usr: Friday and Can you book it for me and get a reference number ?
	Sys: Booking was successful.
	Reference number is : BMUKPTG6.  Can I help you with anything else today?
	Usr: I am looking to book a train that is leaving from Cambridge to Bishops Stortford on Friday.
	Sys: There are a number of trains leaving throughout the day.  What time would you like to travel?
	Usr: I want to get there by 19:45 at the latest.
	Sys: Okay! The latest train you can take leaves at 17:29, and arrives by 18:07. Would you like for me to book that for you?
	Usr: Yes please. I also need the travel time, departure time, and price.
	Sys: Reference number is : UIFV8FAS. The price is 10.1 GBP and the trip will take about 38 minutes. May I be of any other assistance?
	Usr: Yes. Sorry, but suddenly my plans changed. Can you change the Wartworth booking to Monday for 3 people and 4 nights?
	Sys: I have made that change and your reference number is YF86GE4J
	Usr: Thank you very much, goodbye.
	Sys: You're welcome. Have a nice day!
	```

- [CMU SimDial: Synthetic Task-oriented Dialog Generator with Controllable Complexity, SIGDIAL 2018.](https://github.com/snakeztc/SimDial)👦🤖🗣
SimDial is a multi-domain dialog generator chich can generate conversations for slot-filling domains with configurable complexity.

	```
	Domain: Restaurant
	Sys: Welcome to the restaurant recommendation system. What do you need?
	User (0.83): Hello robot. I am looking for a restaurant.
	Sys: Which city are you interested in?
	User (0.75): I am in San Jose. And Korean. Uhm sorry, I	am interested in Chinese food.
	Sys: I believe you said San Jose. I believe you said Chinese.
	Sys: QUERY goal: restaurant food-pref: Chinese location:
	San Jose
	KB: RET restaurant: 17
	Sys: Restaurant 17 is a good choice. What else can I do	for you?
	User (0.6): Not done yet. Is that restaurant open now?
	Sys: QUERY goal: open restaurant: 17 food-pref: Chinese
	location: San Jose
	KB: RET open: yes
	Sys: Yes, it is open right now. What else?
	User (0.69): No 
	```

- [The (6) dialog bAbI tasks, facebook, 2016.](https://research.fb.com/downloads/babi/) 👦🤖🗣    
The set of six tasks for testing e2e task-oriented dialogs systems for restaurant reservation. Task1-5 are synthetically generated data while Task6 is created from human-to-computer dialogs (DSTC2).		
For each task, there are 1000 dialogs for training, 1000 for development and 1000 for testing.

    ```
    U: <SILENCE>
    S: Hello , welcome to the Cambridge restaurant system? You can ask for restaurants by area , price range or food type . How may I help you?
    U: cheap restaurant that serves german food
    S: I'm sorry but there is no restaurant serving german food
    U: what about asian oriental foo
    S: You are looking for a german restaurant right? U: asian
    S: Let me confirm , You are looking for a restaurant in the cheap price range right?
    ```

- [babi plus, Heriot-Watt, 2017.](https://arxiv.org/abs/1709.07840) 🤖🤖🗣    
Synthetically added disfluencies to the dialogs of bAbI-Task 1. And [their code](https://github.com/ishalyminov/memn2n) is also available.

    ```
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

    ```
    DRIVER: I need to find the time and parties attending my optometrist appointment.
    CAR   : I have 3 appointments scheduled, with Alex, your sister, and Jeff. Which are you referring to?
    DRIVER: I want to know about the one that Alex is joining me at.
    CAR   : That optometrist appointment is at 4 pm.
    DRIVER: Thanks.
    CAR   : No problem.
    ```


- [Frames: A Corpus for Adding Memory to Goal-Oriented Dialogue Systems, Maluuba, 2017.](https://datasets.maluuba.com/Frames)👦👦🧙‍      
 A corpus of 1369 human-human dialogues with an average of 15 turns per dialog collected in Wizard-of-Oz.

    ```
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

- [Multimodal EmotionLines Dataset. 2018](https://affective-meld.github.io/)👦🧒🗣     
MELD is a multi-modal (audio/vision/text with an emotion) dataset using Friends TV shows. It has more than 1300 dialogues and 13000 utterances.
<img src="https://raw.githubusercontent.com/jojonki/NLP-Corpora/master/img/meld.jpeg" width="500" />

- [Document Grounded Conversations. EMNLP 2018](https://github.com/festvox/datasets-CMU_DoG)
Conversations that are about the contents of a specified document. The documents were Wikipedia articles about movies.
The dataset contains 4112 conversations with an average of 21.43 turns per conversation.    


	```
	user2: Hey have you seen the inception?
	user1: No, I have not but have heard of it. What is it about
	user2: It’s about extractors that perform experiments using military technology on people to retrieve info about their targets.
	```

- [Personalizing Dialogue Agents, facebook, 2018.](https://github.com/facebookresearch/ParlAI/tree/master/projects/personachat)👦🧒📝    
Two people dialogs, conditioned on personas.
This contains 164,356 utterances (10,981 dialogs).

    ```
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

    ```
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

    ```
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

- [Open Book Question Answering, 2018.](http://data.allenai.org/OpenBookQA)
> OpenBookQA, modeled after open book exams for assessing human understanding of a subject. The open book that comes with our questions is a set of 1326 elementary level science facts. Roughly 6000 questions probe an understanding of these facts and their application to novel situations. This requires combining an open book fact (e.g., metals conduct electricity) with broad common knowledge (e.g., a suit of armor is made of metal) obtained from other sources.         
        
	```
	Question:
	Which of these would let the most heat travel through?
	A) a new pair of jeans.
	B) a steel spoon in a cafeteria.
	C) a cotton candy at a store.
	D) a calvin klein cotton hat.
	Science Fact:
	Metal is a thermal conductor.
	Common Knowledge:
	Steel is made of metal.
	Heat travels through a thermal conductor.
	```
	

- [CoQA, 2018](https://stanfordnlp.github.io/coqa/)🧒🧒🗣  
CoQA is a large-scale dataset for building Conversational Question Answering systems. It contains 127K questions with answers obtained from 8K conversations. Each conversation is collected by paring two crowdworkers to chat about a passage in the form of QAs.    
	```
	Jessica went to sit in her rocking chair. Today was her birthday
	and she was turning 80. Her granddaughter Annie was coming
	over in the afternoon and Jessica was very excited to see
	her. Her daughter Melanie and Melanie’s husband Josh were
	coming as well. Jessica had . . .

	Q1: Who had a birthday?
	A1: Jessica
	R1: Jessica went to sit in her rocking chair. Today was her birthday and she was turning 80.
	Q2: How old would she be?
	A2: 80
	R2: she was turning 80
	```


- [SQuAD 2.0, 2018](https://rajpurkar.github.io/SQuAD-explorer/)📝     

	> SQuAD2.0 combines the 100,000 questions in SQuAD1.1 with over 50,000 new, unanswerable questions written adversarially by crowdworkers to look similar to answerable ones.

- [Spoken SQuAD, 2018](https://github.com/chiahsuan156/Spoken-SQuAD/)🗣    
Artificially generated corpus based on SQuAD by using Google TTS. They used Google TTS to generate the spoken version of SQuAD articles. Then, the generated texts are passed to CMU Sphinx (speech recognizer) to validate whether the generated texts contain a correct answer.

- [ODSQA, 2018](https://github.com/chiahsuan156/Spoken-SQuAD/)🗣    
This is a __Chinese corpus__. Over three thousand questions by 20 Chinese speakers.

### Translation

🚧

### Sentiment Analysis

🚧

### Others
- [WikiHow. 2018](https://github.com/mahnazkoupaee/WikiHow-Dataset)
> WikiHow is a new large-scale dataset using the online WikiHow (http://www.wikihow.com/) knowledge base. Each article consists of multiple paragraphs and each paragraph starts with a sentence summarizing it. By merging the paragraphs to form the article and the paragraph outlines to form the summary, the resulting version of the dataset contains more than 200,000 long-sequence pairs.

- [Spider 1.0, EMNLP 2018](https://yale-lily.github.io/spider)  
A human-labeled dataset for complex and cross-domain semantic parsing and Text-to-SQL Task.    

	```
	Question: What are the name and budget of the departments with average instructor salary greater than the overall average?
	SQL: 
	SELECT T2.name, T2.budget
	FROM instructor as T1 JOIN department as
	T2 ON T1.department_id = T2.id 
	GROUP BY T1.department_id
	HAVING avg(T1.salary) > (SELECT avg(salary) FROM instructor)
	```



- [YouTube AV 50K: an Annotated Corpus for Comments in Autonomous Vehicles, 2018](https://arxiv.org/abs/1807.11227)🧒📝  
Comments from 50K Youtube videos related to autonomous vehicles. The total # of comments is 30,456 including 19,126 annotated comments.

- [SWAG: A Large-Scale Adversarial Dataset for Grounded Commonsense Inference. 
2018.](https://rowanzellers.com/swag/)
SWAG (Situations With Adversarial Generations) is a dataset for grounded commonsense inference. It consists of 113k multiple choice questions about grounded situations.

	```
	On stage, a woman takes a seat at the piano. She
	a) sits on a bench as her sister plays with the doll.
	b) smiles with someone as the music plays.
	c) is in the crowd, watching the dancers.
	d) nervously sets her fingers on the keys. <---

	A girl is going across a set of monkey bars. She
	a) jumps up across the monkey bars.
	b) struggles onto the monkey bars to grab her head.
	c) gets to the end and stands on a wooden plank.  <---
	d) jumps up and does a back flip.
	```

- [Friends TV Corpus, 2011](https://sites.google.com/site/friendstvcorpus/)
The data was created for an analysis of the use of various linguistic structures and a comparison of their use in inter-gender and intra-gender conversation environments in "Friends". The paper's title is "A STUDY INTO THE USE OF LINGUISTIC STRUCTURES USED INTER-GENDER AND INTRA-GENDER IN THE TV SHOW ‘FRIENDS’".    

	```
	1	1	MONICA	F	Monica: There's nothing to tell! He's just some guy I work with!	There's nothing to tell! He's just some guy I work with!	There_EX 's_VBZ nothing_PN1 to_TO tell_VVI !_! He_PPHS1 's_VBZ just_RR some_DD guy_NN1 I_PPIS1 work_VV0 with_IW !_!	0101.txt
	101	1	JOEY	M	Joey: C'mon, you're going out with the guy! There's gotta be something wrong with him!	C'mon, you're going out with the guy! There's gotta be something wrong with him!	C'm_VV0 on_RP you_PPY 're_VBR going_VVG out_RP with_IW the_AT guy_NN1 !_! There_EX 's_VHZ got_VVN 
	```

## References
- [A Survey of Available Corpora for Building Data-Driven Dialogue Systems](https://breakend.github.io/DialogDatasets/)
- [Natural Language Processing Corpora, NLP for Hackers](https://nlpforhackers.io/corpora/)
