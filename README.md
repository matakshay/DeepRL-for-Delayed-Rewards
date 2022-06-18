<h1> Deep Reinforcement Learning for delayed rewards problems </h1>

<p align="justify">
	These experiments study Deep RL methods for Temporal Credit Assignment of delayed rewards in decision processes. Different environment configurations,
	reward strategies and model-free policy evaluation algorithms are compared. The experiments also contrast different neural architectures & loss 		functions for learning more 'immediate' rewards from delayed episodic rewards.
</p>
    

<h2 id="intro"> Introduction </h2>
<p align="justify">
	Reinforcement Learning is one of the most promising areas in modern artificial intelligence. It revolves around training an agent to navigate an 
	environment. The agent interacts with its surrounding by performing actions and getting rewards based on it. It continuously improves its behavioural 
	policy to maximise its cumulative reward.
<br>
	In many practical settings, the reward feedback for an action is not available immediately to the agent - it can be delayed by a few time steps. This 
	is the problem of delayed rewards. Such decision processes are modelled using the generalised framework of a graph where an agent traverses 
	over the vertices (which represent the states of the environment) by performing actions (which are represented by the edges in the graph). One or a 
	few of the vertices in the graph can be associated with probabilistic rewards which get credited when the agent reaches them. There can also be 
	long-term dependencies in this setting, wherein, say a state/action only yields reward when the agent has previously visited a specific state or 
	performed some specific action. The accumulated reward from all these is however available only at the end of an episode. The challenge then is to 
	develop efficient algorithms to analyse such delayed rewards and assign their credit to state-action pairs back in time throughout the episode. We 
	propose to conduct biased random walks over the graph to sample episodes. These are then used in a model-free framework which learns from experience 
	to decompose the accumulated reward and redistribute it among the state-action pairs in the episode, thus converting delayed rewards to more immediate 	   ones. Each of the experiments is discussed in more detail in the subsequent sections.
