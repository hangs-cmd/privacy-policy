# LumaBeat Privacy Policy

Last updated: May 20, 2026 · Effective date: May 20, 2026

LumaBeat (the "App") provides wellness reference metrics such as heart rate (BPM), HRV, and signal quality using a smartphone camera. This Privacy Policy explains what information the App processes, how it is used and protected, and what rights you have.

The App is not a medical device. Measurement results are not intended to diagnose, treat, prevent, or monitor any disease or medical condition, and they should not be used for emergency decisions. If you have health concerns or are worried about your results, please consult a qualified healthcare professional.

## 1. Information We Process

### Camera Data

The App uses the front camera to analyze subtle facial color changes in real time. The App **does not save camera videos, photos, or face images, and does not transmit them externally**. Camera input is processed on the device to calculate wellness reference metrics.

### Health and Wellness Measurement Data (stored on device)

The App stores the following measurement data **on your device** to show your history and charts:

- Heart rate (BPM)
- HRV-related metrics (SDNN, RMSSD, pNN50, LF/HF, respiratory rate)
- Signal Quality Index (SQI and 4 components: SNR, IBI regularity, spectral purity, amplitude stability)
- Measurement time and elapsed duration
- PPG waveform, IBI series, and FFT spectrum
- Lighting profile (normal/dim/bright/warm/cool) and measurement quality information

This data is not a medical record. It is used to display reference history and charts within the App.

### Settings and App Preference Data

The App stores settings required for App functionality on the device, such as language preference, onboarding completion, notification settings, and data-sharing consent state.

### Advertising and Third-Party SDK Data

The App uses third-party SDKs such as Google AdMob and Google User Messaging Platform to provide advertising and consent management. These SDKs may process information such as device identifiers, advertising identifiers, approximate location, ad interaction data, and diagnostic information according to their own policies.

The App does not sell or share health measurement data for personalized advertising purposes.

## 2. How We Use Information

- To provide camera-based wellness measurement features
- To calculate heart rate, HRV, signal quality, and related results
- To show measurement history, charts, and detailed analysis
- To save App settings
- To transmit anonymized measurement data to the cloud for algorithm improvement, only when you explicitly opt in
- To show ads and manage privacy choices
- To improve App stability and manage remote configuration

## 3. Cloud Transmission (Opt-in)

**By default, health measurement data is stored only on your device and is not transmitted externally.**

Within **Settings → Data Sharing**, you can individually enable the following toggles:

| Toggle | Destination | Data Sent |
|--------|-------------|-----------|
| Usage Analytics | Google Firebase | Measure start/complete/cancel events, BPM/SQI buckets, lighting profile, ad impression events, anonymous instance id |
| Health Diagnostics | Supabase | BPM, HRV, SQI, lighting profile, device model family, anonymous install_id, etc. |
| Crash Reporting (Crashlytics) | Google Firebase | Crash stack traces, measurement phase, device model family, anonymous install_id |

When uploading, the App **never transmits device identifiers such as IMEI, advertising ID, or serial numbers**. Device model and OS information is bucketed at a coarse level to prevent re-identification.

Each toggle can be turned off at any time. Turning it off immediately stops further uploads of new data.

### Tier 3 — Raw Signal Report (separate consent)

Tapping the **"Is this measurement inaccurate?"** button on the result screen opens a separate consent dialog. Only with your explicit consent for that specific measurement, the PPG waveform (~15 seconds), FFT spectrum, and IBI series are uploaded to Supabase Storage.

If you do not submit a report, no raw signal is ever transmitted.

## 4. International Data Transfer Disclosure

### Supabase Inc. (Health Diagnostics + Raw Signal Reports)

| Field | Details |
|-------|---------|
| Recipient | Supabase Inc. (US entity) |
| Country | Singapore (Southeast Asia, ap-southeast-1 region) |
| When and How | When you opt into "Health Diagnostics" or submit an inaccuracy report, data is transmitted at measurement end via HTTPS (TLS 1.2+) |
| Items | (Tier 1) BPM, HRV, SQI, lighting profile, measurement timestamp (UTC), device model family, OS major version, app version, country code, anonymous install_id (UUID v4) <br> (Tier 3 reports) Additionally: PPG waveform, FFT spectrum, IBI series, optional user free-text reason |
| Retention | (Tier 1) Retained until you execute "Delete My Cloud Data"; permanent deletion is immediate <br> (Tier 3) 90 days from upload, or immediate when "Delete My Cloud Data" is executed |
| Right to Object | Consent can be withdrawn at any time in Data Sharing settings. New uploads stop immediately upon withdrawal |

### Google LLC (Firebase Analytics / Crashlytics)

| Field | Details |
|-------|---------|
| Recipient | Google LLC (US entity) |
| Country | United States and Google global infrastructure (locations may vary per Google policy) |
| When and How | When you opt into "Usage Analytics" or "Crash Reporting", events are transmitted via HTTPS as they occur |
| Analytics items | Measurement start/complete/cancel events, BPM/SQI buckets, lighting profile, consent changes, ad impression events, anonymous instance id |
| Crashlytics items | Crash stack traces, measurement phase, last lighting profile, device model family, OS version, app version, anonymous install_id |
| Not collected | Advertising identifiers (AAID/IDFA), precise location, contacts, etc., are never transmitted |
| Retention | Per Google Firebase policy (Analytics: default 14 months, Crashlytics: 90 days). Uploads stop upon consent withdrawal |
| Right to Object | Consent can be withdrawn at any time in Data Sharing settings |

## 5. Retention and Deletion

- Measurement data stored on your device is deleted when you delete App data or uninstall the App.
- Anonymized data uploaded to the cloud can be **immediately and permanently deleted** through **Settings → Data Sharing → "Delete My Cloud Data"** in the App. A new anonymous ID is issued at the same time so the deletion severs any link with previous records.

## 6. Children's Privacy

LumaBeat is not directed to children under 14 (or the equivalent age in your jurisdiction) and we do not knowingly collect personal information from such children. If we become aware that such data has been collected, we will delete it promptly.

## 7. Your Rights

You may exercise the following rights:

- Withdraw consent for data processing (Settings → Data Sharing)
- Immediately delete cloud-synced data (Settings → Data Sharing → "Delete My Cloud Data")
- Request restriction, objection, or access (via the contact below)

## 8. Security

LumaBeat uses reasonable technical and organizational measures to help protect user data, including on-device storage, HTTPS/TLS 1.2+ encryption in transit, server-side Row Level Security (RLS) policies, and the use of anonymous identifiers. However, no method of transmission over the Internet or electronic storage is completely secure.

## 9. Changes to This Privacy Policy

This Policy may be updated to reflect changes in App features, laws, regulations, or store policies. If there are material changes, we will provide notice in-app or through this page at least 14 days before the effective date.

## 10. Contact

| Field | Details |
|-------|---------|
| Developer / Company | Dotliner Lab |
| Email | admin@dotlinerlab.com |
| Privacy Policy URL | https://github.com/hangs-cmd/privacy-policy/blob/main/lumabeat/privacy_policy_en.md |
