# mayfair-deploy

The production deploy workflows of Mayfair. This repository is public on purpose: GitHub Free gives approvals, wait timers and environment secrets only on public repositories (checked 13 November 2026). It holds workflow files and two lists, never code or secrets.

* `deploy-production.yml`: deploy or roll back one listed target. It starts by hand, waits for the owner's approval and a 10 minute timer, then checks the commit in the private repository before it deploys.
* `repo-check.yml`: fails the build if anything other than these files appears.
* `targets.txt` and `required-checks.txt`: the two lists the owner controls.

Decisions: OD190 and OD192 in the Mayfair plans.
