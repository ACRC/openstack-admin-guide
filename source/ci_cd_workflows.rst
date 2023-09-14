.. include:: vars.rst

===============================
CI/CD Workflows and Runners
===============================

CI/CD Runners
=============
There are |num_ci_runners| CI/CD runners and they are running as systemd jobs
on |control_host|.

CI/CD Workflows
================
The workflows are located in the `.github` folder of the kayobe config. They
can be run by going to the actions section of |kayobe_config_source_url|. Each
workflow has it's own configuration opetions and depending on the workflow you
choose you may be able to add limits to the command you are going to run.

For example, if you were to run the `Run Overcloud Service Deploy` workflow you
are given the option to limit the hosts that this command runs on and to limit
the services that are deployed. This is useful for making changes to the kayobe
config and limiting them to a single node to ensure everything is working as
expected.

Additonally, on every PR to the kayobe config repo, the `Config Diff` workflow
is run. This workflow will run a diff between the current kayobe config and the
proposed changes. This is useful for ensuring that the changes you are making
are what you expect them to be.
