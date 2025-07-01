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
This page highlights security vulnerabilities and bugs I have discovered, including those reported through bug bounty programs and responsible disclosure to vendors.
</div>

<!-- Add your detailed bug discovery content here, e.g., bug titles, affected systems, dates, and outcomes. -->

<div style="margin-bottom: 2em;"></div>
<div>
  <b>Misinforming Users: Location Permission Misleading in Wear OS</b><br>
  <i>Reported to Google, acknowledged with a bug bounty</i>
  <br><br>
  <b>Description:</b><br>
  We discovered that the location permission prompt shown during the pairing process on Wear OS 2 misinforms users. When a user installs a fitness tracking app that requires location permission on both the wearable and its companion app, the system prompt suggests that location data will only be used on the wearable. However, even if the user denies location permission on the phone, the companion app can still access and transmit location data from the wearable to the Internet, misleading users about their privacy.
  <br><br>
  <b>Impact:</b><br>
  Users may believe that denying location permission on their phone prevents any location data from being transmitted, but due to cross-device sensitive data flows, the data remains accessible and can be sent from the wearable. This undermines user consent and privacy expectations.
  <br><br>
  <b>Technical Details:</b><br>
  - The location prompt during the pairing process (see Figure 1 below) does not accurately reflect the data flow between devices.<br>
  - Even after revoking location permission on the phone (see Figure 2), the wearable can transmit location data via Bluetooth or Wi-Fi.<br>
  - We developed a proof-of-concept app demonstrating this issue, and Google confirmed the finding.
  <br><br>
  <b>Figures:</b><br>
  <img src="/assets/images/figure1_wearos_location_prompt.jpg" alt="Wear OS Location Prompt Misinforming Users" style="max-width: 400px; margin: 1em 0;"><br>
  <i>Figure 1: The location prompt shown on Wear OS 2 at the pairing process misinforms the users.</i>
  <br><br>
  <img src="/assets/images/figure2_wearos_location_toggle.jpg" alt="Wear OS Location Toggle" style="max-width: 300px; margin: 1em 0;"><br>
  <i>Figure 2: Location permission toggle on the smartwatch.</i>
  <br><br>
  <b>Disclosure & Outcome:</b><br>
  We responsibly disclosed this vulnerability to Google, who acknowledged the issue and awarded us a bug bounty.
</div>
<div style="margin-bottom: 2em;"></div> 