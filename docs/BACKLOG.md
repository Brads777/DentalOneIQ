# DentalOneIQ — Backlog

> Last updated: 2026-04-04

## Completed

- [x] Core provider app with all Weave-competitive features (dashboard, schedule, patients, messages, payments, team chat, voicemail, reviews, phone activity, office hours, lab results, prescriptions, to-do list, emergency calls)
- [x] 5-step user onboarding flow (Verify Info → OTP → Photo → Password → Welcome)
- [x] Three OAuth buttons (Google, Microsoft, GitHub) — UI only
- [x] Full 6-KPI Practice Pulse revenue funnel (Leads → Presented → Accepted → Billed → Collected → Feedback)
- [x] Pushed to GitHub (github.com/Brads777/DentalOneIQ)
- [x] Cloned to F:\DentalOneIQ after E: drive failure
- [x] Deployment files recreated (Dockerfile, nginx.conf, cloudbuild.yaml, landing.html, .dockerignore)

## High Priority — Pre-Beta Launch

- [ ] **Wire OAuth to Supabase** — Connect Google/Microsoft/GitHub OAuth buttons to Supabase auth (shared ToolsIQ auth gateway at auth.toolsiq.ai)
- [ ] **GCP Infrastructure Setup**
  - Create Artifact Registry repo `dentaloneiq` in us-central1
  - Create Cloud Run service `dentaloneiq-beta` in us-east1
  - Configure custom domain mapping: dentaloneiq.toolsiq.ai → Cloud Run
  - Set up Cloud Build trigger on `main` branch push
  - SSL certificate (managed by Cloud Run with custom domain)
- [ ] **Docker test build** — Verify image builds and runs locally before pushing

## Medium Priority — Beta Quality

- [ ] Privacy Policy page at toolsiq.ai/privacy (linked from footer)
- [ ] Terms of Service page at toolsiq.ai/terms (linked from footer)
- [ ] Google Analytics 4 or PostHog for beta usage tracking
- [ ] Error tracking (Sentry or Cloud Error Reporting)
- [ ] robots.txt and sitemap.xml
- [ ] Favicon and app icons (PWA manifest)
- [ ] Accessibility audit — aria labels, keyboard nav, color contrast
- [ ] Performance audit — Lighthouse score baseline
- [ ] In-app feedback widget (beta testers)

## Medium Priority — STT / Dictation Integration

- [ ] **MedASR integration** — Google's medical STT (105M params, 421MB, 4.6% WER on medical terms)
- [ ] **SNODENT vocabulary biasing** — 7,000+ dental terms for immediate accuracy boost
- [ ] **Synthetic dental audio generation** — TTS from dental terminology for training data
- [ ] **Fine-tune MedASR on DGX Spark** — dental-specific vocabulary improvement
- [ ] **Barge-in support** — Silero VAD + sherpa-onnx WebSocket streaming

## Low Priority — Post-Beta Roadmap

- [ ] Backend API for real authentication (replace localStorage demo mode)
- [ ] Database integration (Supabase or Cloud SQL)
- [ ] NexHealth PMS integration for real patient/schedule data
- [ ] Multi-location support
- [ ] AI voice agent integration (VoicesIQ)
- [ ] Patient portal (MyDentalIQ) link-up
- [ ] Feature flags to hide unimplemented features
- [ ] PWA / offline support

## Notes

- Shared onboarding flow with Human Receptionist front desk app (same 5 steps, different role)
- MedASR research completed 2026-04-04: 5x better than Whisper on medical terms, runs on DGX Spark
- E: drive (Temu NVMe) failed 2026-04-04 — all projects migrated to F: + GitHub
