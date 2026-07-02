# SovaKeep Privacy Policy

**Last updated: 2026-07-02**

SovaKeep is an envelope budgeting app. It is designed so that your financial
data stays on your device. This policy explains exactly what data the app
handles, where it lives, and what we do — and don't do — with it.

## The short version

- SovaKeep works fully offline. In the standard (local-only) app, **we collect
  nothing**: no account, no analytics, no tracking, and your data never leaves
  your device unless you export it yourself.
- **No ads. No data selling. Ever.** We do not show advertising, do not sell or
  share your data with anyone, and do not embed analytics or advertising SDKs.
  Builds may include heavily privacy-restricted crash reporting for fixing bugs —
  see "Crash reports and in-app feedback" for exactly what that means.
- A future version may offer an **optional** cloud-sync account. The section
  "Optional cloud sync" below applies only if that feature exists in your build
  and you explicitly turn it on.

## What we collect

In the local-only app: **nothing**. SovaKeep has no servers receiving your
data, requires no account, and does not need bank credentials — there is no
bank linking at all.

## What is stored on your device

All app data is stored locally, in a private SQLite database and app
preferences on your device:

- Budgets, envelopes, accounts, transactions, transfers
- Shopping lists, savings goals, debts, recurring-transaction templates
- App settings (theme, currency, budget configuration)
- A randomly generated internal identifier used only to label your data on
  this device — it is not tied to your identity and is never transmitted

This data is accessible only to the SovaKeep app under standard iOS/Android
app sandboxing. Uninstalling the app deletes it (subject to OS backups below).

## Device backups

Your device's operating system may include SovaKeep's data in its normal
device backup — iCloud backup on iOS, Google Drive Auto Backup on Android.
These backups are managed and encrypted by Apple/Google under your own
account, and you control them in your device settings. SovaKeep does not
operate or have access to these backups.

## Data export

You can export your data as CSV files at any time. Exports are created on your
device and go only where you choose to send or save them. Once exported, the
file is under your control and outside the app's protection.

## Notifications

Reminders (recurring transactions, budget periods, savings goals) use local
notifications scheduled entirely on your device. No push-notification service
or external server is involved in the local-only app.

## Crash reports and in-app feedback

The app includes a crash-reporting library ([Sentry](https://sentry.io)).
Whether it is active depends on the build you have:

- **If the build has no reporting endpoint configured, the library is dormant:
  it collects nothing and sends nothing, ever.** The app never touches the
  network.
- **If crash reporting is enabled in your build:** when the app crashes or hits
  an internal error, a technical report is sent to Sentry so we can find and
  fix the bug. Reports contain the device model, OS version, app version, and
  technical details of the error. They are deliberately restricted: no personal
  identifiers, no screenshots, no request headers or IP-based identification,
  and monetary amounts are scrubbed from every report before it leaves the
  device. A small sample of anonymous performance timings (how long screens
  take to load) may also be sent. We use these reports solely to fix bugs and
  never combine them with any other data.

**In-app feedback:** if you use the "Send feedback" option, your message,
basic device/app information (model, OS version, app version), and a
screenshot only if you explicitly attach one are delivered to us through the
same error-reporting service. We use it solely to handle your feedback. In
builds where reporting is disabled, the feedback form cannot deliver messages —
use the contact channel below instead.

## Optional cloud sync

> **This section applies only when a build of SovaKeep includes cloud sync and
> you have explicitly created an account and turned sync on.** The currently
> shipping version is local-only: it contains no sync capability and bundles
> no cloud credentials, so none of the below applies to it.

If you opt in to cloud sync:

- **Account data:** your email address and a password (handled by our backend
  provider, Supabase) are used to create and authenticate your account.
- **Synced data:** your budget data (the same categories listed under "What is
  stored on your device") is copied to our Supabase-hosted backend so it can
  sync across your devices. It is encrypted in transit and at rest on the
  server, but it is **not end-to-end encrypted** — like most sync services,
  the server can technically read synced data. We do not access it except as
  needed to operate the service.
- **Your controls:**
  - You can **pause sync** at any time; the app keeps working offline.
  - You can **switch back to local-only** in the app. This permanently
    hard-deletes all your synced data from the server (no soft-delete copies
    are kept) and signs you out, while your data stays on your device.
  - You can request **account deletion**, which removes your account and any
    remaining server-side data.
- Local data on your device always remains the source of truth; sync is an
  additive layer you control.

## No ads, no selling, no tracking

- We do not show ads and do not work with advertising networks.
- We do not sell, rent, or trade your data — to anyone, for any purpose.
- We do not use analytics, behavioral tracking, or fingerprinting SDKs. The
  only diagnostic code in the app is the crash reporting described above —
  scrubbed of personal and financial data, and entirely inert in builds where
  it is not enabled.
- We do not share your data with third parties. The only third parties ever
  involved are infrastructure providers acting on our behalf: Sentry for crash
  reports (when enabled) and Supabase for optional cloud sync (when you opt
  in).

## Children

SovaKeep is not directed at children under 13, and we do not knowingly collect
any personal information from anyone — including children.

## Changes to this policy

If we change this policy (for example, when cloud sync ships), we will update
this page and the "Last updated" date. Material changes will be called out in
the app's release notes.

## Contact

Questions about privacy? Open an issue on our support tracker:
<https://github.com/chiffad/sovakeep-legal/issues>.

[← Back](index.html)
