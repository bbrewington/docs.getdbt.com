---
title: Create a Python virtual environment
id: create-a-python-virtual-environment
description: "Instructions on creating a Python virtual environment."
pagination_next: "docs/core/create-a-python-virtual-environment"
pagination_prev: null
---

A Python virtual environment is an isolated workspace for Python projects. This prevents libraries and versions used in one project from interfering with others, making it especially helpful when working on multiple projects with differing requirements or avoiding conflicts with global Python installations.

The Python ecosystem offers several tools for creating isolated environments, such as [conda](https://anaconda.org/anaconda/conda), [poetry](https://python-poetry.org/docs/managing-environments/), and `venv`. Among these, `venv` has the fewest additional dependencies and has been included by default in recent Python versions for quite some time.

`venv` will set up a Python virtual environment within the `env` folder.

Users who want to run dbt locally, for example in [dbt Core](/docs/core/installation-overview) or the [dbt Cloud CLI](/docs/cloud/cloud-cli-installation#install-a-virtual-environment) may want to install a Python virtual environment. 


## Prerequisites

- Access to a terminal or command prompt.
- Have [Python](https://www.python.org/downloads/) installed on your machine. You can check if Python is installed by running `python --version` or `python3 --version` in your terminal or command prompt.
- Have [pip installed](https://pip.pypa.io/en/stable/installation/). You can check if pip is installed by running `pip --version` or `pip3 --version`.
- Have the necessary permissions to create directories and install packages on your machine.

## Install a Python virtual environment 

Depending on the operating system you use, you'll need to execute specific steps to set up a virtual environment. 

To install a Python virtual environment, navigate to your project directory and execute the command. This will generate a new virtual environment within a local folder which you can name it anything you want.  [Our convention](https://github.com/dbt-labs/dbt-core/blob/main/CONTRIBUTING.md#virtual-environments) has been to name it `env` or `env-anything-you-want`

<Tabs>
  <TabItem value="Unix/macOS" label="Unix/macOS">
    1. Create your virtual environment:

    ```shell
    python3 -m venv env
    ```

    2. Activate your virtual environment:

    ```shell
    source env/bin/activate
    ```

    3. Verify Python Path:

    ```shell
    which python
    ```

    4. Run Python:

    ```shell
    env/bin/python
    ```
  </TabItem>

  <TabItem value="Windows" label="Windows">
    1. Create your virtual environment

    ```shell
    py -m venv env
    ```

    2. Activate your virtual environment:

    ```shell
    env\Scripts\activate
    ```

    3. Verify Python Path:

    ```shell
    where python
    ```

    4. Run Python:

    ```shell
    env\Scripts\python
    ```
  </TabItem>
</Tabs>

If you're using dbt Core, refer to [What are the best practices for installing dbt Core with pip?](/faqs/Core/install-pip-best-practices.md#using-virtual-environments) after creating your virtual environment. 

If you're using the dbt Cloud CLI, you can [install dbt Cloud CLI in pip](/docs/cloud/cloud-cli-installation#install-dbt-cloud-cli-in-pip) after creating your virtual environment.

## Deactivate virtual environment

To switch projects or leave your virtual environment, deactivate the environment using the command while the virtual environment is active:

```shell
deactivate
```
