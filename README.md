# Gemini Review Automation

This repository includes a GitHub Action that triggers **Gemini Code Assist** review automatically on pull requests.

## 1) Set up free Gemini Code Assist on GitHub

1. Open the marketplace listing: https://github.com/marketplace/gemini-code-assist
2. Click **Install it for free** and connect it to your account or organization.
3. Grant access to the repository where you want review automation.
4. In Gemini settings, choose a **Low** or **Medium** review/context tier first (recommended for strong signal with efficient usage).

## 2) Add the automation workflow

This repository uses `.github/workflows/gemini-review.yml`:

- On `pull_request` **opened** and **synchronize** events
- Posts a PR comment with `/gemini review`
- That comment triggers Gemini Code Assist review automatically

## 3) Why this helps

- Reviews are automated with each PR update.
- Triggering Gemini this way does **not** consume GitHub Copilot credits.
- Gemini's free offering has useful limits for ongoing PR review workflows (see current plan details in the marketplace listing).
