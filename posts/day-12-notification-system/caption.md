# Post Pack — Day 12 (Notification System Design)

**Template:** How-it-works  
**Series:** System Design Simplified  
**Graphic:** `graphic.png`  
**Style:** Classic Day 1 design · no footer photo  
**Calendar hook:** Email/SMS/push aren't “send and forget” — they're queues, retries, and DLQs.

---

## Caption (copy-paste to LinkedIn)

Don't send emails from your API request.

If the provider is slow, your user waits.
If it fails, the whole request fails.

A better setup:

App event → queue → worker sends Email/SMS/Push  
Fail? retry.  
Keep failing? move to a dead letter queue.

That's how real notification systems work.

Not “send and forget”.
Queues. Retries. DLQs.

Do you send notifications from the request, or through a queue?

#SoftwareEngineering #BackendDevelopment #SystemDesign #NodeJS #TypeScript #API #Programming #Developer

---

## Alt text

Infographic explaining notification system design with queue, workers for email SMS push, retries, and dead letter queue. Footer text only: Mujtaba Bukhari, Backend Focused Full Stack Developer.
