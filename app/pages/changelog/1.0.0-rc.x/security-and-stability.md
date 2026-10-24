# ClockUp v1.0.0-rc.1 — Security & Stability

**Pre-release** · Release Candidate

## Overview

The first update to ClockUp's release candidate focuses on strengthening security, improving attendance reliability, and addressing issues discovered during testing.

This release introduces additional request protections, fixes access-control vulnerabilities, improves attendance exports, and expands end-to-end testing as ClockUp moves closer to its first stable release.

## 🔐 Security Improvements

- **CSRF Protection:** Added middleware to help protect against cross-site request forgery.
- **Request Body Limits:** Introduced middleware to limit request body sizes and reduce exposure to oversized payloads.
- **Upload Validation:** Added safety validation for R2 uploads and improved attendance image size validation.
- **Access Control Fixes:** Addressed insecure direct object reference (IDOR) issues affecting clock-in and clock-out operations.
- **CRUD Ownership Validation:** Improved ownership checks for create, read, update, and delete operations.
- **API Surface Reduction:** Removed the users API endpoint.
- **Email Change Verification:** Fixed email verification behavior when users change their email addresses.

## 🕒 Attendance & Export Fixes

- **Scheduled Attendance Processing:** Fixed an issue with cron jobs affecting attendance records.
- **Excel Export:** Fixed issues with downloading attendance records in XLSX format.
- **Kiosk Role:** Added a dedicated kiosk role to support the system's role configuration.

## ⚙️ Reliability & Testing

- **Database Connection Pooling:** Fixed a database connection pooling leak to improve resource management.
- **End-to-End Testing:** Improved client-side E2E tests to strengthen workflow verification.
- **Development OTP Behavior:** Removed the hardcoded OTP used during development, improving the development authentication workflow.
- **Dependency Maintenance:** Added RenovateBot maintenance to support dependency update management.

## 📌 What This Release Means

This release candidate update prioritizes the reliability and security of ClockUp's core workflows. Alongside attendance and export fixes, the additional protections and access-control corrections help prepare the system for broader real-world use.

## ⚠️ Pre-release Status

ClockUp is still in the release-candidate phase. Testing and refinement are ongoing, and further changes may be introduced before version 1.0.0 is declared stable.

## Release Timeline

### v1.0.0-rc.1 — Security & Stability

- Strengthened request, upload, and access-control protections.
- Fixed attendance processing and Excel export issues.
- Improved database connection management.
- Expanded end-to-end testing.
- Refined email-change verification and development authentication behavior.
