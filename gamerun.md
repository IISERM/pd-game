---
    title: How Does the Game Run?
---

<img src="/res/pokemon.png" alt-text="pokemon.png" style="float: right; width:300px">

Once all the strategies are compiled, a round-robin tournament begins on Oyun (including a built-in RANDOM strategy of the simulator). The final scores are tallied as the arithmetic mean of points the strategy received from all its matches. The winning strategy would be one with the highest average. The winning strategy would be one with the highest average.

Another important thing is the ‘survival scaling’ that would occur for all strategies. Oyun also plugs in all the strategies in a simulated evolutionary environment. Successful strategies (the ones gaining high average points) translate to high fitness traits and proportionately increase in number in the virtual population of the next generation.

With this, every strategy’s growth is monitored on a graph. Every strategy starts with the same fraction. Natural selection through competition drives the change in the distribution by proportion of all strategies. It’s run for 200 generations, and the nal fraction of the strategy in the population is multiplied to 1000 and is added to the mean score from the original game.
<figure>
  <img src="/res/oyunsett.png" alt="oyunsett.png"/>
  <figcaption>Figure 4: We will use both options of Oyun for the tournament</figcaption>
</figure>
