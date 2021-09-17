# Github Link
https://github.com/yasiruRathnayaka97/ML-Assignment/

# ML-Assignment
This repository contains the codes submitted to the <b>Pump it Up: Data Mining the Water Table</b> competition.
<br>The submissions I was able to get the highest accuracy is available in the repository.A brief discription of the approach followed in the best submission ([cat_boost_v6](CatBoost_V6.ipynb)) is explained below.

## Preprocessing
1. Removed the duplicates in training data.
2. Following processings steps were done to both train and test datasets.
   * Missing value imputation.
     * ```funder```- replace by mode of funder grouped by region and district code wise.
     * ```installer```- replace by mode of installer grouped by funder wise.
     * ```subvillage``` - replace by mode of subvillages grouped by ward wise.
     * ```public_meeting``` - replace by mode of public_meeting grouped by ward wise.
     * ```scheme managment``` - replace by mode of scheme managment grouped by funder wise.
     * ```scheme name``` -replace by mode of scheme name grouped by funder wise.
     * ```permit``` -replace by mode of permit grouped by funder wise.
   * All the ```gps_height``` less than 0 convert to values higher than 0.
   * Log normalize ```population```, ```amount_tsh``` and ```gps_height```.
   * Alter ```funder``` and ```installer``` columns.

## Feature Engineering
1. ```date_recorded``` column was seperated into 3 featuers, ```date_recorded_year``` ,```date_recorded_month``` and ```date_recorded_day``` by extracting year, month and day from the values in ```date_recorded```.
2. A new feature ```recorded_and_construction_year_differnce```  column was created by taking difference of  ```date_recorded_year``` and ```construction_year```.
3. Log normalize ```recorded_and_construction_year_differnce```.
4. Remove columns ```date_recorded_year``` , ```date_recorded_month```, ```date_recorded_day``` and ```date_recorded```.



## Proof of submission
### Final rank

![Screenshot (38)](https://user-images.githubusercontent.com/57071700/133805136-6d2ae2bf-93ce-409a-b777-69b3939cdafa.png)

### submissions

![Screenshot (37)](https://user-images.githubusercontent.com/57071700/133805153-84c5e2af-c4da-4925-a497-b12f991d749e.png)

