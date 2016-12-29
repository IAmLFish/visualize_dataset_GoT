# visualize_dataset_GoT
Contribution for ["How to Best Visualize a Dataset Easily" Siraj Raval](https://www.youtube.com/watch?v=yQsOFWqpjkE) on YouTube.

I also uploaded this version to kaggle:<br>
<https://www.kaggle.com/iamlfish/d/mylesoneill/game-of-thrones/feature-label-generation-exploration-and-tsne>

# First of all ...
... I do no guarantee for correctness or adequacy. With this project I was learning a bit more how to understand and use t-SNE.

# What I did
* Took a character based perspective on features
* Aimed to use summable/continuous features
* Analyzed commanders
  * Created new features (also together with the battles-data)
  * Created new labels from battle-data

## What you can use in `analysis.ipynb`:
* Exploratory analysis
* Plotting with different labels
* Filtering the mappedTSNE-data with `filterLabel` and `filterValue`
* Adding more battle related or character related features

## Future work suggestions
* Adding t-SNE features as additional features to original feature set `x` for further investigation/queries
* Extending `plotTSNE()` to allow labeling continuous valued labels `y` with colormaps 
* Using different plot tool
* Putting plots into subplots
* Making labels bigger

# Observations:
More described observations can be found in `analysis.ipynb`.

Here are some general insights.

## Observation 1:
`isPopular` seems to have correlations with `boolDeadRelations`.

![title](isPopular_edit.png)

## Observation 2:
Observation 1 seems to hold still.

However, we can see characters labeled with `wasCommander` are seperated from all others (which makes sense because they have way more  distinguishable features than "not-commanders"). 

![title](isPopular_extended.png)

## Observation 3:
Even here, observation 1 seems to hold still.

Characters labeled with `isPopular` also seem to have correlations with `hadMoreWinsThanLosses`

![title](isPopular_commanders_edit.png)
