Portfolio — Projeto de Estudos (HTML + CSS)
==========================================

Descrição
---------
Mini-portfolio estático criado como exercício. Contém páginas básicas: Home (apresentação), Sobre e Currículo, com estilos em CSS e uso opcional de ícones (Font Awesome).

Estrutura do projeto
--------------------
- index.html                  — página principal (hero/apresentação)
- about.html                  — página "Sobre"
- curriculum.html             — página de currículo
- styles/                     — arquivos CSS
  - root.css                  — variáveis e regras globais (central)
  - index.css                 — estilos da home
  - about.css                 — estilos da página Sobre
  - curriculum.css            — estilos da página Currículo
- imagens/                    — imagens do projeto
- README.txt                  — este arquivo

Como abrir / rodar localmente
-----------------------------
Opções:
- Abrir diretamente: abrir index.html no navegador (duplo clique).
- Servidor local (recomendado):
  - No terminal, dentro da pasta do projeto:
    python -m http.server 8000
  - Acesse: http://localhost:8000

Pontos importantes de estilo e arquitetura
-----------------------------------------
- Variáveis CSS centralizadas em styles/root.css:
  - Alterar fontes, cores e espaçamentos a partir do :root.
  - root.css deve ser linkado antes dos outros CSS no <head>.
- Responsividade:
  - Meta viewport necessária em cada HTML:
    <meta name="viewport" content="width=device-width, initial-scale=1">
  - Layout mobile-first com media queries (ex.: max-width: 900px).
  - Em flexbox use min-width: 0 nos itens para evitar overflow.
- Rodapé (footer):
  - Footer deve ficar dentro do <body>.
  - Para que o footer "grude" no final sem ser fixed: body { display:flex; flex-direction:column; min-height:100vh } e main { flex:1 } / footer { margin-top:auto }.
- Imagens e bordas decorativas:
  - Use um wrapper (div) ao redor de <img> para aplicar pseudo-elementos (::before/::after).
  - Evite bordas com valores fracionários (ex.: 0.1px); prefira 1–3px para HiDPI.
- Ícones:
  - Pode usar Font Awesome via CDN ou SVGs inline. Preferir fill="currentColor" para herdar cor.
- Acessibilidade:
  - Sempre usar alt em imagens, foco visível em links/CTA, contraste adequado e teste por teclado.

Melhorias e próximos passos sugeridos
-------------------------------------
- Consolidar regras repetidas em root.css ou em utilitários.
- Padronizar nomes de classes (kebab-case ou BEM) para facilitar manutenção.
- Implementar menu colapsável (hamburger) para telas muito pequenas.
- Adicionar print styles (@media print) para exportar currículo.
- Otimizar imagens e adicionar srcset/sizes.

Contribuição
------------
- Este projeto é pessoal/educacional. Faça fork, ajuste e teste localmente.
- Ao alterar variáveis em root.css, revise todas as páginas.

Autor / Créditos
----------------
Vinícius Augusto de Souza — desenvolvimento e layout.

Licença
-------
Uso pessoal e educativo. Adapte conforme necessário.

Última atualização
------------------
2025-11-07