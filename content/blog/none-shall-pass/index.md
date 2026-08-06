---
title: None Shall Pass
date: '2024-01-02'
author: ''
description: Explores access control strategies for protecting data privacy in software
  systems, using Monty Python references to illustrate security concepts.
tags:
- PrivacyByDesign
- SoftwareSecurity
- Security
draft: false
---

## Overview
The article uses the famous scene from *Monty Python and the Holy Grail* featuring the Black Knight to introduce access control concepts. The Black Knight's refusal to grant passage serves as a metaphor for security mechanisms that prevent unauthorized data access.

## Key Access Control Strategies

The foundation of data protection relies on **"Deny By Default"** - a principle where system administrators cannot access data without following established procedures. This approach prevents mistakes and creates audit trails for accountability.

### Six Access Control Mechanisms

1. **Discretionary Access Control (DAC)** - Object owners set policies determining who can access resources
2. **Mandatory Access Control (MAC)** - Predefined rules and security classifications regulate access
3. **Role-Based Access Control (RBAC)** - Permissions assigned to roles rather than individual users
4. **Attribute-Based Access Control (ABAC)** - Dynamic access based on user, system, and environmental attributes
5. **Rule-Based Access Control** - Administrator-defined rules with specific conditions
6. **Time-Based Access Control** - Temporal restrictions limiting resource access to specific periods

## Implementation Benefits

When planned early in software design, access controls need not be overly complex. The owner can manage many conditions, and "when someone unauthorized obtains access it typically requires significant effort and is easily traced."

## Related Topics
The article notes that when access controls fail or are insufficient, data protection requires additional safeguarding measures—discussed in the follow-up article "Hiding Data in Plain Sight."
