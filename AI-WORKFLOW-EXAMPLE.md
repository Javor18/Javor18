# AI-assisted development: a documented coursework example

## Goal

Prepare a Bash-based Windows forensics project for a clear, reproducible portfolio presentation.

## Author and AI contributions

The author set up the local laboratory, ran the historical tests and captured the screenshots. AI assisted with code and with report wording where applicable. During portfolio preparation, the author approved the scope and confirmed the provenance of the lab evidence; Codex prepared and checked the publication candidate.

## A concrete issue

The original Analyzer compared the initial and final SHA-256 values but could continue to the completion path after a mismatch. The portfolio candidate returns an error before creating a success archive when the hash differs or cannot be read.

## How the correction was checked

Offline regression tests use a synthetic file with a known hash, then change its contents and verify that the mismatch returns an error. Another test replaces the archive operation with a tripwire and confirms that an integrity failure does not invoke it. The test environment does not analyze an actual disk/memory image or run forensic extractors.

## What this demonstrates

Requirement refinement, evidence-based review of AI-assisted code, a bounded correction and verification of failure behavior. It does not establish independent mastery of every forensic tool or production readiness.
