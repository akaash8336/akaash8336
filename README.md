# Akaash Mukherjee

CTO at [Feel Good Interactive](https://playmysh.com). Everything I have written is in private company repos, so the contribution graph below is the activity you can see and this page is the rest.

## What I'm building

[Mysh](https://playmysh.com) is a story game for kids aged 7 to 12. A kid describes a hero in their own words and Mysh turns it into an adventure they steer: every choice shapes the story, they earn gems for traits like bravery and curiosity, and they build their own story worlds. Free, no ads, no in-app purchases. Made in Canada.

I built and run the platform behind it with a small team:

- **The story engine.** An LLM-driven narrative system with separate narrator and referee roles, open-ended chapters, and an ending the kid decides when to take. Playtest robots and tripwire corpora guard story quality in CI.
- **Safety for a kids' product.** A moderation pipeline on both kid input and model output, and a COPPA compliance program with an automated, LLM-run diff gate that reviews every production promotion and blocks the deploy on a new finding.
- **The platform.** A TypeScript monorepo (React, Express, Firestore on GCP, Kubernetes via Helm). Spec-first HTTP APIs (TypeSpec to OpenAPI, enforced at the gateway). Every branch deploys to its own URL with isolated data, and an end-to-end robot plays the game against staging on every merge.
- **Voice, art and languages.** Narrated stories with text-to-speech, generated hero portraits and world art, and the whole game in English, French and Portuguese.
