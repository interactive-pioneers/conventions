# Bug tracking

This document describes bug/issue tracking and reporting requirements.

## Tools

If a related project [JIRA](https://www.atlassian.com/software/jira) board exists, issues and bugs should be tracked there. Repository related issues, e.g. on our open source projects, which are not represented in a JIRA board, should be submitted in the GitHub or GitLab repository issue section. 

## How to report a bug?

Every bug has to be reported in a format that allows to easily understand and reproduce an issue, namely:

### Subject

Subject of the bug report must be descriptive and short.

__Good examples__:
> Submission results in Error on empty email

> Blank screen on first view of Summary

> Form has no subject field

Bad examples:
> This is not working

> My computer does not display it

> Crash

### Body

Every bug report should be described in 3 sections:
- How to reproduce it
- What happened
- What should happen

__Good example__:

``` 
Steps to reproduce:
  1. Open Email submission page
  2. Fill in all mandatory fields
  3. Click Submit

What happens: submission results in Error on empty email

What should happen: submission should not result in Error on empty email as it is not a mandatory field
```

Bad example:

> Something went wrong, it's no more working.

### Additional information

It's strongly encouraged that a bug report includes max. possible information about the platform it appeared on.

If there are fields like `Environment` or `Operating system`, they should be filled in.
