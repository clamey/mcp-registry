# Security Policy

The maintainers of Docker MCP Registry take security seriously. If you discover
a security issue, please bring it to their attention right away!

## Reporting a Vulnerability

Please **DO NOT** file a public issue, instead send your report privately
to [security@docker.com](mailto:security@docker.com).

Reporter(s) can expect a response within 72 hours, acknowledging the issue was
received.

## Automated Security Scanning

This repository uses StackHawk for automated Dynamic Application Security Testing (DAST).
StackHawk scans run:
- On every pull request to the main branch
- On pushes to the main branch
- Weekly on Mondays at 2 AM UTC
- Manually via workflow dispatch

The scans target the security reviewer proxy service to identify potential
vulnerabilities in the running application.

## Review Process

After receiving the report, an initial triage and technical analysis is
performed to confirm the report and determine its scope. We may request
additional information in this stage of the process.

Once a reviewer has confirmed the relevance of the report, a draft security
advisory will be created on GitHub. The draft advisory will be used to discuss
the issue with maintainers, the reporter(s), and where applicable, other
affected parties under embargo.

If the vulnerability is accepted, a timeline for developing a patch, public
disclosure, and patch release will be determined. If there is an embargo period
on public disclosure before the patch release, the reporter(s) are expected to
participate in the discussion of the timeline and abide by agreed upon dates
for public disclosure.

## Accreditation

Security reports are greatly appreciated and we will publicly thank you,
although we will keep your name confidential if you request it. We also like to
send gifts - if you're into swag, make sure to let us know. We do not currently
offer a paid security bounty program at this time.
