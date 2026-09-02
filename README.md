<p align="center">
  <img src="assets/banner.png" width="100%" alt="Hephaestus banner: a hammer drawn as a constellation on a night sky, with the wordmark and the line &quot;AI, forged into working tools.&quot;">
</p>

<p align="center">
  <sub>AI AUTOMATION STUDIO · UNITED STATES · REMOTE</sub>
</p>

<p align="center">
  <strong>A student-led studio that puts an engineer inside your team: forward-deployed, not handed to an account manager.<br>
  We build the work your people still do by hand into a tool that does it for them.</strong>
</p>

<p align="center">
  <em>Fixed quotes. Senior-level engineering. Forged in days.</em>
</p>

<p align="center">
  <a href="https://usehephaestus.com"><img src="https://img.shields.io/badge/live-usehephaestus.com-9E3520?style=flat-square&labelColor=3B2A1C" alt="Live at usehephaestus.com"></a>
  <a href="mailto:kasani@business.unc.edu"><img src="https://img.shields.io/badge/contact-kasani%40business.unc.edu-B0572A?style=flat-square&labelColor=3B2A1C" alt="Contact by email"></a>
  <a href="ARCHITECTURE.md"><img src="https://img.shields.io/badge/read-ARCHITECTURE.md-C9A24A?style=flat-square&labelColor=3B2A1C" alt="Read the architecture write-up"></a>
</p>

<p align="center">
  <img src="assets/screenshots/hero.png" width="100%" alt="The live Hephaestus site: a vellum sheet with torn edges and watercolour washes, the headline &quot;Hephaestus forges workflow automation.&quot; in serif with the second line in rubric red, a Homeric note in the right margin, and a jointed wooden automaton hammering an anvil at the lower right.">
</p>

> **i · Acting of itself.**
> *Automaton* is Greek — αὐτόματον, the thing that acts of itself. Homer uses the adverb of the gates
> of heaven, which swing open with nobody touching them. The word is three thousand years older than
> the industry that borrowed it.
>
> <sub>ILIAD V. 749</sub>

---

<sub>I · HEAT</sub>

## No overhead. *No lock-in.* No waiting.

Engagements stay small and direct: the senior builder who scopes your project is the one who forges it.

**01 · A fraction of agency cost.** No sales layer, no account management baked into the price. You pay for the build itself.

**02 · Production quality.** Documented, tested, and yours to keep. Ships with the code, the docs, and a walkthrough.

**03 · Days, not weeks.** Same-day first reply, a fixed quote within a day, most projects delivered inside a week.

<sub>II · DRAW</sub>

## What we forge

| Service | What it is |
|---|---|
| **Data cleanup** | Hand over the messy spreadsheet; get back clean, deduped, consistently formatted data. |
| **Workflow automation** | The repetitive copy-paste task that eats a week becomes a one-click job that runs itself. |
| **Chatbots & assistants** | A helper that answers questions from your own docs — for your team or your customers. |
| **Document processing** | Contracts, invoices, intake forms, PDFs: the numbers and details you need, pulled out and organized. |
| **Internal tool prototyping** | The dashboard or admin tool you keep meaning to build, delivered as a working v1 in days. |
| **Something else?** | If it can be made faster or smarter with AI, it probably fits. |

A starting menu, not a limit.

<sub>III · BLOW</sub>

## The sheet

<p align="center">
  <img src="assets/screenshots/why.png" width="536" alt="The &quot;No overhead. No lock-in. No waiting.&quot; section of the live site: the numbered pillars set on the vellum sheet, with the second Homeric margin note beside them.">
  <img src="assets/screenshots/phone-hero.png" width="168" alt="The same hero on a phone: the sheet reflows to one column and the margin note narrows beside it.">
</p>

<p align="center">
  <sub>The pillars and the second note in the margin · the phone band.</sub>
</p>

The site is one HTML file and one TypeScript module, no framework. Scroll turns the hour, dawn to
night, and each of seven hammer blows throws wet pigment into the marginalia column, where the words
flow around the blot's own outline. The ink lands in the margin; the hand writes round it.

**[How it is built → ARCHITECTURE.md](ARCHITECTURE.md)**

<sub>IV · STRIKE</sub>

## Four steps, start to handoff

1. **Bring us the raw problem.** A quick call to walk through what you need. We are honest about fit.
2. **Fixed quote, fast.** A clear scope, a fixed price, a delivery date usually within a day, and no hourly meter.
3. **We forge it.** Visible progress and a working result in days, no black boxes.
4. **Handoff + walkthrough.** Handed over with a short walkthrough so your team can run it. It's yours.

<sub>V · WELD</sub>

## The shape of an engagement

The three below are illustrative — the shape of the work we take on, not named client engagements.

| | Problem | Result |
|---|---|---|
| **Law-firm intake extraction** | Paralegals hand-keying details from hundreds of intake PDFs. | Clean, structured records in minutes — reviewed, not retyped. |
| **Ops dashboard** | Weekly numbers scattered across five spreadsheets and a CRM. | One live dashboard the whole team checks each morning. |
| **Support chatbot** | The same twenty questions filling up the support inbox all day. | Instant answers on-site; the inbox is for real issues now. |

<sub>THIS REPOSITORY</sub>

## Under the hood

No source code here: this repo is documentation, diagrams, and screenshots. The engineering write-up
lives in **[ARCHITECTURE.md](ARCHITECTURE.md)**: the scroll-driven colour system, the inverse-kinematic
figure, the three-canvas watercolour model, and the margin trick where a paint-less float and the ink
over it are clipped to one shared polygon so the text wrap and the blot agree to the decimal.

- **Front end.** One static `index.html` plus one typed module, `src/sheet.ts`: 25 kB of JS, 11 kB gzipped.
- **Dependencies.** Zero at runtime. `typescript` and `vite` are the only devDependencies.
- **Renders without JavaScript.** The CSS defaults are a composed late-dusk moment; the script is enhancement.
- **Hosting.** AWS S3 and CloudFront, deployed by GitHub Actions on push to `main` via OIDC.

<sub>VI · QUENCH</sub>

## Small studio. National reach.

An independent AI automation studio working with businesses across the United States: data cleanup,
document processing, assistants, and the internal tools teams keep wishing they had. Book a 30-minute
call and you'll leave it with next steps and a fixed quote the same day.

- **Web** · [usehephaestus.com](https://usehephaestus.com)
- **Contact** · [kasani@business.unc.edu](mailto:kasani@business.unc.edu)
- **Built by** · Sai Kasani · CS + Finance, UNC · Claude Builder Ambassador

> **viii · Honest about fit.**
> A blot that has begun to dry cannot be lifted clean — the pigment has already sunk into the fibre and
> what comes off is only the surface. So the answer arrives on the call, not in a proposal three weeks
> later: if it isn't a good job for us we will say so while it is still wet.

<p align="center">
  <img src="assets/mark.svg" width="30" alt=""><br>
  <sub>© 2026 Hephaestus · Sai Kasani</sub>
</p>
