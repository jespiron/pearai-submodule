---
title: 🦔 Telemetry
description: PearAI collects anonymous usage information
keywords: [telemetry, anonymous, usage info, opt out]
---

# 🦔 Telemetry

## Overview

PearAI collects and reports **anonymous** usage information. This data is essential to understanding how we should improve the product. You can opt out of it at any time. We use [Posthog](https://posthog.com/), an open source platform for product analytics, to collect and store the data. You can review the code [here](https://github.com/trypear/pearai-app/blob/main/gui/src/hooks/CustomPostHogProvider.tsx), or review our official policy [here](https://trypear.ai/privacy).

## What we track

We track

- whether you accept or reject suggestions (never including the code or the prompt)
- the name of the model and slash command used
- the number of tokens generated
- the name of your OS and IDE

All data is anonymous and cleaned of PII before being sent to PostHog.

## How to opt out

The `~/.continue` directory contains a `config.json` file that looks like this:

```json title="~/.pearai/config.json"
{
    "allowAnonymousTelemetry": true,
    ...
}
```

You can turn off anonymous telemetry by changing the value of `allowAnonymousTelemetry` to `false`. Alternatively, you can uncheck the "Continue: Telemetry Enabled" box in VS Code settings.
