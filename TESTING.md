# AI TESTING

## Real Devices

- https://github.com/openclaw/Peekaboo

### Cloud

- https://www.browserstack.com/app-live
  - https://github.com/browserstack/mcp-server
- https://www.testmuai.com/list-of-real-devices/

## WebKit

- https://playwright.dev/docs/browsers#webkit

| Feature / Aspect | Playwright WebKit | Real iOS Safari |
| :--- | :--- | :--- |
| **Core Engine** | Open-source WebKit (Desktop build) | Apple WebKit (iOS native build) |
| **OS Environment** | Windows, Linux, macOS | iOS / iPadOS only |
| **GPU & Rendering** | Desktop graphics / Software emulation | Apple Metal API / Mobile GPU |
| **Mobile UI Elements** | None (Static viewport size) | Dynamic address bar & bottom sheet |
| **Scroll & Touch** | Synthetic events (No momentum scroll) | Native touch layer & inertia scrolling |
| **Fonts & Layout** | Desktop font smoothing, static CSS units | Mobile font anti-aliasing, dynamic units (`svh`) |
| **Best Used For** | Fast, scalable E2E logic & functional tests | Final visual regression & real-device validation |
