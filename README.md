## Workshop: 10 March 2024 


### 1. Create supervised models and save to BigQuery
- using  bigframes.pandas and bigframes.ml
- Create + Evaluate
- Modify **01-CreateModelClassification-BigQuery.ipynb** 
- Create **2 versions of models** with different algorithms or different parameters 
- Model1: 6xxxxxx-01-CreateModel1.ipynb (+ print as 6xxxxxx-01-CreateModel1.pdf )
- Model2: 6xxxxxx-01-CreateModel2.ipynb (+ print as 6xxxxxx-01-CreateModel2.pdf)


### 2. Load models and use to predict new data 
- Modify **02-LoadModelBigQuery.ipynb**
- Model1: 6xxxxxx-02-LoadModel1.ipynb  (+ print as 6xxxxxx-02-LoadModel1.pdf)
- Model2: 6xxxxxx-02-LoadModel2.ipynb  (+ print as 6xxxxxx-02-LoadModel2.pdf)



### 3.  Write query model in BigQuery and run to view the predicted result. 

- Example 

```
SELECT
  *
FROM
  ML.PREDICT(MODEL `ds-on-gcp-411105.DemoSupervisedML.RF_predict_penguin_species`,
    (
    SELECT
      'Biscoe' AS island,
      50.5 AS culmen_length_mm,
      15.9 AS culmen_depth_mm,
      225.0 AS flipper_length_mm,
      5400.0 AS body_mass_g,
      'MALE' AS sex ) );

```


### 4. Write the table to compare the performance of the two versions of models.






