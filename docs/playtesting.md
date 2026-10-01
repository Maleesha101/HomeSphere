# HomeSphere Playtesting Plan

## Test Groups

### Smoke Test
Verify containers start, health checks pass, APK installs, links work, synthetic media loads, and reset works.

### Guided Test
A security-aware tester follows the intended solution with no hidden author knowledge. Record time to first discovery, time per stage, confusing clues, unnecessary rabbit holes, and unintended shortcuts.

### Blind Test
A tester receives only the player-facing challenge description. This is the strongest fairness test.

## Success Metrics

- First useful artifact is discoverable without a hint.
- Every critical transition has an independent supporting clue.
- No critical stage depends on guessing a hidden filename.
- Final chain remains reproducible after reset.
- No unintended host/network access is discovered.

## Regression

build -> start -> smoke test -> intended solve -> reset -> intended solve

If players are stuck, improve evidence before reducing vulnerability complexity. If players solve too quickly, increase evidence correlation rather than arbitrary obscurity.
