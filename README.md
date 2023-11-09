# Spark NLP for Text Manipulation

## Problem Statement
Every day, a massive amount of text information is produced. Sometimes, we cannot afford to read all the articles we want because of time constraint. Also, we sometimes want to extract certain information that is not possible through a simple googling. In this project, we will attempt to build a text summarization model and an information extraction model to help us obtain information efficiently.

## Overview of Steps
1.	Install required software
2.	Obtain the data (“All the news” from Kaggle) and remove null values
3.	Explore the data and create visualization to understand data
4.	Create a random subset of data for the project
5.	Clean the data (remove multiples spaces and other dirty data)
6.	Create a summarization model using Google T5 (Text-to-Text Transfer Transformer)
7.	Create an information extraction model using RegexMatcher
8.	Examine the results from the models

## Big Dataset
“All the news” dataset from Kaggle (https://www.kaggle.com/datasets/snapcrack/all-the-news)
File: articles1.csv
Size: 203.54 MB  |  Sample size: 12.6 MB  |  Format: csv

## Hardware
Ubuntu 22.04.2 LTS 64-bit on VMware 17 Player, 
Intel i7-10750H CPU, 16GB RAM

## Software
Python 3.10.6, PySpark 3.3.1, Java 8 (IMPORTANT)

## Lessons Learned and Pros/Cons
Although T5-small generated summaries, the results are not good enough to be actually useful. T5-base generated better summaries, but because of memory issue, other transformers such as Bart could not be successfully used in this project. We also successfully extracted information using RegexMatcher, but with more advanced methods and more time, we can create a more useful models.
