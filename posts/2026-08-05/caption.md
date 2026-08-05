# Post Pack — 2026-08-05

**Template:** Compare  
**Series:** Authentication Basics  
**Graphic:** `graphic.png`

---

## Caption (copy-paste to LinkedIn)

Most developers know how to issue a JWT.

Fewer handle **token lifetime** correctly.

Here’s the difference:

**Access token**
→ Short-lived
→ Sent on every API request
→ Proves who you are
→ If leaked, the damage window is small

**Refresh token**
→ Longer-lived
→ Stored securely (httpOnly cookie / secure store)
→ Only used to mint new access tokens
→ Never sent to normal APIs

How they work together:
Login → get both → call APIs with access → refresh when access expires

Rule I follow in Node/Koa backends:
**Short access. Long refresh. Rotate both.**

If this helped, save it for your next auth setup.

---

What’s your access token expiry in production — 5 min, 15 min, or longer?

#NodeJS #KoaJS #TypeScript #WebSecurity #JWT #BackendDevelopment #FullStackDeveloper

---

## Alt text (for LinkedIn accessibility)

Infographic comparing access tokens and refresh tokens in JWT authentication. Access tokens are short-lived and sent on API requests. Refresh tokens are long-lived, stored securely, and used only to get new access tokens. Footer: Mujtaba Bukhari, Backend Focused Full Stack Developer.
