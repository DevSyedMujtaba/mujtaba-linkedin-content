# Post Pack — Day 6 (OAuth vs OpenID Connect)

**Template:** Compare  
**Series:** Security Engineering  
**Graphic:** `graphic.png`  
**Style:** Classic navy / blue / red compare (Day 1 design system)  
**Calendar hook:** OAuth authorizes access. OIDC answers *who* the user is.

---

## Caption (copy-paste to LinkedIn)

Most developers use “Login with Google”.

Fewer know the difference between **OAuth** and **OpenID Connect**.

They work together — but they solve different problems.

**OAuth = Authorization**
→ Gives an app permission to access data  
→ Uses scopes like `read:email` or `write:files`  
→ Issues access tokens for APIs  
→ Does NOT tell you who the user is  

**OIDC = Authentication**
→ Built on top of OAuth 2.0  
→ Adds an ID Token (JWT) with user claims  
→ Answers: who just logged in?  
→ Used for SSO / Login with Google / Login with GitHub  

Simple check:
→ “Can this app access my Drive?” = OAuth  
→ “Is this Mujtaba?” = OIDC  

How it works in real apps:
User clicks Login → consent screen (OAuth scopes) → ID Token returned (OIDC) → your backend creates a session / user record

Rule I follow in Node/Koa backends:
**Use OAuth for access. Use OIDC for identity.**

If you're building SaaS login, you almost always need both.

Save this for your next auth setup.

Which one confused you longer — OAuth or OIDC?

#SoftwareEngineering #Programming #Coding #Developer #Tech
#BackendDevelopment #NodeJS #TypeScript #JavaScript #WebDevelopment
#CyberSecurity #OAuth #API #SystemDesign #FullStackDeveloper
#SoftwareDeveloper #CloudComputing #DevOps #CareerGrowth #LearnToCode

---

## Alt text

Infographic comparing OAuth and OpenID Connect. OAuth is authorization for accessing resources with scopes and access tokens. OIDC is authentication built on OAuth that returns an ID Token identifying the user. Footer: Mujtaba Bukhari, Backend Focused Full Stack Developer.
