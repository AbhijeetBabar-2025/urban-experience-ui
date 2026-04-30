# Security Policy

## Scope

This repository contains AI prompt and workflow files — no executable server code, no authentication, no user data storage.

The primary security considerations are:

- **Prompt injection**: the skill reads user-supplied URLs and screenshots. It does not execute arbitrary code from those sources, but agents using this skill should validate external input per their own security policies.


## Reporting a Vulnerability

If you discover a security issue related to the prompt logic, data files, or workflow design:

1. **Do not open a public issue.**
2. Contact the maintainer directly via email [EMAIL_ADDRESS]
3. Include a description of the issue and steps to reproduce.

You should expect a response within 7 days.


