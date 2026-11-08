# Clone: web.agilisolucoesweb.com.br

Clone estático da tela pública (login) de https://web.agilisolucoesweb.com.br/sistema/,
gerado em 08/11/2026 com o REA (`inspect-web-page`, `capture-web-screenshot`,
`export-web-scripts`) a partir de um Chromium headless conectado via CDP.

## O que o REA encontrou

- Aplicação **Java Server Faces (Jakarta Faces)** renderizada no servidor, com
  **PrimeFaces 13.0.4**, **OmniFaces 4.3**, tema `primefaces-avanteweb` e layout
  `barcelona-layout`, jQuery e Bootstrap.
- É uma instância *white label*: logo, favicon e fundo vêm de
  `sistemaweb-publico.s3.amazonaws.com/WhiteLabel/web.agilisolucoesweb.com.br/`.
- A única parte pública é o login (`formLogin`), mais os formulários
  `alterarSenhaForm` (troca de senha) e `formAuth2FA` (autenticação em 2 fatores).
- Toda a lógica (login, telas internas) roda no servidor; o JavaScript é só a
  biblioteca de componentes PrimeFaces e scripts de layout.

## Como abrir

Abra `index.html` no navegador. Os scripts foram removidos e os formulários não
enviam nada (`action="#"`), então é uma réplica visual, sem backend.

## Limitações

- Só a tela de login foi clonada; as telas internas exigem login.
- Fontes Neue Haas (webflow/cdnfonts) e Font Awesome (cdnjs) continuam remotas.
- `rea-evidence/` traz a Evidence do REA, o print do original e o print do clone.
