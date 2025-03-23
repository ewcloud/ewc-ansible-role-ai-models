EWC Ansible Role AI models
==========================

Create a conda environment with the ai-models package and associated plugins to run a set of data-driven weather forecasting models such as panguweather or graphcast. 

Requirements
------------
This ansible role depends on ewc-ansible-role-conda.

Role Variables
--------------
 - `ai_models_env_wipe`: Boolean to decide whether to wipe the environment if exists prior to a reinstallation. Default: no
 - `ai_models_env_name`: Name of the environment containing the software stack. Default: ml-basic
 - `ai_models_env_path`: Path to the environment containing the software stack. Default: `{{ conda_prefix }}/envs/{{ ai_models_env_name }}`
 - `ai_models_create_ipykernel`: Boolean to create a system-wide kernel available. Default: yes
 - `conda_prefix`: Prefix where conda is installed. Default: `/opt/conda`
 - `conda_user`: User owning the conda installation. Default: `root`

Example Playbook
----------------

    - hosts: all
      roles:
         -  ewc-ansible-role-ai-models

License
-------

Apache 2.0.

Author Information
------------------

ECMWF for the European Weather Cloud