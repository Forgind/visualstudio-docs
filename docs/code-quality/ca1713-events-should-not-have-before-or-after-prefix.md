---
title: "CA1713: Events should not have before or after prefix"
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
  - "EventsShouldNotHaveBeforeOrAfterPrefix"
  - "CA1713"
helpviewer_keywords:
  - "CA1713"
  - "EventsShouldNotHaveBeforeOrAfterPrefix"
ms.assetid: 855772a4-aa9e-410b-88c1-c5fba1ca63da
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
  - "multiple"
---
# CA1713: Events should not have before or after prefix

|||
|-|-|
|TypeName|EventsShouldNotHaveBeforeOrAfterPrefix|
|CheckId|CA1713|
|Category|Microsoft.Naming|
|Breaking change|Breaking|

## Cause
The name of an event starts with 'Before' or 'After'.

## Rule description
Event names should describe the action that raises the event. To name related events that are raised in a specific sequence, use the present or past tense to indicate the relative position in the sequence of actions. For example, when naming a pair of events that is raised when closing a resource, you might name it 'Closing' and 'Closed', instead of 'BeforeClose' and 'AfterClose'.

Naming conventions provide a common look for libraries that target the common language runtime. This reduces the learning curve that is required for new software libraries, and increases customer confidence that the library was developed by someone who has expertise in developing managed code.

## How to fix violations
Remove the prefix from the event name, and consider changing the name to use the present or past tense of a verb.

## When to suppress warnings
Do not suppress a warning from this rule.