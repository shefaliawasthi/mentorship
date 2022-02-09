# Refined Design
## Website Overview
- Members input their schedule and availability:
  - Display monthly calendar with times and dates
  - Option to sync Google Calendar
- Members answer set questions. Answers used for matching
  - Common events: Birthday parties, Office parties, School Teamwork
  - Set ~10-15 questions for each event (not too long, but enough info)
  - EITHER multiple-choice (set answers)
    - give a point for every answer (A=1, B=2, C=3, D=4)
    - OPTION 1: use point-value system to match SIMILAR scoring members
    - OPTION 2: use point-value system to match DIFFERENT scoring members
  - OR input answers (free response)
    - use NLP to tokenize and gather overall connotation of the message
    - use a point-value system for connotations (number line where negative emotions = <0 and positive emotions = >0)
  - OR create random matching algorithm
    - no questions asked, answers do not matter
    - use randomizer function: assign students a number, then pair them like drawing names out of a hat without replacement
    - extra feature!
- Organizer mode:
  - Can see all matched pairs and can view everyones schedules
  - Sets number of people in each pair
  - Can toggle which algorithm is used for matching
  - Can rematch (move students around after match)
- Member mode:
  - Input answers, wait to be matched
  - Matched pairs can view potential “meeting dates/times”

## Coding Components
- Main language: Python on GitHub
- Coding UI: ReactJS
- Backend: Python

## Basic Event
- Number of people
- Event Questions (perhaps we can standardize questions for different, but common events)
- Matching algorithm!
- Show matched pairs

## Create Login Page [POSSIBLY]
- Create “classes” so set lists of members that can be saved and referred to later
- Create “saved teams” so specific pairings can be saved 
- Students can sync their calendars with Google Calendar
- OPTION: Members can put in their preferences of who they want to work with
- OPTION: Ask members to sign up with their email accounts. after groups have been made, either create a chatroom with the members using the emails or give members the option to share their contact information with the other members
- OPTION: Shuffle groups button. Provide multiple options so they can be different with a push of w button
