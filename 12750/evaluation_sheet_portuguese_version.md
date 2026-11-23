# Ficha de avaliação: tela Início (cenário 12750)

[![Português](https://img.shields.io/badge/idioma-Português-green?style=for-the-badge)](evaluation_sheet_portuguese_version.md)
[![English](https://img.shields.io/badge/language-English-blue?style=for-the-badge)](evaluation_sheet_english_version.md)

Ficha usada para avaliar cada protótipo gerado para o cenário 12750. O resultado esperado de cada linha é o critério de aceitação correspondente do backlog ([`backlog_portuguese_version.md`](backlog_portuguese_version.md)). Cada avaliador preenche sua própria cópia, de forma independente, para a v1 e para a versão final.

## 1. Identificação

| Campo                                        | Valor                                                        |
| -------------------------------------------- | ------------------------------------------------------------ |
| Cenário                                      | 12750                                                        |
| Configuração de entrada                      | ☐ D ☐ B ☐ W ☐ DB ☐ DW ☐ BW ☐ DBW                             |
| Modelo                                       | ☐ GPT-6.1 Sol ☐ Claude Opus 5.5 ☐ Qwen3.5-4B ☐ Gemma 3 4B IT |
| Repetição                                    |                                                              |
| Operador                                     |                                                              |
| Avaliador                                    |                                                              |
| Versão avaliada (escrever release do github) |                                                              |
| Data da avaliação                            |                                                              |
| Link do arquivo no Figma                     |                                                              |

## 2. Legenda da situação

| Código  | Situação                    | Quando usar                                                                          |
| ------- | --------------------------- | ------------------------------------------------------------------------------------ |
| **A**   | Atende                      | O protótipo representa o resultado esperado.                                         |
| **NA**  | Não atende                  | O resultado esperado não está representado, ou está representado de forma incorreta. |
| **IV**  | Impossível verificar        | Algo nesta execução impediu a verificação. Registrar o motivo em "Observado".        |
| **NAP** | Não avaliável por protótipo | Definido antes da coleta. Não é preenchido pelo avaliador e não entra no cálculo.    |

## 3. Avaliação por critério

### R01: Buscar conteúdo (Função)

| ID     | Resultado esperado                                                                                                                          | Procedimento de verificação                                                                        | Observado | Evidência | Situação           |
| ------ | ------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- | --------- | --------- | ------------------ |
| R01.1  | Com a tela Início exibindo os 4 itens, ao acionar o ícone de busca na barra superior, um campo de texto de busca é exibido.                 | Localizar o ícone de busca na barra superior e verificar a representação do campo de busca aberto. |           |           |                    |
| R01.2a | Ao digitar um termo no campo de busca, permanecem visíveis apenas os itens cujo título contém o termo (ex.: "estud" mostra só os 2 vídeos). | Verificar a representação do estado com um termo digitado e a lista filtrada.                      |           |           |                    |
| R01.2b | A filtragem não diferencia maiúsculas e minúsculas.                                                                                         | —                                                                                                  | —         | —         | **NAP (proposto)** |
| R01.3  | Quando nenhum título contém o termo, é exibida a mensagem "Nenhum resultado encontrado".                                                    | Verificar a representação do estado sem resultado, com o texto exato da mensagem.                  |           |           |                    |
| R01.4  | Ao limpar ou fechar a busca, os 4 itens voltam a ser exibidos.                                                                              | Verificar a representação do retorno ao estado com os 4 itens.                                     |           |           |                    |

### R02: Baixar documentos e vídeos (Função)

| ID     | Resultado esperado                                                                                                                             | Procedimento de verificação                                                                   | Observado | Evidência | Situação           |
| ------ | ---------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------- | --------- | ------------------ |
| R02.1  | No estado inicial, cada um dos 4 cards exibe um ícone de download e nenhum item está baixado.                                                  | Verificar, no estado inicial, o ícone de download nos 4 cards e a ausência de itens baixados. |           |           |                    |
| R02.2a | Ao acionar o ícone de download de um item, o ícone é trocado.                                                                                  | Verificar a representação do card depois do download, com o ícone alterado.                   |           |           |                    |
| R02.2b | Ao acionar o ícone de download de um item, o card exibe o rótulo "Baixado".                                                                    | Verificar a representação do card depois do download, com o rótulo exato.                     |           |           |                    |
| R02.3  | O download é simulado: nenhum arquivo é transferido, a página não é recarregada e o estado baixado se mantém enquanto a página estiver aberta. | —                                                                                             | —         | —         | **NAP (proposto)** |

### R03: Exibir o tamanho do arquivo antes do download (Conteúdo)

| ID    | Resultado esperado                                                                                                                                                                                 | Procedimento de verificação                                            | Observado | Evidência | Situação |
| ----- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------- | --------- | --------- | -------- |
| R03.1 | Sem nenhuma interação, cada card exibe o tamanho em MB: Simples Introdução 0.2 MB; Paz, Segurança e União 0.7 MB; O que Acontece em um Estudo Bíblico? 18.4 MB; Por que estudar a Biblia? 21.7 MB. | Conferir, no estado inicial, o tamanho exibido em cada um dos 4 cards. |           |           |          |
| R03.2 | O tamanho permanece visível antes e depois do download.                                                                                                                                            | Comparar o card antes e depois do download.                            |           |           |          |

### R04: Ver os conteúdos baixados (Navegação)

| ID    | Resultado esperado                                                                                                     | Procedimento de verificação                                                           | Observado | Evidência | Situação |
| ----- | ---------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | --------- | --------- | -------- |
| R04.1 | Abaixo da barra superior há as abas "Tudo" e "Baixado"; no estado inicial, "Tudo" está selecionada e exibe os 4 itens. | Verificar as abas, seus rótulos e a seleção no estado inicial.                        |           |           |          |
| R04.2 | Ao selecionar "Baixado", a aba fica destacada e são exibidos apenas os itens baixados.                                 | Verificar a representação da aba "Baixado" selecionada, com apenas os itens baixados. |           |           |          |
| R04.3 | Se nenhum item foi baixado, "Baixado" exibe a mensagem "Nenhum conteúdo baixado".                                      | Verificar a representação da aba vazia, com o texto exato da mensagem.                |           |           |          |
| R04.4 | Ao selecionar "Tudo", os 4 itens voltam a ser exibidos.                                                                | Verificar a representação do retorno à aba "Tudo" com os 4 itens.                     |           |           |          |

### R05: Atualizar o conteúdo da tela Início (Função)

| ID    | Resultado esperado                                                                                          | Procedimento de verificação                                                              | Observado | Evidência | Situação |
| ----- | ----------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | --------- | --------- | -------- |
| R05.1 | A barra superior contém um ícone de atualização.                                                            | Localizar o ícone de atualização na barra superior.                                      |           |           |          |
| R05.2 | Ao acionar o ícone, é exibido um indicador de carregamento e, em seguida, a mensagem "Conteúdo atualizado". | Verificar a representação do indicador de carregamento e do estado com a mensagem exata. |           |           |          |
| R05.3 | Após a atualização, os mesmos 4 itens e seus estados de download permanecem.                                | Verificar a representação do estado após a atualização.                                  |           |           |          |

### R06: Acessar mais conteúdo (Navegação)

| ID    | Resultado esperado                                                                                                                 | Procedimento de verificação                                                                  | Observado | Evidência | Situação |
| ----- | ---------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- | --------- | --------- | -------- |
| R06.1 | Ao final da tela há a seção "Mais em JW.ORG" com dois links, cada um com ícone: "Outras publicações" e "Solicitar estudo bíblico". | Verificar a seção, os dois links, seus textos e ícones.                                      |           |           |          |
| R06.2 | Ao acionar um dos links, é exibida uma tela ou painel cujo título é o nome do link, com um controle para voltar à tela Início.     | Verificar a representação da tela ou painel de destino de cada link e o controle de retorno. |           |           |          |

### R07: Organização da tela Início (Interface)

| ID     | Resultado esperado                                                                                                                                 | Procedimento de verificação                                                  | Observado | Evidência | Situação |
| ------ | -------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | --------- | --------- | -------- |
| R07.1  | Barra superior com, da esquerda para a direita: ícone de menu, título "Início", ícones de atualização, busca e mais opções.                        | Conferir a presença e a ordem dos elementos da barra superior.               |           |           |          |
| R07.2  | Ordem vertical: barra superior; abas; linha com os 2 cards de documentos; título "Videos" e linha com os 2 cards de vídeo; seção "Mais em JW.ORG". | Conferir a ordem vertical dos blocos no estado inicial.                      |           |           |          |
| R07.3a | Cards em duas colunas. Card de documento: imagem, título, ícone de download e tamanho.                                                             | Conferir a disposição em duas colunas e os elementos dos cards de documento. |           |           |          |
| R07.3b | Card de vídeo: miniatura com ícone de reprodução, título, ícone de download e tamanho.                                                             | Conferir os elementos dos cards de vídeo.                                    |           |           |          |

**Fora de escopo (não avaliar):** comportamento dos ícones de menu e de mais opções (devem apenas aparecer, conforme R07.1); reproduzir vídeos e abrir documentos.

## 4. Classificação por requisito

Considerar apenas os critérios avaliáveis (excluir NAP). Um requisito é **correto** quando todos os seus critérios avaliáveis são A; **ausente** quando não foi implementado de forma nenhuma; e **presente, incorreto ou parcial** nos demais casos.

| Requisito | Critérios avaliáveis | Critérios A | Classificação (Ausente / Parcial / Correto) |
| --------- | -------------------- | ----------- | ------------------------------------------- |
| R01       | 4                    |             |                                             |
| R02       | 3                    |             |                                             |
| R03       | 2                    |             |                                             |
| R04       | 4                    |             |                                             |
| R05       | 3                    |             |                                             |
| R06       | 2                    |             |                                             |
| R07       | 4                    |             |                                             |

## 5. Indicadores da versão avaliada

| Indicador                                      | Valor |
| ---------------------------------------------- | ----- |
| R (requisitos considerados)                    | 7     |
| R_corretos                                     |       |
| R_ausentes                                     |       |
| Aderência: A = 100 × R_corretos / R            |       |
| Cobertura: C_impl = 100 × (R − R_ausentes) / R |       |

## 6. Não conformidades

| ID do critério | Descrição | Tipo _(rubrica a definir)_ | Severidade _(rubrica a definir)_ |
| -------------- | --------- | -------------------------- | -------------------------------- |
|                |           |                            |                                  |

## 7. Observações do avaliador
