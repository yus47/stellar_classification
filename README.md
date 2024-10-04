# Stellar Classification Model

[Link to Dataset](https://www.kaggle.com/datasets/fedesoriano/stellar-classification-dataset-sdss17)

## Background
Stellar classification, a fundamental aspect of astronomy, categorizes stars based on their spectral characteristics. This system extends to galaxies and quasars, forming a crucial framework for astronomical understanding. Early star catalogs, revealing their distribution across the sky, led to the realization of our own galaxy and the existence of numerous others, including Andromeda. As telescopes advanced, galaxies were systematically surveyed, further expanding this knowledge.

**Classifying stellar objects provides numerous benefits, including:**

* **Understanding stellar evolution:** By grouping stars based on their spectral properties, astronomers can trace the life cycles of stars, from their formation to their eventual demise.
* **Determining stellar composition:** Spectral analysis reveals the elements present in a star's atmosphere, providing insights into its chemical makeup and evolutionary history.
* **Measuring distances:** Certain spectral characteristics can be used to estimate the distance to stars and galaxies, enabling astronomers to map the large-scale structure of the universe.
* **Identifying unique objects:** Unusual spectral patterns can highlight peculiar stars or galaxies with unusual properties, such as binary systems, neutron stars, or active galactic nuclei.

This dataset aims to classify stars, galaxies, and quasars based on their spectral properties, contributing to our ongoing exploration of the universe and deepening our understanding of its fundamental building blocks.

## Data Dictionary
While the original dataset has many columns, most of them were columns for IDs, whether it was object ID, photo ID, camera ID, or device ID. There were only six columns used to build the model, that are:
|Column|Data Type|Definition|
|---|---|---|
|`alpha`|numerical|Right Ascension angle (at J2000 epoch)|
|`delta`|numerical|Declination angle (at J2000 epoch)|
|`u`|numerical|Ultraviolet filter in the photometric system|
|`g`|numerical|Green filter in the photometric system|
|`r`|numerical|Red filter in the photometric system|
|`i`|numerical|Near Infrared filter in the photometric system|
|`z`|numerical|Infrared filter in the photometric system|
|`redshift`|numerical|redshift value based on the increase in wavelength|
|**`class`**|Categorical / Target|object class (galaxy coded 0, quasar coded 1, or star coded 2)|

## Model Performance
Using catboost algorithm with one-vs-one classifier and SMOTE-Tomek resampler, this model has 97.7% accuracy accross three class of galaxy, quasar, or star. This model was made using Python version 3.11.9.
