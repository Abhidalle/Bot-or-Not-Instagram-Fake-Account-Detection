#  Bot or Not: Instagram Fake Account Detection

###  The Mission
To build a binary classification engine capable of distinguishing between human users and automated spam bots using metadata-driven patterns.

### The Logic (How the AI plays the game)
The model functions as a digital "bouncer" for Instagram. It doesn't just look at one clue; it calculates a weighted probability based on five specific data points:

1. **Profile Picture:** Bots often lack a personal image.
2. **Bio Length:** Humans write unique bios; bots often have empty or template-based descriptions.
3. **Post Count:** Authentic accounts show a history of activity.
4. **Followers vs. Following:** Bots typically follow thousands of people but have very few followers (a "skewed" ratio).



### The Pipeline
* **Phase 1-3:** Data Wrangling & Feature Selection.
* **Phase 4-5:** Normalizing data using `StandardScaler` to ensure counts (like 10,000 followers) don't overpower binary flags (like profile pic).
* **Phase 6:** Training the `LogisticRegression` brain.
* **Phase 7:** Evaluation using a Confusion Matrix to track True Positives and False Alarms.

### Results
The model achieved a balanced **F1-Score of 0.81**, proving that metadata alone is a powerful predictor for account authenticity.
