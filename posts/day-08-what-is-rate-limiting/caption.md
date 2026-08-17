# Post Pack — Day 8 (What is Rate Limiting)

**Template:** How-it-works  
**Series:** System Design Simplified  
**Graphic:** `graphic.png`  
**Style:** Classic Day 1 design · no footer photo  
**Calendar hook:** Rate limiting protects your API before traffic becomes a problem.

---

## Caption (copy-paste to LinkedIn)

What is **rate limiting**?

It's a safety gate in front of your API.

It controls how many requests a client can make in a given time.

**Example**
→ 100 requests / minute / API key  

If a client goes over the limit:
→ the extra requests are rejected  
→ response: **HTTP 429 Too Many Requests**

**Why it matters**
→ Protects your server from traffic spikes  
→ Stops abuse and bots from melting your API  
→ Keeps the service fair for real users  
→ Protects your database behind the API  

**Without rate limiting**
One noisy client (or attack) can take everyone down.

**With rate limiting**
Excess traffic gets blocked at the edge — before it becomes an outage.

In Node/Koa backends (and API gateways), rate limiting is one of the first production controls I add for public APIs.

Tomorrow: the algorithms behind it (Fixed Window vs Token Bucket).

Save this if you're building APIs.

Is rate limiting already enabled on your public endpoints?

#SoftwareEngineering #Programming #Coding #Developer #Tech
#BackendDevelopment #NodeJS #TypeScript #JavaScript #WebDevelopment
#SystemDesign #API #CloudComputing #FullStackDeveloper #DevOps
#SoftwareDeveloper #Architecture #CyberSecurity #CareerGrowth #LearnToCode

---

## Alt text

Infographic explaining what rate limiting is. Clients send requests through a rate limiter before reaching the API and database. Excess requests return HTTP 429. Footer text only: Mujtaba Bukhari, Backend Focused Full Stack Developer.
