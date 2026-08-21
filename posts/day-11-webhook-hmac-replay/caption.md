# Post Pack — Day 11 (Webhook HMAC + Replay)

**Template:** Code tip  
**Series:** Security Engineering  
**Graphic:** `graphic.png`  
**Style:** Classic Day 1 design · no footer photo  
**Calendar hook:** Signature checks without timestamp/nonce checks still get replayed.

---

## Caption (copy-paste to LinkedIn)

Checking the webhook signature isn't enough.

Someone can capture a valid webhook and send it again later.
Your API will accept it if you only verify HMAC.

You also need:
→ a timestamp (reject old requests)
→ an event ID / nonce (reject duplicates)

HMAC says: this came from Stripe/GitHub/etc.
Timestamp says: this isn't a replay from yesterday.

I see this miss a lot in Node backends.

Do you check timestamps on webhooks, or only the signature?

#SoftwareEngineering #BackendDevelopment #NodeJS #WebSecurity #API #CyberSecurity #TypeScript #Programming

---

## Alt text

Infographic on webhook HMAC and replay protection. Shows that signature verification alone is not enough; timestamp and event ID checks are also required. Footer text only: Mujtaba Bukhari, Backend Focused Full Stack Developer.
