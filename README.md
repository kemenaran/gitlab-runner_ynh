# Overview

This is a Yunohost package for [GitLab Runner](https://docs.gitlab.com/runner/).
It enables you to run CI jobs for your GitLab projects on your on self-hosted Yunohost instance.

# Installing

1. Get a **Runner token** from your GitLab instance.

    _Go to `GitLab > (Your project) > Settings > CI/CD`, and copy the Runner token for your project._

2. **Install** GitLab Runner on your Yunohost instance.

    There are two ways to install this package:
    - Using the Yunohost admin panel: just provide the `https://github.com/kemenaran/gitlab-runner_ynh` URL ;
    - Using the command-line: execute `sudo yunohost app install https://github.com/kemenaran/gitlab-runner_ynh`.

3. **Verify that your runner has been registered** on GitLab.

    _Go to `GitLab > (Your project) > Settings > CI/CD`, and check on the runner section that your runner appears. Once the runner has registered itself, it may take a few more minutes for the runner to signal its activation to GitLab._
    
You can now start new GitLab-CI jobs, and have them picked up by your runner.

# Usage

By default, GitLab-CI jobs using this runner will execute in a `alpine:3` Docker image. However you can define the Docker image used by your project in the `.gitlab-ci.yml` file.

This is your own server, so mind the disk usage. To ensure it doesn't get filled with cache and artifacts, it may be useful to configure the artifacts expiration date in your `.gitlab-ci.yml` file.

# What works

- Registering the runner on a GitLab instance for running CI jobs,
- Executing jobs withing Docker images using the [Docker executor](https://docs.gitlab.com/runner/executors/#docker-executor),
- Controlling the runner status from Yunohost Services panel;
- Upgrading and removing the runner.
