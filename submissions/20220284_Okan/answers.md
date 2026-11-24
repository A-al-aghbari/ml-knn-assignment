# Answers: k-NN Pump Assignment

**Name: Okan Burak Bilgen **
**Student number:20220284**

---

### 1. What does k = 3 mean?
In your own words: how does the model decide whether a new pump is Normal or Faulty?

_Your answer: k = 3 means that when determining the status (normal or faulty) of a new pump, the algorithm looks at the 3 nearest-neighbor pumps in the training set based on scaled sensor data and selects the status shared by the majority._


### 2. Why do we scale the features?
What could go wrong if we used the raw values (mm/s, °C, A) without scaling?

_Your answer: Without scaling, sensor data with bigger numbers control the distance calculation, so datas smaller numbers get ignored and the predictions become inaccurate._


### 3. Read your confusion matrix
- How many **faulty pumps did the model miss** (predicted Normal, really Faulty)?
- How many **false alarms** did it raise (predicted Faulty, really Normal)?
- In a factory, which of these two mistakes is more expensive, and why?

_Your answer:_ 0 false alarms, a faulty pump is more expensive mistake because it can cause unexpected malfunction when using it, but a false alarm only causes an extra checking.


### 4. Predictions for the new pumps

| Pump | Prediction |
| --- | --- |
| NEW1 | normal  |
| NEW2 | faulty |
| NEW3 | normal |

Which pump are you **least sure** about, and why? (Hint: look at its sensor values.)

_Your answer:_ number 2 because its having 6.3mm/s vibration 


### Bonus (optional)
- Which k gave the highest test accuracy?
- Accuracy for k = 3 **with** scaling: ____ and **without** scaling: ____

_Your answer:_

---

### Use of AI tools
Did you use an AI tool? If yes, what for?

_Your answer:_ yes, helped with codes because i had troubles and mistakes when writing them 
