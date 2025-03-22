# Wine Quality Data Analysis Dashboard

This repository contains an interactive data visualization dashboard for analyzing wine quality based on various chemical properties. The dashboard was created as part of SIADS 521 - Data Visualization coursework (Assignmnet 03).

## Overview

This project demonstrates the creation of an interactive dashboard using Panel, HoloViews, and other Python libraries from the HoloViz ecosystem. The dashboard allows users to explore relationships between different chemical properties of wine and their impact on quality ratings.

## Features

- **Multiple Visualization Types**: Correlation heatmaps, histograms, box plots, scatter plots, and regression lines
- **Interactive Elements**: Variable selection, plot type toggling, hover information
- **Tab-based Navigation**: Organized into Overview, Univariate Analysis, and Multivariate Analysis sections
- **Responsive Design**: Adapts to different screen sizes

## Dataset

This dashboard uses the Wine Quality dataset from Kaggle, which contains various chemical properties of wines along with quality ratings. The dataset includes the following features:

- Fixed Acidity
- Volatile Acidity
- Citric Acid
- Residual Sugar
- Chlorides
- Free Sulfur Dioxide
- Total Sulfur Dioxide
- Density
- pH
- Sulphates
- Alcohol
- Quality (target variable)

## Installation

### Requirements

- Python 3.6+
- Panel
- HoloViews
- hvPlot
- Bokeh
- Pandas
- NumPy
- SciPy

### Setup Instructions

1. Clone this repository:
   ```
   git clone https://github.com/TashiSoldin/wine-quality-dashboard.git
   cd wine-quality-dashboard
   ```

2. Create a virtual environment (recommended):
   ```
   python -m venv .env
   source .env/bin/activate  # On Windows, use: .env\Scripts\activate
   ```

3. Install the required dependencies:
   ```
   pip install panel holoviews hvplot bokeh pandas numpy scipy
   ```
   
   Or using conda:
   ```
   conda install -c pyviz panel holoviews hvplot
   conda install -c anaconda bokeh pandas numpy scipy
   ```

4. Launch Jupyter Notebook:
   ```
   jupyter notebook
   ```

5. Open `Dashboard.ipynb` and run all cells.

## Usage

The dashboard is organized into three main tabs:

1. **Overview**: Provides a statistical summary of the dataset and a correlation heatmap to identify relationships between variables.

2. **Univariate Analysis**: Allows exploration of individual variable distributions through histograms or box plots.

3. **Multivariate Analysis**: Enables investigation of relationships between any two selected variables using scatter plots and regression lines.

## Dashboard Walkthrough
The screenshots of the different tabs can be accessed in the Dashboard Screenshots folder

### Overview Tab
The Overview tab provides a high-level summary of the data:
- Data statistical summary table with key metrics
- Correlation heatmap showing relationships between all variables

![Dashboard View 1](https://github.com/user-attachments/assets/ed91f78f-1807-466f-b54c-14d2f36f3c95)

### Univariate Analysis Tab
The Univariate Analysis tab allows for exploration of individual variable distributions:
- Toggle between histogram and box plot views
- View the distribution of all variables at once

![Dashboard View 2a](https://github.com/user-attachments/assets/f4feeb2a-4779-46bf-8592-83dd62092030)

### Multivariate Analysis Tab
The Multivariate Analysis tab enables exploration of relationships between variables:
- Select any two variables to analyze their relationship
- View both scatter plot and regression line for the selected variables
- Hover over plots to see detailed information

![Dashboard View 3](https://github.com/user-attachments/assets/d263abd7-e238-47aa-b730-16a35c4f2dcc)

## Running the Dashboard

To launch the dashboard server:

```python
dashboard.show()
```

This will start a local server and provide a URL (typically `http://localhost:XXXX`) where you can access the dashboard in your web browser.

## Project Structure

- `Dashboard.ipynb`: Jupyter notebook containing the dashboard code and documentation
- `WineQT.csv`: Wine Quality dataset used in the dashboard
- `screenshots/`: Folder containing dashboard screenshots
- `README.md`: This file

## Troubleshooting

If you encounter issues when running the dashboard:

1. **Module not found errors**: Ensure all required packages are installed
   ```
   pip install panel holoviews hvplot bokeh pandas numpy scipy
   ```

2. **Visualization not showing**: Make sure the Panel extension is loaded
   ```python
   pn.extension('tabulator')
   ```

3. **Performance issues**: For large datasets, consider implementing data downsampling

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- Dataset source: [Wine Quality Dataset on Kaggle](https://www.kaggle.com/datasets/yasserh/wine-quality-dataset)
- Built with [Panel](https://panel.holoviz.org/) and the [HoloViz](https://holoviz.org/) ecosystem
