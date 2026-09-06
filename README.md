# app-legal

Legal and support pages for apps developed by Woorlds.

## Pages

- Boxday Privacy Policy: https://woorlds.github.io/app-legal/boxday/privacy/
- Boxday App Support: https://woorlds.github.io/app-legal/boxday/support/
- MindTrade Privacy Policy: https://woorlds.github.io/app-legal/mindtrade/privacy/
- MindTrade App Support: https://woorlds.github.io/app-legal/mindtrade/support/
- Putly Privacy Policy: https://woorlds.github.io/app-legal/putly/privacy/
- Putly App Support: https://woorlds.github.io/app-legal/putly/support/
- Lorumi Privacy Policy: https://woorlds.github.io/app-legal/lorumi/privacy/
- Lorumi App Support: https://woorlds.github.io/app-legal/lorumi/support/

## Shared developer website and advertising

Set each app's App Store Connect **Marketing URL** to https://woorlds.github.io/.
Continue using the app-specific privacy and support URLs listed above.

The shared advertising authorization file is maintained in
[woorlds/woorlds.github.io](https://github.com/woorlds/woorlds.github.io) and served
at https://woorlds.github.io/app-ads.txt. Do not add duplicate app-ads.txt files
here or under individual app folders: this project's URL includes `/app-legal/`,
while Google looks at the developer domain root.

Apps using the same AdMob publisher account and network share the same seller
record. Each app still needs its own AdMob registration, ad units, store link,
and readiness review. See the root website repository's README for onboarding
and verification steps.
