---
title: "Bugs Discovered"
layout: single
permalink: /bugs/
author_profile: true
classes: wide
---

<style>
.page__title {
    color: #494e52 !important;
    font-weight: bold;
}
.page__content {
    font-size: 1em;
    color: #494e52;
}
</style>

<div class="bugs-intro">
This page highlights security vulnerabilities and bugs we have discovered, including those reported through bug bounty programs and responsible disclosure to vendors, acknowledged by Google with a bug bounty, $500.
</div>

<!-- Add your detailed bug discovery content here, e.g., bug titles, affected systems, dates, and outcomes. -->

<div style="margin-bottom: 2em;"></div>
<div>
  <b>Misinforming Users: Location Permission Misleading in Wear OS</b><br>
  We discovered that the location permission prompt shown during the pairing process on Wear OS 2 misinforms users. When a user installs a fitness tracking app that requires location permission on both the wearable and its companion app, the system prompt suggests that location data will only be used on the wearable. However, even if the user denies location permission on the phone, the companion app can still access and transmit location data from the wearable to the Internet, misleading users about their privacy.
  <div style="text-align:center; margin: 1.5em 0;">
    <img src="/assets/images/figure1_wearos_location_prompt.jpg" alt="Wear OS Location Prompt Misinforming Users" style="max-width: 400px; display: block; margin-left: auto; margin-right: auto;">
    <div style="font-size: 0.95em; color: #555; margin-top: 0.5em;"><i>Figure 1: The location prompt shown on Wear OS 2 at the pairing process misinforms the users.</i></div>
  </div>
  <br>
  <b>Impact:</b><br>
  Users may believe that denying location permission on their phone prevents any location data from being transmitted, but due to cross-device sensitive data flows, the data remains accessible and can be sent from the wearable. This undermines user consent and privacy expectations.
  <br><br>
  <b>Technical Details:</b><br>
  - The location prompt during the pairing process (see Figure 1 above) does not accurately reflect the data flow between devices.<br>
  - Even after revoking location permission on the phone (see Figure 2 below), the wearable can transmit location data via Bluetooth or Wi-Fi.<br>
  - We developed a proof-of-concept app demonstrating this issue, and Google confirmed the finding.
  <div style="text-align:center; margin: 1.5em 0;">
    <img src="/assets/images/figure2_wearos_location_toggle.jpg" alt="Wear OS Location Toggle" style="max-width: 300px; display: block; margin-left: auto; margin-right: auto;">
    <div style="font-size: 0.95em; color: #555; margin-top: 0.5em;"><i>Figure 2: Location permission toggle on the smartwatch.</i></div>
  </div>
  <br>
  <b>Disclosure & Outcome:</b><br>
  We responsibly disclosed this vulnerability to Google, who acknowledged the issue and awarded us a bug bounty.
  <br><br>
  <b>Update in Newer Wear OS Versions:</b><br>
  Android & Wear are working on a platform-level solution highlighted by our paper. For the updates in newer version, please see the <a href="https://developer.android.com/training/wearables/apps/permissions" target="_blank">official Android developer documentation</a>.
</div>
<div style="margin-bottom: 2em;"></div> 