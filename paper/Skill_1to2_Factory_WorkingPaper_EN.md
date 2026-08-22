# From Skill 1.0 to Skill 2.0: Industrializing Research Capabilities

*From Skill 1.0 to Skill 2.0: Industrializing Research Capabilities*

<div class="author-block">
<strong>Ye Qing</strong><br/>
<em>August 2026</em>
</div>

---

> **Abstract**: In one sentence: the seller manufactures parts; the buyer assembles the car. Selling-side researchers distill their daily work into standardized parts, while buying-side researchers need not rebuild the wheel — they assemble existing parts into chains that answer specific investment questions. Skill 1.0 addressed whether research capabilities could be encapsulated at all, packaging an Excel database into one integrated capability that AI can execute directly. When the same template scaled to 13 topical databases and roughly 500 analytical logic units, the question shifted to how a growing collection of capabilities should be managed and composed. Against this background, this paper proposes a two-layer incremental methodology. The first layer is a life cycle: research capability evolves from "one thing" into "a box of parts." The seller manufactures parts and puts them on the shelf; the buyer deals with exactly three things — take and use, verify, and change on request. The second layer is capability composition: turning an investment idea into a result takes four steps — decide what to look at, pick parts, assemble and run, and speak up when unsatisfied. A real, fully measured case is presented: a transmission chain from liquidity, to institutional behavior, to credit spreads (data through August 19-20, 2026). Liquidity is loose (1M CD yield 0.50%); banks and brokers are reducing exposure while funds and others are buying; credit spreads remain stable (AAA 3Y 34.9bp, AA- 3Y 99.9bp). The three segments do not move in the same direction, and the persistence of bank and broker reduction is the leading signal most worth tracking. In methodology, this work is incremental rather than substitutive, continuing the claims of the previous paper (see v1) and focusing on two new questions: how to manage capabilities at scale and how to compose them.

**Keywords**: life cycle, capability composition, research capabilities, seller–buyer division of labor, fixed income

---

## 1. Introduction

### 1.1 The Evolution of the Problem

Skill 1.0 addressed whether research capabilities could be encapsulated. Historically, analytical assets such as liquidity condition and credit spread analysis lived as Excel databases containing dozens of sub-sheets, each carrying one analytical view with embedded data retrieval, calculations, threshold judgments, and chart templates. Every week an analyst opened the file, refreshed it manually, scanned the numbers, and wrote commentary by hand. Skill 1.0 packaged these databases into skills an AI can read and execute directly — one skill being one complete capability. At this stage, research capability took the form of "one thing": delivered whole, used whole, and modified only by those with technical skills.

Scale created a new problem. When one production template yielded 13 topic-based databases and roughly 500 analysis logic units, whole-piece delivery no longer held: who maintains which part, whether versions are aligned, whether outputs are trustworthy, how dozens of parts can be chained around a single investment question — none of this existed with one or two skills; scale forced it into existence. Research capability thereby moved from "one thing" to "a box of parts." This paper frames that shift as moving from a workshop to a factory: previously each item was crafted by hand as a whole; now a box of standard parts exists and is assembled on demand. Correspondingly, the way we understand a research system must also advance from inspecting single items to managing a whole box.

### 1.2 Positioning of This Paper

This paper is incremental research. Following the claims of the previous paper on skill-based middleware architecture (see v1), it does not revisit v1's technical details of capability decomposition and encapsulation. Instead it addresses two new questions raised by scale: how to *manage* a growing collection of capabilities — called the life cycle here — and how to *compose* capabilities around a problem — called capability composition. Together these two constitute the methodological increment from Skill 1.0 to Skill 2.0.

## 2. The Life Cycle: Research Capability from "One Thing" to "A Box of Parts"

The life cycle answers where parts come from and how they are used. It naturally splits into two columns by role: the seller governs how parts are produced; the buyer governs how parts are used. This paper deliberately places its weight on the buyer — buying-side researchers are assemblers rather than parts manufacturers, and in daily work they touch exactly three things.

### 2.1 The Seller Side: Manufacturing Parts and Putting Them on the Shelf

Two things on the seller side, in brief. The first is manufacturing: packaging research outputs into standard parts under one template — a directory describing the views contained and when to call them; a contract specifying the expected data inputs; a document spelling out how indicators are computed; a file recording judgment experience (how wide counts as tight, how narrow counts as loose); and output templates prescribing how charts appear and how commentary is organized. The second is shelving: packaging, validating, and publishing parts, with installation on user platforms done by the author. Buyers need not care about any of this; what they receive is a ready-to-use, immediately composable part. Under this template, 13 topic-based databases and roughly 500 analysis logic units have so far been produced.

### 2.2 The Buyer Side: Take and Use, Verify, Change on Request

The three things buyers actually deal with form the backbone of the life cycle.

**Take and use.** Pick whatever parts are needed and use them directly, with no need to understand what lies inside. Say what is wanted, and the AI handles data retrieval, computation, and output in one pass. A liquidity database may hold thirty-odd views, of which a buyer often needs only a few: take what is needed without learning the whole system or loading everything. Where buyers once had to master an entire database before using it, they now need only say what they want.

**Verify.** Whether a result is trustworthy is now checkable. Every capability sits on a baseline — a set of historically reasonable ranges; when a result falls into an extreme position, an alert is raised, and one checks the data chain before believing the conclusion. The worst thing in research is not being wrong; it is being wrong without knowing where, and without others being able to reproduce it. Baselines plus reproducibility make "checkable results" the default action.

**Change on request.** Dissatisfaction is expressed in plain language, and the AI makes the change. Logic changes no longer require code; edits land on a single part without disturbing the rest of the box, and one maintenance point benefits everywhere the part is used. A researcher's experience accrues through repeated rounds of "change on request," and the capability steadily conforms to individual judgment habits.

### 2.3 Design and Implementation: Three Mechanisms That Make Both Columns Work

These experiences are not promised into existence; three mechanisms support them. The first is a unified template: every part follows the same format — directory, contract, formulas, thresholds, and output templates each in their place — assembled neatly, and therefore inspected neatly. The second is module-level updating: changes are scoped to parts, and upgrading one view does not disturb the rest of the box; this is the precondition on which "change on request" rests. The third is baseline validation: every output has a reference frame, and extreme positions trigger an alert; this is the precondition on which "verify" rests. In plain words: the box is packed neatly, parts swap easily, and the scale reads reliably.

## 3. Capability Composition: Turning an Idea into a Result

The life cycle answers how parts are managed; capability composition answers how parts are assembled. Turning a box of parts into a chain that answers a concrete investment question takes four steps, all in plain language.

### 3.1 The Four Steps

**Step one: decide what to look at.** A concrete investment question sets the assembly target — for example, "Liquidity is tightening; will institutions start selling; will credit spreads widen?" The more specific the question, the clearer the chain to be assembled.

**Step two: pick parts.** Consider which capabilities help: take one slice of liquidity, one slice of institutional behavior, one slice of credit spreads. Picking does not touch the inside of any part — every part is pre-assembled and ready to use.

**Step three: assemble and run.** Connect the chosen parts into an end-to-end chain, run it through, and obtain a chart, a table, and a commentary. Every step leaves a trace, so anything once run can be reproduced.

**Step four: speak up when unsatisfied.** Propose changes in one plain sentence and the AI adjusts the assembly; once satisfied, save this assembly for reuse next time — it becomes your own.

The value of capability composition in one sentence: **an investment question is solved not by rebuilding the wheel but by assembling existing parts around the question.** Only when assembly is this simple do buying-side researchers save their attention for judgment rather than for data pulls, calculations, and reconciliation.

### 3.2 Relationship to the Life Cycle: Management Is the Stock; Composition Is the Cooking

These are not two parallel activities but two consecutive stages. The life cycle governs quality and availability: without a unified template, module-level updating, and baseline validation, parts cannot be trusted, swapped, or upgraded, and any assembled chain is unreliable — management is the provisioning of ingredients before the cook begins. Capability composition governs objective and output: turning trusted parts into a specific piece of research — composition is the cooking that is served. Order matters: only after trustworthy parts exist does reliable assembly become possible; without either side, the other does not work.

## 4. Real-World Case and Measurement

### 4.1 Case Background

A three-segment transmission chain — liquidity, institutional behavior, credit spreads — demonstrates capability composition: the liquidity environment is graded, institutional behavior is read for turning points, and credit spread pricing status is assessed. The three parts belong to three independent databases — the liquidity database, the institutional behavior database, and the credit spread database — none of which was built for this particular question. Data come from real data sources, with the latest snapshots dated August 19-20, 2026.

### 4.2 The Liquidity Segment: Environment Grading

The liquidity part grades the environment as loose, neutral, or tight by CD yields. Over the past thirty trading days the 1M CD yield stayed in a narrow band between 0.38% and 0.50%, closing at 0.50% on August 20 — a **loose** reading. Ample liquidity is the starting point of the chain.

### 4.3 The Institutional Behavior Segment: Who Buys, Who Sells

The institutional behavior part reads buying and selling pressure through institutions' net cash-bond purchases. On August 19: large banks net sold CNY 17.12 billion, down a further CNY 8.27 billion week-on-week; small- and medium-sized banks net sold CNY 57.52 billion, down CNY 83.44 billion week-on-week; securities firms net sold CNY 28.14 billion. Meanwhile, funds and products net bought CNY 33.28 billion, up CNY 55.22 billion week-on-week; other institutions net bought CNY 52.93 billion, up CNY 26.29 billion. **Banks and brokers are reducing exposure; funds and others are absorbing.** Against a loose liquidity backdrop, institutional behavior points to active deleveraging — the first tension in the chain.

### 4.4 The Credit Spread Segment: Pricing Status

The credit spread part reads pricing status through 3-year mid-short paper spreads over government bonds. On August 20: AAA 3Y at 34.9bp, AA 3Y at 51.9bp, AA- 3Y at 99.9bp. Spreads sit broadly in the neutral range, and credit pricing is stable — the divergence in institutional behavior has not yet transmitted to prices.

### 4.5 The Transmission-Chain Status Panel and Judgment

The three segments assemble into a single status panel:

| Segment | Reading | Status |
|---|---|---|
| Liquidity | 1M CD yield 0.50% (2026-08-20) | Loose |
| Institutional behavior | Large banks −17.12, SME banks −57.52, securities firms −28.14; funds and products +33.28, others +52.93 (CNY bn, 2026-08-19) | Divergence: banks/brokers reducing, funds/others buying |
| Credit spreads | AAA 3Y 34.9bp, AA 3Y 51.9bp, AA- 3Y 99.9bp (2026-08-20) | Neutral range; stable pricing |

The panel shows: liquidity is loose (1M 0.50%); institutional behavior is divergent — banks and brokers reducing while funds and others buying; credit spreads are stable (AAA 3Y 34.9bp, AA- 3Y 99.9bp). **The three segments do not move in the same direction**: the environment is loose, yet some institutions are actively deleveraging; spreads have not widened visibly on the institutional divergence. For the buying-side researcher there are two implications: first, in the current environment institutional behavior deserves tracking more than spread pricing; second, the persistence of bank and broker reduction is the leading signal for judging whether credit spreads will widen. The point of the case is not the three standalone results but the assembly itself — three parts, none built for the other's question, assembled into an answer for a concrete investment question.

## 5. Discussion

### 5.1 Relationship with v1: Incremental, Not Substitutive

The v1 paper answered how research capabilities are decomposed and encapsulated as wholes; this paper answers how a collection of decomposed capabilities is managed and composed. The two focus points connect end to end, and the underlying idea runs through both unchanged: the seller manufactures parts; the buyer assembles the car. This paper advances v1 rather than rewriting it and substitutes for none of its content; readers interested in encapsulation details should return to the v1 paper.

### 5.2 Limitations

First, the value of capability composition is constrained by the richness of the part library: the more, and the more standardized, the parts, the more efficient the assembly; gaps in the library leave many investment questions with no chain to assemble. Second, the life cycle depends on sustained seller-side maintenance: when part definitions are incomplete, the reliability of assembled results degrades, and "verify" can only catch errors within already existing baselines, not errors in the definitions themselves. Third, the case is a cross-sectional snapshot covering only two trading days (August 19-20, 2026); the transmission from environment, to behavior, to spreads must be validated on a longer time series before it can move from "telling a story" to "showing statistically significant evidence."

### 5.3 Outlook

Three directions. First, more parts: cover more topics so that more investment questions have parts to assemble. Second, more standard contracts: interfaces between parts become increasingly uniform, reducing the friction of cross-database assembly. Third, evolution toward natural language: building on "change on request," let buying-side researchers describe research ideas in plain language and let capability composition generate the assembly directly — further releasing research productivity.

## 6. Conclusion

From Skill 1.0 to Skill 2.0, the change is not a rewrite but an upgrade of research capability from "one thing" to "a box of parts": the life cycle makes parts manageable, and capability composition makes parts assemblable. The seller manufactures parts and the buyer assembles the car — this underlying idea has never changed; what has changed is only the richness of the parts and the ease of assembly. The real-world case shows that assembling three unrelated parts — liquidity, institutional behavior, and credit spreads, none built for the others — into a transmission chain answers a concrete investment question. That is the story of Skill 2.0.

## Appendix

### Appendix A: Life Cycle and Capability Composition at a Glance

```
Life cycle (manage parts: management is the stock)     Capability composition (assemble the chain: cooking)
┌───────────────────────────────────────┐            ┌─────────────────────────────────────────────────┐
│ Seller: manufacture parts, put on shelf │            │ ① Decide what to look at                       │
│ Buyer:  take-and-use, verify,            │            │ ② Pick parts (pre-assembled, ready to use)      │
│         change-on-request                │            │ ③ Assemble and run (traced, reproducible)       │
└───────────────────────────────────────┘            │ ④ Speak up when unsatisfied (save as your own)  │
                                                      └─────────────────────────────────────────────────┘
```

### Appendix B: Real-Data Panel Table (2026-08-19/20)

| Segment | Latest date | Key readings | Judgment |
|---|---|---|---|
| Liquidity | 2026-08-20 | 1M CD yield 0.50% (30-day range 0.38%-0.50%) | Loose |
| Institutional behavior | 2026-08-19 | Large banks −17.12 (WoW −8.27); SME banks −57.52 (WoW −83.44); securities firms −28.14 (WoW −8.34); funds and products +33.28 (WoW +55.22); others +52.93 (WoW +26.29) | Divergence: banks/brokers reducing, funds/others buying |
| Credit spreads | 2026-08-20 | AAA 3Y 34.9bp; AA 3Y 51.9bp; AA- 3Y 99.9bp | Neutral range; stable pricing |

Institutional behavior breakdown (2026-08-19; CNY bn, WoW change in CNY bn):

| Institution | Latest net purchases | WoW change |
|---|---|---|
| Small/medium banks | −57.52 | −83.44 |
| Insurance companies | +12.47 | +4.33 |
| Others | +52.93 | +26.29 |
| Funds and products | +33.28 | +55.22 |
| Large banks | −17.12 | −8.27 |
| Wealth-management products | +10.96 | +0.08 |
| Securities firms | −28.14 | −8.34 |
| Money-market funds | −6.86 | +14.13 |

---

*Continuously updated. Latest version: [github.com/timyefi/skill20-arch](https://github.com/timyefi/skill20-arch)*