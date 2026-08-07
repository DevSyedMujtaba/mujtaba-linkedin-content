# Post Pack — Day 3 (Refresh Token Rotation)

**Template:** How-it-works  
**Series:** Security Engineering  
**Graphic:** `graphic.png`  
**Style:** Dark charcoal + teal/amber timeline (different from Days 1–2)  
**Calendar hook:** A stolen refresh token shouldn't own the account forever.

---

## Caption (copy-paste to LinkedIn)

A stolen refresh token shouldn't own the account forever.

If your refresh token is long-lived and never rotated, theft = persistent access.

That's why production auth uses **refresh token rotation**.

How it works:

1. Client sends the refresh token  
2. Server validates it + checks for reuse  
3. Invalidate the old refresh token  
4. Issue a new access token + a new refresh token  
5. If an old token is reused → revoke the whole token family  

The key idea:
**Every refresh replaces the refresh token.**  
Reuse detection is how you detect theft.

In Node/Koa SaaS backends, I treat refresh tokens like credentials — not like cached JWTs.

Save this if you're hardening auth.

Do you rotate refresh tokens in production today?

#NodeJS #WebSecurity #JWT #Authentication #BackendDevelopment #KoaJS #TypeScript #SystemDesign

---

## Alt text

Dark timeline infographic explaining refresh token rotation in five steps: send refresh token, validate with reuse detection, invalidate old token, issue new access and refresh tokens, and revoke the token family on reuse. Footer: Mujtaba Bukhari, Backend Focused Full Stack Developer.
