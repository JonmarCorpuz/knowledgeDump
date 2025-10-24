# Vertex AI Workbench Overview

[Workbench](https://cloud.google.com/vertex-ai/docs/workbench/introduction) instances are Jupyter notebook-based development environments for the entire data science workflow

* Prepackaged with JupyerLab and preinstalled suite of deep learning packages 
* Provides multi-kernel support and supports the ability to sync with a GitHub repository
* Protected by GCP's authentication and authorization

<br>

# Vertex AI Workbench Features

## Idle Shutdown

Idle shutdown shuts down the WOrkbench instance when there's no kernel activity for the specified time period (Idle shutdown looks for activity in kernels running in `127.0.0.1:8080/api/sessions`, `127.0.0.1:8080/api/terminals`, and `127.0.0.1:8080/api/kernels` by default)

* Helps manage costs
* Requires the Workbench instance to have guest attributes enabled (Enabled by default but can be enabled by adding the `enable-guest-attributes` metadata key to `true`)
* Enabled by default to shutdown your instance after 180 inactive minutes (This can be changed by using the `gcloud workbench instances update INSTANCE_NAME --metadata=idle-timeout-seconds=$SECONDS` command)
* Can be turned off using the `gcloud workbench instances update INSTANCE_NAME --metadata=idle-timeout-seconds=` command

<br>

## Conda Environments

Adding conda environments to a Workbench instance allows users to use kernels that aren't available in the default Vertex AI Workbench instance (*R*, *Apache Beam*, *Earlier frameworks of TensorFlow*, *Earlier frameworks of PyTorch*, *etc.*)

* Adding a conda environment will appear as a kernel in your instance's JupyterLab interface
* Allows you to use kernels that aren't available in Vertex AI Workbench instances

<br>

Add a conda environment
```Bash
# Creates a conda environment.
conda create -n CONDA_ENVIRONMENT_NAME -y
conda activate CONDA_ENVIRONMENT_NAME

# Install packages using a pip local to the conda environment.
conda install pip
pip install PACKAGE

# Adds the conda kernel.
DL_ANACONDA_ENV_HOME="${DL_ANACONDA_HOME}/envs/CONDA_ENVIRONMENT_NAME"
python -m ipykernel install --prefix "${DL_ANACONDA_ENV_HOME}" --name CONDA_ENVIRONMENT_NAME --display-name KERNEL_DISPLAY_NAME

# Optionally remove the default kernel that was created when installing to a given conda environment
rm -rf "/opt/micromamba/envs/CONDA_ENVIRONMENT_NAME/share/jupyter/kernels/python3
```

<br>

| Conda Environment | Description |
| --- | --- |
| | |

<br>

## Cloud Storage Integration

Users can mount a Cloud Storage bucket to the Workbench instance allowing them to browse its contents and work with compatible files from within the JupyerLab interface

* Requires both the `roles/notebooks.runner` and `roles/storage.objectUser` roles to mount a Cloud Storage bucket to a Vertex AI Workbench
* Requires the `storage.buckets.list` permission to allow the **Mount shared storage** button to appear in the JupyterLab interface