# Home Assistant Control 1.1.0

## Highlights

- **30-day free trial with every feature.** No email, account or credit card is required. The trial counts only the days on which you actually open the app.
- The launcher, the top bar and the License panel show the remaining trial days.
- Trial state is stored on the store's server and bound to the machine code shown in the app, so changing the system clock, reinstalling or clearing app data does not reset it.
- Offline-first: the first trial check needs internet access; after that the app can be used offline and queued open days are reported the next time the store is reachable.
- After the trial, a one-time machine-bound offline `HAC-` activation code keeps real-device control enabled. Price is shown on the store's purchase page and at checkout.
- Optional uninstall feedback on Windows: the uninstaller opens a short survey page and continues immediately. Close the page to skip; nothing is sent unless you submit it.
- License recovery now works with the checkout email plus the machine code, even without the order number or the original email.
- New English and Chinese screenshots and trial-first storefront copy.

## Install

1. Download `HomeAssistantControl-Setup.exe` and run it. Windows may show a SmartScreen warning because the build is not code-signed.
2. Start the app. The 30-day trial starts automatically and the launcher shows the remaining days.
3. Choose **Run as control center**, select the home network interface and start it.
4. Sign in to your Xiaomi account and import devices.
5. If you want to keep controlling real devices after the trial, buy a license in the store, submit the machine code and activate the returned `HAC-...` code.

## Notes

- Local control works without internet; Xiaomi login/import and SunLogin cloud plugs need internet.
- Compatibility depends on the device model, firmware and the local protocols it exposes.
- The app is an independent product, not affiliated with Xiaomi, Mijia, SunLogin/Oray or the Home Assistant project.
- The current release contains the Windows installer. The macOS build requires developer signing and notarization; contact support if you need it.
