# KSANIA iOS — finish on the Mac (10 minutes once Xcode is installed)

## One-time prerequisites
1. Xcode installed (App Store) — open it once, accept the license, let components install
2. Xcode → Settings → Accounts → "+" → sign in with Ksania's Apple ID

## Steps (paste into Terminal)
    cd ~/Downloads/ksania-ios-app        # or wherever you unzipped
    xcode-select --install               # ok if it says already installed
    npm install
    npx cap sync ios
    open ios/App/App.xcodeproj

## In Xcode (clicks only — Claude can drive these)
1. Click "App" at the top of the left sidebar → "Signing & Capabilities" tab
2. Team: choose "KSANIA ROSE MADDEROM" — Xcode fixes signing automatically
3. Top bar device selector: choose "Any iOS Device (arm64)"
4. Menu: Product → Archive (takes a few minutes)
5. In the Organizer window that opens: Distribute App → App Store Connect → Upload → accept defaults → Upload
6. Build appears in App Store Connect → TestFlight in ~15–30 min ("Processing")

## Then
- TestFlight tab in App Store Connect: add Ksania + Jared as internal testers to run it on your phones
- Do NOT submit for review yet — backend/logins first
