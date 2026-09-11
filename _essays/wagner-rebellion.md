---
title: "Attack or withdraw? The strange case of the one-day Wagner Group rebellion of 23 June 2023"
date: 2023-11-29
---

*Originally written as the final project for BSE Microeconomics: Game Theory, November 2023.*

## Background

On the 23rd of June 2023, the Wagner Group, a notorious Russian private military company that had been heavily involved in supporting Russian forces in its invasion of Ukraine, staged a dramatic military rebellion. Following months of feuding between the leader of the mercenary group, Yevgeny Prigozhin, and the Russian Ministry of Defence over the war's conduct, the Wagner Group seized control of the major Russian city of Rostov-on-Don and began advancing an armoured column towards Moscow.[^1]

The column faced surprisingly little resistance from Vladimir Putin's government forces during its advance, downing several Russian airforce assets and incurring only minor casualties,[^2] and it seemed an armed insurrection was in full swing. However, the rebellion was amazingly short-lived. Shortly after Putin made a televised address accusing Prigozhin of treason and betrayal, a settlement was brokered on the following day and the Wagner Group withdrew their forces, despite being less than 200km from reaching Moscow.

What prompted such an about-turn from Prigozhin and his paramilitary group? This seems particularly odd given the fact they had faced such a lacklustre response from Russian forces and were so close to the capital. I propose that this unexpected turn of events can be explained via a game of signalling between Putin and the Wagner Group. To do so, I use a modification of the Beer-Quiche Game as originally devised by Cho and Kreps (1987) to explore the strategic dimensions of the decision-making undertaken by both sides.[^3] Additional inspiration was also found in applications of this signalling game to classic military examples from Chinese literature by Cotton and Liu (2011).[^4]

## The set up of the game

The game I describe below begins with the Wagner troop column already closing in on Moscow, but prior to any observable actions from Vladimir Putin.

### Players

There are two strategic players, Putin and Wagner, along with Nature as a third strategy-less player with a fixed mixed strategy and no payoffs.

### Actions

Nature makes Putin *Strong* with a probability of α or *Weak* with a probability of 1 − α. In this context, being strong or weak can refer to not only his leadership and defences in Moscow but also whether he has the backing of elites within the regime in the event of a coup d'état or armed rebellion. At the game's start, both Putin and Wagner receive common knowledge of how α and 1 − α are distributed.

Putin has private knowledge of whether he is a Strong or Weak type and can choose to either:

- *Stay and denounce*: Signal his intention to stay in Moscow by appearing on live television to denounce Wagner (which is what occurred in reality), or;
- *Flee Moscow*: Leave Moscow and hide in safety, leaving the city vulnerable to capture.

Wagner, observing Putin's choices but not knowing his type, can choose to either:

- *Attack*: Continue their military convoy towards Moscow and engage in a military confrontation in the Russian capital, or;
- *Withdraw*: Cease their advance and return to their base of operations (as what transpired in reality).

### Payoffs

Three objects of value are identified in this game: the value of strategic control over Moscow (and, by extension, the instruments of government), the strategic value of the advancing Wagner Group forces, and the strategic value of Putin as the leader of the Russian Federation.

The value of having strategic control over Moscow has been normalised to 1. The strategic value of Wagner's advancing troops is some value a, while the strategic value of Putin is denoted as b. I safely assume here that 0 < a < b < 1 (that is, the Wagner mercenaries are strategically worth less than Putin as a leader who is worth less than control of the entire Russian government) and that both strategic players, Putin and Wagner, understand and value each object the same amount. The payoffs here are zero-sum given the high-stakes military context and are described as follows:

- If Wagner plays *Withdraw*, regardless of Putin's type or actions, the payoffs are (0, 0). That is, no armed confrontation occurs in Moscow and no player gains or loses utility.
- If Putin plays *Flee Moscow* and Wagner plays *Attack*, the payoffs are (−1, 1). The Kremlin is left without coordinated leadership and Wagner forces are able to enter the capital and seize control of government. Putin loses strategic control of the country while Wagner gains it.
- If Putin is a Strong type and Wagner plays *Attack* after observing Putin play *Stay and denounce*, the payoffs are (a, −a). This is because their forces are neutralised, so Wagner loses a, while Putin gains a for eliminating a rebellious force.
- If Putin is a Weak type and Wagner plays *Attack* after observing *Stay and denounce*, the payoffs are (−(1 + b), (1 + b)). That is, Putin is unable to maintain leadership and Wagner gains control of the Kremlin and captures Putin as well, so they gain (1 + b), while Putin loses that amount.

The extensive form representation of this game is depicted below:

![Extensive form representation of the Wagner-Putin signalling game](/assets/wagner-game-base.jpg)

## Solutions to the game

Before I solve this game, I make two immediate observations based on the payoffs and possible actions presented for this game:

1. Wagner will always play *Attack* if they observe Putin, regardless of type, playing *Flee Moscow* since this will always be a dominant strategy for their lower information set.
2. Given this, it is clearly the case that if Putin is Strong he will always play *Stay and denounce* since that will yield a higher payoff for the Strong type.

I now proceed to identify any pooling or separating Perfect Bayesian Equilibria, in either pure or mixed strategies, where strategies are sequentially rational given beliefs.

### Case 1: Pooling equilibria — Putin always flees regardless of type

This equilibrium can be immediately ruled out since, as stated above, a Strong Putin will have an incentive to deviate and will always play *Stay and denounce*.

### Case 2: Pooling equilibria — Putin always stays regardless of type

Now consider an equilibrium where both a Strong and Weak Putin always choose to play *Stay and denounce*. Wagner cannot distinguish between types and believes that Pr(Strong \| Stay and denounce) = α, Pr(Weak \| Stay and denounce) = 1 − α, and that Pr(Strong \| Flee Moscow) = Pr(Weak \| Flee Moscow) = 0. They will always play *Attack* in their upper information set if their expected utility of doing so is greater than playing *Withdraw* (which is zero). That is, they will attack if −α(a) + (1 − α)(1 + b) > 0.

This occurs if the probability α of Nature assigning Putin the Strong type is α < (1 + b) / (1 + a + b). However, given sequential rationality, a Weak Putin would then have an incentive to deviate from this strategy and play *Flee Moscow* since a Weak Putin would only lose −1 compared to −(1 + b) if he chose to stay, which means this cannot be a viable equilibrium since beliefs are inconsistent with strategies.

This indicates that there is a stable pooling equilibrium, where Putin always plays *Stay and denounce* and Wagner always plays *Withdraw* if α ≥ (1 + b) / (1 + a + b).

### Case 3: Separating equilibrium — A Strong Putin flees and a Weak Putin stays

It is easily shown that this cannot be an equilibrium. As already noted, a Strong Putin will have an incentive to defect and play *Stay and denounce*.

### Case 4: Separating equilibrium — A Strong Putin stays and a Weak Putin plays a mixed strategy between staying and fleeing

Up to this point, my analysis has not considered mixed strategies. This is because a Strong Putin has a dominant pure strategy, ruling out mixing, and because in Case 2 Putin will always play *Stay and denounce* regardless of type. Here, however, there is the possibility of a Weak Putin playing a mixed strategy between staying and fleeing, which also implies a potential mixed strategy for Wagner.

Let β be the probability that a Weak Putin plays *Stay and denounce* and (1 − β) be the probability that a Weak Putin plays *Flee Moscow*.

Likewise, let γ be the probability that Wagner plays *Attack* when they observe the action *Stay and denounce* and (1 − γ) be the probability that they play *Withdraw* when they observe this (and as already established, Wagner will always attack if they observe *Flee Moscow*).

I notate the extensive form representation with these mixed strategy probabilities, as well as highlight the dominant strategies, to assist with the analysis:

![Extensive form representation annotated with mixed strategy probabilities](/assets/wagner-game-mixed.jpg)

A Weak Putin mixes in response to the γ probability of attack and is indifferent if their expected value between staying and fleeing are the same. That is, if −γ(1 + b) = −1, which solves for γ = 1 / (1 + b). Note that 1/2 < γ < 1 since I have assumed that 0 < b < 1.

When Wagner observes Putin play *Stay and denounce*, their beliefs are Pr(Strong \| Stay and denounce) = α and Pr(Weak \| Stay and denounce) = β(1 − α).[^5]

Wagner mixes between *Attack* and *Withdraw* and for beliefs to be consistent with strategies, they will be indifferent between the two when the expected value of attacking Putin given that he is Strong plus the expected value of attacking Putin given that he is Weak and has played *Stay and denounce* with probability β is equal to the value of playing *Withdraw*. This is given by the formula:

−a · Pr(Strong \| Stay and denounce) + (1 + b) · Pr(Weak \| Stay and denounce) = 0

That is, Wagner is indifferent if the expected value is −α(a) + (1 − α)β(1 + b) = 0. Rearranging this expression shows that this occurs when a Weak Putin plays β = [α / (1 − α)] · [a / (1 + b)]. It is always the case, given the setup of the game's parameters, that 0 < β < 1. This also has the implication that there will never be conditions under which a Weak Putin would choose a pure strategy and exclusively play *Flee Moscow*.

## Results

Two Perfect Bayesian Equilibria have been identified in this game:

1. A pure strategy pooling equilibrium where Putin, regardless of type, always plays *Stay and denounce*. Wagner always plays *Withdraw* when they observe this and always plays *Attack* if they observe *Flee Moscow*. This equilibrium is possible under the condition that α ≥ (1 + b) / (1 + a + b).
2. A mixed strategy separating equilibrium where a Strong Putin always plays *Stay and denounce* while a Weak Putin plays a mixed strategy of [α / (1 − α)] · [a / (1 + b)] probability of staying and 1 − [α / (1 − α)] · [a / (1 + b)] probability of fleeing. If Wagner observes *Stay and denounce*, they play *Attack* with a probability of 1 / (1 + b) and *Withdraw* with a probability of b / (1 + b), and always plays *Attack* if they observe *Flee Moscow*.

## Discussion

Both Perfect Bayesian Equilibrium solutions to this game are plausible given what was observed in reality, which was the withdrawal of the Wagner forces before any significant military confrontations with the Russian government occurred. It also shows that a seemingly toothless gesture, i.e. a televised address and denouncement of Wagner by the Putin administration, was a signal that the Wagner Group had to genuinely consider as it showed Putin's intention to stay in the capital and confront them from a potentially strong position.

Regarding the pure strategy pooling equilibrium, notice that it is sustained given a sufficiently large α which can be cleanly expressed in terms of the ratio of the value of Putin and control of government (1 + b) to the sum of all three objects of value in this game (1 + a + b). Perhaps once the march was initiated but before a formal government response, α was revealed to be a fairly high probability. For instance, maybe it was revealed to Prigozhin that there was a high likelihood the political elite would still support Putin, despite the various campaign setbacks and economic sanctions imposed on Russia due to the conflict in Ukraine.

Similarly, the mixed strategy separating equilibrium is also a prediction from the game that can plausibly align with real-world outcomes. That is, we potentially observed Wagner play *Withdraw* from their mixed strategy after Putin played *Stay and denounce* either as a Strong type or as a Weak type. Concerning the latter type, it could indeed have been the case that during this brief period of crisis, Putin was sufficiently weak in his position to have been unable to meaningfully confront an attack from Wagner. Even so, the mixed strategy identified for the Putin player in this game means that it was still within the realms of possibility for a Weak Putin to choose to stay and, in doing so, pretend to be in a strong position.

Of course, all models have limitations. This signalling game focuses on the key decisions within the single day of the failed Wagner Group rebellion. It does not, for instance, explore the strategic dimensions of the rivalry between the Wagner Group and the Russian military establishment that precipitated this mutiny. Nor does it consider longer term consequences since the game concludes with either a defeated Putin, a defeated Wagner column, or a peaceful withdrawal of mercenary forces.

Indeed, the withdrawal that transpired in real life was not the true conclusion to the rebellion. After the settlement agreement on the 24th of June, Yevgeny Prigozhin was permitted to leave for Belarus with all charges dropped and it seemed an equilibrium outcome was reached. Then exactly two months to the day after his failed march on Moscow, Prigozhin was killed in a plane crash along with several other senior Wagner leaders in what many international commentators deemed almost certainly a targeted state assassination.[^6] Given that it has been nearly two years since the full-scale Russian invasion of Ukraine in February 2022, triggering countless casualties, a humanitarian crisis, and global economic disruption, one has to wonder what might have happened had different decisions been made during those crucial hours on the 23rd of June 2023.

## References

[^1]: Al Jazeera (2023) [*Timeline: How Wagner Group's revolt against Russia unfolded*](https://www.aljazeera.com/news/2023/6/24/timeline-how-wagner-groups-revolt-against-russia-unfolded).
[^2]: BBC News (2023) [*Wagner revolt: How many planes and people did Russia lose?*](https://www.bbc.com/news/world-europe-66031403)
[^3]: Cho, In-Koo & Kreps, David (1987) Signaling games and stable equilibria. *Quarterly Journal of Economics* 102(2): 179–221.
[^4]: Cotton, Christopher & Liu, Chang (2011) 100 Horsemen and the empty city: A game theoretic examination of deception in Chinese military legend. *Journal of Peace Research* 48(2): 217–223.
[^5]: Note that their other beliefs are Pr(Strong \| Flee Moscow) = 0 and Pr(Weak \| Flee Moscow) = (1 − β)(1 − α), so all beliefs sum to 1.
[^6]: Wall Street Journal (2023) [*Wagner Chief Yevgeny Prigozhin, Who Clashed With Russian Military, Dies*](https://www.wsj.com/world/russia/yevgeny-prigozhin-wagner-mercenary-russia-dies-7da9cea).
