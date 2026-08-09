---
title: The Impossible Security Goal Your Team Should Set Anyway
date: '2025-01-07'
author: Snake Eyes Software
description: A guide proposing that teams adopt an ambitious security goal of remediating
  all vulnerabilities within 60 days, emphasizing systems and habits over traditional
  goal-setting approaches.
tags:
- SecurityPractices
- SoftwareEngineering
- SoftwareSecurity
draft: false
aliases:
- /site/2025/01/the-impossible-security-goal-your-team-should-set-anyway/
---

![Header image](images/header.jpg)

## Time for a New Year's Resolution: Your Software Security KPI—A Perfectly Secure Product

In *The One Thing* by Gary Keller and Jay Papasan, the authors explore how long-term goals function as behavior-change mechanisms. They advocate for SMART goals with very low odds of achievement—almost impossible targets.

### What Would That Goal Look Like for Software Security?

**Goal:** Any security vulnerability finding in any environment by any scan or vendor will be remediated in 60 days.

**How to Measure:** Track findings as recorded and verify that no findings persist beyond 60 days.

**Achievable:** Arguably.

> "System Over Goals" – Scott Adams

Scott Adams challenges goal-focused thinking, arguing that systems-oriented people succeed whenever they apply their methods. He states: "Systems people succeed every time they apply their systems, in the sense that they did what they intended to do" (Forbes).

Software engineers work with systems daily but rarely examine the operating environment they inhabit, often finding themselves in perpetual firefighting mode. Technical debt and vulnerabilities accumulate rapidly as a result.

---

## Habit 1: Stop Tracking Vulnerabilities

Rather than abandoning tracking entirely, the focus should shift from vulnerabilities themselves to actionable metrics. Current security programs reduce risk through remediation while neglecting development process quality—guaranteeing failure.

Instead of debating exploitability and reachability, teams should investigate root causes. The key metric: how many vulnerabilities become test cases or static analysis rules, with production incidents trending toward zero.

## Habit 2: Leverage Run Time Protections

![Habits image](images/habits.jpg)

Firewalls, API Gateways, RASPs, and ADRs provide essential defense layers deployable and updatable rapidly. They offer valuable insights into user behavior and anomaly detection.

Standardizing logging, traceability, and observability becomes mandatory for new code, with retrofitting of existing systems essential. While development time increases initially, teams become more efficient, and support improves—ultimately proving cost-effective.

Track runtime protection rule lifespan; these should deactivate upon underlying fixes, with duration trending toward the 60-day goal.

## Habit 3: Keep Third Party Libraries Up To Date

Modern software consists primarily of third-party libraries. Most organizations lack sound update processes, operating on "if it isn't broke, don't fix it" mentality—ironically discouraging their own customers from lagging versions.

Libraries should be incorporated using specific versions, verified against known-good releases, and reviewed for malicious code. All libraries should originate from internal sources, not directly from the Internet.

**Critical factor:** Proper library management requires dedicated time for comprehensive test coverage. Without trusting test cases, teams cannot achieve genuine security.

> "Evaluating the security of a system requires being curious about the system"

## Habit 4: Practice New Mindsets

**First:** If product teams prioritize security and quality genuinely, delivery speed becomes secondary. Leadership should examine total cost of ownership and potential savings from measured pacing.

**Second:** Organizations must foster curiosity. Effective vulnerability discovery involves questioning: "What happens if I do X?" Effective curiosity requires deep system understanding. Hack-a-thons—not just after-hours activities—bring developers, architects, and stakeholders together. Consider offering monetary rewards for solutions delivering maximum business value.

**Third:** Simplify data classification approaches. Focus on three core principles: Least Privilege, Role-Based Access Control (RBAC), and encrypting all non-essential data. This means encrypting user data by default.

## Habit 5: Improve Automated Tests

Smart Fuzzing forms DAST's basis, using intelligent random values triggering specific vulnerability types based on technology assumptions.

Vulnerability and penetration tests follow similar principles. Red Teams combine smart fuzzing with behavioral analysis. Both approaches transform into effective automated tests through development-security team partnerships, building comprehensive, aggressive integration testing suites.

## Habit 6: Challenge Technology Changes

Few organizations truly need diverse technology stacks. While certain technologies excel at specific tasks, complexity often outweighs benefits. Teams frequently experiment with trending technologies for status rather than strategic necessity.

The real challenge: maintaining technological concurrency while making strategic changes only when genuinely beneficial.

## Habit 7: Get Back to Testing For Vulnerabilities

Standard methods—static, interactive, dynamic, ADR, RASP, and SCA scanning—remain essential, implemented systematically.

Static analysis and SCA should occur during development, at check-in, during builds, and in regular automated scans.

DAST belongs in production-like staging environments and, depending on organizational maturity, in production itself.

Mature organizations should implement Bug Bounty Programs, identifying subtle vulnerabilities automated testing might miss. These findings convert into automated tests preventing regression.

---

![Conclusion image](images/conclusion.jpg)

## Are You Up For the Challenge?

The 60-day remediation goal might be impossible—that's not the point. The goal creates systems and habits transforming organizational security approaches.

These seven habits form a system that doesn't guarantee perfect security but creates environments where security becomes intrinsic to development rather than afterthought.

Success measures consistency in applying habits and their influence on daily decisions. When teams embrace these practices as standard operations, they succeed at the system level regardless of 60-day achievement.

The real question: "Are we building and following systems making our software inherently more secure?" That's worth pursuing, one habit at a time.
