# Kepler Exoplanet Classifier

I made a machine learning project that looks at NASA Kepler exoplanet candidates and sorts them into three groups: **CONFIRMED** **CANDIDATE** and **FALSE POSITIVE**. I used the Kepler Objects of Interest dataset to do this. I tried out a few machine learning models and picked LightGBM because it worked the best. I also used SHAP to see how the model makes its predictions.

## Project Overview

The Kepler Space Telescope found thousands of exoplanets by looking at small dips in a stars brightness.. Not every signal is a real planet. Some are noise or other things happening in space.

In this project I built a machine learning pipeline to automatically sort these signals into three categories:

- CONFIRMED

- CANDIDATE

- FALSE POSITIVE

## Dataset

I used the NASA Kepler Objects of Interest dataset. The thing I was trying to predict was the `koi_disposition`. The dataset has a lot of information about the planets like:

- How it takes them to go around their star

- How long it takes them to pass in front of their star

- How much lighter the star gets when the planet passes in front

- How big the planet is

- How hot the planet is

- How much light the planet gets from its star

- How close the planet passes to the center of its star

- Lots of other Kepler features

## Machine Learning Pipeline

I did the following steps:

- Cleaned up the data

- Handled missing values

- Picked the important features

- Changed the labels into numbers

- Split the data into training and testing sets

- Used stratified 5 fold cross validation

- Compared models

- Adjusted the model settings

- Evaluated the final model

- Used SHAP to explain the predictions

## Models Compared

I tried out the following models:

- Random Forest

- XGBoost

- CatBoost

- LightGBM

LightGBM worked the best so I picked it as the final model.

## Explainability

I used SHAP to see how the model makes predictions. The explainability part includes:

- A SHAP Beeswarm Plot

- A SHAP Feature Importance plot

- A SHAP Waterfall Plot

- A SHAP Dependence Plot

## Project Structure

My project is set up like this:

```text

kepler-exoplanet-classifier/

│

├── README.md

├── LICENSE

├── requirements.txt

├── notebook.ipynb

├── report.pdf

│

└── images/

├── confusion_matrix.png

├── feature_importance.png

├── shap_beeswarm.png

├── shap_bar.png

├── shap_waterfall.png

└── shap_dependence.png

```

## Results

The final LightGBM model did a job on the test data and correctly classified most exoplanet candidates. It was really good, at finding ** POSITIVE** cases but it got confused between **CONFIRMED** and **CANDIDATE** cases because they are similar.

## What I Learned

From this project I learned how to:

- Clean up real world data

- Try out different machine learning models

- Use cross validation

- Adjust model settings

- Evaluate classification models

- Use SHAP to explain predictions

- Build a machine learning workflow

## Requirements

To run the project you need to install the required libraries:

```bash

pip install -r requirements.txt

```

## Running the Project

To run the project you need to:

Clone the repository:

```bash

git clone https://github.com/<your-username>/kepler-exoplanet-classifier.git

```

Move into the project directory:

```bash

cd kepler-exoplanet-classifier

```

Install dependencies:

```bash

pip install -r requirements.txt

```

Launch Jupyter Notebook:

```bash

jupyter notebook

```

Open `notebook.ipynb` and run all cells.

## License

This project is released under the MIT License.

## Acknowledgements

I want to thank:

- NASA Kepler Mission

- NASA Exoplanet Archive

- India High School Exoplanet Data Challenge

For helping me with this project.