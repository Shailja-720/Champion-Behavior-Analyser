# Champion-Behavior-Analyser
Mapping gameplay choices to player behavior for a healthier, more engaging gaming community
Understanding Player Behavior through Champion Choice
Online multiplayer games create fascinating ecosystems of player interactions, where gameplay mechanics and personal behaviors merge into complex social patterns. Our project was inspired by this world—particularly by the recurring question: Do certain in-game choices, like champion selection, correlate with toxic or disruptive behavior?
 
Inspiration
The initial inspiration came from observing that discussions in online gaming communities often revolve around stereotypes tied to champion selection. Some players claim that certain “aggressive” champions attract toxic players, while others believe difficult champions cause frustration that manifests as negative behavior. We wanted to explore whether data could actually confirm or challenge these perceptions.
By merging concepts from behavioral psychology, social computing, and data science, we sought to uncover quantifiable relationships hidden within massive behavioral datasets.
 
What We Learned
Through this project, we learned that player toxicity is not a single variable but a multi-dimensional construct with psychological, social, and contextual dependencies.
We discovered that traditional statistical methods struggle with the nonlinear interactions between variables like champion role, player experience, and recent match outcomes.
To address this, we applied machine learning techniques capable of modeling complex relationships:
P(Y="toxic"∣X_"champion" ,X_"context" ,X_"history" )
where $ Y $ represents the probability of disruptive behavior, and $ X $ encompasses features like champion attributes and past player performance metrics.
This probabilistic framework allowed us to infer correlations while acknowledging uncertainty and variance within the data.
 
How We Built the System
The system development followed an iterative data-science pipeline:
	Data Collection – We gathered anonymized match data, player reports, chat logs (tokenized for privacy), and metadata for each champion (role, difficulty, win rate, and playstyle vectors).
	Feature Engineering – Variables were grouped into behavioral, contextual, and mechanical categories. Champion traits such as burst potential, flexibility across roles, and crowd-control capability were numerically encoded.
	Normalization – We applied min-max scaling and time-dependent normalization to ensure consistent comparisons across patches.
	Modeling – Techniques like logistic regression, random forests, and gradient-boosted trees were trained to detect associations. For non-linear effects, we also experimented with deep neural networks:f(X)=σ(W_2⋅"ReLU"(W_1 X+b_1)+b_2)where $ f(X) $ outputs toxicity probability scores.
	Validation – Cross-validation and precision-recall metrics were used to evaluate model fairness and performance, particularly across player experience tiers.
 
Challenges Faced
Building the system revealed several key challenges:
	Label Ambiguity: Defining “toxic” behavior proved difficult. Player reports often reflected subjective annoyance rather than objective misconduct.
	Causality vs. Correlation: Even if model outputs suggested that picking a certain champion increased toxicity risk, separating cause from preference bias required deeper experimental design.
	Data Bias: Popular champions generated more data, creating imbalance in the dataset. Undersampling and SMOTE techniques were used to mitigate this.
	Community Sensitivity: Normalization of toxicity meant some players perceived mild toxicity as “normal,” complicating label accuracy.
 
Impact and Future Work
Our results provide actionable insights for developers: champions with higher mechanical complexity or polarizing playstyles often showed stronger associations with frustration-driven behaviors. These findings can inform matchmaking algorithms, balance adjustments, and player education initiatives.
Looking ahead, we plan to incorporate temporal behavior modeling using recurrent neural networks to capture evolving player patterns and employ explainability tools like SHAP to make model insights transparent to both developers and players.
