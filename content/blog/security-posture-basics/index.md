---
title: Security Posture Basics
date: '2023-10-11'
author: ''
description: An overview of security posture fundamentals, covering weaknesses, vulnerabilities,
  threats, and risk management strategies.
tags:
- SoftwareSecurity
- Security
draft: false
aliases:
- /site/2023/10/security-posture-basics/
---

## Core Pillars

A software product's security posture depends on preserving three fundamental elements: confidentiality, integrity, and availability. The more ways these can be compromised, the weaker the overall security position becomes.

## Types of Weaknesses

Two primary weakness categories exist:

**Architecture Flaws**: Design decisions or missing coding standards. Example: allowing students to enter class identification codes themselves rather than verifying against actual student records.

**Coding Defects**: Programming errors that create vulnerabilities. Example: missing authorization checks when group leaders attempt to remove members.

## Key Concepts

**Vulnerability**: A specific instance where application security can be exploited, such as unscanned file uploads combined with unrestricted file naming and shared storage access.

**Threat**: How vulnerabilities are exploited, comprising a threat actor (person or system) and an exploit (the actual degrading action). Threats need not be malicious—unintentionally uploading wrong files also qualifies.

## Risk Management

Once vulnerabilities are identified, teams evaluate risk by considering:
- **Impact**: Consequences if the threat occurs (expressed as dollars or categories)
- **Likelihood**: Probability of occurrence (percentages or categories)

Organizations can respond through four approaches:
- **Remediate**: Fix the underlying issue
- **Mitigate**: Add protective mechanisms
- **Transfer**: Shift risk to another party
- **Accept**: Tolerate the risk if mitigation costs exceed potential damage

The optimal response balances solution costs against threat consequences.
