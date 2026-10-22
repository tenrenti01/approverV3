# DPWH RIS — the approver portal

This repo holds ONE app: the portal where approvers sign slips, and where fuel
attendants scan the QR and release the fuel.

## Put it online

1. New repository -> name it (for example `dpwh-ris-approver`) -> **Public**
   (free GitHub Pages needs public) -> Create.
2. Upload everything in this folder, at the top level. Do not nest it in
   another folder. The page must be a lowercase `index.html`.
3. Settings -> Pages -> Deploy from a branch -> main -> / (root) -> Save.
4. After a minute your address is:

       https://YOURNAME.github.io/dpwh-ris-approver/

## Connect it to Apps Script

The first time someone opens it, the app asks for the APPROVER project's
`/exec` address and the office passcode, with a "Test my link" button. Both are
kept in that browser, so it is asked once per device and never again.

Pasting the Requester address here is caught and refused.

## Nothing to set here for emails

`SITE_URL` belongs in the REQUESTER project only — that is the app that sends
the emails and builds the QR codes.

## Installing it

Open the address and the browser offers to install it as **RIS Approve**, with
its own icon and window. The request form is a separate repo and installs as
its own app.

Approvers still sign in with their own PIN every session. That is deliberate —
a signature should not be one unlocked phone away.

## No secrets live here

The Sheet, the PINs, the signatures and the passcode are all in Apps Script.
Never paste any of them into these files — this repo is public.
