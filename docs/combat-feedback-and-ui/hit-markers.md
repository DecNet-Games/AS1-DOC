---
layout: default
title: "Hit Marker Feedback"
parent: "Combat Feedback & UI"
nav_order: 1
---

# Hit Marker Feedback

`HitMarkerFeedback.cs` gives instant visual and auditory confirmation whenever a player's shot strikes a valid target.

---

## Visual & Audio States

- **Body Hit**: White crosshair tick marks expand outward and fade over `0.12s`. Plays a subtle hit sound.
- **Headshot Hit**: Distinct crimson-red tick marks with `1.4x` scale expansion. Plays an audible critical chime.
- **Kill Confirmation**: Extended red cross with combo registration.
