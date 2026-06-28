# GoTagMe 🚨

A lightweight, zero-dependency panic recovery middleware for Go. Instead of letting your application fail silently or digging through raw server logs, **GoTagMe** catches the panic, structures the stack trace, and sends a styled alert straight to your Discord channel—tagging you directly so you can fix it instantly.

## Features
- 🔄 **Drop-in Middleware:** Seamlessly integrates with `chi`, `gin`, or standard `net/http`.
- 🔔 **Instant Tagging:** Pings your exact Discord User ID when things break.
- 📦 **Custom Context:** Pass a `map[string]any` to attach request IDs, user context, or environmental data to the alert.
- 🕒 **Async & Safe:** Dispatches alerts in a separate goroutine so your HTTP response lifecycle isn't blocked.
- 🛑 **Rate-Limit Safe:** Automatically clips long stack traces to stay under Discord's 2000-character payload limit.
