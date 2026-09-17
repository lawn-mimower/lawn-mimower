## Mihir Mohite

I build LLM systems that have to be right, and embedded rigs that have to be measured.

Mostly Python, Node and C++ — retrieval pipelines, agent evaluation, and sensor hardware
that talks back over WiFi.

---

### Work

**[lawmaster](https://github.com/lawn-mimower/lawmaster)** — retrieval over Indian
industrial law · `Python` `FastAPI` `LightRAG`
43 statutes, 1,210 pages, much of it Hindi. Uniform chunking destroys legal text, so a
router splits the corpus four ways — definitions, sections, tables, amendments — and
sends each to the store that fits it. Answers cite back to the source page.

**[luna-reasoning-eval](https://github.com/lawn-mimower/luna-reasoning-eval)** — how much
reasoning a task actually needs · `Python`
11 suites, four effort modes, ~9,000 API calls, a cost ledger on every one. For most
tasks, maximum effort bought nothing measurable. Ships with an adversarial audit of its
own conclusions.

**[foresites](https://github.com/lawn-mimower/foresites)** — construction snag tracking
over WhatsApp · `Node` `React` `Python` `AWS`
Site staff report defects with a photo or voice note; it lands in Postgres, gets
assigned, and is tracked to a signed-off resolution. Four subsystems, including a Lambda
agent that turns plain English into SQL and a chart.

**[stereo-vergence-scanner](https://github.com/lawn-mimower/stereo-vergence-scanner)** —
2D room mapping on £15 of parts · `C++` `Python`
Two time-of-flight sensors on two servos, verging on a point like a pair of eyes. A
single sweeping sensor can't tell a wall from the edge of a doorway; two verged ones can.

**[imu-drift-compensation](https://github.com/lawn-mimower/imu-drift-compensation)** —
measuring gyro drift instead of assuming it · `C++` `Python`
Fits the drift of a stationary MPU6050 and subtracts it live, so the correction comes
from the sensor's own behaviour rather than a datasheet constant.

---

`Python` · `Node/Express` · `React` · `C++ (ESP8266)` · `FastAPI` · `Postgres` ·
`AWS Lambda / S3` · `scikit-learn`

📫 [mihir.moe@gmail.com](mailto:mihir.moe@gmail.com)
