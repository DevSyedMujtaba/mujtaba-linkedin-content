# Post Pack — Day 5 (How JWT Signatures Work)

**Template:** How-it-works  
**Series:** Backend Deep Dives  
**Graphic:** `graphic.png`  
**Style:** Soft slate + cyan diagram (different from Days 1–4)  
**Calendar hook:** A JWT isn't encrypted by default — it's signed. That difference matters.

---

## Caption (copy-paste to LinkedIn)

A JWT is **signed**, not encrypted.

That means:
→ Anyone can read the payload  
→ But nobody can change it without the secret  

A JWT has 3 parts:

`header.payload.signature`

1. Encode header + payload  
2. Sign with the server secret  
3. Server checks the signature on every request  

If the signature doesn't match → reject.

Don't put secrets inside the JWT.
Put only what you're okay exposing.

Save this for your next auth setup.

#SoftwareEngineering #Programming #Coding #Developer #Tech
#BackendDevelopment #NodeJS #TypeScript #JavaScript #WebDevelopment
#CyberSecurity #JWT #API #SystemDesign #FullStackDeveloper
#SoftwareDeveloper #CloudComputing #DevOps #CareerGrowth #LearnToCode

---

## Alt text

Soft slate infographic explaining how JWT signatures work. Shows header, payload, and signature blocks, then four verification steps. Callout notes that signed is not encrypted and secrets should not go in claims. Footer: Mujtaba Bukhari, Backend Focused Full Stack Developer.
