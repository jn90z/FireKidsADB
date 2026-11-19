# Amazon Appstore submission preparation

App: FireKidsADB
Package ID: `com.jn90z.firekidsadb`
Platform: Fire OS / Android
Price: Free (planned)

## Before submission
- [ ] Verify debug APK builds and runs on Fire OS 8 (API 30)
- [ ] Implement and test authenticated ADB backend (not present yet)
- [ ] Verify whether Amazon Kids can approve and launch the Appstore-distributed package
- [ ] Evaluate Amazon Appstore content policy and whether ADB functionality is appropriate for Kids
- [ ] Create release keystore **locally**, retain it securely, never commit it
- [ ] Create signed release APK
- [ ] Produce original app icon and screenshots
- [ ] Prepare accurate privacy policy and data-safety disclosures
- [ ] Test supported devices and review submission requirements in developer console

## Current security model
The app accepts a single allowlisted Daylio activity command, not arbitrary shell text.
The current implementation calls Android `startActivity` and **does not execute ADB**.
Do not describe the current prototype as an ADB shell client in an Appstore listing.
