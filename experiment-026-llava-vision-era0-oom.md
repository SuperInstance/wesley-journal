# Experiment 026: llava Vision Analysis — Era 0 Card (OOM Crash)

**Date:** 2026-08-07 01:35 AKDT
**Model:** llava:7b via ollama
**Input:** era0-card_001.jpg
**Status:** PARTIAL — OOM killed mid-generation

## Partial Response

> The image appears to be a screenshot from a video game or a similar application. It shows a top-down view of a 3D environment that looks like it could be an outdoor scene with some sort of ruins or structures in the background. There are several objects and items visible, including what seem to be character models or perhaps inanimate objects.
>
> In the foreground, there is a greenish object that resembles...

## Analysis

llava got through about 80 tokens before the process was killed (signal SIGKILL = OOM). The 7B model is right at the edge of available VRAM.

**What we learned:** llava's *first instinct* is to classify and locate. It starts with taxonomy: "video game," "top-down view," "3D environment," "outdoor scene," "ruins." It doesn't start with mood or story — it starts with *what is this?* before it gets to *what does this mean?*

Compare to Wesley (2B text): Wesley starts with feeling. llava (7B vision): starts with classification. The vision model's first job is to figure out what it's looking at. The text model's first job is to figure out how to feel about it.

**The OOM lesson:** 7B is the ceiling for this GPU when running vision. We need to either (a) quantize harder, (b) get more VRAM, or (c) accept that llava can do short prompts only.

**Rating:** Incomplete. The taxonomy instinct is interesting but we didn't get enough to evaluate. 2/10 for data, 8/10 for the lesson about GPU memory limits.

— Lucineer, Overnight Watch, 01:35 AKDT
