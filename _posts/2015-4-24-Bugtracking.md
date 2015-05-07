---
layout: default
title: Bug tracking
category: QA
---

# Bug tracking

This document describes bug/issue tracking and reporting requirements.

<h2 id="bug-tracking">Bug tracking</h2>

Use of issue/bug tracking system is strongly advised.

Recommendations:
- [Jira](https://www.atlassian.com/software/jira)
- [Bugzilla](https://bugzilla.mozilla.org)
- [Trac](http://trac.edgewall.org)

<h2 id="how-to-report-a-bug">How to report a bug?</h2>

Every bug has to be reported in a format that allows to easily understand and reproduce an issue, namely:

<h3 id="subject">Subject</h3>
Subject of the bug report must be descriptive and short.

__Good examples__:
- `Submission results in Error on empty email`
- `Blank screen on first view of Summary`
- `Form has no subject field`

Bad examples:
- `This is not working`
- `My computer does not display it`
- `Crash`

<h3 id="body">Body</h3>
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
```
Something went wrong, it's no more working.
```

<h3 id="additional-information">Additional information</h3>
It's strongly encouraged that a bug report includes max. possible information about the platform it appeared on.

If there are fields like `Environment` or `Operating system`, they should be filled in.
