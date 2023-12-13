<var name="tutorial-number" value="2"/>
<var name="tutorial-yaml-file" value="tutorial-2.yml"></var>

# Tutorial 2: Creating a Workflow with Multiple Jobs

## Objective
Learn how to create and manage a workflow with multiple jobs using Nektos/Act. This tutorial will demonstrate how to structure a workflow to run several tasks in sequence or in parallel.

## Introduction
In this second tutorial, we'll advance our understanding of GitHub Actions workflows by handling multiple jobs. This capability is essential for complex workflows where different tasks need to be executed in a specific order or simultaneously.


## Workflow File
<snippet id="workflow-directory">
For this tutorial, we will be using the ```%tutorial-yaml-file%``` file located in the ```.github/workflows``` directory of the repository.
</snippet>

This workflow is designed to echo a simple message, providing an easy start to using Nektos/Act.

## Step-by-Step Implementation
<include from="Running-a-Workflow.md" element-id="step-by-step"/>



#### Observe the Output:
Observe how Nektos/Act handles the execution of multiple jobs, either sequentially or in parallel, based on the workflow configuration.

## Debugging Tips
Ensure that all jobs are correctly defined and have the necessary dependencies.
If jobs are not running as expected, check the run conditions and requirements for each job.
Verify that the workflow file is correctly formatted and follows the GitHub Actions syntax.

## Practical Applications
Understanding multi-job workflows is crucial for complex CI/CD processes, where different stages of building, testing, and deployment are handled in separate jobs.

## Summary
This tutorial has introduced you to the concept of multi-job workflows in GitHub Actions. By using Nektos/Act, you have learned how to locally test and debug complex workflows that involve multiple jobs.