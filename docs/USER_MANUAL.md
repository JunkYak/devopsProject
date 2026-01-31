# Jenkins User Manual

## Freestyle Project
- Used to demonstrate basic CI concepts.
- Pulls source code from GitHub.
- Executes Python and Maven build steps.
- Archives build artifacts.
- Publishes test results.

## Multibranch Pipeline
- Automatically discovers branches from GitHub.
- Executes different CI stages based on branch type:
  - Main branch: Full CI pipeline
  - Feature branches: Test execution
  - Release branches: Security scan stage

## How to Run Jobs
1. Open Jenkins Dashboard.
2. Select the required job.
3. Click "Build Now".
4. View console output for build logs.
