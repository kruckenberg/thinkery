[[Stuart Russell]] believes we erred in attempting to give intelligent machines **definite** goals. That is, we've mistakenly thought that machines are intelligent to the extent that their actions can be expected to achieve *their* objective. Truly beneficial intelligent machines would, through their actions, help us achieve *our* objectives. 

What's wrong with *definite* objectives? In short, we don't know how to precisely specify our objectives. Even if we could, our objectives can change.

[[Stuart Russell]] proposes, then, three principles for beneficial machines:
1. The machine's only objective is to maximize the realization of human preferences [^human-preferences]
2. The machine is initially uncertain about what those preferences are.
3. The ultimate source of information about human preferences is human behavior.

[^human-preferences]: According to Russell, "preferences are all-encompassing; they cover everything you might care about, arbitrarily far into the future. And they are yours: the machine is not looking to identify or adopt one ideal set of preferences but to understand and satisfy . . . the preferences of each person."

He's calling for perfect altruism and bedrock humility in intelligent machines as well as a recognition about the fuzziness and malleability in our preferences. [[Eliciting Preferences]] becomes a fundamental problem.

# Provably Beneficial Machines  
  
Can we build AIs that are guaranteed -- mathematically proven -- to be beneficial?  
  
- Any such proof "should hold _regardless of how smart the components become_".  
- We can't ask for a proof that AIs will produce optimal results. That's computationally infeasible. Instead, we should ask that AIs make "best possible" decisions.  
- Such a proof will probably not be an iron-clad guarantee, but rather a proof of "very high probability"  
- A proof won't be much assurance if it begins from untrue premises. And premises about the real world always fudge a bit. In more mature engineering disciplines, good engineers have some intuition about how reasonable their starting assumptions are. We probably won't have the benefit when it comes to designing AIs. "So, we are going to have to be very careful in examining our assumptions. When a proof of safety succeeds, we need to make sure it's not succeeding because we have made unrealistically strong assumptions or because the definition of safety is too weak."  
  
## The off-switch game  
  
As long as an intelligent machine (1) remains uncertain about its human's preferences and (2) is perfectly altruistic (and loyal?), we can prove that the intelligent machine will always allow itself to be switched off. The intelligent machine, because it is perfectly altruistic, wants to please its human and, because it is uncertain what will please its human, keeps open the possibility that the human would prefer that the intelligent machine be switched off (or taken out of the decision). Its willingness to be terminated (or taken out of the decision) will hold even if the intelligent machine knows that its human sometimes makes mistakes, or so Russell claims. He provides a simple case -- a single decision where any probability that the machine's decision will frustrate rather than further its human's preferences (which is all we mean when we say that the machine is uncertain about its human's preferences). Does that result hold when we consider:  
  
- human fallibility (and the machine's knowledge of human fallibility)  
- non- or less-bounded decisions. Why wouldn't the machine take into consideration all the benefit he is more sure it could provide in future if it is not switched off?  
- a human's uncertainty about his or her preferences (including the case where the human's preferences have not yet been formed)  
  
Won't the machine's uncertainty diminish over time, eventually reaching a point where the machine is certain it understands its human's preferences and so no longer defers (because no additional information would change its model)? Yes. If the machine initially gave some weight to the human's true preferences, its model should converge on those true preferences. If the machine's model initially excludes the human's true preferences (for example, it does not include one or more values), the machine's model should converge on what, in its possibility space, is closest to its human's true preferences.

