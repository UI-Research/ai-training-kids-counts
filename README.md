# AI Training Session for KIDS COUNT Data Institute

## Prep Work Instructions
The following steps are needed to be able to run the exercise in the Quarto notebook `ai-exercise-session-plan.qmd` interactively:

1. Install R and RStudio on your computer if you haven't already. You can refer to the instructions from my colleague Aaron Williams contained in `installing-R.md`.

2. Install Quarto from the official site: https://quarto.org/docs/get-started/

3. Install the necessary packages in R. You can do this by running the following commands in your RStudio console:

```
install.packages(c("tidyverse", "tidycensus", "tigris", "sf", "viridis", "scales"))
```
4. Download these materials to run for the exercise. If you are a Git and GitHub user, you can clone the repository using the following command in your terminal:
```
git clone https://github.com/UI-Research/ai-training-kids-counts.git
```

If not, you can click the green "Code" button on the GitHub repository page and select "Download ZIP". After downloading, save the contents to a folder on your computer.

5. Open the `ai-training-kids-count.Rproj` file in a new RStudio session. You're ready to go!

## Available Examples

### Main Exercise (Arkansas Tract-Level Analysis)
- **File:** `ai-exercise-session-plan.qmd`
- **Focus:** Documentation, debugging, and visualization of Arkansas child poverty data
- **Level:** Beginner to Intermediate

### NEW: County-Level Analysis (R + Python)
- **Files:** `ai-exercise-new-example.qmd` (R) and `ai-exercise-new-example.ipynb` (Python)
- **Focus:** Human+AI workflow for multi-state county child poverty analysis
- **Level:** Intermediate
- **Duration:** ~20 minutes
- **Key Features:**
  - Step-by-step human+AI collaboration
  - Copy-paste prompts for efficiency
  - Risks & uncertainty guidance
  - Equivalent R and Python implementations

#### Running the New Examples:

**R Version:**
```r
# In RStudio, open ai-exercise-new-example.qmd and run chunks
# Or extract and run as script:
knitr::purl("ai-exercise-new-example.qmd")
source("ai-exercise-new-example.R")
```

**Python Version:**
```bash
# Install required packages:
pip install pandas matplotlib seaborn

# Run in Jupyter:
jupyter notebook ai-exercise-new-example.ipynb

# Or run all cells:
jupyter nbconvert --execute ai-exercise-new-example.ipynb
```

## Solutions and Reference Materials
- **File:** `ai-exercise-session-plan-solutions.qmd`
- **Contains:** Complete solutions for all exercises, including the new county-level example
- **Use:** Reference implementation and troubleshooting guide




