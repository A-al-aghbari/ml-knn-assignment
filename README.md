# Assignment: Detecting Faulty Pumps with k-Nearest Neighbors

**Course:** Introduction to Machine Learning · Automation Engineering
**Type:** Individual assignment
**Deadline:** _[date set by the instructor]_
**Weight:** _[set by the instructor]_

---

## The task

A factory monitors **300 water pumps** with three sensors:

| Column | Meaning | Unit |
| --- | --- | --- |
| `vibration_mm_s` | Vibration of the pump | mm/s |
| `temperature_c` | Motor temperature | °C |
| `current_a` | Motor current | A |
| `status` | Condition of the pump (the label) | `Normal` or `Faulty` |

Build a **k-Nearest Neighbors (k-NN) model with k = 3** that predicts whether a pump is `Normal` or `Faulty` from its three sensor readings.

> The dataset is synthetic (generated for teaching), but it behaves like real pump monitoring data.

## What you will practise

- Loading and exploring data with pandas
- Splitting data into training and test sets
- Scaling features with `MinMaxScaler`
- Training and evaluating a k-NN classifier with scikit-learn
- Uploading your work to GitHub with a pull request

## Files in this repository

```
ml-knn-assignment/
├── README.md                 ← you are here: instructions
├── requirements.txt          ← Python packages needed
├── data/
│   ├── pump_data.csv         ← 300 labelled pumps
│   └── new_pumps.csv         ← 3 new pumps to predict
├── starter/
│   └── knn_assignment.ipynb  ← the notebook you will complete
└── submissions/
    ├── README.md             ← how to name your folder
    └── _template/
        └── answers.md        ← questions to answer
```

## Steps

| Part | What to do | Points |
| --- | --- | --- |
| 1 · Explore | Load the data, count Normal / Faulty pumps, scatter plot of vibration vs temperature | 15 |
| 2 · Prepare | Choose X and y, split 80/20 (`random_state=42`, `stratify=y`), scale with `MinMaxScaler` | 15 |
| 3 · Train | `KNeighborsClassifier(n_neighbors=3)` on the scaled training data | 20 |
| 4 · Evaluate | Test accuracy and confusion matrix | 20 |
| 5 · Predict | Predict the 3 pumps in `new_pumps.csv` | 10 |
| 6 · Answers | Answer 4 short questions in `answers.md` | 20 |
| **Bonus** | Accuracy for k = 1 … 15, and k = 3 with vs without scaling | +10 |
| | **Total** | **100 (+10)** |

All instructions are inside the starter notebook. Fill in every cell marked `# TODO`.

**You can work in Jupyter, VS Code or Google Colab.** On Colab, upload the notebook plus the two CSV files from `data/` into the same Colab folder. You can also download the data directly:

- [pump_data.csv](https://raw.githubusercontent.com/A-al-aghbari/ml-knn-assignment/main/data/pump_data.csv)
- [new_pumps.csv](https://raw.githubusercontent.com/A-al-aghbari/ml-knn-assignment/main/data/new_pumps.csv)

---

## How to submit (pull request)

Everyone submits to **this one repository**, each student in their **own folder**.

### 1. Fork the repository
Click **Fork** (top right of this page). This makes your own copy under your GitHub account.

### 2. Create your folder
In **your fork**, create the folder `submissions/<studentnumber>_<FirstName>/`, for example:

```
submissions/20231234_Ahmed/
```

Use English letters only, no spaces.

**In the browser:** open `submissions/`, click **Add file → Create new file**, and type `20231234_Ahmed/answers.md` as the file name (the `/` creates the folder). Paste in the contents of `_template/answers.md`, fill it in, and click **Commit changes**.

### 3. Upload your notebook
Open your new folder, click **Add file → Upload files**, drag in your completed `knn_assignment.ipynb`, then click **Commit changes**.

Your folder must contain exactly these two files:

```
submissions/20231234_Ahmed/
├── knn_assignment.ipynb   ← completed notebook, run from top to bottom
└── answers.md             ← your answers
```

### 4. Open a pull request
In your fork, click **Contribute → Open pull request**. Use the title **`Submission: 20231234_Ahmed`**, tick the checklist, and click **Create pull request**.

### 5. Check the automatic test
A check runs on your pull request. It confirms that:
- only your own folder was changed,
- both files are there,
- your notebook runs without errors.

A red ✗ means something is wrong: click **Details**, fix it in your fork, and commit again. The pull request updates automatically. **Do not open a second pull request.**

> The first time you submit, the instructor may need to approve the check before it runs. That is normal.

### Using Git on the command line instead
```bash
git clone https://github.com/<your-username>/ml-knn-assignment.git   # your fork
cd ml-knn-assignment
mkdir submissions/20231234_Ahmed
cp starter/knn_assignment.ipynb submissions/20231234_Ahmed/
cp submissions/_template/answers.md submissions/20231234_Ahmed/
# ... complete both files ...
git add submissions/20231234_Ahmed
git commit -m "Submission: 20231234_Ahmed"
git push
```
Then open the pull request on GitHub as in step 4.

---

## Rules

- **Individual work.** You may discuss ideas, but your code and answers must be your own.
- **Do not copy from other students' pull requests.** Pull requests are visible, and similar submissions get zero.
- **Do not change** files outside your own folder.
- Commits after the deadline are not graded.
- Using AI tools: allowed for learning and debugging. Say how you used them at the end of `answers.md`, and be ready to explain every line.

Questions? Ask in class or open an **Issue** in this repository.
