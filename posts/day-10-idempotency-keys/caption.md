# Post Pack — Day 10 (Idempotency Keys)

**Template:** How-it-works  
**Series:** Distributed Systems  
**Graphic:** `graphic.png`  
**Style:** Classic Day 1 design · no footer photo  
**Calendar hook:** Retries are normal. Duplicate charges and duplicate jobs shouldn't be.

---

## Caption (copy-paste to LinkedIn)

Network fails. Client retries.

Without an idempotency key, you might charge the customer twice.

Send a unique key with the request:

`Idempotency-Key: 7f3a9c2e-...`

Same key + same request = same result.
No duplicate payment. No duplicate job.

Stripe does this. Most payment APIs expect it.

If your API handles money or side effects, you need this.

Do you use idempotency keys in your APIs?

#SoftwareEngineering #BackendDevelopment #NodeJS #TypeScript #SystemDesign #API #Programming #Developer

---

## Alt text

Infographic explaining idempotency keys. Client retries a payment with the same key and the server returns the same result without charging twice. Footer text only: Mujtaba Bukhari, Backend Focused Full Stack Developer.
