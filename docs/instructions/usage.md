# **Usage**

The workflow is organized as a stepwise procedure, where the steps can be turned on/off through Boolean flags. It is configured by one <a href=../json_input target="_blank">input file</a> in JSON format, named `workflow_input.json`, which must be properly filled by the user before starting. 

The execution is managed by the Python script `workflow_main.py` in the main folder. All the other scripts are in the folder `py`, while bash scripts for submitting jobs to the computational
nodes are in the folder `sh`. 

To run, activate the software environment as explained <a href=../../spack/env_spack target="_blank">here</a>, or using a different package manager, and type (assuming the JSON <a href=../json_input target="_blank">input file</a> is in the working folder):

```plaintext
python /path-to-sofware/cheese-ptha-master/workflow_main.py --sitename SITENAME --input_workflow /path-to-wdir/workflow_input.json
```

The steps marked as `True` in the JSON <a href=../json_input target="_blank">input file</a> will be executed. Of course, if one single step is required, the previous ones are assumed to be already executed.

In production mode, it is strongly recommended to run the workflow preventing the process from receiving the SIGHUP (Signal Hang UP) signal upon closing or exiting the terminal:

```plaintext
nohup pyhton /path-to-software/cheese-ptha-master/workflow_main.py --sitename SITENAME --input_workflow /path-to-wdir/workflow_input.json &
```

A new folder, called SITENAME, is created within the working folder, and all the outputs will be directed there.

