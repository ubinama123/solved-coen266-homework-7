Download Link: https://assignmentchef.com/product/solved-coen266-homework-7
<br>
In this assignment, you will design agents for the classic version of Pacman, including ghosts. The code base has not changed much from the previous Pacman assignment, but please start with the attached multiagent.zip, rather than intermingling files from the previous Pacman assignment.

<table width="681">

 <tbody>

  <tr>

   <td colspan="2" width="681"><strong>Files you’ll edit:</strong></td>

  </tr>

  <tr>

   <td width="137">multiAgents.py</td>

   <td width="543">Where all of your multi-agent search agents will reside.</td>

  </tr>

  <tr>

   <td colspan="2" width="681"><strong>Files you might want to look at:</strong></td>

  </tr>

  <tr>

   <td width="137">pacman.py</td>

   <td width="543">The main file that runs Pacman games. This file also describes a Pacman GameState type, which you will use extensively in this assignment.</td>

  </tr>

  <tr>

   <td width="137">game.py</td>

   <td width="543">The logic behind how the Pacman world works. This file describes several supporting types like AgentState, Agent, Direction, and Grid.</td>

  </tr>

  <tr>

   <td width="137">util.py</td>

   <td width="543">Useful data structures for implementing search algorithms. You don’t need to use these for this assignment, but may find other functions defined here to be useful.</td>

  </tr>

  <tr>

   <td colspan="2" width="681"><strong>Supporting files you can ignore:</strong></td>

  </tr>

  <tr>

   <td width="137">graphicsDisplay.py</td>

   <td width="543">Graphics for Pacman</td>

  </tr>

  <tr>

   <td width="137">graphicsUtils.py</td>

   <td width="543">Support for Pacman graphics</td>

  </tr>

  <tr>

   <td width="137">textDisplay.py</td>

   <td width="543">ASCII graphics for Pacman</td>

  </tr>

  <tr>

   <td width="137">ghostAgents.py</td>

   <td width="543">Agents to control ghosts</td>

  </tr>

  <tr>

   <td width="137">keyboardAgents.py</td>

   <td width="543">Keyboard interfaces to control Pacman</td>

  </tr>

  <tr>

   <td width="137">layout.py</td>

   <td width="543">Code for reading layout files and storing their contents</td>

  </tr>

 </tbody>

</table>






















Welcome to Multi-Agent Pacman

First, play a game of classic Pacman by running the following command:

python pacman.py

and using the arrow keys to move. Now, run the provided ReflexAgent in multiAgents.py

python pacman.py -p ReflexAgent

Note that it plays quite poorly even on simple layouts:

python pacman.py -p ReflexAgent -l testClassic

Inspect its code (in multiAgents.py) and make sure you understand what it’s doing.

<h1>Task: Reflex Agent</h1>

Improve the ReflexAgent in multiAgents.py to play respectably. The provided reflex agent code provides some helpful examples of methods that query the GameState for information. A capable reflex agent will have to consider both food locations and ghost locations to perform well. Your agent should easily and reliably clear the testClassic layout:

<strong>Experiment 1: </strong>

python pacman.py -p ReflexAgent -l testClassic

<strong>Experiment 2: </strong>

Try out your reflex agent on the default mediumClassic layout with one ghost or two (and animation off to speed up the display):

python pacman.py –frameTime 0 -p ReflexAgent -k 1 python pacman.py –frameTime 0 -p ReflexAgent -k 2

How does your agent fare? It will likely often die with 2 ghosts on the default board, unless your evaluation function is quite good.