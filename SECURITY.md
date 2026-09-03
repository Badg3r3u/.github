# Security policy

These repos (`ownscan`, `ownscan-action`, `ownkit`) are **defensive hygiene tools**. They read files you already have. They do not scan other people’s systems and they do not use any credential they find.

## If ownscan reports a real secret

1. Rotate that credential at the provider (GitHub, AWS, Slack, etc.).
2. Remove it from the repo, including git history if it was committed.
3. Treat the old value as compromised even if you deleted the line on `main`.

## Reporting a vulnerability in these tools

If you found a bug in ownscan / ownscan-action / ownkit themselves (missed detections are not vulnerabilities; a way to exfiltrate runner secrets, execute untrusted code, or leak token contents in logs is):

- Open a **private** GitHub security advisory on the affected repo, or
- Email the account owner via GitHub if advisories are not enabled yet

Please include the repo, a short repro, and impact. Do not attach live credentials.

Do not file public issues that include real secrets.
