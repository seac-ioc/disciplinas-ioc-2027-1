# Disciplinas de Pós-Graduação – IOC/Fiocruz

Site estático publicado pelo GitHub Pages com a vitrine das disciplinas dos Programas de Pós-Graduação do Instituto Oswaldo Cruz.

## Conteúdo do repositório

| Arquivo | Função |
|---|---|
| `index.html` | Página única da vitrine (dados, estilos e scripts embutidos). Gerada automaticamente pelo fluxo **HTML_Disciplinas** do Power Automate. |
| `404.html` | Página de "não encontrada" que leva de volta à vitrine. |
| `.nojekyll` | Arquivo vazio que desliga o processamento Jekyll do GitHub Pages; o site é servido exatamente como está. |
| `README.md` | Estas instruções (não aparecem no site). |

## Publicação inicial (uma única vez)

1. No GitHub, crie um repositório **público** (ex.: `disciplinas-ioc`).
2. Envie para a **raiz** do repositório todos os arquivos da pasta OneDrive `/Núcleo de Automação/HTML Disciplinas/Site_GitHub` (Add file → Upload files). Confira se o `.nojekyll` foi enviado; arquivos iniciados por ponto ficam ocultos em alguns sistemas — se faltar, crie-o no GitHub em Add file → Create new file, nome `.nojekyll`, conteúdo vazio.
3. Em **Settings → Pages**: Source = *Deploy from a branch*; Branch = `main`; Pasta = `/ (root)`; Save.
4. Após 1 a 2 minutos o site estará em `https://<usuario-ou-organizacao>.github.io/<repositorio>/`.

## Atualização das disciplinas

1. Atualize a planilha `Fonte de Dados - HTML Disciplinas.xlsx` (tabela `TabelaBaseDisc`).
2. Execute o fluxo **HTML_Disciplinas** (gatilho manual).
3. Envie ao repositório somente o novo `Site_GitHub/index.html`, substituindo o anterior (Add file → Upload files → Commit changes).
4. O GitHub Pages republica automaticamente em 1 a 2 minutos. A data de atualização aparece no rodapé da página.

## Cuidados

- Não envie ao repositório a planilha nem outros arquivos da pasta `HTML Disciplinas`: tudo o que estiver no repositório público fica acessível na internet.
- A página não depende de arquivos externos e funciona em qualquer endereço (domínio próprio ou subpasta do `github.io`).
- Domínio próprio (opcional): configure em Settings → Pages → Custom domain; o GitHub cria o arquivo `CNAME` no repositório.
