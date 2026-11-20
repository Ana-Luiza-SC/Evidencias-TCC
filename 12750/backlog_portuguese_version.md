# Backlog: tela Início (cenário 12750)

Tela única de um app de conteúdos educativos com documentos e vídeos. Cada item abaixo é um requisito; os critérios de aceitação definem o comportamento esperado.

## Dados exibidos na tela (simulados)

| Tipo | Título | Tamanho |
|---|---|---|
| Documento | Simples Introdução | 0.2 MB |
| Documento | Paz, Segurança e União | 0.7 MB |
| Vídeo | O que Acontece em um Estudo Bíblico? | 18.4 MB |
| Vídeo | Por que estudar a Biblia? | 21.7 MB |

Estado inicial: nenhum item baixado; aba "Tudo" selecionada.

## R01: Buscar conteúdo

- **Categoria:** Função
- **Descrição:** O usuário pode buscar documentos e vídeos da tela pelo título.
- **Critérios de aceitação:**
  1. Dado que a tela Início exibe os 4 itens, quando o usuário aciona o ícone de busca na barra superior, então um campo de texto de busca é exibido.
  2. Dado o campo de busca aberto, quando o usuário digita um termo, então permanecem visíveis apenas os itens cujo título contém o termo, sem diferenciar maiúsculas e minúsculas (ex.: "estud" mostra só os 2 vídeos).
  3. Quando nenhum título contém o termo, então é exibida a mensagem "Nenhum resultado encontrado".
  4. Quando o usuário limpa ou fecha a busca, então os 4 itens voltam a ser exibidos.

## R02: Baixar documentos e vídeos

- **Categoria:** Função
- **Descrição:** Cada documento e vídeo pode ser baixado a partir do seu card.
- **Critérios de aceitação:**
  1. Dado o estado inicial, cada um dos 4 cards exibe um ícone de download e nenhum item está baixado.
  2. Quando o usuário aciona o ícone de download de um item, então o item passa ao estado baixado, indicado pela troca do ícone e pelo rótulo "Baixado" no card.
  3. O download é simulado: nenhum arquivo é transferido, a página não é recarregada e o estado baixado se mantém enquanto a página estiver aberta.

## R03: Exibir o tamanho do arquivo antes do download

- **Categoria:** Conteúdo
- **Descrição:** Cada item baixável mostra seu tamanho antes de ser baixado.
- **Critérios de aceitação:**
  1. Sem nenhuma interação, cada card exibe o tamanho do arquivo em MB: Simples Introdução 0.2 MB; Paz, Segurança e União 0.7 MB; O que Acontece em um Estudo Bíblico? 18.4 MB; Por que estudar a Biblia? 21.7 MB.
  2. O tamanho permanece visível antes e depois do download.

## R04: Ver os conteúdos baixados

- **Categoria:** Navegação
- **Descrição:** Abas permitem alternar entre todos os conteúdos e apenas os baixados.
- **Critérios de aceitação:**
  1. Abaixo da barra superior há as abas "Tudo" e "Baixado"; no estado inicial "Tudo" está selecionada e exibe os 4 itens.
  2. Quando o usuário seleciona "Baixado", então a aba fica destacada e são exibidos apenas os itens no estado baixado (R02).
  3. Se nenhum item foi baixado, "Baixado" exibe a mensagem "Nenhum conteúdo baixado".
  4. Quando o usuário seleciona "Tudo", então os 4 itens voltam a ser exibidos.

## R05: Atualizar o conteúdo da tela Início

- **Categoria:** Função
- **Descrição:** O usuário pode atualizar o conteúdo da tela.
- **Critérios de aceitação:**
  1. A barra superior contém um ícone de atualização.
  2. Quando o usuário aciona o ícone, então é exibido um indicador de carregamento e, em seguida, a mensagem "Conteúdo atualizado" (atualização simulada, sem backend).
  3. Após a atualização, os mesmos 4 itens e seus estados de download permanecem.

## R06: Acessar mais conteúdo

- **Categoria:** Navegação
- **Descrição:** Uma seção ao final da tela leva a recursos adicionais.
- **Critérios de aceitação:**
  1. Ao final da tela há a seção "Mais em JW.ORG" com dois links, cada um com ícone: "Outras publicações" e "Solicitar estudo bíblico".
  2. Quando o usuário aciona um dos links, então é exibida uma tela ou painel cujo título é o nome do link, com um controle para voltar à tela Início (destino simulado, sem acesso externo).

## R07: Organização da tela Início

- **Categoria:** Interface
- **Descrição:** A tela segue a estrutura da interface original.
- **Critérios de aceitação:**
  1. Barra superior com, da esquerda para a direita: ícone de menu, título "Início", ícones de atualização, busca e mais opções.
  2. Ordem vertical: barra superior; abas; linha com os 2 cards de documentos; título "Videos" e linha com os 2 cards de vídeo; seção "Mais em JW.ORG".
  3. Cards em duas colunas. Card de documento: imagem, título, ícone de download e tamanho. Card de vídeo: miniatura com ícone de reprodução, título, ícone de download e tamanho.

## Fora de escopo

- Ícone de menu e ícone de mais opções: devem aparecer (R07), mas não têm comportamento exigido.
- Reproduzir vídeos e abrir documentos: não exigido; o ícone de reprodução é apenas visual.
