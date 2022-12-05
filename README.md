# BrainHack Nordic 2022 - DataLad Workshop

Welcome to the code and content repository of the hands-on workshop: ***Research Data Management with [DataLad](https://www.datalad.org/)***, part of the TrainTrack of the [BrainHack Nordic 2022](https://ohbm.github.io/hackathon2021/traintrack/) event.

### Presenter:
[Stephan Heunis](https://jsheunis.github.io/)
- Research Software Engineer at the [Psychoinformatics lab](https://www.psychoinformatics.de/),
Institute of Neuroscience and Medicine, Brain &amp; Behavior (INM-7), Germany


## Summary

Learn how to use the free and open source tool [DataLad](https://www.datalad.org/) to do continuous Research Data Management throughout the lifecycle of a research project. Topics include:

- DataLad datasets
- Version control
- Data consumption & transport
- Dataset nesting
- Computationally reproducible execution
- Publishing datasets
- Using published datasets

## Slides

Slides: [brainhack-nordic-datalad](https://jsheunis.github.io/brainhack-nordic-datalad)

The session follows the slides step by step.

The workshop's content is largely based on:
- The [Research Data Managment with DataLad](https://psychoinformatics-de.github.io/rdm-course/) course, developed by the Psychoinformatics team (with special thanks to [Michał Szczepanik](https://github.com/mslw))
- The [Introduction to DataLad for Yale](https://handbook.datalad.org/en/latest/code_from_chapters/yale.html) workshop, by [Adina Wagner](https://github.com/adswa)


## Cloud-compute environment

The workshop will be done in the browser on a cloud server with JupyterHub:
[https://datalad-hub.inm7.de](https://datalad-hub.inm7.de)

This server has been set up prior to the start of the workshop. It has `datalad`,
`datalad-container`, `singularity`, and all other internal dependencies pre-installed.

All you have to do is log in to the server (at the start of the workshop) and start using it:
- Log in using the email address with which you registered for the brainhack
- Select a password when logging in for the first time; remember it!

We will then do the workshop steps via the terminal.


## Local installation (not required)

For ease of use and to minimise delays, we suggest you use the provided cloud-compute envoironment.

However, if you are confident that you can set up your machine with DataLad successfully, you can run the workshop on your own laptop.

#### Installation instructions

1. Install `git`, `git-annex` and `datalad`: [select the appropriate installation route](https://www.datalad.org/#install) for your setup.
2. Instal the extension `datalad-container`: `pip install datalad-container`
3. Install `singulariy`: https://docs.sylabs.io/guides/latest/admin-guide/installation.html



## Scenario: the life of digital objects

Alice is a PhD student.

She works on a fairly typical research project: neuroimaging data collection and processing.
- The exact kind of data is actually not **that** relevant
- From the first sample to the final result: it is a cumulative process

When working locally, Alice likes to have an automated record of:
- when a given file was last changed
- where it came from
- what input files were used to generate a given output
- why some things were done.

Even without sharing, all of these records are essential for her future self, because:
- the project is exploratory; there are often large changes to her analysis scripts
- she enjoys the comfort of being able to return to a previously recorded state

All of the above is ***local* version control**.

Alice's work not confined to a single computer. She uses:
- laptop
- desktop
- remote server

She therefore needs and has an automatic and efficient way to synchronise data.

Also, some of the data are collected and analysed by colleagues from another team:
- they all work together on synchronized data with centralized storage
- their system preserves the origin & authorship of changes
- they can easily combine simultaneous contributions without conflicts

This is ***distributed* version control**.

When Alice needs to work on a subset of data at a given time:
- all her files are kept on a server
- only a few files are rotated into and out of the laptop/desktop/server as/when she needs them

At the end of the projet, Alice needs to publish all project data:
- this could be raw data or outputs or both
- she needs to publish data completely or selectively, depending on data use restrictions

All of the activities and processes mentioned above are typical data management issues which we will touch upon during this workshop, using DataLad as our primary tool.