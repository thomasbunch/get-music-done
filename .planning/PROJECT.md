# GMD (Get Music Done)

## What This Is

A fork of [get-shit-done](https://github.com/glittercowboy/get-shit-done) specialized for audio plugin development. GMD extends GSD with agentic testing feedback loops for VST/AU plugins, multi-instance parallel workflows, and tooling optimized for JUCE-based development. All original GSD functionality remains intact — GMD only adds capabilities.

Created by honorr. Full credit to glittercowboy for the original GSD project this builds upon.

## Core Value

Agents that can actually test audio plugins — visual UI inspection, audio output verification, and automated edge case discovery — closing the feedback loop that currently requires manual DAW testing.

## Requirements

### Validated

<!-- Inherited from GSD fork — all existing functionality preserved -->

- ✓ Project initialization workflow — existing
- ✓ Phase planning and execution — existing
- ✓ Parallel agent spawning — existing
- ✓ Verification and gap closure — existing
- ✓ Multi-agent orchestration — existing
- ✓ All 24 slash commands — existing
- ✓ All 11 subagents — existing

### Active

<!-- New GMD-specific capabilities -->

- [ ] Plugin testing agents with visual UI inspection
- [ ] Sample rate/buffer size matrix testing
- [ ] Edge case test generation for plugins
- [ ] Audio output verification (approach TBD via research)
- [ ] Multi-instance parallel workflows (4 Claude Code instances coordinating via shared .planning/)
- [ ] Rebrand to GMD throughout codebase
- [ ] Attribution to original GSD in README and docs
- [ ] npm package as `gmd-cc` (no conflict with `get-shit-done-cc`)

### Out of Scope

- Removing any existing GSD functionality — this is additive only
- Supporting frameworks other than JUCE — focused scope for v1
- Real-time audio streaming to Claude — not technically feasible

## Context

**Origin:** Fork of glittercowboy/get-shit-done, the Claude Code workflow system for structured project execution.

**Plugin Development Stack:**
- JUCE framework (C++)
- Existing testing: pluginval, unit tests
- Gap: No agentic feedback loops for visual/audio/behavioral testing

**Current Pain Points:**
- Manual testing in DAW for visual and audio verification
- Sequential workflow when parallel development is possible
- No automated edge case discovery for plugin behavior

**Codebase State:**
- Already mapped via `/gsd:map-codebase`
- See `.planning/codebase/` for architecture, structure, conventions

## Constraints

- **Package naming**: Must be `gmd-cc` to avoid npm conflict with `get-shit-done-cc`
- **Attribution**: README must credit glittercowboy/get-shit-done as upstream
- **Additive only**: No removing existing GSD commands, agents, or workflows
- **JUCE focus**: Plugin testing agents target JUCE projects specifically

## Key Decisions

| Decision | Rationale | Outcome |
|----------|-----------|---------|
| Fork rather than contribute upstream | Niche audio focus doesn't fit general-purpose GSD | — Pending |
| Shared .planning/ for multi-instance coordination | Simpler than message passing, leverages existing state management | — Pending |
| Visual inspection via screenshots | Claude can analyze images, practical for UI testing | — Pending |
| Audio verification approach | Needs research — bit-exact vs perceptual vs metrics | — Pending |

---
*Last updated: 2026-01-17 after initialization*
