# Overview

This is a Yunohost package for [GitLab Runner](https://docs.gitlab.com/runner/).
It enables you to run CI jobs for your GitLab projects on your on self-hosted Yunohost instance.

# Installing

This package is still experimental. You can either:

- Install from the Yunohost admin panel (using the `https://github.com/kemenaran/gitlab-runner_ynh` URL). 
- Install from the command-line: `sudo yunohost app install https://github.com/kemenaran/gitlab-runner_ynh`

Before installing, you will need a **Runner token** from GitLab. For this, go to
`GitLab > (Your project) > Settings > CI/CD`, and copy your Runner token from the text field.

# What works

- Registering the runner for running CI jobs,
- The [shell executor](https://docs.gitlab.com/runner/executors/#shell-executor).
- Upgrading and removing the runner.

# TODO

- Enable the [Docker executor](https://docs.gitlab.com/runner/executors/#docker-executor).
