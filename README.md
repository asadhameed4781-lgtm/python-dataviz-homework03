# Homework 2: emissions and trade

**Deadline: Monday, 30 November 2026.**

Read [assignment.pdf](assignment.pdf) for the question, variables and deliverable.
Submit one figure with its title and notes by pushing it to your own fork.
The repository number continues the earlier `python-dataviz-homework02` name;
this is the second assessed figure assignment.

## Get the files

1. Open [the homework repository](https://github.com/ulrichwohak/python-dataviz-homework03).
2. Click **Fork**, choose your own GitHub account and keep the repository name.
3. Clone your fork. Replace `YOUR-USERNAME` with your GitHub username:

```bash
git clone https://github.com/YOUR-USERNAME/python-dataviz-homework03.git
cd python-dataviz-homework03
```

Both data files are included in `data/`; no data-fetch command is needed.
Definitions and sources are in [data/README.md](data/README.md).

## Optional Python starter

The starter notebook only loads and previews the data. From this repository's root:

```bash
uv sync --locked
uv run jupyter lab
```

Open [analysis.ipynb](analysis.ipynb) and select **Python 3 (ipykernel)**.
Run it from the repository root so the relative data paths work.

## Submit your figure

1. Save your final figure, including its title and notes, as **`figures/submission.pdf`**
   or **`figures/submission.png`**. Submit one of these files.
2. Commit the file and push it to the **`main` branch of your own fork** by
   **Monday, 30 November 2026**. For a PDF:

```bash
git add figures/submission.pdf
git commit -m "Submit Homework 2 figure"
git push origin main
```

For a PNG, use `figures/submission.png` in the `git add` command.

3. Open your fork on GitHub and check that the submitted figure appears in `figures/`
   and opens correctly. A file saved only on your computer has not been submitted.

Only the figure and its attached notes are assessed. You do not need to submit
code or a separate written response, and you do not need to open a pull request.

Original course material and code are covered by the [MIT licence](LICENSE).
The data retain their source licences, documented in [data/README.md](data/README.md).
