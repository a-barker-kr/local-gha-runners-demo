<var name="tutorial-number" value="1"/>
<var name="tutorial-yaml-file" value="tutorial-%tutorial-number%.yml"></var>
<var name="act-command" value="act -W .github/workflows/%tutorial-yaml-file%"></var>

# Tutorial 1: Running a Simple Bash Script

## Objective
Learn to run a basic GitHub Actions workflow locally using Nektos/Act. This introductory tutorial is aimed at demonstrating the ease of executing workflows in your local environment.

## Introduction
In this tutorial, we'll explore the foundational step of running a GitHub Actions workflow using Nektos/Act. This is an essential skill for any developer looking to leverage the power of CI/CD pipelines locally. We will be using a simple Bash script to understand the process.


## Workflow File
<snippet id="workflow-directory">
For this tutorial, we will be using the ```%tutorial-yaml-file%``` file located in the ```.github/workflows``` directory of the repository.
</snippet>

This workflow is designed to echo a simple message, providing an easy start to using Nektos/Act.

## Step-by-Step Implementation
<snippet id="step-by-step">
<note>Make sure Docker is running, as Nektos/Act requires it.</note>
<procedure>
<step>
Open your terminal to the root level of the project
</step>
<step>
Ensure the <code>%tutorial-yaml-file%</code> is in the <code>.github/workflows</code> directory.
</step>
<step>
Run the workflow using Nektos/Act by executing the following command in your terminal:
<code-block lang="bash">%act-command%</code-block>
</step>
</procedure>
</snippet>



#### Observe the Output:
Look for the console output that should echo the message from the Bash script.

## Debugging Tips
If the workflow does not run, ensure that Docker is operational on your machine.
Check for typos or formatting issues in the ```%tutorial-yaml-file%``` file.
Consult the [Nektos/Act GitHub repository](https://github.com/nektos/act) for common issues and solutions.

## Practical Applications
Running simple workflows locally helps in quick iterations and testing of CI/CD pipelines. It's a fundamental skill that aids in building more complex workflows efficiently.

## Summary
This tutorial guided you through the basics of executing a GitHub Actions workflow locally using Nektos/Act. You've learned to run a simple workflow, which is a critical step towards mastering the development and testing of CI/CD pipelines in your local environment.