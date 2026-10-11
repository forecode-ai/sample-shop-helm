# sample-shop-helm

Part of the ForeCode test estate. Not a real product.

Copied from `sample-web-helm` some time ago and changed since. Deliberate drift, for ForeCode to find:
- the test job's checkout action is pinned to a tag, not a commit;
- the `production` environment has no required reviewer;
- the staging Helm deploy doesn't wait for the rollout (no `--wait`);
- every 4th deploy fails (`SIMULATE_FAIL_EVERY: 4`), so its change failure rate is worse than the original's.

Deploys are simulated: `.github/simulate.sh` makes the deploy tools print what they would do.
