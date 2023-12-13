<var name="tutorial-number" value="4"/>
<var name="tutorial-yaml-file" value="tutorial-%tutorial-number%.yml"></var>
<var name="act-command" value="act -W .github/workflows/%tutorial-yaml-file% --env-file .env --secret-file .secrets"></var>

# Tutorial 4: Advanced Workflow Features

## Objective
This tutorial aims to delve into advanced features of GitHub Actions, including conditional logic and action composition, using Nektos/Act for local testing. Understanding these advanced features allows for more dynamic and efficient workflows.

## Introduction
GitHub Actions offers a range of advanced features that can optimize your CI/CD pipelines. Conditional logic allows for more control over when and how jobs or steps are executed, while action composition enables the reuse of actions or parts of workflows. In this tutorial, we'll explore these capabilities and see how they can be applied in local development environments using Nektos/Act.

## Workflow File
<snippet id="workflow-directory">
For this tutorial, we will be using the ```%tutorial-yaml-file%``` file located in the ```.github/workflows``` directory of the repository.
</snippet>

This workflow is designed to echo a simple message, providing an easy start to using Nektos/Act.

## Step-by-Step Implementation
<include from="Running-a-Workflow.md" element-id="step-by-step"/>



#### Observe the Output:
When running the advanced-features-workflow.yml with Nektos/Act, it's important to observe how the different conditional methods influence the workflow's execution. Here's what to look for in the terminal output:

1. **`if`: Conditional Execution**
   - Checks for specific conditions to decide if a job or step should run. Look for whether the step "Conditional Execution" runs based on the branch name and event type.
2. **`startsWith`: Branch Name Check**
    - Evaluates if the branch name starts with a specific string (feature/). Observe if the workflow behaves differently when run on different branches.
3. **`always()`: Unconditional Execution**
   - This condition ensures that a step runs regardless of the success or failure of previous steps. The "Final Step" should always execute, so check for its output in every scenario.

Additionally, here are other conditions to be aware of:

1. **`success()`: Success Check**
   - Returns true if all the previous steps were successful. Look for steps that execute only after successful completion of prior steps.
2. **`failure()`: Failure Check**
   - Activates when any of the previous steps failed. Notice if specific steps execute only when an earlier step fails.
3. **`cancelled()`: Cancellation Check**
   - This will be true if the workflow was cancelled. While harder to observe in a standard run, it's useful for handling cleanup or notifications in the event of cancellation.

For each of these conditions, closely watch the terminal output to see how they affect the workflow. This will provide insights into how different conditions can be leveraged to create dynamic and responsive GitHub Actions workflows.

For a comprehensive understanding of all the conditional methods available in GitHub Actions, refer to GitHub's official documentation on workflow syntax for GitHub Actions: [Context and expression syntax for GitHub Actions](https://docs.github.com/en/actions/learn-github-actions/expressions). This resource provides detailed information on various contexts, functions, and operators you can use in your workflows.

## Debugging Tips
- If conditional steps or jobs are not behaving as expected, double-check their if statements for correct syntax and logic.
- Ensure that composed actions are correctly referenced and accessible.

## Practical Applications
Advanced features like conditional logic and action composition are critical for creating efficient, dynamic, and reusable workflows, which are essential for complex CI/CD processes.

## Summary
This tutorial guided you through some of the advanced features available in GitHub Actions, enhancing your ability to create sophisticated workflows. Using Nektos/Act, you've learned how to apply these features in a local development context.