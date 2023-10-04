#LLM

[Tree of Thoughts: Deliberate Problem Solving with Large Language Models](https://arxiv.org/abs/2305.10601)
Tree of Thoughts extends or is a generalization of [[Chain of Thought]] approaches (which can be thought of as a special case of Tree of Thoughts approaches).

Allows language models "to perform *deliberate* decision making by considering multiple different reasoning paths and self-evaluating choices to decide the next course of action, as well as looking ahead or backtracking when necessary to make global choices."

# Rough Description of Technique
Think of problem solving as a search problem over the space of potential solutions. Straightforward stochastic token generation cannot *deliberate*; it cannot explore, look ahead or evaluate candidate solutions. The idea is, at each step, to generate and evaluate multiple possible next steps, and evaluate them, using lookahead or some heuristic, in order to choose which candidates should be further pursued and which should be abandoned. 
# Analogs in Human Deliberation
Human deliberation serves as a model. The authors in particular reference Kahneman's two decision-making systems. Stochastic token generation is "reminiscent" of System 1 -- the "fast" system. Tree of Thoughts is more like System 2 -- the "slow" system. When we're deliberating, we hold in thought multiple possibilities, develop them and evaluate and sometimes backtrack. 

I wonder if a more robust, less superficial account of System 2 thinking or better developed accounts of human problem solving and decision making would suggest different and more robust mechanisms. For example, the authors quote Newell, et al, [Report on a general problem solving program](http://bitsavers.informatik.uni-stuttgart.de/pdf/rand/ipl/P-1584_Report_On_A_General_Problem-Solving_Program_Feb59.pdf):

> A genuine problem-solving process involves the repeated use of available information to initiate exploration, which discloses, in turn, more information until a way to attain the solution is finally discovered.

What strategies do humans use to generate alternatives? Perhaps this question is less pressing when using a language model: we need only allow the model to use its stochastic generative capabilities n times. But maybe we could be smarter about it. Perhaps the model could be prompted in different ways to generate useful alternatives. Would those prompts differ depending on the type of problem or the domain?

What strategies to humans use to distill new information from these alternatives and apply that new information to the other options? Suppose I'm contemplating what I want to eat for dinner:
  - I first consider ordering sushi. I score this possibility.
  - I consider making a sandwich. I score this possibility.
  - I next consider ordering pizza. As I do so, I realize the pizza shop might not be open. Indeed it's not.

So I can obviously reject my pizza delivery option. But how do I know that this new consideration should cause me to go back and reassess my sushi-ordering plan but need not cause me to reassess my sandwich-making plan? Is my heuristic for evaluating alternatives static, or can it improve with exploration and assessment?