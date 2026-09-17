## Mihir Mohite

I build agentic systems and instrument embedded hardware — and I spend most of my
effort on the part in between: checking whether the thing actually works.

Two of the repos below exist mainly because I didn't trust my own results. One is an
adversarial audit that retracted a recommendation I'd already shipped. The other is a
scanner whose interesting output isn't the map, it's the disagreement between two
sensors looking at the same point.

---

### Selected work

**[luna-reasoning-eval](https://github.com/lawn-mimower/luna-reasoning-eval)** · Python
How much reasoning does a task actually need? 11 suites, four effort modes, ~9,000 API
calls, a cost ledger on every one. The answer for most suites was *none of it* — effort
made no measurable difference, which is the finding worth having.

Then I audited my own conclusions and found a separator bug: the parser split on `;`
while the prompt template joined on `, `, silently truncating 96 of 96 handover payloads.
The "sufficiency" result built on top of it was an artifact. McNemar tests knocked three
more claims from *measured* to *unsupported*. `AUDIT.md` classifies every finding as
definitely wrong / unsupported / fragile, with a column for whether it changes a
decision.

**[lawmaster](https://github.com/lawn-mimower/lawmaster)** · Python, FastAPI, LightRAG
Retrieval over Indian industrial and environmental law — 43 statutes, ~1,210 pages, much
of it Hindi, a lot of it tables.

Uniform chunking destroys what makes legal text answerable, so a router splits the corpus
four ways and sends each to the store that fits: definitions become one chunk per term,
sections keep their hierarchy, rate tables go to SQLite because they're useless as prose,
amendments get resolved as diffs rather than retrieved. Answers carry chunk-ID citations
back to the source page.

**[foresites](https://github.com/lawn-mimower/foresites)** · Node, React, Python, AWS
Snag management for construction sites, reported over WhatsApp. Site staff send a photo
or a voice note; it lands in Postgres, gets assigned, and is tracked to a signed-off
resolution with proof. Four subsystems — WhatsApp webhook, REST API, React dashboard, and
a Lambda agent doing plain-English → SQL → chart.

The constraint that shaped it: the people who find problems on site will not learn new
software, so the reporting side had to stay inside WhatsApp.

**[stereo-vergence-scanner](https://github.com/lawn-mimower/stereo-vergence-scanner)** · C++, Python
Two time-of-flight rangefinders on two servos, verging on a common point at each bearing
like a pair of eyes. A single sweeping sensor can't tell a wall from the edge of a
doorway; two verged ones can, because a smooth surface returns a predictable
relationship and a depth discontinuity doesn't.

Getting that right took being wrong twice. A fixed tolerance flagged 103 of 179 bearings
on a *flat wall* as edges. The real cause was geometry I'd assumed away: verged beams
only coincide at one distance, and elsewhere land `B·|1 − r/R|` apart — 6.7cm at half a
metre, on a perfectly smooth surface. Disagreement only means something as a residual
against that.

**[imu-drift-compensation](https://github.com/lawn-mimower/imu-drift-compensation)** · C++, Python
A gyro integrated over time drifts. This measures the drift on a stationary MPU6050, fits
it with linear regression, and feeds the coefficients back to subtract it live — so the
correction comes from what the sensor actually does, not a datasheet constant.

---

### What I reach for

Python · Node/Express · React · C++ (ESP8266/Arduino) · FastAPI · Postgres/Supabase ·
AWS Lambda & S3 · scikit-learn · MATLAB

RAG and agent pipelines, LLM evaluation, and small embedded sensor rigs.

---

📫 [mihir.moe@gmail.com](mailto:mihir.moe@gmail.com)
