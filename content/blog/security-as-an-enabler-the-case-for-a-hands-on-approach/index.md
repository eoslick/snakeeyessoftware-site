---
title: 'Security as an Enabler: The Case for a Hands-On Approach'
date: '2024-03-21'
author: Snake Eyes Software
description: 'Examines whether security functions as a gatekeeper or enabler across
  different authentication approaches: building custom solutions, purchasing commercial
  platforms like Okta, or blending open-source tools like Keycloak.'
tags:
- SecurityPractices
- SoftwareSecurity
draft: false
---

Posted on March 21, 2024

## Overview

The traditional "build vs. buy" decision in software development oversimplifies the actual choices teams face. A more nuanced perspective examines the balance between building solutions internally and purchasing external services. Using authentication in "MyOwnTutorial" as a case study reveals how security can function as either a gatekeeper or a facilitator.

## Three Approaches to Authentication

### Build: Custom Authentication Solution

**Security as a Gate:** Creating an internal authentication system requires deep security expertise. The approach demands extensive threat modeling, security testing, and compliance validation. While tailored to specific needs, this path creates bottlenecks as security reviews and vulnerability assessments must precede deployment.

**Security as an Enabler:** Security teams can partner directly with product teams by developing the authentication system themselves. Rather than blocking progress, the security team becomes a vendor to the product group, implementing preferred application security testing strategies while managing documentation and support.

### Buy: Commercial Solutions like Okta

**Security as a Gate:** Third-party solutions simplify implementation but introduce vendor dependency concerns. Security teams establish rigorous vendor evaluation criteria and mandate threat modeling before integration, potentially delaying timelines.

**Security as an Enabler:** Security facilitates rapid adoption by handling integration complexities. The team manages logging, secret management, and creates documentation, enabling product teams to implement the solution efficiently.

### Blend: Open-Source Tools like Keycloak

**Security as a Gate:** Hybrid approaches require vigilant integration practices to prevent vulnerabilities where custom code meets open-source components. Comprehensive planning and ongoing policy management are essential.

**Security as an Enabler:** Security assumes ownership of deployment, coding, and maintenance. The team becomes the proprietor of tools, code, and support, shifting from oversight to active partnership.

## Core Principle

"Security must be a consideration in each scenario, functioning either as an enabler or as a gate."

Authentication exemplifies this broader principle across the entire software development lifecycle. When security teams adopt hands-on approaches—such as developing logging libraries or optimizing event management—they transition from gatekeeping to enabling. True shared responsibility requires security to engage deeply, shaping development practices rather than simply reviewing them.
