# asmg_workflow
asmg_workflow is a package for scientific workflow construction. This package is inspired by several projects that require large number of steps with conditional logic. Tools like [apache airflow](https://airflow.apache.org/docs/apache-airflow/stable/index.html) and Pypeln(https://cgarciae.github.io/pypeln/) have similar goals with a much larger ecosystem. However, the size, complexity and ecosystem quirks did not suit these tools to the specific goal of this tool. This tool is for building a set of steps that create files needed for an experiment, run that experiment, and then process the output. And after a workflow is established, to use it as a piece in another larger experiment while logging the progress with a simple logging system.

# Installation 
## Method 1 - Directly from Github
```shell
pip install git+https://github.com/sandersa-nist/asmg_workflow.git
```
## Method 2 - Clone then Install
1. Use your favorite way to clone the repo or download the zip file and extract it.  
2. pip install to that location (note pip expects a unix style string 'C:/asmg_workflow/')

```shell
pip install <path to top folder>
```

# Workflow
1. Define the tasks to be done. Each task can be a predefined one, or a new task defined through inheritance.
2. Define the dependencies for each task. There are several stock dependencies and checkers, if a new dependency is needed, it is just a dictionary that uses a function that returns true if met or false if not met.
3. Add the dependencies to the tasks 
4. Add the tasks to the workflow

# [Jupyter Example](./examples/workflow_tasks_example.ipynb)