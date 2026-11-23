# Assignment: Detecting Faulty Pumps with k-Nearest Neighbors

| | |
| --- | --- |
| **Course** | Introduction to Machine Learning · Automation Engineering |
| **Type** | Individual assignment |
| **Deadline** | **Monday 30 November 2026, 23:59 (Cyprus time, UTC+2)** |
| **How to submit** | A pull request to this repository (step-by-step guide below) |

---

## Submission at a glance

1. **Fork** this repository to your own GitHub account.
2. Complete the starter notebook `starter/knn_assignment.ipynb`.
3. In your fork, create your folder: `submissions/<studentnumber>_<FirstName>/`
4. Put **two files** in it: `knn_assignment.ipynb` and `answers.md`.
5. Open a **pull request** titled `Submission: <studentnumber>_<FirstName>`.
6. Wait for the green ✓ on your pull request **before the deadline**.

The full instructions are in **[How to submit: step by step](#how-to-submit-step-by-step)**.

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

### What you will practise

- Loading and exploring data with pandas
- Splitting data into training and test sets
- Scaling features with `MinMaxScaler`
- Training and evaluating a k-NN classifier with scikit-learn
- Submitting your work on GitHub with a pull request

### Parts and points

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

All detailed instructions are inside the starter notebook. Fill in every cell marked `# TODO`.

### Files in this repository

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
    ├── README.md             ← folder naming rules
    └── _template/
        └── answers.md        ← the questions to answer
```

---

## Doing the assignment

You can work in **Google Colab** (easiest, nothing to install), **Jupyter** or **VS Code**.

### Option A: Google Colab

1. Download the starter notebook: open [`starter/knn_assignment.ipynb`](starter/knn_assignment.ipynb) and click the **Download raw file** button (↓ icon, top right of the file).
2. Download the two data files:
   [pump_data.csv](https://raw.githubusercontent.com/A-al-aghbari/ml-knn-assignment/main/data/pump_data.csv) and
   [new_pumps.csv](https://raw.githubusercontent.com/A-al-aghbari/ml-knn-assignment/main/data/new_pumps.csv)
   (right-click → *Save link as…*).
3. Go to [colab.research.google.com](https://colab.research.google.com) → **File → Upload notebook** → choose `knn_assignment.ipynb`.
4. Click the **folder icon** on the left, then **Upload**, and upload both CSV files.
5. Complete the notebook, then click **Runtime → Restart session and run all** and check there are no errors.
6. Download it: **File → Download → Download .ipynb**.

### Option B: Jupyter or VS Code on your computer

1. Clone your fork (see [Using Git on the command line](#using-git-on-the-command-line-optional)).
2. Install the packages: `pip install -r requirements.txt`
3. Copy `starter/knn_assignment.ipynb` into your submission folder and complete it there.
4. Run **Restart & Run All** and check there are no errors.

---

## How to submit: step by step

Everyone submits to **this one repository**. Each student works in **their own folder**, so nobody's work overwrites anybody else's.

### Step 0 · Create a GitHub account (if you don't have one)

Sign up for free at [github.com/signup](https://github.com/signup). Your university email lets you apply for the free [GitHub Student Developer Pack](https://education.github.com/pack) too (optional).

### Step 1 · Fork this repository

1. Make sure you are logged in to GitHub.
2. At the top right of this page, click **Fork → Create fork**.
3. You now have your own copy at `github.com/<your-username>/ml-knn-assignment`.

> **Do all the next steps in your fork**, not in the original repository. Check that the page shows *your* username at the top left.

### Step 2 · Create your folder and `answers.md`

Your folder name is **`<studentnumber>_<FirstName>`**: English letters only, no spaces, for example `20231234_Ahmed`.

1. In your fork, open the **`submissions`** folder.
2. Click **Add file → Create new file**.
3. In the file name box, type: `20231234_Ahmed/answers.md` (with **your** number and name). Typing the `/` creates the folder.
4. Open [`submissions/_template/answers.md`](submissions/_template/answers.md) in another tab, copy all of it, and paste it into your new file.
5. Write your answers.
6. Click **Commit changes… → Commit changes**.

### Step 3 · Upload your notebook

1. Open your new folder `submissions/20231234_Ahmed/`.
2. Click **Add file → Upload files**.
3. Drag in your completed **`knn_assignment.ipynb`**. Keep this exact file name.
4. Click **Commit changes**.

Your folder must now contain **exactly these two files**:

```
submissions/20231234_Ahmed/
├── knn_assignment.ipynb   ← completed notebook, run from top to bottom
└── answers.md             ← your answers
```

### Step 4 · Open a pull request

1. Go to the main page of your fork.
2. Click **Contribute → Open pull request**.
3. Check the direction at the top: **base repository: `A-al-aghbari/ml-knn-assignment`** ← **head repository: `<your-username>/ml-knn-assignment`**.
4. **Title:** `Submission: 20231234_Ahmed`
5. In the description, fill in your name and student number and tick every box in the checklist.
6. Click **Create pull request**.

You have now submitted. Open **only one** pull request.

### Step 5 · Check the automatic test

A check called **Check submission** runs on your pull request. It confirms that:

- you changed files only inside your own folder,
- your folder name is correct,
- both files are there,
- your notebook runs from top to bottom without errors.

| You see | Meaning |
| --- | --- |
| 🟡 Yellow dot | The check is running, or waiting for the instructor to approve it (normal for your first submission) |
| ✅ Green ✓ | Everything is fine |
| ❌ Red ✗ | Something is wrong: click **Details** to read the error, then see [Fixing problems](#fixing-problems) |

### Step 6 · Making changes after you submit

You can update your work **until the deadline**:

1. Go to your folder **in your fork**.
2. Edit `answers.md` (pencil icon ✏️), or upload a new `knn_assignment.ipynb` with the same name to replace the old one.
3. Commit the change.

Your pull request updates **automatically**. Do **not** open a new pull request.

### Final checklist before the deadline

- [ ] My folder is named `<studentnumber>_<FirstName>` and is inside `submissions/`
- [ ] It contains `knn_assignment.ipynb` and `answers.md`, and nothing else
- [ ] My notebook ran with **Restart & Run All** and shows all outputs and plots
- [ ] All questions in `answers.md` are answered
- [ ] I opened **one** pull request titled `Submission: <studentnumber>_<FirstName>`
- [ ] The check on my pull request is green ✓ (or waiting for approval)

---

## Fixing problems

| Error message in **Details** | What to do |
| --- | --- |
| `Folder name '...' is wrong` | Rename your folder to `<studentnumber>_<FirstName>`, e.g. `20231234_Ahmed`. The easiest way is to create a new correctly named folder, upload both files again, and delete the old files. |
| `Only change files inside your own submissions/ folder` | You edited another file (e.g. the README or the starter notebook). Open that file in your fork and undo your change, or delete your fork, fork again and repeat the steps. |
| `Change exactly one folder` | You created more than one folder. Delete the extra one. |
| `Missing submissions/.../answers.md` (or `knn_assignment.ipynb`) | Upload the missing file. Check the spelling: lower-case, with underscores. |
| The **Run your notebook** step failed | Your notebook has an error. Scroll to the bottom of the log to see which cell failed, fix it, run **Restart & Run All**, and upload it again. |
| I opened two pull requests | Close the extra one (button at the bottom of the pull request). |

Still stuck? Open an **Issue** in this repository (**Issues → New issue**) or ask in class. Do this **before** the deadline.

---

## Using Git on the command line (optional)

If you prefer Git instead of the browser:

```bash
# 1. Clone YOUR fork (replace <your-username>)
git clone https://github.com/<your-username>/ml-knn-assignment.git
cd ml-knn-assignment

# 2. Create your folder with the two files
mkdir submissions/20231234_Ahmed
cp starter/knn_assignment.ipynb submissions/20231234_Ahmed/
cp submissions/_template/answers.md submissions/20231234_Ahmed/

# 3. Complete both files, then upload them
git add submissions/20231234_Ahmed
git commit -m "Submission: 20231234_Ahmed"
git push
```

Then open the pull request on GitHub as in [Step 4](#step-4--open-a-pull-request). Later changes: edit, then `git add`, `git commit` and `git push` again.

---

## Rules

- **Deadline:** Monday 30 November 2026, 23:59 (Cyprus time). Commits made after the deadline are not graded.
- **Individual work.** You may discuss ideas, but your code and answers must be your own.
- **Do not copy from other students' pull requests.** Pull requests are public, and similar submissions get zero.
- **Do not change** any file outside your own folder.
- **AI tools** are allowed for learning and debugging. Say how you used them at the end of `answers.md`, and be ready to explain every line of your code.

Good luck!
