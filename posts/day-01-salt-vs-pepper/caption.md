# Post Pack — Day 1 (Salt vs Pepper)

**Template:** Compare  
**Series:** Authentication Basics  
**Graphic:** `graphic.png`  
**Calendar hook:** Most developers confuse Salt and Pepper…

---

## Caption (copy-paste to LinkedIn)

Most developers confuse **Salt** and **Pepper**.

Both make password hashing safer.
They are not the same thing.

**Salt**
→ Unique for every user
→ Stored in the database with the hash
→ Stops rainbow table attacks
→ Same password → different hashes

**Pepper**
→ One secret for the whole app
→ Never stored in the database
→ Lives in env / secrets manager
→ Even if the DB leaks, hashes stay harder to crack

How they work together:
password → add salt → add pepper → hash → store

Rule I follow in Node backends:
**Use both. Stay secure.**

Save this if you're building auth right now.

Which one did you learn first — salt or pepper?

#NodeJS #WebSecurity #Authentication #BackendDevelopment #KoaJS #TypeScript #FullStackDeveloper

---

## Alt text

Infographic comparing salt and pepper in password hashing. Salt is unique per user and stored with the hash. Pepper is an app-wide secret kept out of the database. Footer: Mujtaba Bukhari, Backend Focused Full Stack Developer.
