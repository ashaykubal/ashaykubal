# Ashay Kubal
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/ashaykubal/) [![Website](https://img.shields.io/badge/ashaykubal.com-1a365d?style=flat&logo=safari&logoColor=white)](https://ashaykubal.com)

## Professional Experience

With 20+ years in engineering including 10+ building products, I'm a Product leader who believes the best products are built by teams or individuals who have a functional understanding of where each brick fits before building the entire house, i.e. they can all rally around a shared vision. I'm a lifelong learner & servant leader in equal parts.

By day, I build Enterprise products in the AI/ML, Search & Applied Data & Analytics space. After hours, I'm deep in the weeds building hobby projects and POCs. I like hard problems at the intersection of AI, retrieval, long-horizon agentic orchestration and complex data. Also a fan of anime, action RPGs, and football (the kind with actual feet).

Currently focused on implementing automated, effective Context Engineering & token usage optimization techniques for AI agents. 

## My Public Repos

**[AFIX - Agentic Financial Interoperability eXchange](https://github.com/QBall-Inc/afix)**

AFIX defines a shared vocabulary for agent governance at firm boundaries. It specifies what structured metadata must cross when a governed agent in one institution calls a governed agent in another — without prescribing how either firm governs itself internally. AFIX is transport-neutral: it provides binding specifications for both Google's Agent-to-Agent (A2A) protocol and Anthropic's Model Context Protocol (MCP). The goal is interoperability, not uniformity.

Bloomberg, FactSet, and LSEG have each independently built equivalent governance middleware layers around MCP — covering identity, access control, audit, and rate limiting. JPMC, Morgan Stanley, and BlackRock all have active AI governance programs. Framework-level coordination exists through bodies like FINOS CC4AI. What does not exist is any coordination on governance interchange: when your governed agent calls my governed agent, there is no shared vocabulary for the metadata that should accompany that call. Every integration currently requires bespoke negotiation of what identity means, what an audit event looks like, and who carries liability. AFIX proposes to fix that.

**[CLEAR - Persistent memory, intelligent context, and structured project management for Claude Code](https://github.com/QBall-Inc/clear)**

CLEAR is a Claude Code plugin that gives Claude persistent memory across sessions, structured project management, and intelligent context injection. It solves the fundamental problem of agentic AI development: every session starts from zero.

CLEAR fixes this by maintaining a persistent .clear/ state directory in your project that tracks:

**Knowledge System** — technical decisions, architectural patterns, lessons learned, business rules, stakeholders, people and processes captured as structured documents and linked to relevant code files where applicable and surfaced on demand with full-text search via SQLite FTS5. The knowledge system supports automated and on-demand supersession, deprecation and tuning so that it is always fresh.
**Project Plans** — phased plans with workpackages, milestones, dependencies, and progress tracking
**Session State** — session numbers, token usage monitoring, handoff documents for continuity
**Context Injection** — hooks that automatically surface relevant knowledge when Claude reads or writes files linked to knowledge entries

**The result:** Claude starts every session knowing what it knew last time. It surfaces relevant decisions when you touch related files. It tracks your project's progress across phases and workpackages. And it does this without you having to ask. The entire system is orchestrated via a system of skills and CLI scripts that are invoked using hooks on session start / prompt submit / pre & post tool use.

**[The Bulwark](https://github.com/QBall-Inc/the-bulwark)**

AI coding agents suffer from fundamental quality issues:

1. **Entropy Drift**: Code quality degrades as context fills and complexity increases
2. **Semantic vs Engineering Compliance**: Agents satisfy requests literally but fail engineering requirements
3. **Self-Review Bias**: Agents cannot objectively review code they generated in the same context
4. **Mock-Heavy Testing**: Agents write tests that verify mocks, not actual system behavior
5. **Fix-Declare-Done Pattern**: Fixes declared complete without verification

This led to the conception of "The Bulwark", a Claude Code plugin that enforces "Defense-in-Depth" quality governance using:

- **Hooks**: Deterministic enforcement via PostToolUse (Exit 2 blocking)
- **Sub-Agents**: Isolated context specialists with structured output
- **Skills**: Progressive disclosure of heuristics and patterns
- **Pipeline Orchestration**: F# pipe syntax for complex workflows
- **`just`**: Deterministic command interface with log-based output

**[Essential Agents & Skills](https://github.com/ashaykubal/essential-agents-skills)**

Production-grade agents and skills for AI-assisted development. These tools enforce code quality, catch test suite problems, validate assets against standards, and improve multi-agent workflows. Most of these agents and skills are also offered by The Bulwark plugin.




