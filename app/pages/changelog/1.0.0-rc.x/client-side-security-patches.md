# ClockUp v1.0.0-rc.3 — Client-Side Security Patches

**Pre-release** · Release Candidate

## Overview

This release continues refining ClockUp ahead of version 1.0.0, focusing on credential handling, client-side resource integrity, email verification, and repository maintenance.

These changes strengthen the project's technical foundation and improve the development workflow as release-candidate testing continues.

## 🔐 Security & Integrity

- **Credential Handling:** Fixed an issue involving client credentials stored on disk, improving credential management.
- **Subresource Integrity (SRI):** Fixed the SRI configuration for MediaPipe Tasks Vision, helping ensure the externally loaded library matches its expected integrity hash.

## ✉️ Authentication Improvements

- **Email Verification Refactor:** Refactored the email OTP verification flow into a dedicated email verification flow, improving organization and clarity in the authentication implementation.

## 🛠️ Repository Maintenance

- **Git Attributes:** Added `.gitattributes` configuration to help manage merge conflicts when integrating changes across the core repository and derived repositories.

## 📌 What This Release Means

This update focuses on reducing technical friction and improving the integrity of ClockUp's authentication and client-side dependencies. Repository-level improvements also help make future updates easier to integrate and maintain.

## ⚠️ Pre-release Status

ClockUp remains in the release-candidate phase. Further testing, fixes, and refinements may be needed before version 1.0.0 is released as stable.

## Release Timeline

### v1.0.0-rc.3 — Security & Maintenance

- Fixed client credential handling.
- Corrected SRI configuration for MediaPipe Tasks Vision.
- Refactored the email verification flow.
- Added Git attributes to help resolve merge conflicts.
