---
title: Automated segment management
description: Learn about how segments are automatically managed in Customer Insights - Journeys.
ms.date: 10/08/2024
ms.topic: article
author: alfergus
ms.author: alfergus
search.audienceType: 
  - admin
  - customizer
  - enduser
---

# Automated segment management

To optimize resources, Customer Insights - Journeys automatically manages the refresh frequency of your unused segments. "Unused segments" are segments that were created more than 30 days ago and haven't been used in journeys, emails, or other segments in the last 15 days. This feature aims to improve the customer experience by reducing the impact of unused segments on the performance of active campaigns, allowing improved processing speed for segments in active use.

## How automated segment management works

This feature detects segments created more than 30 days ago that haven't been used in the last 15 days and sets them to a once-a-day refresh cadence. This means that the unused segments are still refreshed, but only once per day. When an unused segment is used again in a journey, email, or other segment, the refresh rate is automatically restored to the normal cadence. This feature is fully automated and doesn't require any input or action from users.
