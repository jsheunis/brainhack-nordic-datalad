# BrainHack Nordic 2022 - DataLad Workshop

Welcome to the code and content repository of the hands-on workshop: ***Research Data Management with DataLad***, part of the TrainTrack of the [BrainHack Nordic 2022](https://ohbm.github.io/hackathon2021/traintrack/) event.

---
### Presenters:
[Stephan Heunis](https://github.com/jsheunis)

---

## Summary

Learn how to use the free and open source tool DataLad to do continuous Research Data Management throughout the lifecycle of a research project. Topics include:

- DataLad datasets
- Version control
- Data consumption & transport
- Dataset nesting
- Computationally reproducible execution
- Publishing datasets
- Using published datasets

## Slides

Slides: [brainhack-nordic-datalad](https://jsheunis.github.io/brainhack-nordic-datalad)

The sessions follows the slides step by step.

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

- Alice is a PhD student.
- She works on a fairly typical research project: data collection & and processing.
  - Exact kind of data not relevant for us
  - first sample → final result: cumulative process

#+REVEAL:split

- When working locally, Alice likes to have an automated record of:
  - when a given file was last changed
  - where it came from
  - what input files were used to generate a given output
  - why some things were done.
- Even without sharing, essential for her future self
- Project is exploratory: often large changes to her analysis scripts
- Enjoys comfort of being able to return to a previously recorded state

This is *local* version control.

#+REVEAL:split

- Alice's work not confined to a single computer
  - laptop / desktop / remote server
  - automatic and efficient way to synchronise
- Some data collected / analysed by colleagues from other team
  - all synchronize with centralized storage
  - preserving origin & authorship
  - combining simultaneous contributions

This is *distributed* version control.

#+REVEAL:split

- Needs to work on a subset of data at a given time
  - all files are kept on a server
  - few files are rotated into and out of the laptop
- Needs to publish data at project's end
  - raw data / outputs / both
  - completely or selectively

... all these were typical data management issues which we will touch upon during this workshop,
using DataLad as our primary tool.