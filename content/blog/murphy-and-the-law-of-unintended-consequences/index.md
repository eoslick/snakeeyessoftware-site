---
title: Murphy and The Law of Unintended Consequences
date: '2024-06-03'
author: Snake Eyes Software
description: A software security professional shares lessons learned from a chaotic
  weekend involving car rental mishaps, a ruined hotel room, lost wallet, and poor
  error handling across multiple businesses.
tags:
- Psychology
- SecurityPractices
- Behavioral Psychology
- Software Engineering
draft: false
aliases:
- /site/2024/06/murphy-and-the-law-of-unintended-consequences/
---

Posted on June 3, 2024

You all know Murphy, right? The one whose law revolves around anything that can go wrong will go wrong.

And you probably know the Law of Unintended Consequences: all actions have consequences, whether intentional or unintentional.

One of the reasons I have remained in software security is because I have a knack for finding those unintended consequences. This time, I found many of them. In many disparate but related systems. Including myself.

It was supposed to be a great weekend of seeing friends and family. Everything started out fine. The flight was departing kind of later than expected, but we still arrived around the planned 10:30 PM arrival time. What happened over the next roughly 10 hours would have made Murphy proud.

## User Interface

![sulking-2](images/sulking.webp)

Immediately after exiting the rental facility, confusion arose over which car belonged to which company. The author picked an Avis vehicle instead of a Hertz one.

**Lesson Number 1:** "User messaging needs to be crystal clear." When customers are tired or rushed, layouts should restrict confusion points. Better signage or physical barriers would have prevented this error.

**Lesson Number 2:** Remote key systems that lack clear company identification create authorization bypass risks. Customers miss identifying details when keys aren't physically handed to them.

## Feature Creep

The second rental was an electric vehicle—a surprise feature the author wasn't prepared for on a driving-intensive trip.

**Lesson Number 3:** "Feature flags are a great way for testing" but shouldn't deploy new features that create major user friction without clear expectations.

## Race Conditions

![cancelcards](images/cancelcards.webp)

The reserved vehicle situation demonstrates inventory management failures.

**Lesson Number 4:** Systems should prevent access to unavailable or reserved items through physical separation or key management protocols rather than relying on user compliance.

## Maybe Resetting Input Fields is Good?

After retrieving the correct car, the author realized the wallet was missing. Usually kept inside the wallet with the license, the separation caused the loss to go unnoticed initially.

**Lesson Number 5:** While interface resets are typically frustrating, they might prompt users to verify critical items. However, personal responsibility ultimately matters—checking for belongings remains the user's duty.

## Remove Access to Dead Functions

![hoteldisaster](images/hoteldisaster.webp)

The hotel room assigned was marked "Do Not Sell" but was rented anyway. The room contained severe damage: missing drawer, dented wardrobe, filthy floor, and bathroom issues.

**Lesson Number 6:** Dead code or disabled features shouldn't execute in production. "Do Not Sell" inventory should be completely removed from rental systems, not just flagged.

## Error Handling and Disaster Recovery

Multiple organizations failed to address the situation adequately:

- The hotel front desk and general manager offered only alternative room nights, not refunds
- Hotels.com submitted a ticket but ultimately sided with the hotel
- Visa declined the dispute, stating that occupying the room constituted acceptance of its condition

**Lesson Number 7:** "Mistakes happen. Things go wrong." Each organization had opportunities for recovery but failed at critical junctures. Poor error handling across systems compounds customer frustration. The credit card company's position that safety concerns don't warrant disputes seems fundamentally flawed for customer protection.

The author credits Hertz employees with managing difficult situations effectively, but finds fault with Sonesta Select's system design, Hotels.com's passthrough indifference, and Visa's rigid dispute policies.
