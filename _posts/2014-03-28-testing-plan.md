---
layout: post
title: Testing Plan
---

## Coding Standards
All code will be automatically evaluated against Drupal Coding Standards, documented at https://drupal.org/coding-standards, using the PHP Code Sniffer tool.  The PHP Lint tool is also run to check custom modules' PHP syntax for parse errors.  By using git and an installer created for this project, the team will ensure that PHP Code Sniffer and PHP Lint execute automatically upon each developer's local code commit.  It will also execute as part of integration testing.

## Developer Testing
Before integrating their custom code with the shared 'integration' branch, developers will carry out appropriate testing to ensure their code is working as expected.  This may involve manual or automated testing as is appropriate.  Automated test will follow the Behat test framework

At a minimum, one automated test will be written for each JIRA user story that creates new site functionality.  At a minimum, one manual test will be conducted for each JIRA epic.

## Peer Review
Before any code is merged into the integration branch, using the GitHub pull request workflow a peer review for best practices will occur.  The first step of peer review is to check that the requirements and testing instructions stated in the JIRA issue have indeed been completed.  The second step is to review the code itself.  The GitHub pull request workflow allows the developers to quickly identify code changes that have been made and discuss these changes.

## Integration Testing
There will be an integration environment and integration branch that is dedicated to integration testing.   Once code is merged into this branch, the full suite of automated tests will run in this environment.  This continuous integration is a best practice that allows defects, regressions, and malformed code to be discovered as early as possible in the development process.  The outcome of integration testing will be visible in a Jenkins dashboard that provides numerous code quality metrics, including results from automated testing.

The integration environment will also be used by the Acquia team for manual functional testing and content review.

## User Acceptance Testing
Once the functionality for a given release has passed integration testing and review, the releases code and content will be placed in the staging environment for user acceptance testing (UAT).  UAT will be conducted by members of a stakeholder team.   In most cases, the scope of UAT will include site structure, functionality, and content migration.  In some cases, a round of UAT will focus on site structure and functionality to ensure expectations are met before any content is migrated.
