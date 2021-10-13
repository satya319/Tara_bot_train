# installation process
 * Install Python
 * Then install conda
 * Then install rasa by `pip3 install rasa`
 * Start a new project by command `rasa init`
 * Train rasa with new training details `rasa train`
 * Start rasa for input by command `rasa shell` or `rasa run --cors`
 * Now open the three file `nlu.yml , stories.yml, domain.yml` for adding new train data. It will be the modified data for personal chat bot.
 * First at the file named `nlu.yml` for example add  
```
   - intent: bot_introduction
  examples: |
    - what is your name?
    - who are you?
 ```
 * Secondly at the file named `stories.yml` for example add 
```
- story: bot introduction
  steps:
  - intent: bot_introduction
  - action: utter_introduction
```
* In the third step, in file name called `domain.yml` for example add 
```
 utter_introduction:
  - text: "My name is Tara, I am your virtual assistance created by StudyandMasti Team."
```
* in the nlu file the questions are asked by the users. In the stories.md file it is for the class name and in the domain.yml file the reply by the bot is present.