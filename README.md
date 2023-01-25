# Group Permissions Migrator (Non-UC to UC backed)
This is a Notebook based utility for migrating the permissions of non-uc groups to there uc counterparts


## Pre-requisites
1. Ensure that the workspace has UC enabled
2. For each `non-UC` group ensure a `UC` counterpart group is also created with the a prefix of `uc_`
   For Example: `Non-UC` group with the name `"fe_ams"` should have the counterpart UC based group `"uc_fe_ams"`

## Usage
Once the pre-requisites are met.
* The utility is meant to be ran by `Admins`
* Import the `UC_group_permission_migrator.dbc` in the workspace
* Run `uc_nb1 ( _get_permissions_ )` first. This collects the permissions for the non-uc groups across different data artifacts and stores them to a table
* And then run `uc_nb2 ( _set_permissions_ )` this will read the table created in the previous step and setup the permissions to the uc counterpart groups

## Types of objects supported
1. Jobs
2. Clusters
3. Cluster Policies
4. DLT Pipelines
5. Pools
6. SQL Warehouses
7. MLFlow Models
8. Repos
9. Notebooks
10. Directories

## Feedback
Feel free to directly reach out to the 

* Developer (souvik.pratiher@databricks.com) 
* Project Reviewer (birbal.das@databricks.com)

All kinds of feedbacks are welcomed.
