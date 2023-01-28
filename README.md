# ATitanicSuccess
Repository for the AutoIce challenge: [AutoIce](https://platform.ai4eo.eu/auto-ice)

## Team Members
- Sam Jackson
- Struan Bowie
- Dillon Leahy
- Grace Hopkins

## Datasets
Note that you need to download these separately from the repository. Repository contains a gitignore to avoid downloading 250GB of data.

You do not NEED all of this data. If you want to try any modelling, you will require the Ready-To-Train Training data (~56GB).

Any testing will only require the Ready-To-Train Test data (~3GB).


- [Raw Training](https://data.dtu.dk/articles/dataset/Raw_AI4Arctic_Sea_Ice_Challenge_Dataset/21284967?backTo=/collections/AI4Arctic_Sea_Ice_Challenge_Dataset/6244065)
- [Ready-To-Train Training](https://data.dtu.dk/articles/dataset/Ready-To-Train_AI4Arctic_Sea_Ice_Challenge_Dataset/21316608?backTo=/collections/AI4Arctic_Sea_Ice_Challenge_Dataset/6244065)
- [Raw Test](https://data.dtu.dk/articles/dataset/Raw_AI4Arctic_Sea_Ice_Challenge_Test_Dataset/21762848?backTo=/collections/AI4Arctic_Sea_Ice_Challenge_Dataset/6244065)
- [Ready-To-Train Test](https://data.dtu.dk/articles/dataset/Ready-To-Train_AI4Arctic_Sea_Ice_Challenge_Test_Dataset/21762830?backTo=/collections/AI4Arctic_Sea_Ice_Challenge_Dataset/6244065)

## Setting Up

Downloading this Git repository should get you set-up for the most part. To save difficulty with version-matching, I have included an environment.yml.
Given that we all use anaconda, we will make an anaconda environment and load the version requirements from the YAML file. 

To get started, open up your anaconda prompt in the same location as this git repository and use the command:

`conda env create --name <envname> --file=environment.yml`

Note that envname will dictate what you write to open the environment, I have used `autoice`.
You only have to run this command once!

From now on, to open the environment, you just have to type:

`conda activate <envname>`


## Task
Task is to use SAR (Synthetic Aperture Radar) data to map "accurate" sea ice maps.
Primarily, the challenge aims to improve retrieval of parameters such as:
- Sea Ice Concentration
- Stage of Development (of sea ice)
- Floe Size (form)

Formerly, ice charting methods are done manually through multi-sensor satellite imagery but more satellite imagery available so it is becoming more time-consuming and machine learning creeping in.

## Plan

Plan does not really exist yet.
Firstly, need to focus on loading the data and creating base code.

Typically, machine learning approach is a few steps:
1. Prepare data - what is useful? how is it useful? how do we collect it?
2. Decide on a model and throw data at the model - why is it the best model?
3. Empirically test hyperparameters on the model - just keep running model

## Testing Process & Due Date
Top 5 teams considered winning teams.
Due Date: 17/04/23 (17th April 2023)

Testing Algorithm is a formula, measuring each retrieved parameter separately. 
It is a measurement that we can implement locally and see how we would do.
(Note that we do not test our model on the same test data as them - they have their own)


| Parameter              | Metric | Weighting |
| ---------------------- | ------ | --------- |
| Sea Ice                | R2     | 2/5       |
| Stage of Development   | F1     | 2/5       |
| Floe Size              | F1     | 1/5       |

Formulas for metrics are found [here](https://platform.ai4eo.eu/auto-ice/data)


