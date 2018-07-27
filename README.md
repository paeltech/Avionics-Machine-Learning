# Avionics-Machine-Learning

The problem

An aircraft's onboard avionics computing system connects all of the systems on board a plane into one streamlined architecture. The data captured during flight by the avionics computing system is used to streamline aircraft performance and improve aircraft design.

Avionics
https://youtu.be/bSbReXT_bBs video about avionics

Press UP to enter the speed menu then use the UP and DOWN arrow keys to navigate the different speeds, then press ENTER to change to the selected speed.

Click on this button to mute or unmute this video or press UP or DOWN buttons to increase or decrease volume level.
Maximum Volume.

A key component of the avionics system is the hard disk used to store data for subsequent inspection and analysis. Hard disks are often the first hardware component to fail and limit product life-cycles. Identifying hard disks that are likely to fail and need replacement is key to preventing data loss and ensuring systems remain online.

S.M.A.R.T. (Self-Monitoring, Analysis and Reporting Technology) is a monitoring system in hard disk drives and solid-state drives that measures indicators of drive reliability. The indicators measured by S.M.A.R.T can be used to identify hard disks that are likely to fail.

We would like to use S.M.A.R.T. data to predict a possible hard drive failure in an avionics computing system. We then can deploy software running on the host system to copy critical data to another storage device, preventing data loss, and the failing drive can be replaced.

S.M.A.R.T
https://youtu.be/YNGUP1t8MYA video about smart

Press UP to enter the speed menu then use the UP and DOWN arrow keys to navigate the different speeds, then press ENTER to change to the selected speed.

Click on this button to mute or unmute this video or press UP or DOWN buttons to increase or decrease volume level.
Maximum Volume.
The data

Our hard disk data includes basic drive information along with the S.M.A.R.T. statistics reported by each drive. The daily snapshot of one drive is one record or row of data. We have data from the period covering January to December 2016. When a drive fails, the 'failure' column is set to 1 on the day of failure, and starting the day after, the drive will be removed from the dataset. Each day, new drives are also added. This means that total number of drives each day may vary.

The first row of the each file contains the column names, the remaining rows are the actual data. The columns are as follows:

Date – The date of the record in yyyy-mm-dd format

Serial Number – The manufacturer-assigned serial number of the drive

Model – The manufacturer-assigned model number of the drive

Capacity – The drive capacity in bytes

Failure – Contains a “0” if the drive was OK and “1” if the drive failed that day

2016 SMART Stats – 80 columns of data, that are the values for 40 different SMART stats as reported by the given drive
Your challenge

You will need to read, clean and fit models to the data. You will be asked to fit machine learning models to predict if a drive will fail. Using this model you will then be asked to make some recommendations for maintaining data integrity in an avionics computing system
Assessment flow

1. Import and clean data

2. Inspect and visualize the data

3. Feature engineering

4. Model fitting

5. Model evaluation

6. Produce recommendations

The assessment is split by these tasks
Submission

Launch the virtual labs and open the notebook

ML_summative_submission.ipynb

in the folder

ML 20 Summative

when you have completed the assignment, save the final notebook as 

ML_summative_submission_complete.ipynb

and push it to the github classroom

Each task in the notebook has it's own heading eg. Task 1: Import and clean data. Insert all your code related to that task in cells below. When you are done with that task move onto the next until you have complete all the tasks
Task descriptions

Here is some more detail on what we expect for each task

Task 1 Import and clean data

As always the first step is to import the libraries you will need for this exercise, along with the standard libaries for data manipulation and plotting, you will need to import machine learning libraries too. Once we have the libraries we need imported, we can import our data. The raw data file  for this exercise is

ml_summative_raw.csv

and can be found in the ML_summative folder

Some of our columns have lots of missing data and NA values. You will need to clean this data by dropping some rows or replacing NA's. Once you are finished your data should be clean and ready to use. i.e. no missing data, column are in the correct format.

Task 2 Inspect and visualize the data

Before we start any analysis it is important to understand the structure of the data we are working with. What is the range of each variable, how is it distributed, are there outliers, show the variables are related etc. Produce some plots that help you to understand the structure of the S.M.A.R.T variables

Task 3 Feature engineering

Based on what you learnt about your data through your visualizations, you might want to manipulate it somehow. Perhaps you want to drop some outliers, or remove a highly correlated variable, maybe you want to rescale data with a strange distribution. Feature engineering is the most creative part of machine learning. There is no definitively right or wrong answer. But coming up with clever variables can make you final model more accurate. Try to come up some new variables. Ideas include using the date somehow.

Task 4 Model fitting

The meat and potatoes of the exercise - fitting models. You will need to perform a few standard steps first. This will include, but not be limited to:  encodeing categorical variables/factors , defining predictors and response variables. splitting data to evaluate model fit later.

Once you have finished these prep steps, you will have to choose an appropriate model type to fit to these data. You are welcome to try multiple models, or combine multiple models. Whatever works best, it's up to you. But remember, not all models are appropriate and some are more accurate than others

Task 5 Model evaluation

How good is your model? Produce some metrics or visuals that give a measure of how well the model performs

Task 6 Produce recommendations

Well done, by now you have an advanced model capable of making accurate predictions on new data. 

We just received the latest SMART statistics from hard drives operating the avionics systems on a fleet of aircraft. You can find the data at

ml_summative_predict.csv

in the ML_summative folder

All the drives are currently working, but we don't want to take any risks. We need to replace all the drives that are at risk of failing. Use your model to make predictions on this new data. List the serial numbers of the 5 hard drives most likely to fail
