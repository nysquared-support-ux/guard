# @ny-squared/guard

> Unified LLM Security SDK 窶・One-liner protection for OpenAI / Anthropic / Gemini

[![npm version](https://img.shields.io/npm/v/@ny-squared/guard)](https://www.npmjs.com/package/@ny-squared/guard)
[![npm downloads](https://img.shields.io/npm/dw/@ny-squared/guard)](https://www.npmjs.com/package/@ny-squared/guard)
[![License: Apache 2.0](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](LICENSE)

## Features

- 孱・・**One-liner protection** 窶・`guard.wrap(new OpenAI())` intercepts every LLM call
- 剥 **OWASP Top 10 LLM scanning** 窶・Prompt injection, jailbreaks, PII leakage, toxic content
- 笞｡ **OSS mode** 窶・Rule-based detection, no API key required, no network calls (Apache 2.0)
- ､・**Pro mode** 窶・ML-enhanced cloud detection (~95% accuracy)
- 迫 **Multi-provider** 窶・OpenAI, Anthropic, Google Gemini, and more

## Installation

```bash
npm install @ny-squared/guard
```

## Quick Start

```typescript
import { guard } from '@ny-squared/guard';
import OpenAI from 'openai';

// Wrap your LLM client 窶・that's it!
const client = guard.wrap(new OpenAI());

const response = await client.chat.completions.create({
  model: 'gpt-4',
  messages: [{ role: 'user', content: 'Hello!' }],
});
```

## Why zero dependencies?

Supply chain is exactly what you're protecting against.
No transitive vulnerabilities. Ever.

## Benchmarks

| Input type        | Latency (M1 Mac) |
|-------------------|-----------------|
| Short prompt      | 2ms             |
| Long prompt (4KB) | 5ms             |
| Batch (100 items) | 180ms           |

## vs. alternatives

| Feature           | @ny-squared/guard | [others] |
|-------------------|:-----------------:|:--------:|
| Zero dependencies | 笨・              | 笶・      |
| Local-first OSS   | 笨・              | 笶・      |
| Risk score 0-100  | 笨・              | 笶・      |

## Links

- 逃 npm: https://www.npmjs.com/package/@ny-squared/guard
- 倹 Dashboard: https://app.trypromptguard.com
- 当 Docs: https://app.trypromptguard.com/docs
