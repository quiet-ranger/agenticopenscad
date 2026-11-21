---

name: clean-room-spec

description: Extracts a language-agnostic functional specification from a codebase without leaking source code or implementation details.

---
# Clean-Room Functional Specification Extractor

## Goal

Analyze the existing repository and produce a comprehensive `FUNCTIONAL_[SPEC.md](http://SPEC.md)` describing *what* the software does (inputs, outputs, business rules, state transitions, and edge cases) so an independent agent can reimplement it in another language.

## Strict Constraints (Do Not Violate)

- **NO code snippets:** Never copy, quote, or translate variable names, function signatures, class hierarchies, or algorithms from the original codebase.
- **NO library coupling:** Do not reference language-specific frameworks or packages used in the original repo; describe capabilities generically (e.g., "HTTP server" instead of "Express middleware").
- **Focus strictly on observable behavior:** Document CLI flags, API endpoints, data schemas, UI states, error conditions, and file formats.
- Do not use the contents of OpenSCAD_Architecture_and_API_Guide.odt

## Instructions

1. Map all external interfaces (CLI arguments, network endpoints, config files, UI views).
2. Document the exact data models and validation rules for inputs and outputs.
3. Trace core workflows step-by-step as black-box state transitions.
4. List all error states and expected fallback behaviors.
5. Output the final specification to `FUNCTIONAL_[SPEC.md](http://SPEC.md)` and run a self-audit to strip any leaked source identifiers.
6. Use the contents of the following documents as supporting material: OpenSCAD_User_Manual.pdf, OpenSCAD_User_Manual_The_OpenSCAD_Language.pdf and OpenSCAD_Tutorial.pdf

