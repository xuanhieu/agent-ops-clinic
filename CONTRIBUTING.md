# Contributing to Agent Ops Clinic

This is an educational, local-first bilingual lab. Pull requests that make the lesson more reproducible, secure, accessible, or welcoming are encouraged.

## Good first contributions
- Fix a typo or improve English / Vietnamese translation in `i18n.js`.
- Add a deterministic unit test for human approval/budget/risk gate behavior.
- Improve keyboard navigation or mobile responsiveness with screenshots.
- Write a new fictional, privacy-safe exercise scenario and its regression tests.
- Clarify how the simulation differs from production systems.

## Process
1. Open an issue describing the learner pain point or bug, with steps to reproduce.
2. Fork and create a small feature branch.
3. Run `node --test` and `node scripts/smoke.mjs` before your PR.
4. Include before/after screenshots for any UI change (mobile and desktop).
5. Explain limitations clearly; do not introduce external APIs or telemetric collection without discussion.

Do not include credentials, real customer data, private project code, or copyrighted illustrations. Respect upstream ownership for any copied code.
