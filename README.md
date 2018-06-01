# Data Acquisition

This section imports data on 23 spieces of mushrooms, including the attributes listed below and the target that classifies the mushrooms as edible or poisonous.
The data and documentation were downloaded from [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/mushroom).

The subsequent analysis will reduce dimensionality of the attributes to two principal components and evaluate performance of several classifiers, including Logistic Regression, KNN, Decision Tree, Random Forest, SVC, Naive Bayes and Neural Network, in predicting whether a mushroom with particular attributes is edible or not.

The next step, which describes data cleaning and processing, is described [here](link).

Number of Attributes: 22 (all nominally valued)

```
Attribute Information: (classes: edible=e, poisonous=p)<br/>
     1. cap-shape:                bell=b,conical=c,convex=x,flat=f,<br/>
                                  knobbed=k,sunken=s<br/>
     2. cap-surface:              fibrous=f,grooves=g,scaly=y,smooth=s<br/>
     3. cap-color:                brown=n,buff=b,cinnamon=c,gray=g,green=r,<br/>
                                  pink=p,purple=u,red=e,white=w,yellow=y<br/>
     4. bruises?:                 bruises=t,no=f<br/>
     5. odor:                     almond=a,anise=l,creosote=c,fishy=y,foul=f,<br/>
                                  musty=m,none=n,pungent=p,spicy=s<br/>
     6. gill-attachment:          attached=a,descending=d,free=f,notched=n<br/>
     7. gill-spacing:             close=c,crowded=w,distant=d<br/>
     8. gill-size:                broad=b,narrow=n<br/>
     9. gill-color:               black=k,brown=n,buff=b,chocolate=h,gray=g,<br/>
                                  green=r,orange=o,pink=p,purple=u,red=e,<br/>
                                  white=w,yellow=y<br/>
    10. stalk-shape:              enlarging=e,tapering=t<br/>
    11. stalk-root:               bulbous=b,club=c,cup=u,equal=e,<br/>
                                  rhizomorphs=z,rooted=r,missing=?<br/>
    12. stalk-surface-above-ring: fibrous=f,scaly=y,silky=k,smooth=s<br/>
    13. stalk-surface-below-ring: fibrous=f,scaly=y,silky=k,smooth=s<br/>
    14. stalk-color-above-ring:   brown=n,buff=b,cinnamon=c,gray=g,orange=o,<br/>
                                  pink=p,red=e,white=w,yellow=y<br/>
    15. stalk-color-below-ring:   brown=n,buff=b,cinnamon=c,gray=g,orange=o,<br/>
                                  pink=p,red=e,white=w,yellow=y<br/>
    16. veil-type:                partial=p,universal=u<br/>
    17. veil-color:               brown=n,orange=o,white=w,yellow=y<br/>
    18. ring-number:              none=n,one=o,two=t<br/>
    19. ring-type:                cobwebby=c,evanescent=e,flaring=f,large=l,<br/>
                                  none=n,pendant=p,sheathing=s,zone=z<br/>
    20. spore-print-color:        black=k,brown=n,buff=b,chocolate=h,green=r,<br/>
                                  orange=o,purple=u,white=w,yellow=y<br/>
    21. population:               abundant=a,clustered=c,numerous=n,<br/>
                                  scattered=s,several=v,solitary=y<br/>
    22. habitat:                  grasses=g,leaves=l,meadows=m,paths=p,<br/>
                                  urban=u,waste=w,woods=d<br/>
```
The following function reads the raw data:

```
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
from sklearn.model_selection import train_test_split
from sklearn.decomposition import PCA
import pylab

def read_mushroom_data():
    
    df = pd.read_csv('/Users/eagronin/Documents/Data Science/Portfolio/Project Data/mushrooms.csv')
    
    return df
``` 

Next step: [Data Preparation](link)
