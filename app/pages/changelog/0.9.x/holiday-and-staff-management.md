# PETER — Holiday & Staff Management

**Beta Release** · Internal

## Overview

This release introduces a holidays API and clock presets for staff creation, improving the foundation for holiday-related functionality and making staff configuration more convenient.

It also includes improvements to OTP email templates, fixes to OTP resend behavior, and refinements to client-side rendering and hydration.

## 🗓️ Holidays API

A new API for holidays has been introduced.

- Added endpoints for holiday-related functionality.
- Established an API foundation for retrieving and managing holiday information.
- Prepared the system for future enhancements to holiday-aware attendance workflows.

This provides a foundation for incorporating holidays into attendance management as the system evolves.

## 🕒 Clock Presets for Staff Creation

Staff creation now supports clock presets.

- Added clock presets when adding staff members.
- Simplified the configuration of staff clock settings.
- Improved consistency when configuring staff attendance-related details.

This makes staff setup more convenient by providing preset options instead of requiring every setting to be configured manually.

## ✉️ OTP Email Improvements

The email templates used for one-time passwords (OTPs) have been improved.

- Refined OTP email presentation.
- Improved the consistency of authentication-related emails.
- Made OTP messages clearer and more polished for recipients.

## 🔐 OTP Resend Fix

Fixed an issue involving OTP resend behavior when reloading the client application.

This improves the OTP verification experience and helps ensure that the resend workflow behaves more consistently during page reloads.

## ⚙️ Client-Side Improvements

Client-side rendering and hydration have also been refined.

- Improved hydration behavior using lazy-loaded components.
- Refined how components are loaded and initialized.
- Improved the handling of client-side rendering transitions.

These changes support a more consistent rendering experience as the application grows.

## 📌 What This Release Means

This release expands PETER's supporting attendance functionality through a new holidays API and more convenient staff configuration.

Alongside these additions, authentication email refinements, OTP resend fixes, and client-side improvements help make everyday workflows more consistent.

## ⚠️ Beta Status

PETER remains in beta and is under active development. Features, behavior, architecture, and implementation may continue to change before the eventual `1.0.0` stable release.

## Release Timeline

### Holiday & Staff Management

Introduced a holidays API and clock presets for staff creation, with supporting improvements to OTP emails, verification behavior, and client-side rendering.
