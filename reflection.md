# 💭 Reflection: Game Glitch Investigator

Answer each question in 3 to 5 sentences. Be specific and honest about what actually happened while you worked. This is about your process, not trying to sound perfect.

## 1. What was broken when you started?

- What did the game look like the first time you ran it?
- List at least two concrete bugs you noticed at the start  
  (for example: "the hints were backwards").

When i first ran the game i noticed the did look like it was made correctly since easy, hard, and normal mode were all the same. The logic for the hints on the guesses was backwards. The secret number kept changing and the game levels were switched for normal and hard. 

---

## 2. How did you use AI as a teammate?

I used claude code for this  project. One correct suggestion the ai gave to me was to move some of the logic of this program from the app to logic python files. The ai didnt really give me any suggestions that were incorrect though it was trying to overengineer the bug fixes where minimal changes were needed.

## 3. Debugging and testing your fixes

- How did you decide whether a bug was really fixed?
- Describe at least one test you ran (manual or using pytest)  
  and what it showed you about your code.
- Did AI help you design or understand any tests? How?

I decided a bug was fixed because i would manually test that feature by playing the game and use different values to make sure the functionality worked correctly. one example, i had to test if the difficulty were correctly set by swtching back and forth between them in the game to see in the ranges changed. Claude didnt help me with tests once i knew what the logic was doing and fixed it i was able to manually test it in the game.
---

## 4. What did you learn about Streamlit and state?
The secret number kept changing because the code converted the secret number to a string on every even number attempt. I would explain that in streamlit, everytime you interact with a part of the app, it doesnt just update that part but reruns the entire python file start to finish. this makes some stuff get wiped while certain things stay the same. The change I made to make it stable was removing the if/else block that was doing the conversion and just always passing the secret directly to check_guess.

---

## 5. Looking ahead: your developer habits

One tool was using ai with a claude.md file and updating as i went. one thing i would do different is that i wouldnt take the ai's first suggestion because sometimes it is way more than is needed or required. This project made me more skeptical of ai generated code and solutions and that I should question the ai on what it says and gives me.