# @ny-squared/guard

> Unified LLM Security SDK — One-liner protection for OpenAI / Anthropic / Gemini

[![npm version](https://img.shields.io/npm/v/@ny-squared/guard)](https://www.npmjs.com/package/@ny-squared/guard)
[![npm downloads](https://img.shields.io/npm/dw/@ny-squared/guard)](https://www.npmjs.com/package/@ny-squared/guard)
[![License: Apache 2.0](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](LICENSE)

## Features

- 🛡️ **One-liner protection** — `guard.wrap(new OpenAI())` intercepts every LLM call
- 🔍 **OWASP Top 10 LLM scanning** — Prompt injection, jailbreaks, PII leakage, toxic content
- ⚡ **OSS mode** — Rule-based detection, no API key required, no network calls (Apache 2.0)
- 🤖 **Pro mode** — ML-enhanced cloud detection (~95% accuracy)
- 🔗 **Multi-provider** — OpenAI, Anthropic, Google Gemini, and more

## Installation

```bash
npm install @ny-squared/guard
```

## Quick Start

```typescript
import { guard } from '@ny-squared/guard';
import OpenAI from 'openai';

// Wrap your LLM client — that's it!
const client = guard.wrap(new OpenAI());

const response = await client.chat.completions.create({
  model: 'gpt-4',
  messages: [{ role: 'user', content: 'Hello!' }],
});
```

## Links

- 📦 npm: https://www.npmjs.com/package/@ny-squared/guard
- 🌐 Dashboard: https://app.trypromptguard.com
- 📖 Docs: https://app.trypromptguard.com/docs
