# Carrier-density reporting for photonic-grade graphene

**Status: work in progress.** A standards proposal with a supporting evidence annex, compiled with AI assistance and pending a human archive pass. Values, statuses and references may change. Last revised Nov 3, 2026.

## The proposal

Add a photonic-grade profile, as a companion part or an extension of the IEC TS 62607-6 series (6-10, 6-16, 6-23 and 6-32), so that graphene films intended for photonic use report:

1. **Carrier density and mobility separately**, not only sheet resistance, for pristine graphene on wafer-scale films and device test structures.
2. **For electrical methods, a measured gate capacitance and the test structure used**, rather than an assumed dielectric constant.
3. **Interband absorption at the operating wavelength**, with the assumed Fermi velocity stated.

## Why

At 1550 nm, graphene's interband absorption is Pauli-blocked once the Fermi level exceeds about 0.40 eV, roughly 1.2×10¹³ carriers per cm². Published processes leave residual doping from near zero to about 2×10¹³ cm⁻², so whether a film absorbs at the operating wavelength can depend on ordinary process choices such as transfer method, resist and passivation. Reported values also depend strongly on the test structure and extraction method, which is why items 1 and 2 are paired.

Gated modulators can tolerate part of this at a cost in drive voltage. The case is strongest for devices whose doping is not gate-compensated, where tolerance data is still missing.

## What is in this repository

| File | Contents |
|---|---|
| `index.html` | The proposal page (served via GitHub Pages): proposal, chart, kill conditions, standards baseline, evidence, open items |
| `evidence-table.md` | Full evidence annex with verification status per row |
| `references.csv` | Reference list and DOI-gate status |
| `data/residual_doping.csv` | Values behind the chart |

## Kill conditions

The proposal is unnecessary if any of these holds. Current status, as of Nov 3, 2026:

| ID | Kill condition | Status |
|---|---|---|
| K1 | A standard already specifies carrier density or Fermi level for graphene films | Partly met; the photonic case remains open. IEC TS 62607-6-16:2022 covers carrier concentration by the FET voltage-shift method (semiconducting 2D materials), IEC TS 62607-6-23:2025 covers Hall-bar mobility and sheet resistance, and IEC TS 62607-6-32 (gated TLM, names doping) is in development. None found specifies measured gate capacitance and operating-wavelength absorption for pristine photonic-grade graphene. |
| K2 | Residual-doping spread is small relative to photonic device tolerance | Partly met for gated modulators. Not tested for non-gate-compensated devices. |
| K3 | No method delivers carrier density reproducibly at wafer scale | Not met. THz mapping and measured-capacitance GFET maps exist. |
| K4 | No volume buyer needs photonic-grade graphene specifications | Weak evidence against. Not decisive. |

## How to help

The most useful checks are the ones this repository cannot do on its own:

- **K1:** read IEC TS 62607-6-16, clause 3.2 of 62607-6-23 and the 62607-6-32 draft, and say whether carrier density or doping are reported quantities and whether a measured gate capacitance is required. Members of IEC TC 113 or ISO TC 229 can also give the current stage of 6-32 and say whether other work items touch carrier density or Fermi level.
- **K2:** photonic device groups can say how much residual doping their devices tolerate, especially passive or non-volatile devices without a compensating gate.
- **Evidence:** corrections to any row in the evidence table, and doping data for graphene on ferroelectric HZO, which the search so far has not found.

Please open an issue with the source and, where possible, a DOI.

## Method and limits

- Rows in the evidence table come from published papers and standards listings. Statuses were checked against registry and publisher pages on Nov 3, 2026. Of the standards, only the free preview of IEC TS 62607-6-23 was read (contents, introduction, annex titles); none was read in full.
- Values from different methods (Raman, Hall, field-effect, THz) are compared for scale only. The reported spread mixes process differences with method differences.
- Conversions to carrier density use E_F = ħv_F√(πn) with v_F = 10⁶ m/s and ignore thermal broadening.
- AI assistance was used to search, compile and draft. Nothing here has had a human archive pass yet.

## License

To be added before publication.
