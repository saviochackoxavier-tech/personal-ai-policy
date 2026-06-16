# 🤖 My Personal AI Policy

> A living document for responsible and ethical AI collaboration in my software development practice.
> Created as part of the **[AI Fluency program by Anthropic](https://www.anthropic.com)**.

---

## 📋 Table of Contents
- [Usage Rules](#-usage-rules)
- [Data & Privacy](#-data--privacy)
- [Quality Control](#-quality-control)
- [Ethics & Dilemmas](#-ethics--dilemmas)
- [Disclosure Templates](#-disclosure-templates)
- [Stakeholder Considerations](#-stakeholder-considerations)
- [How This Was Built](#-how-this-was-built)

---

## ✅ Usage Rules

### Encouraged uses
| Context | AI Role |
|---|---|
| Boilerplate & scaffolding | Generate repetitive setup code, config files, test stubs |
| Debugging | Explain error messages, suggest diagnostic steps |
| Documentation | Draft README files, inline comments, API docs |
| Learning | Explain concepts, compare approaches, answer "how does X work" |
| Code review support | Spot issues and suggest improvements on my own code |

### Use with caution ⚠️
- **Architecture decisions** — AI can propose, but I own the final call and must understand trade-offs
- **Security-sensitive code** — authentication, encryption, input validation. Always review independently
- **Performance-critical paths** — AI may not account for specific runtime constraints
- **Learning new skills** — use AI to check my work, not replace the struggle of learning

### Personal restrictions ❌
- No pasting client codebases or proprietary algorithms into public AI tools
- No submitting AI-generated code to assessments or interviews without disclosure
- No deploying AI-generated code without reading and understanding every line

---

## 🔒 Data & Privacy

### What I will never share with AI tools
- **API keys, credentials, tokens, or secrets** — even in test/dev environments
- **Client PII** — names, emails, IDs, health data, financial data (anonymise or use synthetic replacements)
- **Proprietary business logic** or unreleased product code
- **Internal infrastructure details** — server IPs, DB schemas with real names, network topology

### Tool preferences
- [ ] Prefer enterprise/private API tools that don't train on inputs (e.g. Claude API, GitHub Copilot Business)
- [ ] Disable conversation history for sensitive work sessions
- [ ] Sanitise code snippets before sharing (strip real variable names, replace data values)
- [ ] Review employer's AI policy before using AI on work code

---

## 🎯 Quality Control

### AI code review checklist (run before every merge)
1. **Read every line** — I understand what each line does before it goes anywhere
2. **Run the tests** — AI-generated code always goes through my existing test suite
3. **Check for hallucinated APIs** — verify that functions, libraries, and versions actually exist
4. **Security scan** — check for injection risks, unvalidated inputs, exposed secrets
5. **Fit assessment** — does it match existing patterns, conventions, and architecture?
6. **Dependency audit** — are any new packages introduced? Are they maintained and trusted?

### Accuracy standards by context
| Context | Standard |
|---|---|
| 🟢 Personal projects | Functional review + tests |
| 🟡 Team codebases | Full checklist + team PR review + AI disclosure in commit |
| 🔴 Production / client | Full checklist + security review + human pair review |

---

## ⚖️ Ethics & Dilemmas

### Dilemma 1 — A client's data would help me build a better solution. Can I use it with AI?
**Framework:** Ask three questions first. (1) Does your contract permit sharing their data with third-party tools? (2) Does the AI tool's data usage policy allow training on your inputs? (3) Have you anonymised it? If any answer is unclear or no — don't do it. Use synthetic data or describe the structure without real values.

### Dilemma 2 — My employer hasn't said anything about AI. Does silence mean it's okay?
**Framework:** Silence is not permission. Most IP agreements assign code ownership to the employer, which extends to AI-assisted code. Ask directly. Propose a clear policy if one doesn't exist.

### Dilemma 3 — Am I hurting my own growth by relying on AI too early?
**Framework:** For skills still being built — try first without AI, then use it to review or explain your attempt. For routine tasks already mastered — AI is a legitimate time-saver. Key test: *Can I debug or extend this code without AI assistance?*

### Dilemma 4 — AI-generated code could automate a colleague's role. What's my responsibility?
**Framework:** Be transparent with your team. Distinguish between AI as a tool that amplifies your work vs. a replacement for human roles — and raise the latter as an organisational conversation, not a quiet implementation.

### Dilemma 5 — I shipped AI-generated code with a bug. Who is responsible?
**Framework:** I am. Full stop. AI is a tool, not a collaborator with accountability. This is why the quality checklist is non-negotiable. Blaming the AI is not a defensible position.

---

## 📣 Disclosure Templates

### Git commit / PR description
```
feat: add user authentication flow

AI-assisted: Initial implementation scaffolded with Claude.
All code reviewed, tested, and understood before merge.
Security logic independently verified.
```

### Team Slack / async message
> Hey team — heads up that I used AI (Claude) to help draft the initial version of [module/feature]. I've reviewed it thoroughly and it passes all tests, but flagging it so you can give it an extra eye in review if you'd like.

### Client deliverable
> Note on development process: portions of this codebase were developed with AI assistance (large language model tools). All AI-generated code was reviewed, tested, and validated by the development team prior to delivery. We maintain full accountability for code quality and correctness.

### When is more detailed disclosure appropriate?
| Level | Context |
|---|---|
| 🟢 Minimal | Personal projects, internal tools with no external users |
| 🟡 Standard | Team repos, open source contributions, client code |
| 🔴 Full disclosure | Regulated industries (health, finance), public-facing safety-critical systems, formal assessments |

---

## 👥 Stakeholder Considerations

| Stakeholder | What they care about |
|---|---|
| Employer / client | IP ownership, tool approval, data security, quality liability |
| Team members | Trust, code review expectations, workload fairness |
| End users | Software reliability, data handling, right to know AI was involved |
| Junior devs / mentees | What norms I model, whether AI shortcuts harm their learning |

### Questions I ask for each stakeholder
- Would they want to know about this AI use? Would they be surprised if they found out later?
- Could my AI use harm them — through errors, data leaks, or unfair competitive advantage?
- Am I setting an expectation (about my speed or capability) they're not aware of?
- If this became standard practice on the team, would the outcome be good for everyone?

---

## 🛠 How This Was Built

This policy was created as part of the **AI Fluency program by Anthropic**, using Claude as a thinking partner to explore ethical considerations from multiple perspectives.

**Tools used:** Claude (claude.ai)  
**Program:** [AI Fluency by Anthropic](https://www.anthropic.com)  
**Date created:** June 2026  

> This is a living document. I review and update it as my practice evolves.

---

*Built with intention. Deployed with accountability.*
