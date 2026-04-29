# GRE Quant Logger — Pro Version

**Coach Aditya Goenka** · goenka.aditya.kol@gmail.com

> ⚠️ This is a licensed product. Access requires a registered email.  
> Purchase at: https://[YOUR-USERNAME].github.io/gre-free/pricing.html

## What's Included (Pro)
- All 88 subtopics across 9 GRE Quant topics
- All 4 difficulty levels (Easy, Medium, Hard, Extreme Hard)
- Unlimited questions per session
- Practice Mode with instant feedback + explanations
- Exam Mode with timed full analysis
- My Progress dashboard
- Send to Tutor

## Access Control
This app uses email + device fingerprint authentication via Cloudflare Workers.  
Students must register with their purchase email to unlock the app.

## File Structure
```
gre-pro/
├── gre_practice_logger_pro.html    ← Main app (auth-gated)
├── pricing.html                    ← Sales page
└── bank/
    ├── index.json                  ← Bank manifest
    └── arithmetic/
        ├── percentages.json
        └── fractions_decimals.json
```

## Adding a New Subtopic
1. Generate questions using the gre-question-gen skill
2. Save JSON to `bank/topic/subtopic.json`
3. Update `bank/index.json` with new entry
4. Update `pricing.html` BANK array (`done: true`)
5. Commit and push — live immediately

## Running Locally (for testing)
```bash
python3 -m http.server 8080
# Open http://localhost:8080/gre_practice_logger_pro.html
```
Auth will call the live Cloudflare Worker — internet required.
