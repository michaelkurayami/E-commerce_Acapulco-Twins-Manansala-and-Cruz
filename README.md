# E-Commerce Sales Analytics Dashboard

A student project that analyzes an e-commerce sales dataset with Python and presents the results in a website built with a single HTML file.

The project is organized into two main parts:

1. **Data analysis:** A Jupyter Notebook (`.ipynb`) is used to load, clean, explore, and analyze the dataset, and to run forecasting and machine-learning experiments.
2. **Web dashboard:** `Index.html` presents key findings, KPI cards, charts, and dataset information in a clean dashboard layout.

---

## Project Features

### Python analysis

The Jupyter Notebook is used for:

- Loading the e-commerce CSV dataset.
- Inspecting the dataset and its columns.
- Checking and cleaning the data.
- Removing duplicate records when present.
- Exploring sales performance and trends.
- Comparing categories, regions, and payment methods.
- Examining customer ratings and delivery performance.
- Performing time-series forecasting.
- Evaluating machine-learning models.
- Creating charts and visualizations.

The notebook includes exploratory analysis and predictive-analysis sections. The exact outputs depend on the dataset and the results produced when the notebook is run.

### Website dashboard

`Index.html` is a standalone webpage designed to present the analysis. It includes:

- A dashboard header and project information.
- KPI summary cards.
- Monthly sales and performance charts.
- Category, regional, and payment analysis charts.
- Customer and revenue distribution visualizations.
- Forecasting and model-evaluation visualizations.
- Dataset profile and analysis overview.

The chart images currently embedded in the HTML are snapshots taken from the notebook outputs. They do not update automatically when the CSV or notebook results change. To refresh the dashboard charts, rerun the notebook, generate updated chart images, and replace the embedded chart images in `Index.html`.

---

## Project Folder Structure

Your folder may look similar to this:

```text
E-commerce_Dataset_web_Acapulco_Manansala_Cruz/
│
├── .venv/                                  # Local Python virtual environment
├── .gitignore                              # Files and folders Git should ignore
│
├── dashboard_data/                         # Exported dashboard data, if generated
├── Data/
│   └── E-Commerce Sales Analytics.csv      # Original dataset
│
├── Image/                                  # Project images, if used
├── images/                                 # Website or analysis images, if used
│
├── e-commerce-analytics-eda-ml-forecast-fixed-v2.ipynb
│                                           # Python analysis notebook
│
├── Index.html                              # Website dashboard
└── README.md                               # Project documentation
```

Folder and notebook names may differ depending on the names used on your computer. Keep the CSV filename and its location consistent with the path configured in the notebook.

---

## Requirements

- Python 3
- Visual Studio Code (VS Code), or another Jupyter-compatible environment
- Jupyter Notebook support in VS Code
- Python packages imported by the notebook
- A web browser such as Google Chrome
- Git and a GitHub account (for publishing the project)

Install the packages required by the notebook. For example, if the notebook imports these libraries and they are not installed:

```bash
python -m pip install pandas numpy matplotlib seaborn scikit-learn statsmodels
```

Install only the packages that the notebook actually uses. If a library is missing when you run a cell, install that library in the active Python environment.

---

## How to Run the Python Notebook

1. Open the project folder in VS Code.
2. Make sure the CSV dataset is in the `Data` folder.
3. Open the `.ipynb` notebook.
4. Select the Python environment or kernel you want to use.
5. Confirm that the notebook's dataset path points to the CSV file on your computer.
6. Run the notebook cells in order, preferably using **Run All**.
7. Check that the cells complete without errors and that the charts and analysis outputs appear.

### Dataset path

The notebook should read the CSV using a Python variable containing the path, for example:

```python
df = pd.read_csv(dataset_path)
```

Do not put quotation marks around `dataset_path` in this statement. Writing `pd.read_csv('dataset_path')` makes Python search for a file literally named `dataset_path`.

If the notebook cannot find the CSV, check:

- The CSV file is named `E-Commerce Sales Analytics.csv`.
- The file is inside the expected `Data` folder.
- The path-detection code points to the correct folder.
- The notebook is running from the project directory you expect.

---

## How to Open the Website Locally

1. Open the project folder in VS Code.
2. Find `Index.html` in the Explorer.
3. Open the file in VS Code.
4. Save it with `Ctrl + S`.
5. Open it in a browser:
   - Double-click `Index.html` in File Explorer, or
   - Right-click the file in VS Code and choose **Open with Live Server** if the Live Server extension is installed.

The current dashboard is a static HTML page. It does not run the Python notebook in the browser.

---

## How the Project Works

```text
Kaggle CSV dataset
        |
        v
Python Jupyter Notebook
        |
        +--> Data loading and cleaning
        |
        +--> Exploratory data analysis
        |
        +--> KPI calculations and summaries
        |
        +--> Forecasting and model evaluation
        |
        +--> Charts and visualizations
                    |
                    v
             Index.html dashboard
                    |
                    v
             Website in a browser
```

Python performs the data processing and analysis. The HTML page presents selected results and visualizations.

---

## Git and `.gitignore`

A `.gitignore` file tells Git which files and folders should not be included in commits.

Create a file named exactly `.gitignore` in the root of the project folder. A suggested starting point is:

```gitignore
# Python virtual environments
.venv/
venv/
env/

# Python cache
__pycache__/
*.py[cod]

# Jupyter temporary files
.ipynb_checkpoints/

# VS Code workspace settings
.vscode/

# Operating system files
.DS_Store
Thumbs.db

# Temporary and log files
*.tmp
*.log
```

The `.gitignore` file does not remove files already tracked by Git. It only prevents untracked matching files from being added in future commits.

Keep `Index.html` in the repository. Keep any chart or data files that the website needs. If you decide to exclude the original CSV, make sure the notebook and dashboard do not depend on that CSV being available to website visitors.

---

## Publish the Website with GitHub Pages

1. Create a GitHub repository for the project.
2. Add the project files you intend to publish.
3. Commit and push the files to GitHub.
4. Open the repository on GitHub.
5. Go to **Settings → Pages**.
6. Under the build and deployment settings, choose **Deploy from a branch**.
7. Select the branch containing your website (commonly `main`) and the project root (`/`).
8. Save the settings and wait for GitHub Pages to publish the site.
9. Open the website URL shown in the Pages settings.

Make sure the homepage file is named `index.html` in lowercase if GitHub Pages does not recognize `Index.html` as the default homepage. If necessary, rename it to `index.html` and update any references to the filename.

---

## Important Notes and Limitations

- The website is a static page. It cannot execute Python or automatically read a local CSV file.
- The charts embedded in the current HTML are static snapshots. They will not refresh by themselves when the dataset changes.
- The `dashboard_data` folder is useful for exported results, but the current page does not automatically load files from it.
- Do not upload your `.venv` folder to GitHub.
- Check dataset licensing and usage conditions before publishing the raw CSV.
- If you publish the dashboard publicly, only include data that you are permitted to share.

---

## Project Goal

The goal of this project is to use an e-commerce dataset to examine sales performance, customer and product patterns, and predictive-analysis results, then communicate the findings through a clear and accessible web dashboard.

**Tools used:** Python, Jupyter Notebook, pandas, data-visualization and machine-learning libraries used by the notebook, HTML, VS Code, Git, and GitHub Pages.
