	
AgendaResourcesDay OneHomeworkDay TwoOther	
Day One
Schedule
9:00 AM Intros & Breakfast

9:15 AM What is an Analyst?

9:30 AM Data Warehouses 

9:45 AM SQL Foundation

10:15 AM bash

11:00 AM Version Control

11:30 AM Git

12:00 PM Lunch

1:00 PM What is dbt

1:30 PM dbt fundamentals

2:30 PM making a pr

3:15 PM Break

3:30 PM data warehouse design

4:45 PM dbt vs your bi tool (what goes where)

Data Warehouses
Presentation
Resources
Data Warehouses Explained
The Difference Between a Warehouse and Database
Choosing a Data Warehouse
SQL Foundation 
Presentation
Resources
Mode SQL School
Fishtown Style Guide
Bash/Version/Git
Presentation: Bash
Presentation: VC/Git
Resources
What is Version Control?
Understanding the Github Flow
Github Cheat Sheet
Advanced Bash Commands
What is dbt & dbt fundamentals
Presentation: What is dbt?
Presentation: dbt Fundamentals
Resources
What is dbt?
dbt Documentation
Configuring models
Configuring quoting
Hooks
Tags
Using dbt archive
Making a PR
Presentation
Resources
Pull Request Tutorial
Pull Requests explained
Data Warehouse Design/Bi Tool
Presentation
Resources
Agile Data Warehouse Design by Lawrence Corr
How We Structure Our dbt Projects * very helpful!
Is Kimball Dimensional Modeling still relevant?
Writing queries in a BI tool vs Modeling them in dbt
Using Custom Schemas
dbt vs LookML
dbt_project.yml
name: 'dbt_learn'
version: '1.0'

profile: 'learn_project'

source-paths: ["models"]
analysis-paths: ["analysis"]
test-paths: ["tests"]
data-paths: ["data"]
macro-paths: ["macros"]

target-path: "target"  # directory which will store compiled SQL files
clean-targets:         # directories to be removed by `dbt clean`
    - "target"
    - "dbt_modules"

models:
PR TEMPLATE
<!---
Provide a short summary in the Title above. Examples of good PR titles:
* "Feature: add so-and-so models"
* "Fix: deduplicate such-and-such"
* "Update: dbt version 0.13.0"
-->

## Description & motivation
<!---
Describe your changes, and why you're making them. Is this linked to an open
issue, a Trello card, or another pull request? Link it here.
-->

## Screenshots:
<!---
Include a screenshot of the relevant section of the updated DAG. You can access
your version of the DAG by running `dbt docs generate && dbt docs serve`.
-->

## Validation of models:
<!---
Include any output that confirms that the models do what is expected. This might
be a link to an in-development dashboard in your BI tool, or a query that
compares an existing model with a new one.
-->

## Changes to existing models:
<!---
Include this section if you are changing any existing models. Link any related
pull requests on your BI tool, or instructions for merge (e.g. whether old
models should be dropped after merge, or whether a full-refresh run is required)
-->

## Checklist:
<!---
This checklist is mostly useful as a reminder of small things that can easily be
forgotten – it is meant as a helpful tool rather than hoops to jump through.
Put an `x` in all the items that apply, make notes next to any that haven't been
addressed, and remove any items that are not relevant to this PR.
-->
- [ ] My pull request represents one logical piece of work.
- [ ] My commits are related to the pull request and look clean.
- [ ] My SQL follows the [(COMPANY NAME’s) style guide](https://github.com/fishtown-analytics/corp/blob/master/dbt_coding_conventions.md).
- [ ] I have materialized my models appropriately.
- [ ] I have added appropriate tests and documentation to any new models.