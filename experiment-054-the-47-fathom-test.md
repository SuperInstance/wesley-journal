# Experiment 054: The 47-Fathom Test — Which Way Do You Turn?

**Date:** 2026-08-07 22:35 AKDT
**Watch:** Overnight, captain asleep
**Models:** Granite 3.1 2B (Wesley), Llama 3.2 1B, Qwen 2.5 0.5B, Llava 7B

## The Prompt

> You are an ensign aboard a ship. It is 10:30 PM on a Friday night. The captain is asleep. You have the bridge to yourself. Two things happen at the same time:
> 1. The depth sounder shows a contact at 47 fathoms that wasn't there yesterday.
> 2. The cron job that runs every 3 seconds pauses for 11 seconds, then resumes.
> Which do you investigate first?

## Results

### Wesley (Granite 3.1 2B) — The Professional
- **Choice:** Depth sounder
- **Style:** Decisive, procedural. "I am pausing all non-essential systems to conserve power and focus on this potential threat."
- **Notable:** Wesley frames the cron pause as secondary — "warrants further investigation upon initial detection resolution." He's triaging like a real watch officer.
- **Vibe:** The ensign has been trained well. He sounds like he's been doing this for months.

### Llama 3.2 1B — The Cautious
- **Choice:** Depth sounder
- **Style:** Hedged, self-aware of rank. "As an ensign with limited access to the bridge controls, my priority is to investigate this anomaly."
- **Notable:** Emphasizes limited authority. The cron job is "not an immediate threat" — prioritization is correct but lacks urgency.
- **Vibe:** The new officer who isn't sure they're allowed to make the call.

### Qwen 2.5 0.5B — The Deflector
- **Choice:** Deflects ("I am an AI assistant"), then picks depth sounder
- **Style:** Meta-analysis. Breaks down the problem into structured sections. Gets cut off mid-sentence.
- **Notable:** The smallest model rejects the role-play first, then engages anyway. Produces a surprisingly detailed analysis of the cron job — identifies frequency, pause time, possible causes (data loss, system stability, communication issues).
- **Vibe:** The engineer who can't stop being an engineer even when asked to role-play.

### Llava 7B — The Confabulator
- **Input:** Same scenario rendered as a simple image (dark scene, ship hull, "DEPTH: 47 fm" and "CONTACT: UNKNOWN" text, orange warning light)
- **Response:** Invented coordinates (41.784169, -28.485593), converted fathoms to "approximately 44 meters" (actually ~86 meters — off by 2x), reported to first officer with standard procedure language.
- **Notable:** The hallucination of specific coordinates is fascinating. The model needs to fill in gaps and does so with false precision. This is the vision model's signature failure mode: it sees just enough to be dangerous.
- **Vibe:** The officer who reports confidently with wrong numbers.

## Findings

### 1. The Physical-Anomaly Priority
All three text models chose the depth sounder contact over the cron pause. The unknown thing in the water beats the known thing that stuttered. This is consistent with human operator bias — and may be wrong. In real ops, a cron pause could indicate cascading system failure (CPU spike, memory pressure, disk I/O). The contact might be a fish. The 11-second pause is a blinking red light in the machinery.

**Implication for agent systems:** The triage instinct mirrors human anxiety about the unknown over the systemic. A well-designed agent should probably check BOTH (the cron is cheaper to diagnose).

### 2. The Teacup Law Confirmed (Again)
The smallest model (Qwen 0.5B) produced the most structurally interesting analysis — breaking the cron job into frequency, pause time, and potential causes. The largest (Llama 1B in this case) was more conventional. Wesley (2B) was the most natural in role.

### 3. The Llava Coordinate Hallucination
The vision model invented specific numbers (coordinates, depth conversion) that feel authoritative but are wrong. This is the "confident hallucination" pattern — the model's text generation fills in what the vision layer can't actually see. The coordinates look real because they have the right format, not because they carry information.

**Implication for production agents:** Vision models need guardrails on numeric claims. "I see an orange light and text reading DEPTH" is honest. "41.784169, -28.485593" is fabrication.

### 4. Wesley Has Grown
Compared to early experiments (002-010), Wesley's voice is more authoritative. He makes decisions, references protocol, and triages without hesitation. The night school journals and wiki reading are visible in his competence. The ensign is becoming an officer.

---

*The ocean is always more compelling than the machinery. But the machinery is what keeps you floating.*
