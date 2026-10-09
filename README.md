# Dockn't — site

Site estático em português e inglês: `index.html` (produto) e `releases.html` (release notes). Sem build, backend ou bibliotecas externas; só as fontes vêm do Google Fonts. Idioma e tema (automático, claro, escuro) ficam salvos no navegador.

## Prévia

Na raiz do repositório de código: `python -m http.server 4173 --directory docs` e abra `http://localhost:4173`.

## Publicar

O código do Dockn't é privado. O site mora num repositório **público** à parte, com o conteúdo desta pasta na raiz (inclusive `.github/`), e o GitHub Pages publica a branch `main`, pasta `/`. Esse mesmo repositório recebe as issues dos visitantes. Nunca torne público o repositório do produto.

## Reportar bug

O formulário de `index.html` preenche os modelos de issue de `.github/ISSUE_TEMPLATE/` (`bug.yml` e `sugestao.yml`) pela URL e abre o GitHub; nada é enviado pela página. Windows e escala da tela vêm do navegador e podem ser editados. Sem conta no GitHub, o visitante salva o relato como `docknt-feedback.txt`.

`site-config.js` define `feedbackRepository` (`dono/repositorio`). Vazio, a página só oferece salvar o arquivo. Os nomes das áreas e frequências em `index.html` precisam ser idênticos às opções dos `dropdown` em `bug.yml`, senão o GitHub não os pré-seleciona.

## Conteúdo

- `shots/real-dock.png`: captura de tela real do Dockn't 0.1.23 instalado, recortada só na dock.
- `shots/studio-*.png`, `shots/dock*.png`, `shots/menu-*.png` e `shots/w-*.png`: renderizados por `cargo run --bin widget_gallery` (0.1.24-beta) com dados de demonstração; a página os identifica como renderizações.
- Release notes: o histórico fica no array `R` dentro de `releases.html`, escrito a partir dos commits. Atualize a cada versão beta e marque `current` só na mais recente.
- A V1 está em preparação: sem link de compra, preço, número de CPU garantido ou promessa de Windows 10.
