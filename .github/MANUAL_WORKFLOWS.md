# Manual Workflow Triggers

The ModOrganizer repository supports manual triggering of CI/CD workflows from the GitHub Actions UI.

## Available Manual Workflows

### Build ModOrganizer 2
- **Workflow file**: `.github/workflows/build.yml`
- **Description**: Builds the complete ModOrganizer 2 application
- **Manual trigger**: Available via GitHub Actions UI

### Lint ModOrganizer 2
- **Workflow file**: `.github/workflows/linting.yml`  
- **Description**: Runs code formatting and linting checks
- **Manual trigger**: Available via GitHub Actions UI

## How to Manually Trigger Workflows

1. Navigate to the **Actions** tab in the GitHub repository
2. Select the workflow you want to run from the left sidebar:
   - "Build ModOrganizer 2" 
   - "Lint ModOrganizer 2"
3. Click the **"Run workflow"** button on the right side
4. Select the branch you want to run the workflow on (typically `master`)
5. Click **"Run workflow"** to start the manual execution

## When to Use Manual Triggers

Manual workflow triggers are useful for:
- Testing builds on specific branches without creating a PR
- Running builds after configuration changes
- Triggering builds for testing purposes
- Re-running failed workflows due to transient issues

## Automatic Triggers

Workflows will still run automatically on:
- Push to `master` branch (build workflow only)
- Opening, updating, or reopening pull requests
- Push to any branch (linting workflow only)

Manual triggers complement these automatic triggers and do not replace them.