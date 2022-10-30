# cs3244-pg26
CS3244 Group Project Repo for PG26

## How to contribute
**Important:** Please try to get familiar with Git and GitHub first (we'll be using it for the rest of our project)!

Here are several industry-standard steps you should be doing to contribute towards the project:
0. Pull the newest updates on `main` by using `git pull` on the branch. (optimally, do this daily or every other day)
1. Create your own branch that stems out from `main`.
   * Reminder to `git checkout` to the branch you just created! (preferably, use `git checkout -b <branch_name>` to create a new branch and checkout immediately to said branch)
2. Work on stuff **in your personal branch**.
   * Commit to your personal branch periodically to save your work history!
3. After you've finished, push the branch onto the remote (aka GitHub's servers) by using `git push`.
   * Note: GitHub may give you an error message on the first time you push a new branch by telling you to type in `git push --set-upstream origin <branch_name>`. To fix, just type in whatever they said onto the terminal!
4. **Important:** Make a pull request (aka a "PR") to the `main` branch and set @wilsonwid as reviewer!
   * Please also DM @wilsonwid on Telegram for faster responses!


## File organisation
The data that has been collected is in `.csv` format and organised into two major folders: `data_raw` and `data_processed`.

Aside from this, @hari-dharan has kindly added data of points of interest (i.e. locations of amenities) taken from OneMap's API. These points of interest include ATMs, bus stops, hawker centres, libraries, and other places that can influence a resale flat's value. Their complete list can be seen in the `data_raw` and `data_processed` folders, organised into different subfolders depending on their type.

As a guideline:
* `data_raw` contains all the raw data taken from either the OneMap API or from the HDB resale flat dataset.
* `data_processed` contains all the processed data taken from either of those locations

TL;DR: you should normally only use `data_processed` for all the analysis work that you do.

**Important note:**
* The 'main' data file that you should refer to is `engineered_data.csv`, which is under `data_processed/resale_flat_prices`.
  * There are still several categorical columns for this file, including `town`, `flat_type`, `flat_model`, and `address`. It would be good if you can integrate these into the final model, e.g. removing the `_ROOM` for each `flat_type` or one-hot encode the rows of `flat_model` (please search the term "one-hot-encoding" if you've never heard of it!). 
  * However, each of these columns have implicit numerical equivalents, such as `latitude` and `longitude` (or their `_rad` equivalents) for `town` and `address`, as well as `floor_area` for `flat_type`, and hence it might not actually affect the data that much!
  * `sale_date` can also be encoded based on its month so as to provide more clarify for the model.
  * The target for the regression is to accurately predict `psm`, which is the per-square-metre price of the resale flat.

## Current plans/things to do
* Cloning the repository into each of your local machines ("locals")
* Fiddling with your assigned models and getting familiar with the things you can do with them
