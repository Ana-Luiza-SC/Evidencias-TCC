# TCC-evidences

[![Português](https://img.shields.io/badge/idioma-Português-green?style=for-the-badge)](README.md)
[![English](https://img.shields.io/badge/language-English-blue?style=for-the-badge)](README.en.md)

Input artifacts, evaluation instruments and proof-of-concept evidence for the experiment of the undergraduate thesis **"Prototipação de interfaces com IA generativa: efeitos das modalidades de entrada sobre produtividade, aderência aos requisitos, esforço de refinamento e custos"** (_Interface prototyping with generative AI: effects of input modalities on productivity, requirements adherence, refinement effort and costs_).

- **Authors:** Ana Luiza Soares de Carvalho and Matheus de Alcântara Campos da Silva
- **Advisor:** Profa. Dra. Elaine Venson
- **Program:** Software Engineering — University of Brasília (UnB), Faculdade de Ciências e Tecnologias em Engenharia (FCTE)

---

## About the experiment

The experiment compares how different **input modalities**, alone and combined, and different **generative AI models** affect the generation and refinement of interface prototypes.

| Factor              | Levels                                                  |
| ------------------- | ------------------------------------------------------- |
| Input configuration | D, B, W, DB, DW, BW, DBW                                |
| Model               | GPT-6.1 Sol, Claude Opus 5.5, Qwen3.5-4B, Gemma 3 4B IT |

- **D:** use case diagram
- **B:** backlog with requirements and acceptance criteria
- **W:** wireframe

The three artifacts of each scenario convey the same set of requirements (content equivalence); what changes between them is the form of representation.

Runs are carried out in OpenCode, and prototypes are created in **Figma** through an MCP server. The prototype is a non-executable representation of the interface and its states.

## Scenarios

Scenarios come from the IUS-GUI dataset and are identified by the interface's `rico_id`. The five interfaces with six or more user stories were selected.

| `rico_id` | Theme                         | Status in this repository                     |
| --------- | ----------------------------- | --------------------------------------------- |
| 12750     | Educational videos            | Available (also used in the proof of concept) |
| 7991      | Recipes                       | To be added                                   |
| 10364     | Football (matches and news)   | To be added                                   |
| 9070      | Stocks and investments        | To be added                                   |
| 1106      | Travel (transport and hotels) | To be added                                   |

## Repository structure

```
TCC-evidences/
├── README.md                  ← Portuguese version
├── README.en.md               ← this file (English)
├── prompts/                   ← prompts for each input configuration (prompt-<config>-portuguese.txt, translated in -english.txt)
├── 12750/                     ← scenario input artifacts and evaluation sheet
│   ├── backlog_<language>_version.md
│   ├── use_case_diagram_<language>_version.png
│   ├── wireframe_<language>_version.png
│   └── evaluation_sheet_<language>_version.md
└── poc/                       ← proof-of-concept evidence (scenario 12750)
    ├── PoC 12750 - registro das execuções.xlsx   ← run log spreadsheet
    ├── poc-capturas-tela-organizadas/            ← screenshots + indice.csv
    ├── poc-sessões/                              ← OpenCode sessions (.json) and ambiente/
    └── protótipos/                               ← prototypes generated in Figma (.pdf)
```

## Proof of concept

The proof of concept was run with scenario 12750, in all seven input configurations, with GPT-6.1 Sol (`GP`) and Claude Opus 5.5 (`CL`). The run order was drawn at random (`00_sorteio_*`).

- **Screenshots:** `<order>_<model>-<config>_<phase>.png`, with phases `1-inicio-prompt-digitado` (prompt typed), `2-inicio-enviado` (sent), `3-pergunta` (question), `4-resposta-execucao` (answer/run) and `5-fim` (end). `indice.csv` maps each file to its original name.
- **Sessions:** one `.json` per run, exported from OpenCode; `ambiente/` records the OpenCode version, the system and the Figma MCP.
- **Prototypes:** one PDF per run, named `<model> - <config>`.

The PoC files keep their Portuguese names.

## Language of the artifacts

**The artifacts used in the runs are in Portuguese** (`*_portuguese_version.*` files). The same applies to the prompts in `prompts/` (`*-portuguese.txt` used; `*-english.txt` translations). The English versions (`*_english_version.*`) are translations provided only to make the material accessible to other readers and **were not used in the experiment**.

## Evaluation sheet

Each prototype is evaluated independently by both authors, at the first evaluable version (v1) and at the final version, based on the scenario's acceptance criteria.

| Level       | Classifications                                                  |
| ----------- | ---------------------------------------------------------------- |
| Criterion   | Met · Not met · Unable to verify · Not assessable in a prototype |
| Requirement | Absent · Present, incorrect or partial · Correct                 |

- **Not assessable in a prototype:** a criterion that depends on real behavior (processing, state persistence or network) and cannot be verified in a non-executable prototype. It is defined before data collection, for each criterion of each scenario, and is excluded from the adherence and coverage calculations.
- **Unable to verify:** recorded during the evaluation of a specific run, with the reason.

The evaluation sheet for scenario 12750 is in [`12750/evaluation_sheet_english_version.md`](12750/evaluation_sheet_english_version.md) (translation); the version used in the experiment is [`12750/evaluation_sheet_portuguese_version.md`](12750/evaluation_sheet_portuguese_version.md).

## Data source

The scenarios were built from the **IUS-GUI** dataset (Kolthoff et al., 2024), version identified by commit `5c8b465961b386d9d1d2f406e6ed116f8f985093`:

- GitHub: <https://github.com/IUS-GUI-Prototyping/IUS-GUI/tree/5c8b465961b386d9d1d2f406e6ed116f8f985093>
- Zenodo: <https://zenodo.org/records/10652222>

**This repository does not redistribute the IUS-GUI dataset.** It contains only material produced by the authors from it: backlogs, diagrams, wireframes and evaluation sheets. Simulated data (e.g., titles and file sizes) and interface states are adaptations by the authors.

## How to cite

> CARVALHO, A. L. S. de; SILVA, M. de A. C. da. **TCC-evidences**: artefatos de entrada do experimento. 2026. GitHub. Version v1.0. Available at: <https://github.com/Ana-Luiza-SC/TCC-evidences/releases/tag/v1.0>.

```bibtex
@misc{tcc_evidences_2026,
  author       = {Carvalho, Ana Luiza Soares de and Silva, Matheus de Alcântara Campos da},
  title        = {{TCC-evidences}: artefatos de entrada do experimento},
  year         = {2026},
  howpublished = {GitHub},
  note         = {Versão v1.0},
  url          = {https://github.com/Ana-Luiza-SC/TCC-evidences/releases/tag/v1.0}
}
```
