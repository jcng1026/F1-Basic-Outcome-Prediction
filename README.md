# F1 Basic Outcome Prediction

This project uses Formula 1 race data to prepare a classification dataset and
compare machine-learning models for predicting race outcomes. The data
preparation and modeling workflows are provided as RapidMiner process files.

## Project contents

- `data_cleaning.rmp` joins and prepares the raw race, results, circuit,
  constructor, driver, and qualifying data.
- `F1_cleaned_classification_dataset.rmhdf5table` is the prepared dataset used
  by the classification workflows.
- `Decision_Tree_F1_Model.rmp`, `Logistic_Regression_F1_Model.rmp`,
  `Naive_Bayes.rmp`, and `Random_Forest.rmp` train and evaluate individual
  classifiers.
- `Algorithm_Comparison.rmp` combines model performance results for comparison.
- The `*_raw.rmhdf5table` files contain the source tables used for data
  preparation.

## Running the workflows

Open the `.rmp` files in RapidMiner Studio. The processes retrieve data from a
repository folder named `BDA_Assignment`; import the supplied `.rmhdf5table`
files there using their file names as repository entry names. Run
`data_cleaning.rmp` to prepare the classification dataset, then run the
individual model processes or `Algorithm_Comparison.rmp`. If using a different
repository location, update the Retrieve and Store operators in the processes
to match.
