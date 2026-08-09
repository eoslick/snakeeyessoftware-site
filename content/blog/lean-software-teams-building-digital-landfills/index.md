---
title: Lean Software Teams Building Digital Landfills
date: '2025-07-15'
author: Snake Eyes Software
description: Software teams spend millions building features with minimal value while
  security vulnerabilities rise. The article critiques misapplication of Lean Manufacturing
  principles in software development.
tags:
- appsec
- SoftwareSecurity
draft: false
aliases:
- /site/2025/07/lean-software-teams-building-digital-landfills/
---

![landfill](images/landfill.png)

Software development teams invest millions in features that provide minimal user value while security vulnerabilities proliferate. According to the author, "at least 80% of development effort creates features that drive little user value," drawing on Pareto's Principle.

Despite rapid CI/CD pipelines, organizations essentially run assembly lines producing unwanted inventory.

## The Lean Manufacturing Lie

References to *The Phoenix Project* and *The Unicorn Project* by Gene Kim demonstrate how Lean Manufacturing principles were adapted to software. However, the author contends these applications misunderstand fundamental differences:

**Predictable Production Time**: Toyota manufacturing has known cycle times; software sprints create artificial predictability without genuine insight into actual development complexity.

**Limited Product Changes**: Auto manufacturers update models annually, while software products change constantly. Each user story represents essentially new work, not repetition.

**Known Demand**: Unlike market research for vehicles, software demand relies on user stories and assumptions. Given how little actual value emerges from most implementations, true demand remains questionable.

## Architecture and Developer Time: The Real Constraints

Low-value features create persistent liabilities:

- Code requiring security maintenance
- Expanded attack surfaces needing monitoring
- Dependencies demanding updates
- Complexity impeding future development

## The Real Waste Pipeline

The author notes that while companies celebrate deployments, they accumulate:

- Feature bloat with minimal user engagement
- Security debt—with 22,254 vulnerabilities disclosed by mid-2024, a 30% increase from 2023
- Technical debt from outdated libraries and shortcuts
- Patch failures—60% of data breaches stem from unpatched known vulnerabilities

## The Real Throughput Question

Rather than asking "How fast can we ship features?" organizations should ask: "How fast can we deliver high-value, quality features while eliminating waste?"

## Your Next Sprint Planning

Before planning sprints, teams should verify:

1. **Usage Evidence**: Data proving users want the feature
2. **Security Impact**: Attack surface created
3. **Maintenance Cost**: Long-term security and maintenance burden
4. **Value Measurement**: How success will be determined

## The Choice

Teams can optimize deployment pipelines while building low-value, vulnerable features, or apply genuine Lean principles: eliminate waste, prioritize customer value, and treat security as a quality constraint.
