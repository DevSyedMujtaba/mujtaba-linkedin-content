# Post Pack — Day 15 (Pre-signed URLs)

**Template:** Mistake vs Fix  
**Series:** System Design Simplified  
**Graphic:** `graphic.png`  
**Style:** Classic Day 1 design · no footer photo  
**Calendar hook:** A public bucket with obscure URLs is not authorization.

---

## Caption (copy-paste to LinkedIn)

A long random URL is not security.

If your S3 bucket is public and someone shares the link, that file is open forever.

That's not authorization.
That's hoping nobody finds it.

Use a pre-signed URL instead:

→ temporary link  
→ expires after a few minutes  
→ scoped to one file  
→ created by your backend  

Obscure links leak.
Signed links expire.

Are your file links temporary, or permanent?

#SoftwareEngineering #BackendDevelopment #AWS #SystemDesign #NodeJS #TypeScript #API #CyberSecurity

---

## Alt text

Infographic comparing public obscure URLs versus pre-signed URLs for file access. Pre-signed URLs expire and are scoped. Footer text only: Mujtaba Bukhari, Backend Focused Full Stack Developer.
