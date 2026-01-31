# Jenkins Troubleshooting Guide

## Maven Command Not Found
- Ensure Maven is configured in Jenkins Global Tool Configuration.
- Use Jenkins Maven build steps instead of command line execution.

## Build Fails on Windows with 'sh' Command
- The 'sh' command is Linux-specific.
- On Windows systems, use 'bat' instead of 'sh'.

## No Test Results Found
- This occurs when no test cases are present.
- Enable "Do not fail the build on empty test results".

## Git Repository Not Found
- Verify repository URL and branch configuration.
- Ensure at least one commit exists in the repository.
