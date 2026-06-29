title: "What I Actually Learned After 6 Months of Exploring AI"date: "2026-01-15"tags: ["AI", "Learning", "Engineering"]image: "https://picsum.photos/seed/aicurious2026/800/600.jpg"excerpt: "Not the hype — the real stuff. Using AI to cross-check circuits, catch edge cases, and think through problems I couldn't solve alone."
What I Actually Learned After 6 Months of Exploring AI
Six months ago I decided to stop reading about AI and start actually using it. Not in the "generate a blog post" sense — in the "can this help me understand a BJT circuit better?" sense. Here's what I found.

AI as a Thinking Partner, Not an Answer Machine
The biggest shift was realizing that AI's value isn't in giving me answers — it's in forcing me to ask better questions. When I'd describe a circuit to an LLM and it'd respond with something slightly wrong, I'd have to articulate exactly why it was wrong. That process of correcting the AI taught me more than the AI itself.

def verify_bjt_bias(vcc, rb, rc, beta, vbe=0.7):    """Calculate and verify BJT operating point"""    ib = (vcc - vbe) / rb    ic = beta * ib    vce = vcc - ic * rc    is_active = vce > vbe    is_saturated = vce < vbe    return {        'ib_ua': round(ib * 1e6, 2),        'ic_ma': round(ic * 1e3, 2),        'vce_v': round(vce, 2),        'region': 'active' if is_active else 'saturation',        'stable': is_active    }
Where AI Genuinely Helped
Cross-checking calculations — Running my math past an AI caught two sign errors in a lab report that I'd missed for hours
Explaining concepts I was stuck on — "Explain MOSFET threshold voltage like I'm an EE student who keeps confusing Vth with Vgs" gave me the analogy that finally clicked
Generating test cases — For my GPA calculator, I asked AI to come up with weird grading scenarios. It found 3 edge cases I hadn't considered
Where AI Failed Hard
Flutter layout code — Consistently suggested deprecated APIs and widgets that don't exist
Resistor value selection — Suggested standard values that would have put my BJT deep into saturation
Security analysis — Gave me a sanitized input function with a regex so trivially bypassable it was almost funny
The Real Takeaway
AI is an incredible tool for curiosity-driven learning — if you already know enough to verify what it tells you. The danger isn't that AI is wrong sometimes. The danger is that it sounds confident when it's wrong. As an engineering student, I'm trained to question everything. That mindset turns out to be the perfect filter for working with AI.

I'm going deeper in 2026 — exploring local models, fine-tuning, and actually understanding what happens inside the neural network. The curiosity isn't slowing down.
