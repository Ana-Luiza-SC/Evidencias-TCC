# TCC-evidences

[![Português](https://img.shields.io/badge/idioma-Português-green?style=for-the-badge)](README.md)
[![English](https://img.shields.io/badge/language-English-blue?style=for-the-badge)](README.en.md)

Artefatos de entrada e instrumentos de avaliação do experimento do Trabalho de Conclusão de Curso **"Prototipação de interfaces com IA generativa: efeitos das modalidades de entrada sobre produtividade, aderência aos requisitos, esforço de refinamento e custos"**.

- **Autores:** Ana Luiza Soares de Carvalho e Matheus de Alcântara Campos da Silva
- **Orientadora:** Profa. Dra. Elaine Venson
- **Curso:** Engenharia de Software — Universidade de Brasília (UnB), Faculdade de Ciências e Tecnologias em Engenharia (FCTE)

---

## Sobre o experimento

O experimento compara como diferentes **modalidades de entrada**, isoladas e combinadas, e diferentes **modelos de IA generativa** afetam a geração e o refinamento de protótipos de interface.

| Fator                   | Níveis                                                  |
| ----------------------- | ------------------------------------------------------- |
| Configuração de entrada | D, B, W, DB, DW, BW, DBW                                |
| Modelo                  | GPT-6.1 Sol, Claude Opus 5.5, Qwen3.5-4B, Gemma 3 4B IT |

- **D:** diagrama de caso de uso
- **B:** backlog com requisitos e critérios de aceitação
- **W:** wireframe

Os três artefatos de cada cenário comunicam o mesmo conjunto de requisitos (equivalência de conteúdo); o que muda entre eles é a forma de representação.

As execuções são conduzidas no OpenCode, e os protótipos são criados no **Figma** por meio de um servidor MCP. O protótipo é uma representação não executável da interface e de seus estados.

## Cenários

Os cenários vêm da base IUS-GUI e são identificados pelo `rico_id` da interface. Foram selecionadas as cinco interfaces com seis ou mais histórias de usuário.

| `rico_id` | Tema                          | Situação neste repositório                     |
| --------- | ----------------------------- | ---------------------------------------------- |
| 12750     | Vídeos educativos             | Disponível (também usado na prova de conceito) |
| 7991      | Receitas                      | A incluir                                      |
| 10364     | Futebol (jogos e notícias)    | A incluir                                      |
| 9070      | Ações e investimentos         | A incluir                                      |
| 1106      | Viagens (transporte e hotéis) | A incluir                                      |

## Estrutura do repositório

```
TCC-evidences/
├── README.md                  ← este arquivo (português)
├── README.en.md               ← versão em inglês
├── prompts/                   ← prompts de cada configuração de entrada (prompt-<config>-portuguese.txt, com tradução em -english.txt)
└── 12750/
    ├── backlog_portuguese_version.md
    ├── backlog_english_version.md
    ├── use_case_diagram_portuguese_version.png
    ├── use_case_diagram_english_version.png
    ├── wireframe_portuguese_version.png
    ├── wireframe_english_version.png
    ├── evaluation_sheet_portuguese_version.md   ← ficha de avaliação (usada)
    └── evaluation_sheet_english_version.md     ← tradução da ficha
```

## Idioma dos artefatos

**Os artefatos utilizados nas execuções estão em português** (arquivos `*_portuguese_version.*`). O mesmo vale para os prompts em `prompts/` (`*-portuguese.txt` usados; `*-english.txt` traduções). As versões em inglês (`*_english_version.*`) são traduções disponibilizadas apenas para facilitar o acesso de outros leitores e **não foram utilizadas no experimento**.

## Ficha de avaliação

Cada protótipo é avaliado de forma independente pelos dois autores, na primeira versão avaliável (v1) e na versão final, com base nos critérios de aceitação do cenário.

| Nível     | Classificações                                                           |
| --------- | ------------------------------------------------------------------------ |
| Critério  | Atende · Não atende · Impossível verificar · Não avaliável por protótipo |
| Requisito | Ausente · Presente, incorreto ou parcial · Correto                       |

- **Não avaliável por protótipo:** critério que depende de comportamento real (processamento, persistência de estado ou rede) e não pode ser verificado em um protótipo não executável. É definido antes da coleta, para cada critério de cada cenário, e não entra no cálculo da aderência nem da cobertura.
- **Impossível verificar:** registrado durante a avaliação de uma execução específica, com o motivo.

A ficha do cenário 12750 está em [`12750/evaluation_sheet_portuguese_version.md`](12750/evaluation_sheet_portuguese_version.md), com tradução em [`12750/evaluation_sheet_english_version.md`](12750/evaluation_sheet_english_version.md).

## Origem dos dados

Os cenários foram elaborados a partir da base **IUS-GUI** (Kolthoff et al., 2024), versão identificada pelo _commit_ `5c8b465961b386d9d1d2f406e6ed116f8f985093`:

- GitHub: <https://github.com/IUS-GUI-Prototyping/IUS-GUI/tree/5c8b465961b386d9d1d2f406e6ed116f8f985093>
- Zenodo: <https://zenodo.org/records/10652222>

**Este repositório não redistribui a base IUS-GUI.** Ele contém apenas o material produzido pelos autores a partir dela: backlogs, diagramas, wireframes e fichas de avaliação. Dados simulados (por exemplo, títulos e tamanhos de arquivos) e estados da interface são adaptações dos autores.

## Como citar

> CARVALHO, A. L. S. de; SILVA, M. de A. C. da. **TCC-evidences**: artefatos de entrada do experimento. 2026. GitHub. Versão v1.0. Disponível em: <https://github.com/Ana-Luiza-SC/TCC-evidences/releases/tag/v1.0>.

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
