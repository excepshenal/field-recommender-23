# field-recommender-23
Built a recommender system for Field Intelligence, Inc.'s pharmaceutical e-commerce platform during 2023 summer internship.

All scripts with the same number subscript perform the same dataset cleaning and output formatting (just different computational models). The corresponding (private) dataset is listed at the top of the documentation.

Recommended scripts:
* _5 (not _6, which misleadingly displays “sl_sold”) for the **count** (not revenue) approach, and can be used with the 0809/0811/0813 query template.
* _7 for the **revenue** approach, and can be used with the 0809/0811/0813 query template.
* See also aggregator script.

Results and evaluation (and runtimes):
* There’s no clear winner yet among the models, despite hints of LightGCN overfitting, but it seemed from the pharmacist team that LightGCN still had potential.
* BPR is by far the fastest. BiVAE and LightGCN are slower in different domains.
* nDCG / rnDCG are weak measures for model performance, though they are the best we have. They can only really tell you if the model is terrible (if nDCG or rnDCG < around 0.2) or if the model is way overfitting (if rnDCG > around 0.7).
