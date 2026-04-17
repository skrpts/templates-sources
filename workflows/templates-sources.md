---
type: workflow
id: templates-sources
title: "Source Templates"
description: "Source templates — API docs, style guides, competitor profiles, and reference material"
tags: [Production, Templates]
connections:
  - target: source-api-docs
    type: uses
  - target: source-style-guide
    type: uses
  - target: source-competitor-profile
    type: uses
  - target: source-brand-guidelines
    type: uses
  - target: source-research-notes
    type: uses
  - target: source-meeting-transcript
    type: uses
  - target: source-customer-feedback
    type: uses
  - target: source-technical-docs
    type: uses
  - target: llm-service
    type: runs_on
metadata:
  estimated_duration: "1 minute"
  trigger: manual
  template: true
output_step: "source-api-docs"
composite_steps:
  - "source-api-docs"
  - "source-style-guide"
  - "source-competitor-profile"
  - "source-brand-guidelines"
  - "source-research-notes"
  - "source-meeting-transcript"
  - "source-customer-feedback"
  - "source-technical-docs"
execution:
  - skill: "source-api-docs"
    step_type: "generation"
---

## Overview

This skrpt contains 8 source templates for use when creating new source nodes. Import this skrpt to add these templates to your template picker.

## Templates

### Reference

- **API Documentation** — Reference documentation for an API endpoint or service
- **Style Guide** — Writing style and tone guidelines for content generation
- **Brand Guidelines** — Brand identity rules for consistent content across channels
- **Meeting Transcript** — Store meeting transcripts for reference
- **Technical Documentation** — Technical reference documentation

### Business

- **Competitor Profile** — Structured profile of a competitor for market analysis workflows
- **Customer Feedback** — Store customer feedback and survey responses

### Research

- **Research Notes** — Collected research findings for reference in analysis workflows

