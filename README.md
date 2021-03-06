# apcsp_create

[![Deploy to Netlify](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://github.com/abhinavpappu/apcsp-create)

Project for the AP Computer Science Principles CREATE task.

It's a code editor that allows you to actually run the pseudo code that APCSP uses. There's even a turtle simulator so you can use commands such as MOVE_FORWARD()!

Try it out here: https://apcsp-code.netlify.com/

Version of the pseudocode this project supports: [ap-computer-science-principles-exam-reference-sheet.pdf](./ap-computer-science-principles-exam-reference-sheet.pdf)

#### Notes:
  - You can use `=` or `<-` instead of `←` (you can also use `←` if you really want)
  - Similarly you can use `<=`, `>=` instead of `≤`, `≥` respectively
  - Limitation: In order to enable step forward and step backward, we save every "state" of the program. For convenience of implementation, I define that every function call (and only function calls) constitutes a state change (which you can observe with the step forward and backward commands). The entire set of states is precalculated when you click on run. Therefore, any program that uses more than 1000 "states" (function calls) is assumed to contain an infinite loop and the program terminates. If you're running a super long program on this tool for some reason, please run it locally and change the variable `MAX_STATES` in `App.vue`

Feel free to open issues for any bugs or any updates to the language specification! (Or attempt to read through the mess of code and contribute yourself!)