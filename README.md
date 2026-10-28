# Operable Futures: AI Systems for AEC

**Research Studio: Smart Construction · MaAI01 · IAAC 2026/27**

This repository is the main directory for the studio. Each team's project lives in its own repository and is linked here as a [git submodule](https://git-scm.com/book/en/v2/Git-Tools-Submodules) under [`projects/`](projects/).

---

## About the Studio

It has become harder to know what is real. What we see and read is increasingly generated, filtered or simply untrue. But data is not fiction: every measurement is a trace of something that actually happened, a wall that cracked or a material that was wasted. Architecture, engineering and construction (AEC) together form one of the most physical sectors there is, and AI is now entering every part of it. What will survive the reality check, and what will remain another image?

Operable Futures is a design studio on AI tools for AEC. Students design and build tools that use AI to address a real problem in the life of a building project, from design to end-of-life. The goal is not speculative renderings but **feasible, testable and operable systems**. Each project is framed as an engineering mission; depending on the problem, the outcome may be agentic software, MCP connectors, spatial data pipelines, AR/VR environments or physical prototype controls.

### Questions We Raise

- **Where is the problem?** Which moments in an AEC project are slow, wasteful, risky or poorly executed, and who experiences them?
- **What data exists?** What traces does that moment leave: drawings, BIM models, sensor readings, schedules, material records, images?
- **What could AI generate?** A prediction, a design option, a classification, a plan? Why AI, rather than a rule, a script or a skilled person?
- **Where are the limits?** What can the data not tell us? How is the output verified against physical reality: loads, tolerances, costs, schedules?
- **Who is affected?** Who uses the tool, who carries the risk, and who is responsible when it is wrong?

### The Four AEC Stages

Each team anchors its problem in one stage of an AEC project:

| Stage | Scope |
|---|---|
| **Design & Pre-Construction** | Feasibility, design, engineering, estimating, permitting |
| **Procurement & Off-Site Manufacturing** | Materials, suppliers, prefabrication, logistics |
| **On-Site Execution** | Assembly, sequencing, progress, quality, safety |
| **Operation & End-of-Life** | Use, maintenance, reuse, deconstruction |

### Thinking Method: Zoom Out, Zoom In

- **Zoom out:** look at what happens before and after the problem. Where does it really start, and what does it cause later?
- **Zoom in:** break the problem into parts small enough to build and test.

> *Example:* prefab panels arrive on site and do not fit. Zooming out shows the cause is earlier: the factory cut them from an old version of the model. Zooming in, the team picks one small part to work on: checking the model version before cutting.

---

## Student Projects

| Team | Project | Members | AEC Stage | Repository |
|---|---|---|---|---|
| 1 | **Roofscapes (Re)Imagined:** unlock your roof's potential, shape your building's future. Shows Barcelona apartment owners what their rooftop could become (added floor, shared roof, solar, green or cool roof) from public data and roof photos. | Sindhuja Davuluri, Breno Sader, Daria Basha | Design & Pre-Construction | [`projects/Roofscapes_ReImagined`](projects/Roofscapes_ReImagined) |
| 2 | **PMI: Project Management Intelligence.** Builds an initial Gantt chart from drawings, budgets and material schedules, then updates it and flags delivery risks when project information changes. | Chloe Hraibeh, Nandini Rathod, Ahmed Belahcen | Design & Pre-Construction | [`projects/PMI`](projects/PMI) |
| 3 | **Concrete Evidence:** rebar inspection and impact estimation before the pouring of concrete. Checks each bay with a phone against the drawings and Código Estructural tolerances, returning OK, Warning or Stop. | Akanksha Dhumal, Diego Alpízar Vázquez, Akshat Dayal | On-Site Execution | [`projects/Concrete_Evidence_AI`](projects/Concrete_Evidence_AI) |
| 4 | **Sentra:** real-time construction progress tracking platform. Monitors milestones, identifies potential delays and turns construction data into actionable insights. | Amelia Courtney, Emmanuel Márquez Granados, Karthikeyan Saravanan | On-Site Execution | [`projects/Sentra`](projects/Sentra) |
| 5 | **Cost Wise ULLADA.** AI-assisted renovation cost estimation from images. | Bo De Roeck, Sneha Sachin Shenoy, Sanjana Kiran | Design & Pre-Construction | [`projects/ULLADA`](projects/ULLADA) |
| 6 | **Second Look:** an early warning check for homes nobody inspects. Measures and classifies a photographed crack, applies auditable rules and decides whether an engineer must look next. | Jerome Eid, Luis Wulf | Operation & End-of-Life | [`projects/SeconD_Look`](projects/SeconD_Look) |
| 7 | **Nomad:** let's find you a home. Checks an IFC model of a vacant building against CTE, Catalan and Barcelona rules for conversion to housing, and proposes ranked fixes. | Bars Babila, Bhavini Manot, Álvaro Miñé | Design & Pre-Construction | [`projects/Nomad`](projects/Nomad) |
| 8 | **Fit-Well:** fit material, fit space. Turns a client's references and brief into project parameters and returns an honest cost range backed by comparable built projects. | Hetashri Kalyani, Ugochinyere Megwa, Samiha Abeda Nur | Design & Pre-Construction | [`projects/Fit_Well`](projects/Fit_Well) |
| 9 | **SpecSynth AI:** stop non-compliant products reaching the spec. Extracts manufacturer data into material schedules, validates it against project requirements and links every value to its evidence. | Fawad Saleem, Soumyajyoti Datta, Kazuko Nakao | Procurement & Off-Site Manufacturing | [`projects/SpecSynth_AI`](projects/SpecSynth_AI) |
| 10 | **Right Fit:** material approval, rethought. Checks material approval forms and data sheets against the specification, BOQ, codes and past reviewer comments, and suggests products that fit. | Jeff El Khoury, Sahil Mansoor Khan, Luca Obejdeanu | Procurement & Off-Site Manufacturing | [`projects/RightFit`](projects/RightFit) |

<!-- Add one row per team when its submodule is added. -->

### Cloning this repository

```bash
# Clone with all student projects
git clone --recurse-submodules <this-repo-url>

# Or, if already cloned
git submodule update --init --recursive

# Pull the latest commit from every project
git submodule update --remote --merge
```

### Adding a team project (faculty)

```bash
git submodule add <team-repo-url> projects/<team-name>
git commit -m "Add <team-name> project"
```

Then add the team to the table above.

### Expected structure of a team repository

Each team repository should follow the Spec-Driven Development layout used in the studio:

```
<team-repo>/
├── AGENTS.md                 # System constitution for the agent harness
├── README.md                 # Problem & data brief, team, how to run
├── spec/
│   └── constitution/
│       ├── mission.md
│       ├── roadmap.md
│       └── tech_stack.md
├── src/                      # Features
├── tests/                    # Tests, including the non-AI baseline comparison
└── docs/
    ├── BLOG_POST             # IAAC blog post draft
    └── PITCH_DECK            # 10-slide startup pitch
```

---

## Workflow

The course runs in three overlapping clusters. The design narrative (the problem, its context and its argument) and the technical system (data, agents, prototype) develop in parallel and inform each other throughout: the problem is defined as the prototype reveals what the data can and cannot do.

### Cluster 1: Concept & Idea Development (¼ of the course)

Teams move from initial ideas to a defined problem, challenged by an industry expert and placed within one of the four stages. In parallel, they map the available data and set up the repository.

- Initialized repository with `AGENTS.md` system constitution
- SDD constitution: `spec/constitution/mission.md`, `roadmap.md`, `tech_stack.md`
- Hierarchical Problem Segmentation Tree (from macro to atomic level)

### Cluster 2: Build (½ of the course)

Teams translate the concept into specifications and build the core system using Spec-Driven Development. Agents connect through MCP to real data sources, and every tool is tested against the non-AI way of doing the same task.

- Agent harness working in Plan and Build modes
- MCP connections to external data sources
- Features in `src/` with tests in `tests/`, including the baseline comparison
- Physical or digital proof of concept (BIM generator, AR/VR prototype, material simulation, physical test)

### Cluster 3: Operability & Demonstration (¼ of the course)

Teams build an interface, test the system under realistic conditions, and consolidate the narrative.

- Deployable product interface (Web UI, Streamlit or Obsidian dashboard)
- IAAC blog post (`docs/BLOG_POST`): project, agent harness architecture and outcomes
- 10-slide startup pitch deck (`PITCH_DECK`)
- Final studio defense: live operable system demonstration and startup pitch before an external jury

---

## Technical Approach: Harness Engineering & Spec-Driven Development

The studio moves away from unconstrained "vibe coding" and image generation toward **Harness Engineering** and **Spec-Driven Development (SDD)**: designing the boundaries within which each AI agent works, so that its outputs are reliable, verifiable and grounded in physical reality.

- **Probabilistic models, physical reality.** Language models predict plausible outputs; they do not understand loads, physics or material costs. Agents must be connected to verified data and their results tested.
- **Narrowing the solution space.** Open prompts produce arbitrary results. The designer defines what the agent may and may not do, through explicit rules and negative constraints (what *not* to do).
- **Context hygiene.** Long sessions degrade the agent's context. Reset sessions deliberately (`/compact`, `/clear`) and keep project knowledge in persistent files rather than in conversation.

---

## Schedule

| Date | Phase | Activities | Target outcome |
|---|---|---|---|
| Oct 8 | Intro | Intro session | |
| Oct 15 | Concept | Teams form. Each student brings one idea and one reference (startup, product or research). An industry expert challenges ideas and data claims; each team chooses one problem and anchors it in a stage. | One problem with a clear stage, a named user and a plausible path to data. |
| Oct 22 | Concept | Studio intro, the four AEC stages, harness/SDD principles. Idea pitches. | Students can tell a real, evidence-based AEC problem and know what is already being built in the market. |
| Oct 29 | Concept + Build | Segmentation tree. Full data mapping (availability, access, format, gaps). Repo + `AGENTS.md` setup. | Teams know what data exists and what it cannot tell; the agent runs on real data for the first time. |
| **Nov 6** | **Midterm** | **Midterm presentations** (submission deadline Nov 5) | |
| Nov 12 | Concept + Build | Full SDD constitution, first feature with tests, first MCP connection attempt. | Teams can argue why AI is needed, with a first feature measurable against the baseline. |
| — | Hackathon week | No studio | Beta version |
| Nov 26 | Build | Full plan/build harness, MCP connectors to all mapped sources, roadmap features, context hygiene. | The agent works within defined boundaries across several live sources; the system grows feature by feature from specs. |
| Dec 3 | Build | Features + tests, comparison against the non-AI method, refined problem and data map. | Measurable evidence of whether the tool beats the baseline, where it fails, and which data gaps cause it. |
| Dec 10 | Build + Operability | Physical/digital PoC. Limits and ethics check: data ownership, bias, responsibility. UI build and testing. | The system is checked against physical reality and its risks and responsibilities are explicit. |
| Dec 14 | Operability | UI build, testing in realistic conditions, narrative draft. | The story matches what the system does; final tweaks. |
| **Dec 17** | **Final** | **Final presentations** | |

---

## Deliverables

1. **Problem & data brief:** the problem, placed within a project stage, the data behind it, and answers to the 8 questions of the [Heilmeier Catechism](https://www.darpa.mil/about/heilmeier-catechism).
2. **Project repository:** `AGENTS.md`, specifications, code and tests, including a comparison against the non-AI approach.
3. **Operable prototype:** a working tool with a usable interface, supported by a physical or digital proof of concept.
4. **Lean Canvas:** a one-page summary of the problem, users, solution and value.
5. **Final presentation:** a live demo and a pitch with a pitch deck.
6. **IAAC blog post:** project documentation following the IAAC Publication Guidelines.

All material must be submitted to the IAAC Google Drive, and a blog post curated on [blog.iaac.net](https://blog.iaac.net) for each project, within one week after the end of the studio.

## Learning Objectives

By the end of the course, students will be able to:

- Define a real problem in the construction process, supported by evidence.
- Evaluate critically where AI is the appropriate tool, and where it is not.
- Design and build an operable AI tool connected to verified data sources.
- Identify the ethical implications of AI in construction and address them in design.
- Communicate and defend a project to technical and industry audiences.

---

## Faculty

- **Rasha Sukkarieh** — Faculty. Architect and R&D Manager of the Robotics Lab at IAAC, leading research in circularity and digital construction. Brings the industry perspective and entrepreneurial mindset to the studio.
- **Nacho Monereo** — Faculty. Architect, computational designer and robotics expert working at the convergence of AI, robotic fabrication and computational construction. Leads the technical dimension of the studio. [nachomonereo.com](https://nachomonereo.com)
- **Salvador Cantuarias** — Faculty Assistant. Architect and AI engineer working on rule-based database architecture, ontology engineering, automated reasoning and knowledge retrieval.

## References

- MoureDev / Brais Moure — *Aprender a Programar con Agentes de IA* (Harness Engineering & Agentic Guardrails)
- Steph Ango (kepano) — Obsidian Skills Specification & Agentic File Protocols
- [Model Context Protocol (MCP) Specification](https://modelcontextprotocol.io/)
- Maier, M. W., & Rechtin, E. — *The Art of Systems Architecting*
- INCOSE — *Systems Engineering Handbook*
- [Heilmeier Catechism (DARPA)](https://www.darpa.mil/about/heilmeier-catechism)

---

[Institute for Advanced Architecture of Catalonia (IAAC)](https://iaac.net) · MaAI 2026/27
