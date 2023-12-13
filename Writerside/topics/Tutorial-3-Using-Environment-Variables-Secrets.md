<var name="tutorial-number" value="3"/>
<var name="tutorial-yaml-file" value="tutorial-%tutorial-number%.yml"></var>
<var name="act-command" value="act -W .github/workflows/%tutorial-yaml-file% --env-file .env --secret-file .secrets"></var>

# Tutorial 3: Using Environment Variables &amp; Secrets

## Objective
This tutorial focuses on integrating and managing environment variables and secrets within a GitHub Actions workflow using Nektos/Act. Understanding how to use these elements is key for handling sensitive data and configuration settings in your CI/CD pipelines.

## Introduction
Environment variables and secrets are essential for managing configuration and sensitive data in your workflows. In this tutorial, we'll learn how to define and use them effectively in a GitHub Actions workflow, and how to work with them locally using Nektos/Act.


## Workflow File
<snippet id="workflow-directory">
For this tutorial, we will be using the ```%tutorial-yaml-file%``` file located in the ```.github/workflows``` directory of the repository.
</snippet>

This workflow is designed to echo a simple message, providing an easy start to using Nektos/Act.

## Step-by-Step Implementation
<include from="Running-a-Workflow.md" element-id="step-by-step"/>



#### Observe the Output:
After running the command, you can observe the output directly in your terminal. Act will display the logs of each step in the workflow as it's executed. Here's what to look out for in the output:

1. **Echoed Environment Variables:**
   - Look for lines where the workflow echoes the environment variables `DB_HOST` and `LOG_LEVEL`.
   - These should match the values you've set in your `.env` file.
2. **Echoed Secrets:**
   - The output should also include lines where the workflow echoes the `API_KEY` and `DB_PASSWORD` secrets.
   - For security reasons, ensure that actual secret values are not printed in logs.
3. **GitHub API Call Result:**
   - The most crucial part to observe is the output from the GitHub API call using `GITHUB_TOKEN`.
   - If the `GITHUB_TOKEN` is valid, you should see a JSON response listing the repositories.
   - If there's an authentication issue, you'll likely receive an error message in the response.

## Debugging Tips
- Make sure all environment variables and secrets are correctly defined and accessible in the workflow.
- If a step fails due to missing or incorrect environment variables, verify their values and names.
- Remember, secrets should not be hardcoded in the workflow file for security reasons.

## Practical Applications
Using environment variables and secrets is crucial for maintaining security and flexibility in CI/CD workflows, especially when dealing with sensitive data or API keys.

## Summary
This tutorial provided insight into the use of environment variables and secrets in GitHub Actions workflows. Through Nektos/Act, you've seen how to handle these securely and effectively in a local development environment.