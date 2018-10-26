# ADR008: Continuous delivery workflow

## Status

Accepted

## Context

If a Reliability Engineer on support has to make a change to a Service Team's deployment or
cluster to resolve an issue or perform a critical upgrade, they need to know
how to perform a release, where to look for the code and need confidence that
any changes they make have not broken the deployment.

Traditionally this problem has been addressed with the use of "Team Manuals"
that document release processes, locations of project repositories and who
should have access. These manuals can get out of sync with processes, and
processes often differ significantly between teams.


## Decision

We will provide the tools and guidance for teams to practice [continuous delivery](https://en.wikipedia.org/wiki/Continuous_delivery)

We expect this to improve the effciency of supporting multiple services by:

* promoting a consistant pattern for deployment accross teams (merging PRs)
* giving confidence to those making changes to deployments (culture of testing/staging releases)
* giving confidence that the desired state of deployment is what is commited to git

## Consequences

* We will likely have to run and maintain CI/CD tooling
* CI/CD toolings is an area where people have quite strong opinions
* Some teams may have complicated "gated" pipelines where human approval is required