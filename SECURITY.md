# Security Policy

## Supported Versions

Since this is a web-based game hosted via GitHub Pages, only the latest deployment is supported. We recommend all users play the latest version available at the official URL.

| Version | Supported          |
| ------- | ------------------ |
| Latest  | :white_check_mark: |
| Older   | :x:                |

## Reporting a Vulnerability

We take the security of **Divya Astra** seriously. If you discover a security vulnerability, please follow these steps to report it responsibly:

### 1. Do Not Open a Public Issue
To protect the integrity of the game and our users' data, please **do not** report security vulnerabilities through public GitHub issues.

### 2. How to Report
Please email the details of the vulnerability to:
**ngornalli@gmail.com**

In your email, please include:
* A description of the vulnerability.
* Steps to reproduce the issue (including scripts or screenshots if applicable).
* The potential impact of the vulnerability.

### 3. Response Timeline
* We will acknowledge receipt of your report within **48 hours**.
* We will provide an estimated timeline for a fix within **1 week**.
* We will notify you once the vulnerability has been patched.

## Security Architecture & Scope

This project uses a **Client-Side Architecture** hosted on GitHub Pages with a **Supabase** backend.

### Known Public Keys
The following keys found in `index.html`, `catalog.html`, or `config.js` are **intended to be public**:
* `SUPABASE_URL`
* `SUPABASE_KEY` (The `anon` / `public` key)

**This is not a vulnerability.** Security is handled via **Row Level Security (RLS)** policies on the Supabase database itself, which restrict unauthorized data modification or deletion.

### Out of Scope
* Attacks requiring physical access to a user's device.
* Social engineering attacks against users.
* "Self-XSS" (pasting malicious code into your own console).
* Reports indicating that the `anon` key is visible (this is by design).

## Acknowledgements
We appreciate the efforts of security researchers who help keep our project safe. If your report leads to a valid security fix, we will gladly acknowledge your contribution (unless you prefer to remain anonymous).
