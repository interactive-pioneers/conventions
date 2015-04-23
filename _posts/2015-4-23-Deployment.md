---
layout: default
title: Deployment to servers
---

# Deployment to servers

Deployment to servers should always be done with universal encapsulated `deploy`.

## Important

1. Keys for the deploy user can be obtained from Dev Lead or KeePass, e.g. from `Dev server` storage.
2. Any project should always feature staging system that can be used for production-like testing.
3. Deployment should ideally feature CI system, e.g. Bamboo.
4. Built code should not be checked into version control.
5. For projects for which built code is deployed, system build and deploy is preferred (see pt. 3).
  1. For Rails projects CI system can also be used, but [Capistrano](https://github.com/capistrano/capistrano) deployments are preferred. Capistrano can still be triggered by a CI system allowing HipChat notifications etc.
  2. For static (e.g. [Assemble](https://github.com/assemble/assemble)) projects, due to the build process, CI system (Bamboo) is strongly recommended, for build and deploy.
6. All deployments should be pubkey-specific, no password authentication should be allowed on any servers.
7. No deployments should be with `root` user as well as no server should allow root login.
