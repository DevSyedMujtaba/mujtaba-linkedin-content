# Post Pack — Day 9 (Rate Limiting Algorithms)

**Template:** Compare  
**Series:** System Design Simplified  
**Graphic:** `graphic.png`  
**Status:** Ready for tomorrow  
**Calendar hook:** Fixed-window limits lie under burst traffic.

---

## Caption (copy-paste to LinkedIn)

Fixed-window rate limits look fine in demos.

They lie under burst traffic.

**Fixed Window**
→ Count requests in a clock window (e.g. per minute)  
→ Counter resets hard at the boundary  
→ Easy to build  
→ Problem: users can burst at the edge of two windows  

Example:
100 requests at 00:59  
+ 100 requests at 01:00  
= 200 requests in ~2 seconds  
…while your “limit” was 100/minute.

**Token Bucket**
→ Tokens refill at a steady rate  
→ Each request spends one token  
→ Short bursts are allowed  
→ Sustained abuse still gets blocked  

This matches real API traffic much better.

**Rule of thumb**
→ Fixed window = simple internal tools  
→ Token bucket / sliding window = public APIs  

In Node/Koa backends (and at the API gateway), I care more about the **traffic shape** than the simplest counter.

Rate limiting isn't just “max 100 requests”.
It's choosing the algorithm that won't surprise you in production.

Save this for your API design notes.

Which one do you use today — fixed window, sliding window, or token bucket?

#SoftwareEngineering #Programming #Coding #Developer #Tech
#BackendDevelopment #NodeJS #TypeScript #JavaScript #WebDevelopment
#SystemDesign #API #CloudComputing #FullStackDeveloper #DevOps
#SoftwareDeveloper #Architecture #CyberSecurity #CareerGrowth #LearnToCode

---

## Alt text

Infographic comparing fixed window and token bucket rate limiting. Footer text only: Mujtaba Bukhari, Backend Focused Full Stack Developer.
