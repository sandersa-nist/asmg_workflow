# asmg_workflow - "Applied Systems Metrology Group Workflow"
asmg_workflow is a package for scientific workflow construction. This package is inspired by several projects that require large number of steps with conditional logic. Tools like [apache airflow](https://airflow.apache.org/docs/apache-airflow/stable/index.html) and [Pypeln](https://cgarciae.github.io/pypeln/) have similar goals with a much larger ecosystem. However, the size, complexity and ecosystem quirks did not suit these tools to the specific goal of this tool. This tool is for building a set of steps that create files needed for an experiment, run that experiment, and then process the output. And after a workflow is established, to use it as a piece in another larger experiment while logging the progress with a simple logging system.

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
# Use Case
Have you developed procedural code to run an experiment over and over? Each time you do this, you have to develop a set of tasks and put them in order with some conditional logic. Once you do this, you almost always have to do it again in the future. It would be handy to re-use the tasks and be able to rearrange them in the order forced by the conditional logic of each problem. This package allows you to do that and then keep building more and more complicated chains of those type of situations.   

1. 

# Workflow
1. Define the tasks to be done. Each task can be a predefined one, or a new task defined through inheritance.
2. Define the dependencies for each task. There are several stock dependencies and checkers, if a new dependency is needed, it is just a dictionary that uses a function that returns true if met or false if not met.
3. Add the dependencies to the tasks 
4. Add the tasks to the workflow


# Code Structure
This repository relies on [simulations.py](./experimental_design/experimental_designs.py) for its functionality, for API style documentation see [documentation](https://sandersa-nist.github.io/experimental_design/documentation/experimental_design/experimental_designs.html).

# [Example](./examples/workflow_tasks_example.ipynb)
# [API Documentation](https://sandersa-nist.github.io/asmg_workflow/documentation/asmg_workflow.html) 

# Contact
Aric Sanders [aric.sanders@nist.gov](mailto:aric.sanders@nist.gov)


# NIST Disclaimer
Certain commercial equipment, instruments, or materials (or suppliers, or software, ...) are identified in this repository to foster understanding. Such identification does not imply recommendation or endorsement by the National Institute of Standards and Technology, nor does it imply that the materials or equipment identified are necessarily the best available for the purpose.