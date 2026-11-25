# MolForge

**Drug-discovery data and tools in one place.** Look up a compound, an approved drug or a protein target, check drug-likeness, and map the patents and papers around a molecule, without opening four different sites.

[molforge.ai](https://molforge.ai) · [Documentation](https://molforge.ai/docs) · [Journal](https://molforge.ai/journal) · [Pricing](https://molforge.ai/pricing)

## What you can do today

| | |
|---|---|
| **Compounds** | Search more than 92 million small molecules by name, identifier or structure, with computed properties. |
| **Drugs** | Read the profile of an approved drug: targets, indications, safety signals, patent expiry. |
| **Protein targets** | Explore a target, its diseases and the drugs known to act on it. |
| **Patents and papers** | Map the patent landscape and the literature around a molecule. |
| **Formulation** | Screen a drug against polymers. This is a screening estimate; each result states how far it can be trusted. |

It is free to start, with no card required.

## For AI assistants

MolForge runs an MCP server, so an assistant can fetch a record instead of answering from memory.

```
https://molforge.ai/mcp
```

- Nine tools: seven are free (compound, drug and target lookups, similarity search), two are paid and state their price first.
- In Claude: Settings → Connectors → Add custom connector, or `claude mcp add --transport http molforge https://molforge.ai/mcp`.
- A ready-made [Claude skill](https://molforge.ai/skills/molforge-drug-discovery/SKILL.md) tells the assistant which tool to pick.
- Machine-readable entry points: [`llms.txt`](https://molforge.ai/llms.txt) and the [agent card](https://molforge.ai/.well-known/agent-card.json).

## How we work

- **A number comes with its source and its size.** "r = 0.84 on 721 molecules held out", not "highly accurate".
- **We say what a tool does not do.** Computed values are labelled as computed; estimates carry their measured error.
- **When we get something wrong, we write it up.** The [Journal](https://molforge.ai/journal) covers each milestone, corrections included, in English, French, Spanish and German.

## Research projects

Work in progress, built on quantum-chemistry calculations of how a molecule's surface charge looks to a solvent:

- [mfsig.com](https://mfsig.com): sigma-profiles from density functional theory.
- [molbasis.com](https://molbasis.com): closed-form property equations fitted on those profiles.
- A sample of 20 computed profiles is on [molforge.ai/dft-snapshots](https://molforge.ai/dft-snapshots).

## Contact

- General: contact@molforge.ai
- Security: see [`security.txt`](https://molforge.ai/.well-known/security.txt)

Most of our code lives in private repositories.
