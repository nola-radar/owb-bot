#OMGWTFBBQ Bot  
Awesome self learning slack bot based off
http://blog.templeton.host/self-training-nlp-enabled-slack-bot-tutorial/
using botkit https://github.com/howdyai/botkit

Say, `!TRAIN` to begin a skill training then simply fill out the generated JS file for the skill functionality.
`Backup` function allows for pushing to git repo to save custom added functions

Added built-in functions:
* Help: Listing of builtin and custom added commands
* Info: Uptime and instance/system information
* Google: LMGTFY function
* Backup: backup to git (set repository in Backup.js, maaybe change to commit/push to branch instead of master)
* FuckOff: Fuck of as a service
* CatFacts: Self explainitory
* TheRules: Asimov three laws of robotics
* Jokes: random jokes on command
* RPS: rock, paper, scissors (in progress)
* Jeopardy: Jeopady game (in progress)
* ????

OVER 9000 FT OVERVIEW
- `Index.js` kicks everything off & runs the base logic
- `builtins.js` and `custom-phrases.json` are arrays of skills and the keywords to trigger them
- `src/ears.js` uses botkit to listen/interact with slack
- the `!TRAIN` keyword initiates training mode via `src/train.js` to add a new skill to `custom-phrases.json` and a js code stub in the skills folder
- `src/brain.js` uses the natural NLP package to recognize defined skill keywords and execute the coresponding skill js file
