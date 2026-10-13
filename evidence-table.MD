# Proposal: Carrier-Density Reporting for Photonic-Grade Graphene

**Status: work in progress.** This is a developing standards proposal with a supporting evidence annex, compiled with AI assistance and **pending a human archive pass**. No item is closed until that pass is complete.

## The proposal

Extend IEC TS 62607-6-10, or add a companion part, so that graphene films intended for photonic use report:

1. **Carrier density and mobility separately**, not only sheet resistance.
2. **For electrical methods, a measured gate capacitance and the test structure used**, rather than an assumed dielectric constant.
3. **Interband absorption at the operating wavelength** (e.g. 1550 nm), with the assumed Fermi velocity stated.

## Why

At 1550 nm, graphene's interband absorption is Pauli-blocked once |E_F| exceeds about 0.40 eV (≈1.2×10¹³ cm⁻²). Published wafer-scale processes leave residual doping anywhere from near zero to about 2×10¹³ cm⁻², and at least two sit at or across that edge before any gate is applied. Existing standards cover structure (ISO/TS 21356 series) and sheet resistance (IEC TS 62607-6-10), but none specifies carrier density, Fermi level, or absorption at the operating wavelength.

## Kill conditions

The proposal is unnecessary if any of these holds. Status is as of Oct 2026, pending archive pass.

| | Kill condition | Status | Who can check |
| --- | --- | --- | --- |
| K1 | An existing or in-progress IEC/ISO deliverable already specifies carrier density or Fermi level for graphene films | Not met in published standards or the ISO/TS 21356-2 scope; in-progress work programmes unknown | A TC 113 / TC 229 member |
| K2 | Residual-doping spread across realistic processes is small relative to photonic device tolerance | Not met: Wu 2023 (300 mm) and Murros 2026 (Run 7) sit at or across the 1550 nm edge | Literature (done); device groups for tolerance |
| K3 | No method can deliver carrier density reproducibly at wafer scale | Not met: THz n/μ mapping (Buron 2015) and measured-capacitance GFET maps (Murros 2026) exist | Literature (done) |
| K4 | No volume buyer needs photonic-grade graphene specifications | Weak evidence against: 300 mm pilot-line modulators and dedicated graphene-photonics fabs; not decisive | Industry |

## Contents

| File | What it holds |
| --- | --- |
| [`index.html`](index.html) | The proposal as a readable page (GitHub Pages) |
| [`evidence-table.md`](evidence-table.md) | Annex A: standards baseline, evidence table, method comparison, open items |
| [`data/residual_doping.csv`](data/residual_doping.csv) | Every quoted doping value with source, method and conditions |
| [`references.csv`](references.csv) | All references with identifier, verification route, and DOI-gate status |

## Verification state

- DOI gate: all cited references pass (see `references.csv`). Three DOIs (Buron, Wu, Yusuf) came from citing papers rather than direct resolution; click each once before deployment.
- One source (Ge(110)/Si growth, 2023) failed the gate and is excluded.
- The 1550 nm edge is computed: E_F = ħv_F√(πn), v_F = 10⁶ m/s, thermal broadening and Fermi-velocity renormalization ignored.
- Doping values come from Raman, Hall and field-effect methods and are compared for scale only.

*Work in progress. Last updated Oct 12, 2026.*
