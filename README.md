# Riddle Me This

## UX

- As a user I want to play a mind-bending guessing game and possibly compare my achievements against other players
    - The game features 49 questions and points system that allows players to compete against one another
- As a user I want to be able to skip questions that prove to be too hard
    - There's an option for users to skip any question they don't know the answer to. Supplying a wrong answer results in negative points being awarded.
- As a user I want to have a visually pleasing experience
    - This one's a bit subjective, but I think the combination of background image, website colors and transparency isn't the worst.


## Features

- 49 questions ranging from very easy to being quite a puzzle
- Persistent Highscores - saved to file and retrieved upon restaring the environment
- Javascript Free - All you no-script paranoid people can rejoice!
- Easy to navigate - the game consists of one page really

## Future features

- Possibly implement highscores.pkl pruning after it reaches certain size
- Ability for active users to chat

## Technologies Used

- [Flask framework] (http://flask.pocoo.org/) - to learn it and make use of the 'views' concept

## Testing

1. Giving out correct answers to incoming questions advances round and awards points as expected
    - Wrong answers give negative points
    - Not supplying any answer and pressing submit counts as a wrong answer, as expected

2. Upon answering the last question I was able to start the game over
3. Upon pressing the 'skip' button I was taken to the next question as expected
4. Supplying username and pressing 'submit' allows me to start the game
    - Tried very long usernames and they look unappealing both in the scoreboard and highscores
        - This will be solved by adding a limit of 15 characters in the username input box
5. Tried pressing browser's 'back' button while being on question 3, which took me to the page with question 2, however the game still expects the answer to question 3
    so technically I'm giving a correct answer to the question I see (and had a shot at before) but the script is expecting answer to question 3 and awards me negative points
    Don't know the proper solution to this at the moment

## Deployment

1. wget -O- https://toolbelt.heroku.com/install-ubuntu.sh | sh
2. Created heroku account
    - Created new app with name project-3-riddle
    - next in the console 'heroku login'
    - next heroku git:remote -a project-3-riddle
    - echo web: python run.py > Procfile
    - sudo pip3 freeze --local > requirements.txt
    - git add . & commit
    - git push heroku master



This section should describe the process you went through to deploy the project to a hosting platform (e.g. GitHub Pages or Heroku).

In particular, you should provide all details of the differences between the deployed version and the development version, if any, including:

Different values for environment variables (Heroku Config Vars)?
Different configuration files?
Separate git branch?
In addition, if it is not obvious, you should also describe how to run your code locally.


















