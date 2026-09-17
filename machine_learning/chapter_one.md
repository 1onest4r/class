### What is "Machine Learning"
- it means to feed a big chunks of data to machine to make it learn something
	- traditionally humans make the rules. In machine learning computer looks at past examples (training set) to figure out the rules itself and make predictions on brand-new information.
### WHY ML?
- it's good at solving complex problems with no clear rules
- problems with long lists of rules
- a system that needs to adapt to new environment automatically whenever fresh data comes in
- discovering hidden insights that humans wouldn't normally would notice
### Categories of ML
---
#### Supervised learning
- the developer feeds the machine with a data that is already correct (called labels)
	- classification where it categorizes
	- **regression**: predicting a specific continuous number
#### Unsupervised learning
- gives a data let it find the hidden patterns or natural groupings on its own
	- **clustering:** grouping similar instances together

---
#### Batch learning (offline)
- it trains with only given data and once it goes online it stops learning and if the developer wishes to update it requires them to start completely from scratch
#### Online learning
- the system learns continuously and incrementally in small steps as data arrives in real time

---
#### Instance based learning
- basically cache prediction?

#### Model based learning
- the computer studies the examples to build simplified and general rule or formula (model) then uses that to make predictions.
---
### Main challenge and pitfalls
#### Bad data problems
- **not enough data**
- **unrepresentative data** (if examples don't accurately reflect real world, the predictions will be flawed)
- **poor quality data**
#### Bad model problems
- **overfitting** (the model is too complex and memorizes random noise and tiny detail in the training data rather than general patterns as a result it works great in local space but fails on new data)
- **underfitting** (the model is too simple)

### Test validation
- testing on new data
- no free lunch theorem (there is no single best algorithm that works perfectly for everything one must make reasonable assumptions)