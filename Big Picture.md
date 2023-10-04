(Being a summary or overview of AI)
(Based, initially, on reading _Artificial Intelligence: A Modern Approach_)

# What Is Artificial Intelligence?
There are roughly four approaches formed by independently answering two questions:
1. Are humans the model of [[intelligence]], or is there a human-independent standard of intelligence (rationality)?
2. Is [[intelligence]] principally concerned with thought or with action?

| | Human-like | Rational |
| :---: | :---: | :---: |
| **Thought-focused** | "cognitive modeling approach" | "'laws of thought' approach" |
| **Agentic** | Turing test: machines act like humans| Rational (optimal) agents |

"Modern" artificial intelligence is almost exclusively concerned with *rational agents*.

# Agents and environments
Agents *perceive* and *act* on their environment. An agent's actions (or its choice of actions) can depend on its built-in knowledge and its percept sequence to do, but on nothing else.

An *agent function* maps perception sequences to actions, but this is an external characterization of the agent. An agent function would reveal all possible percept sequences, the agent's full repertoire of actions, and how its perceptions map to actions (but would only implicitly and probably incompletely specify the agent's built-in knowledge). The agent is implemented and internally represented by an *agent program*.

# Rational action is "good" action
An agent's choice is rational if it maximizes its *performance measure*, given the evidence of its percept sequence and its built-in knowledge. That is, rational decisions are not necessarily perfect decisions and does not require omniscience. 

Put another way, what is rational at any given time depends on:
  - the performance measure that defines the criterion of success
  - the agent's repertoire of actions
  - the agent's built-in knowledge of the environment
  - the agent's learned knowledge ([[Stuart Russell]] & Norvig say "the agent's percept sequence to date", but it need not be the case, I think, that the agent has managed to learn -- and learn correctly -- from its percept sequence)

An *autonomous* agent's repertoire of actions will include something like "information gathering" or "exploration" or "learning" so that its actions will not be bound by its built-in knowledge. 

# Task Environments
A **task environment** specifies the environment and the agent that acts within it (including that agent's goal or performance measure, its sensors, and its actuators). The task environment is the problem to which the agent program is a solution. The design of a successful agent depends on the characteristics of the task environment.

Task environments can be characterized in a number of dimensions:
- observability, or how much of the environment is perceivable by the agent: unobservable <--> partially observable <--> fully observable
- number of agents: single-agent <--> multi-agent
	- relationship between agents: cooperative <--> competitive
- nondeterministic <--> deterministic
	- the "laws" of the environment might be deterministic, but if the environment is sufficiently complex and calculation of the environment's next state from its current state is an intractable problem for the agent, the agent will treat the environment as nondeterministic
- atomicity of experience: episodic <--> sequential
- dynamism: static <--> dynamic
	- what's important is whether the environment can or is likely to change while the agent deliberates (that is, does the agent need to account for changes to the environment occurring while the agent deliberates)
- discrete <--> continuous
- unknown <--> known, how much the agent knows about the environment's "laws of physics"

# Types of Agents
## Simple Reflex Agent
A simple reflex agent selects actions on the basis of the current percept (ignoring the rest of the percept history). In code, this typically looks like a condition-action rule --  an if-then statement, a boolean circuit, or a "neural" circuit.

The chief advantage of such an agent is simplicity. In basing its decision only on the current perceptual input, the agent need not keep any internal representation of the environment and its table mapping percept sequences to actions will be much briefer. But such agents are not very intelligent. In particular, they are not well-suited to environments that are not completely observable. Despite this limitation, they can be useful components of a more sophisticated, composite agent. 

## Model-based Reflex Agent
Model-based agents improve on simple reflex agents by keeping an internal representation of the environment. To do so, such agents:
  - need to have some way to encode the knowledge it has about the environment
  - to update its internal representation, it needs: 
	  - a **transition model**: it's knowledge of how the world changes over time both as a result of the agent's actions and independent of the agent's actions.
		  - Side note: [[Francis Bacon]], in one way, forces us to include our own actions in our transition models of the world: [[nature]] is our model of how the world changes independently of our actions; art is our model of how the world changes because of our action. Bacon's insight is that those two models can and should be combined. Maybe.
	  - a **sensor model**: it's knowledge of how its percepts reflect the world ("reflect" probably isn't the right word)
	  - A state-updating function that uses its current representation, any new percepts or actions, the transition model, and the sensor model to update its internal representation. 
- rules that can be actuated based on that internal representation rather than a single, immediate percept

Naively, I might have thought that the state update is simply a new "all-in" perception of the world (rather than a function I execute before my next perception). But of course that can't be right. To plan my action, I need to be able to anticipate (to infer) future states. And I take notice of certain features in my next percept because they don't match what I'd anticipated I'd perceive.
## Goal-based Agents

## Utility-based Agents
