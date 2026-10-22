# SENAI Esports

Hub estático com os jogos feitos pelos alunos. Quem entra clica em **Entrar**, escolhe um jogo, vê as informações e clica em **Jogar**. Sem login, sem servidor e sem banco de dados.

## Estrutura

| Caminho | O que é |
|---|---|
| `index.html` | Abre o hub (`hub/index.html`) |
| `hub/index.html` | Página de entrada e lista de jogos |
| `hub/games.js` | **A lista de jogos**: nome, link, descrição, capa, controles |
| `hub/img/` | Capas dos jogos (16:9) |
| `hub/legal.html` | Termos de Uso e Política de Privacidade |
| `poeira-morta.html` | O jogo Poeira Morta (FPS de zumbis), que roda neste mesmo site |
| `fonts/`, `hub/fonts/`, `vendor/` | Fontes (licença OFL) e Three.js (MIT), servidos daqui mesmo |

## Adicionar ou mudar um jogo

1. Abra `hub/games.js`. No topo tem a explicação de cada campo.
2. Copie um bloco `{ ... }`, troque o nome, o link e os textos, e salve.
3. Se tiver capa, coloque a imagem em `hub/img/` (16:9) e preencha `img: 'img/arquivo.jpg'`. Sem capa, o hub mostra o nome do jogo.

Não use fotos de pessoas nas capas sem autorização delas.

## Testar

Abra `index.html` no navegador. Funciona sem internet (os jogos de outros sites precisam de internet).

## Publicar no Render

1. No Render: **New → Static Site** e escolha este repositório (branch `main`).
2. **Build Command**: deixe vazio. **Publish Directory**: `.`
3. Crie o site. A cada push na `main`, o Render publica de novo sozinho.

Também funciona no GitHub Pages ou no Netlify, do mesmo jeito.

## Privacidade

O hub não pede dados, não usa cookies nem ferramentas de rastreamento e não carrega arquivos de outros sites. Ao clicar em Jogar num jogo externo, o hub avisa que a pessoa está indo para outro site. Detalhes em `hub/legal.html`.

## Poeira Morta (desenvolvimento)

O `poeira-morta.html` é gerado por `node build.js` a partir de uma pasta `src/`, que não está neste repositório. Veja o `CLAUDE.md` para a organização do código do jogo.

---

Projeto estudantil independente e sem fins lucrativos. Não é um site oficial do SENAI e não tem vínculo com o SENAI ou a CNI. Cada jogo pertence aos seus criadores.
