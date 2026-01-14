# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Static NFC contact card website for Cache River Mill & MetalWorks team members. Hosted on GitHub Pages and designed for NFC tag linking (Android & iOS compatible).

## Technology Stack

- Pure HTML5/CSS (no JavaScript, no build tools)
- vCard 3.0 format for contact files
- GitHub Pages for hosting

## Architecture

Each team member has their own directory containing:
- `index.html` - Responsive contact card page with action buttons (Add to Contacts, Call, Text, Email)
- `contact.vcf` - vCard file for direct contact import

Root level contains the primary contact (Nicolas Wade) plus shared assets like `logo.png`.

**URL Pattern:** `/{person-name}/` routes to individual contact pages via GitHub Pages.

## Adding a New Contact

1. Create a new directory with the person's name (lowercase, no spaces)
2. Copy an existing `index.html` and `contact.vcf` as templates
3. Update the HTML with:
   - Person's name in `<title>` and `<h1>`
   - Organization in `<p>`
   - Phone number in `tel:` and `sms:` links
   - Email in `mailto:` link
   - Path to `contact.vcf`
4. Update the vCard with:
   - `N:` (Last;First format)
   - `FN:` (Full name)
   - `ORG:`, `TEL:`, `EMAIL:`

## Deployment

Push to GitHub and the site auto-deploys via GitHub Pages. No build step required.
