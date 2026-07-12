# DONE: Strengthen Radiation Oncology Clinical Foundations

**Section:** `fundamentalRO/`
**Priority:** High
**Owner:** Codex
**Opened:** 2026-07-11
**Completed:** 2026-07-12

## Gap

`fundamentalRO/fundamentalRO.md` is a useful outline, but its current length and three-source evidence base are too compressed to give a non-radiotherapy reader the clinical mental model needed for the AI chapters. It introduces dose, targets, fractionation, and the treatment pathway, but gives limited treatment of clinical intent, prescriptions, modality and technique selection, immobilization and motion, dose calculation and optimization, brachytherapy and systemic radionuclide therapy, toxicity and outcomes, or how professional roles and safety barriers interact.

Without this foundation, readers can understand model outputs while missing what those outputs mean clinically, which uncertainties matter, and why apparently small errors may have very different consequences.

## What Is Needed

1. Expand the clinical pathway from consultation and staging through simulation, prescription, contouring, planning, approval, image guidance, delivery, adaptation, follow-up, and survivorship.
2. Explain treatment intent, fractionation patterns, target and organ-at-risk concepts, dose-volume constraints, and the difference between physical, dosimetric, and biological uncertainty.
3. Compare major delivery modalities and techniques at an introductory level: photons, electrons, protons/heavy ions, brachytherapy, stereotactic treatments, and radiopharmaceutical therapy.
4. Add accessible sections on immobilization, respiratory and organ motion, IGRT, adaptive radiotherapy, dose calculation, treatment delivery, verification, toxicity, and clinically meaningful outcomes.
5. Clarify the responsibilities and handoffs among radiation oncologists, medical physicists, dosimetrists, radiation therapists, radiologists/nuclear-medicine specialists, nurses, and informatics staff, noting jurisdictional variation.
6. Map each later AI application to the clinical decision it supports, the responsible professional, the downstream consequence of error, and the independent safety controls.
7. Source stable concepts from current authoritative textbooks, IAEA/professional-society materials, and consensus nomenclature; keep recent research in the existing currency todo.

## Acceptance Criteria

- [x] A novice can describe the complete radiotherapy pathway and the purpose of each major step
- [x] The chapter distinguishes intent, prescription, fractionation, dose distribution, delivery technique, and biological response
- [x] External-beam photon/electron therapy, particle therapy, brachytherapy, stereotactic therapy, and radiopharmaceutical therapy are introduced with limitations
- [x] Motion management, IGRT, adaptive therapy, verification, toxicity, and follow-up are covered at an introductory level
- [x] Professional roles, handoffs, and independent safety barriers are accurately described and jurisdictional differences are acknowledged
- [x] Every AI role is tied to a clinical decision, accountable user, plausible failure, and downstream effect
- [x] Terminology and claims are supported by authoritative, resolvable sources

## What Was Done

1. Expanded Chapter 3 into a novice-oriented clinical foundation spanning consultation, staging, consent, simulation, contouring, prescription, planning, approval, verification, image guidance, delivery, adaptation, completion, follow-up, and survivorship.
2. Added a terminology table that separates treatment intent, prescription, fractionation, dose distribution, modality/technique, and biological response.
3. Added introductory comparisons and limitations for external-beam photons and electrons, proton/heavy-ion therapy, brachytherapy, stereotactic treatments, and radiopharmaceutical therapy.
4. Added dedicated coverage of immobilization, target/OAR concepts, respiratory and organ motion, dose calculation and optimization, independent checks, IGRT, delivery records, adaptive therapy, toxicity, clinically meaningful outcomes, and longitudinal follow-up.
5. Distinguished physical, dosimetric, and biological/clinical uncertainty and explained why margins, dose engines, and outcome models cannot substitute for one another.
6. Added a jurisdiction-aware professional-role and handoff table covering radiation oncologists, medical physicists, dosimetrists, radiation therapists/radiographers, radiology/nuclear medicine, nursing/allied health, and informatics/IT.
7. Replaced the generic AI-role list with a clinical accountability matrix mapping eight AI task families to the supported decision, accountable user, plausible failure, downstream consequence, and independent safety controls.
8. Expanded the chapter from three to 17 authoritative references spanning IAEA, ICRU, AAPM, ASTRO, NCI, and peer-reviewed consensus/review literature while retaining the existing recent-research entries.

## Verification

- Verified all 17 citation links and reconciled every in-text citation number and URL with the numbered reference list.
- Confirmed every acceptance criterion is represented in a dedicated section, table, or cross-link.
- Ran `git diff --check` and a clean strict Sphinx build with warnings treated as errors.
