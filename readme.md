## G9 Innovation

The Goal of this ReadMe is to explain the architecture of our code and what very notebook does. 

- The directory 'data' contains all the files we've used during this project: 
   - The file 'df_aircraft.csv' contains all the aircraft names of the Database
   - 'df_airline.csv' contains all the airline names of our Database
   - 'df_airport.csv' contains all the airport names of our Database
   - 'df_country.csv' contains all the countries of our Database
   - 'tagger_eval.csv' contains the evaluation dataframe for the Bert sentence tagger. This permitted us to know how good our model is in performing named entity recognition on our dataset. 
   - 'tagger_train.csv' contains the train dataframe for the Bert sentence tagger. This permitted us to train our named entity recognition model.
   - The directory 'bdd' contains the dataset we used to build our markov chain model
      - 'df_bdd.csv' is our database of actions representing the different interaction of the dashboard's users.
      - 'df_facts.csv' is the Database of facts we created for the intent facts. If the user of the Database chooses this intent, our bot randomly returns one fact about Planes, serial killers, Pirates or Data Science. 
      - 'df_transitions.csv' is a action-action matrix where we store the propabilities of going from an action to another one. This matrix permits us to predict the next action of a user and to recommand it. 

- The directory 'scrap' contains the notebooks we used in order to scrap the informations about the airlines, the airports, the countries. These notebooks permitted us to build our DataFrame of airline names etc.. 

- 'Bert_tagger.ipynb': This notebook is the one we use to train our Bert Sentence Tagger. 

- 'Chatbot_Vo.ipynb' : This notebook contains the main program of our Chatbot. It calls all the other notebooks in which we've declared the usefull functions? 

- 'constants.ipynb'  : In this notebook, we store all the constant variables we use during this project. It permits our code to be more flexible to variable name changing. 
Inside this file, pay attention to modify the variable 'route' which is a relative path to our files with the absolute one in order to run the code correctly.

- 'contexte.ipynb'   : This Notebook contains the work we've done the first week for the context extraction from a tweet/comment. The code inside permits us to understand what a comment/tweet is about in order to give a contextualized answer to the users. 

- 'dictionnaries.ipynb': In this notebook, we build the different dictionnaries(synonyms, etc) for the sentence generation task. 

- 'functions.ipynb'   : This notebook contains the code for the different functions we're using commonly in the other notebooks. This permits us to ensure a modularity of our code and not to repeatly develop the same functions in our project. 

- 'G9_final.ipynb'    : This is the final notebook of our project. It's the commentend version in which we explain our work with different sections (introduction etc).

- 'generate_sentence.ipynb': This is the code that permits us to generate the sentences for our sentence tagger model. We use the outputs of this notebooks to build the 'tagger_train.csv' and 'tagger_eval.csv' dataframes in order to train and evaluate our Bert sentence tagger model. 

- 'markov.ipynb'      : This is the notebook that permits us to build the markov chain model in order to recommand new actions to the users. 

- 'tag_to_filter.v1.ipynb' : This is the notebook that permits us to go from the Bert sentence tagger model's output to a json file format according to what we're storing in the actions database. This json format is choosen in adequation with the dashboard group. 
