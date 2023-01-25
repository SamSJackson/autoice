# ATitanicSuccess [AutoIce]
Repository for the AutoIce challenge: [AutoIce](https://platform.ai4eo.eu/auto-ice)

## Team Members
- Sam Jackson
- Struan Bowie
- Dillon Leahy
- Grace Hopkins

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

Formulas are found [here](https://platform.ai4eo.eu/auto-ice/data)


