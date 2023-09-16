- observer starts with some vague estimate of the true reward function (a prior probability over possible reward functions)  
- refine the estimate (update the probability distribution) as more behavior is observed  
  
IRL algorithms need to be generalized from single-agent settings to multi-agent settings. We need algorithms that work when the human and robot are part of the same environment, interacting with each other. One method: assistance games (or "cooperative inverse reinforcement learning". By playing the game, an intelligent machine works out for itself its human partner's preferences. Russell offers the paperclip game as an example. To teach Robbie her preferences, Harriet has to make decisions that "signal" her preferences. She signals her preferences by choosing an equilibrium solution. Harriet, that is, has to be pretty smart and do lots of thinking in order to teach Robbie, by her actions, her preferences. Maybe we can improve on this by allowing Robbie to ask questions.  
  
## References on Inverse Reinforcement Learning  
  
- Paper introducing the idea of inverse reinforcement learning: Stuart Russell, "Algorithms for inverse reinforcement learning," in _Proceedings of the 11th Annual Conference on Computational Learning Theory_  
- Original paper on structural estimation of Markov decision processes: Thomas Sargent, "Estimation of dynamic labor demand schedules under rational expectations"  
- First algorithms for IRL: Andrew Ng and Stuart Russell, "Algorithms for inverse reinforcement learning," in _Proceedings of the 17th Internal Conference on Machine Learning_  
- Better algorithms for inverse reinforcement learning: Pieter Abbeel and Andrew Ng, "Apprenticeship learning via inverse reinforcement learning"  
- IRL as Bayesian updating: Deepak Ramachandran and Eyal Amir, "Bayesian inverse reinforcement learning"  
- assistance games: Dylan Hadfield-Menell et al., "Cooperative inverse reinforcement learning"  
- Difficulties in learning complex human preferences:  
  - Avrim Blum, Lisa Hellerstein, and Nick Littlestone, "Learning in the presence of finitely or infinitely manh irrelevant attributes"  
  - Lori Dalton, "Optimal Bayesian feature selection"  