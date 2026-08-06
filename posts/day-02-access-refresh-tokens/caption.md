# Post Pack — Day 2 (Access + Refresh Tokens)

**Template:** Compare  
**Series:** Security Engineering  
**Graphic:** `graphic.png`  
**Calendar hook:** Short-lived proof vs long-lived renewer — get lifetime wrong and security breaks.

---

## Caption (copy-paste to LinkedIn)

Most apps issue a JWT.

Fewer handle **token lifetime** correctly.

Get this wrong and security breaks in production.

**Access token**
→ Short-lived (minutes)
→ Sent on every API request
→ Proves who you are *right now*
→ If stolen, the damage window is small

**Refresh token**
→ Longer-lived (days/weeks)
→ Stored securely (httpOnly cookie / secure store)
→ Only used to mint new access tokens
→ Never sent to normal business APIs

How production auth usually works:
Login → issue both → call APIs with access → refresh when access expires

Rule I follow in Node/Koa backends:
**Short access. Long refresh. Rotate both.**

Save this if you're designing auth for a SaaS product.

What’s your access token expiry in production — 5 min, 15 min, or longer?

#NodeJS #KoaJS #TypeScript #WebSecurity #JWT #BackendDevelopment #SystemDesign #FullStackDeveloper

---

## Alt text

Infographic comparing access tokens and refresh tokens in production authentication. Access tokens are short-lived and sent on API requests. Refresh tokens are long-lived, stored securely, and used only to get new access tokens. Footer: Mujtaba Bukhari, Backend Focused Full Stack Developer.
