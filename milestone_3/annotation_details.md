# Annotation Details

## 1. Links 

### 1.1 Intermediary Annotation Files

Our intermediary annotation files are present [here](https://github.ubc.ca/us45/COLX_523_group3/tree/master/src/data/annotations).

There are four sub folders in the `annotation` folder, one for each team member where each folder has the annotations done and reviewed by the team member (4 files in total)

Here are the links to the annotations done and reviewed by each team member :

1) Badr -

2) Oksana - https://github.ubc.ca/us45/COLX_523_group3/tree/master/src/data/annotations/oksana

3) Sneha - https://github.ubc.ca/us45/COLX_523_group3/tree/master/src/data/annotations/sneha

4) Utkarsh - https://github.ubc.ca/us45/COLX_523_group3/tree/master/src/data/annotations/utkarsh

### 1.2. Link to Final Annotation

The link to the final annotation file is here - 

## 2. Code

The code used to scrap the data and prepare it for annotating can be found [here](https://github.ubc.ca/us45/COLX_523_group3/blob/master/src/scraper.py)!

## 3. Discussion about the Annotation Process

The annotation process went quite smoothly, each of us managed to annotate around 25 documents in total and review 75 documents which were annotated by the other three team members. We used an open source data labeling tool called [label studio](https://labelstud.io) for tagging named entities in our corpus.

For calculating our inter annotator agreement score, we used F1 score as a metric. We merged all the 4 files in each team member's sub folder (One annotated file and three reviewed annotations) and calculated the matches based on the majority among the four us. for example, If one team member did no tag a Citation but the other three team members tagged it, then that particular tag will be considered as part of gold standard.

Steps we followed for the annotations :

1) Use the scraper to fetch the legal documents (.txt files) and divide them among the 4 us.

2) Change the extension of the .txt files to .html. (.html files are compatible in label studio)

3) Once we launch label-studio, we import all the files to be annotated which get uploaded on the interface.

4) We add all the entity labels as per our annotation guidelines before we start the annotation.

5) Once we finished annotation as per the guidelines, we export all the annotations as a single .json file.