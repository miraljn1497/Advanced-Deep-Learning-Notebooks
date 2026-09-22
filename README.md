# Advanced-Deep-Learning-Notebooks
miraljn1497/Advanced-Deep-Learning-Notebooks

Notebook-based studies for exploring classification models and model explanations. The notebooks present outputs as tables, printed text, figures, and model displays for readers studying decision trees, linear SVM classification, and SHAP explanations.

Included studies

Decision tree classification

The decision tree study uses the Iris dataset and includes:





A baseline decision tree with test evaluation



A two-feature decision-boundary view



A five-fold parameter search over maximum depth, split size, leaf size, and the Gini or entropy criterion



Interpretation of the selected tree



A later numeric pipeline using scaled Iris measurements

The parameter search selected a Gini tree with maximum depth 3, minimum leaf size 1, and minimum split size 2. Its captured best cross-validation accuracy was 0.9733333333333334.

The later numeric pipeline used an entropy tree with depth 4, minimum split size 5, and minimum leaf size 1. Its captured accuracies were:





Training: 0.983



Test: 0.967



Five-fold cross-validation: 0.917

These results come from separate branches and should not be interpreted as one continuous improvement sequence.

Linear SVM classification

The SVM workflow uses cleaned Penguins data with three classes:





Adelie



Chinstrap



Gentoo

It selects bill length, bill depth, flipper length, and body mass as measurements, removes incomplete rows, and creates a species-colored pair plot. The classification workflow uses a stratified split with 20% held out and random_state=42. The measurements are standardized using the training data before transforming the test data.

A linear SVM with C=1.0 is fitted and evaluated with accuracy, a confusion matrix, precision, recall, and F1 scores. The captured test set contains 67 samples, with displayed accuracy of 1.000 and no displayed off-diagonal confusion-matrix errors.

The notebook contains repeated Iris references, but the later preparation, training, prediction, and evaluation use Penguins data.

Combined SHAP explanations

The combined explanation study uses the Iris dataset to generate SHAP outputs for two fixed models:





Logistic Regression using standardized features



Random Forest using the original, unstandardized features

The study reserves 20% of the data for testing while preserving class proportions. It produces SHAP values and visual displays for the fitted models.

These figures are explanation outputs only. The study does not establish hyperparameter tuning, validated predictive performance, or which model performs better. The captured Logistic Regression figure is not verified as a Logistic Regression explanation, and its SHAP feature-perturbation setting is reported as deprecated; reproducing that explanation may require updating the SHAP setup.

Working with the notebooks

Results are available in notebook cells as captured outputs. Inspect the tables, printed text, figures, and model displays directly in the notebooks.

Notebook outputs should be treated as captured results rather than a persistent or callable result service:





A later run is not guaranteed to produce the same output.



Outputs are not separately addressable artifacts.



Other applications cannot request the displayed results externally.



There is no separate repeatable application launch procedure.



To produce or inspect a new result, work from the notebooks themselves.

Interpreting the studies

Keep each result tied to its documented dataset, preprocessing path, model configuration, and workflow branch. In particular:





Treat the decision-tree results as Iris results; the notebook’s Penguins-oriented prose and categorical-feature improvement claim are unresolved narrative, not results from the inspected branches.



Treat the SVM classification workflow as Penguins-based despite the notebook’s earlier Iris dataframe and repeated Iris references.



Treat SHAP figures as model explanations, not predictive-performance benchmarks.
