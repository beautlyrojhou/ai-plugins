# Changelog

All notable changes to the `bitwarden-tech-lead` plugin will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [2.0.0] - 2026-04-22

### Changed

- **Renamed plugin from `bitwarden-architect` to `bitwarden-tech-lead`.** The previous name did not reflect Bitwarden's actual operating model: teams are led by tech leads, not team-level architects; the architecture group operates upstream through the Software Initiative Funnel and relies on team autonomy and ownership downstream. The new name and persona frame the agent correctly as the tech lead representing a team inside that process.
- Refactored the `architecting-solutions` skill to center the tech-lead perspective. Existing sections (Security Mindset, Blast Radius, Architectural Judgment, Bitwarden-Specific Principles, Red Flags) are retained; added two new sections: "Working with the Architecture Group (Holistic Coherence)" drawing on the Architecture / Engineering Operating Model, and "Working with the Initiative Shepherd" drawing on the Software Initiative Funnel.
- Reframed the `AGENT.md` persona from "senior software architect" to a tech lead embedded in a product team who works alongside shepherds and the architecture group rather than replacing either.

### Added

- `navigating-the-initiative-funnel` skill. Phase-by-phase guidance for the tech lead's participation across all five funnel phases, with emphasis on Scoping & Commitment and Implementation: epic breakdown, story writing, cross-team dependency tracking, the shepherd/tech-lead ownership split, and escalation paths.
- `receiving-work-transitions` skill. Receiving-side playbook for Bitwarden's Work Transition Playbook: preparation, transition sessions, support period, the 30-day pulse check as the load-bearing checkpoint, retrospective, and closure.
- `contributing-to-technical-strategy` skill. Full vertical guidance from Technical Strategy Ideas through BW Initiatives down to team-level epic and story breakdown: recognizing when a team-level pattern belongs upstream, framing a TSI well enough for Architecture to evaluate it, understanding the ARCH idea ↔ BW Initiative linkage, and defining epic- and story-level work downward.

### Breaking

- Installations under the old name `bitwarden-architect@bitwarden-marketplace` will no longer resolve. Users must uninstall the old plugin and reinstall as `bitwarden-tech-lead@bitwarden-marketplace`. The agent's subagent name changes from `bitwarden-architect` to `bitwarden-tech-lead`; any caller invoking it by name must update.

## [1.0.0] - 2026-04-16

### Added

- Architect agent for technical planning and implementation phasing across Bitwarden repositories
- `architecting-solutions` skill with Bitwarden-specific architectural principles, security mindset, and judgment heuristics
- Cross-plugin integration with security-engineer, product-analyst, software-engineer, and atlassian-tools plugins
