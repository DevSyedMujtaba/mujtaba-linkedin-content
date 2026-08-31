# Post Pack — Day 14 (File Upload Architecture)

**Template:** How-it-works  
**Series:** System Design Simplified  
**Graphic:** `graphic.png`  
**Style:** Classic Day 1 design · no footer photo  
**Calendar hook:** Streaming uploads through your Node API is how you invent timeouts.

---

## Caption (copy-paste to LinkedIn)

Don't upload files through your Node API.

Client → Node → S3 sounds simple.
But big files make your server slow, eat memory, and time out.

Better flow:

1. Client asks API for an upload URL  
2. API returns a pre-signed URL  
3. Client uploads straight to S3  
4. API only saves the file metadata  

Your backend stays light.
Uploads stay fast.

Do you still pipe files through your API?

#SoftwareEngineering #BackendDevelopment #NodeJS #SystemDesign #AWS #TypeScript #API #Programming

---

## Alt text

Infographic comparing bad file uploads through a Node API versus direct-to-cloud uploads with pre-signed URLs. Footer text only: Mujtaba Bukhari, Backend Focused Full Stack Developer.
