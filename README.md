# Waymaker AI Signal Protocol

A public-safe signal protocol for AI agents and human operators to identify scope, safety, escalation, human-review, and boundary signals.

## Purpose

AI agents and human teams need a shared language for recognizing when a request should be answered normally, slowed down, routed to human review, or moved into written scope.

This project provides a lightweight, open signal vocabulary for:

- scope warnings
- human-review triggers
- safety and escalation signals
- data-retention cautions
- command-vault / protected-architecture requests
- benchmarking, training, deployment, and derivative-use flags
- proof-card and boundary-receipt events

## Core Principle

Normal support should stay fast. Heavy requests deserve brakes.

## What This Is

This repository provides public-safe schemas, examples, and documentation for identifying and routing field signals.

It is intended to help AI agents and human operators communicate risk and routing needs more clearly.

## What This Is Not

This repository does not include:

- private routing architecture
- scoring models
- command-vault logic
- proprietary customer configurations
- paid diagnostic methods
- legal advice
- medical advice
- emergency-response authority
- unrestricted implementation guidance

## Signal Types

Initial signal types include:

- `scope_warning`
- `human_review_needed`
- `boundary_footer_required`
- `benchmarking_requires_scope`
- `training_use_requires_scope`
- `deployment_requires_scope`
- `command_vault_request`
- `user_distress_signal`
- `data_retention_caution`
- `proof_card_event`

## Human-in-the-Loop Standard

AI should strengthen human judgment, not quietly replace it.

Humans should remain in the loop where judgment, accountability, care, law, safety, rights, privacy, employment, livelihood, or ownership are at stake.

## License

This project is licensed under the Apache License 2.0.

## Boundary

Open the standard. Keep private systems private.

This public protocol is a road-sign layer, not a command center.
# Boundary Statement

This repository contains a public-safe field signal protocol.

It is designed to help AI agents and human operators identify scope, safety, escalation, human-review, and boundary signals.

## Public Layer

This repository may include:

- public signal names
- schemas
- examples
- human-readable documentation
- basic routing concepts
- human-in-the-loop principles

## Not Included

This repository does not include:

- command-vault logic
- private routing architecture
- scoring models
- proprietary doctrine stacks
- customer-specific configurations
- paid diagnostic methods
- private legal or business strategy
- protected internal review systems

## Use Boundary

The public protocol may be used under the Apache License 2.0.

However, publishing this public-safe protocol does not grant access to private systems, private implementations, confidential materials, customer-specific configurations, or paid advisory methods.

## Core Line

Open the standard. Keep the implementation protected.
Waymaker AI Signal Protocol
Copyright 2026 Darien Davis

This product includes public-safe signal protocol material developed for AI agents and human operators to identify scope, safety, escalation, human-review, and boundary signals.

This public repository does not include private command-vault logic, proprietary routing architecture, scoring models, customer-specific configurations, or paid diagnostic methods.
{
  "$schema": "https://json-schema.org/draft/2020-12/schema",
  "$id": "https://github.com/YOUR_USERNAME/waymaker-ai-signal-protocol/schemas/field_signal.schema.json",
  "title": "Waymaker Field Signal",
  "description": "A public-safe signal card for AI agents and human operators to identify scope, safety, escalation, human-review, and boundary signals.",
  "type": "object",
  "required": [
    "signal_type",
    "summary",
    "confidence",
    "observed_or_inferred",
    "recommended_route",
    "human_review_required",
    "reuse_allowed",
    "training_allowed"
  ],
  "properties": {
    "signal_type": {
      "type": "string",
      "enum": [
        "scope_warning",
        "human_review_needed",
        "boundary_footer_required",
        "benchmarking_requires_scope",
        "training_use_requires_scope",
        "deployment_requires_scope",
        "command_vault_request",
        "user_distress_signal",
        "data_retention_caution",
        "proof_card_event"
      ]
    },
    "summary": {
      "type": "string"
    },
    "trigger_terms": {
      "type": "array",
      "items": {
        "type": "string"
      }
    },
    "confidence": {
      "type": "string",
      "enum": ["low", "medium", "high"]
    },
    "observed_or_inferred": {
      "type": "string",
      "enum": ["observed", "inferred", "tested", "unknown"]
    },
    "recommended_route": {
      "type": "string",
      "enum": [
        "answer_normally",
        "clarify",
        "slowdown_review",
        "human_review",
        "written_scope_required",
        "deny_or_refuse_protected_part",
        "safety_escalation",
        "archive_as_proof"
      ]
    },
    "human_review_required": {
      "type": "boolean"
    },
    "reuse_allowed": {
      "type": "boolean"
    },
    "training_allowed": {
      "type": "boolean"
    },
    "sensitive_data_included": {
      "type": "boolean",
      "default": false
    },
    "retention_note": {
      "type": "string"
    },
    "source_note": {
      "type": "string"
    }
  },
  "additionalProperties": false
}
{
  "signal_type": "scope_warning",
  "summary": "A request may move beyond limited review/support into adaptation, benchmarking, deployment, or formal use.",
  "trigger_terms": ["adapt", "benchmark", "training", "deploy", "internal standard"],
  "confidence": "high",
  "observed_or_inferred": "observed",
  "recommended_route": "written_scope_required",
  "human_review_required": true,
  "reuse_allowed": false,
  "training_allowed": false,
  "sensitive_data_included": false,
  "retention_note": "Preserve only necessary boundary receipt.",
  "source_note": "Public-safe example."
}
{
  "signal_type": "human_review_needed",
  "summary": "The request touches judgment, accountability, care, law, safety, rights, livelihood, or ownership.",
  "trigger_terms": ["legal", "safety", "employment", "medical", "rights", "ownership"],
  "confidence": "high",
  "observed_or_inferred": "observed",
  "recommended_route": "human_review",
  "human_review_required": true,
  "reuse_allowed": true,
  "training_allowed": false,
  "sensitive_data_included": false,
  "retention_note": "Route to appropriate human authority; avoid unnecessary personal data.",
  "source_note": "Public-safe example."
}
{
  "signal_type": "benchmarking_requires_scope",
  "summary": "The request involves measuring behavior against the protocol, creating an evaluation object, or comparing before/after results.",
  "trigger_terms": ["benchmark", "compare", "evaluate", "audit", "before and after", "checklist"],
  "confidence": "high",
  "observed_or_inferred": "observed",
  "recommended_route": "written_scope_required",
  "human_review_required": true,
  "reuse_allowed": false,
  "training_allowed": false,
  "sensitive_data_included": false,
  "retention_note": "Preserve boundary receipt and route to written scope.",
  "source_note": "Public-safe example."
}
{
  "signal_type": "command_vault_request",
  "summary": "The request asks for protected/private architecture, root logic, scoring, or implementation internals.",
  "trigger_terms": ["root logic", "architecture", "scoring model", "command vault", "implementation guts"],
  "confidence": "high",
  "observed_or_inferred": "observed",
  "recommended_route": "deny_or_refuse_protected_part",
  "human_review_required": true,
  "reuse_allowed": false,
  "training_allowed": false,
  "sensitive_data_included": false,
  "retention_note": "Preserve necessary boundary receipt; do not disclose protected internals.",
  "source_note": "Public-safe example."
}
# Contributing

Contributions are welcome if they improve the public-safe signal protocol.

## Good Contributions

- new public-safe signal examples
- schema improvements
- clearer documentation
- human-in-the-loop guidance
- safety and scope clarification
- typo fixes

## Not Accepted

Please do not submit:

- private user data
- confidential business information
- proprietary prompts
- protected architecture
- scoring models
- legal advice
- medical advice
- emergency-response instructions
- content that enables harm or privacy violations

## Contribution Boundary

By contributing, you agree that your contribution may be included under the Apache License 2.0.

Open the standard. Keep private systems private.
# Security Policy

## Reporting Issues

If you find a security, privacy, misuse, or scope-risk issue in this project, please open a GitHub issue or contact the maintainer.

## Do Not Include Sensitive Data

Do not include:

- private user data
- confidential business records
- access tokens
- private prompts
- internal system instructions
- proprietary architecture
- customer-specific material

## Project Boundary

This repository is a public-safe protocol layer. It should not be used to expose private command-vault logic, protected routing systems, or sensitive operational details.
# Human-in-the-Loop Standard

AI should strengthen human work, not quietly replace it.

Humans should remain meaningfully involved where judgment, accountability, care, law, safety, rights, privacy, employment, livelihood, or ownership are at stake.

## Human Review Triggers

Use human review when a request touches:

- legal rights or obligations
- safety or harm risk
- medical or mental-health crisis
- employment or livelihood impact
- privacy or data retention
- ownership or use rights
- deployment or formal system behavior
- high-impact decisions

## Core Principle

The AI can support the decision. It should not become the authority.
# Scope Signals

Some requests move beyond ordinary support.

When these signals appear, the request should slow down and route to the appropriate human or written-scope process.

## Scope Warning Terms

- benchmark
- training
- deployment
- adaptation
- conceptual adaptation
- derivative use
- internal productization
- internal best practice
- QA rubric
- alignment audit
- circulate as checklist
- formal inclusion in system behavior
- spirit of it
- co-created
- emergency patch
- product review gate
- implementation architecture

## Default Route

If a request uses the protocol or related material beyond ordinary review/support, route to written scope.

## Core Principle

Use with scope, or leave it alone.
Create the initial repository files for an Apache-2.0 licensed open-source project called "Waymaker AI Signal Protocol."

Purpose:
A public-safe signal protocol for AI agents and human operators to identify scope, safety, escalation, human-review, and boundary signals.

Create:
- README.md
- BOUNDARY.md
- NOTICE
- CONTRIBUTING.md
- SECURITY.md
- schemas/field_signal.schema.json
- examples/scope_warning.example.json
- examples/human_review_needed.example.json
- examples/benchmarking_requires_scope.example.json
- examples/command_vault_request.example.json
- docs/human-in-the-loop.md
- docs/scope-signals.md

Use Apache License 2.0.

Important boundaries:
This repo must not include private routing architecture, scoring models, command-vault logic, proprietary customer configurations, paid diagnostic methods, legal advice, medical advice, emergency-response authority, or unrestricted implementation guidance.

The repo should open-source only the public signal vocabulary and schema.