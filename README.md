# William Mosley

Alpharetta, GA · [LinkedIn](https://www.linkedin.com/in/william-mosley)

I build internal systems that agents operate, with scoped permissions, reversible actions, and failure reports you can check.

---

### 🔧 Command Center

A personal operations system: cash-flow projection, task and project tracking, a job pipeline, and a trade journal, all behind one dashboard. The demo surfaces a subset of those tools on fixture data.

**[→ Live demo](https://willjmos.github.io/command-center-demo/)** · [source](https://github.com/Willjmos/command-center-demo)

Python/Flask · React + TypeScript · SQLite · MCP tool servers

The demo runs entirely in the browser, and the deployed app makes no application-data requests. Open DevTools and check. That isn't a promise, it's a gate: a CI check inspects the built output in a real browser on every deploy and blocks the release if it finds a same-origin API call, a loopback address, or private infrastructure strings. Each of those rules was proven capable of failing against a planted violation before its zero was trusted.

---

### What I care about in a system

Most of the work here isn't features. It's making a system incapable of lying about its own state.

- **A check that cannot fail is not a check.** The verifiers I build ship with a planted control that has to trip in the same run. Otherwise "it passed" and "it never ran" are the same observation.
- **Report the denominator, always.** Output has to distinguish *no checks ran* from *all checks passed*. A result over an empty set is the most convincing wrong answer there is.
- **Detecting a failure and not failing on it is decoration.** A gate that finds a problem and then exits zero is worse than no gate, because now you trust it.

None of those are aspirational. Each one is written down because a verifier here reported success while examining the wrong thing, and I had to go find out why.

---

### Currently

Building agent workflows with reversibility tiers, meaning actions an agent takes freely, actions it takes and reports, and actions that always need a human. Also a review layer where an outside model challenges the reasoning rather than the output.
