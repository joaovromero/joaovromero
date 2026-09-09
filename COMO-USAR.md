# Como usar no GitHub

1. Extraia o ZIP no seu computador.
2. Abra o repositório público **joaovromero/joaovromero**.
3. Na raiz do repositório, substitua o **README.md** e envie a pasta **assets** completa. Não envie apenas o ZIP.
4. Confirme que `README.md` está ao lado da pasta `assets`, sem uma pasta extra envolvendo os dois.
5. Salve com **Commit changes** e abra seu perfil. As animações começam automaticamente.

O perfil exige um repositório público com o mesmo nome de usuário e um README.md na raiz. [Documentação do GitHub](https://docs.github.com/en/account-and-profile/how-tos/profile-customization/managing-your-profile-readme).

## Arquivos

| Arquivo | Função |
| --- | --- |
| README.md | Estrutura do perfil e links clicáveis |
| assets/header.svg | Apresentação e ilustração vetorial animada |
| assets/profile.svg | Cartões de perfil e formação |
| assets/tech-carousel.svg | Carrossel contínuo com ícones incorporados |
| assets/studying.svg | Temas de estudo com animação de digitação |
| assets/dashboard-heading.svg | Título da seção de estatísticas |
| assets/footer.svg | Encerramento com brilho suave |
| assets/*-mobile.svg | Composições para telas de até 600 pixels |
| assets/linkedin.svg, repositories.svg, followers.svg, stars.svg | Botões de navegação |

## Personalizar

- **Nome, idade e formação:** edite o texto no README (atributos `alt`) e os elementos `<text>` dos SVGs correspondentes, incluindo as versões `-mobile`.
- **Paleta:** fundo `#101827`, cartão `#151F32`, verde-água `#00E5C3`, azul `#538BFF`, texto `#F2F6FC`.
- **Velocidade do carrossel:** altere `32s` em `.track` nas duas versões do carrossel. Um número maior deixa o movimento mais lento.
- **Tecnologias:** os sete cartões têm intervalos de 150 pixels. As duas cópias são idênticas; o deslocamento de um ciclo é 1050 pixels. Ao adicionar ou remover cartões, atualize as duas cópias e a distância do ciclo.
- **Link do LinkedIn:** já usa o endereço que você enviou. `%C3%A3` representa o caractere `ã` no endereço.
- **Estudos:** altere os textos nas duas versões de `studying.svg` e na lista do README. Cada tema aparece por 5 segundos, dentro de um ciclo de 30 segundos.

## Animações e compatibilidade

O GitHub remove scripts e estilos diretamente aplicados ao HTML do README. As animações deste pacote ficam dentro de imagens SVG locais: digitação, cursor, ícones flutuantes, brilho e carrossel. [Pipeline de renderização do GitHub](https://github.com/github/markup).

Os SVGs não carregam imagens, fontes, scripts ou folhas de estilo externas. Os ícones estão incorporados como vetores; isso evita a restrição a recursos externos quando um SVG é exibido como imagem. [SVG como imagem — MDN](https://developer.mozilla.org/en-US/docs/Web/SVG/Guides/SVG_as_an_image).

As imagens usam `prefers-reduced-motion`: quando o visitante ativa a redução de movimento, os efeitos param e o conteúdo permanece visível. Todos os temas de estudo também estão disponíveis em texto na seção expansível.

Os botões são links HTML envolvendo imagens. Não há efeitos de hover que dependam de eventos dentro do SVG, pois imagens inseridas no README não recebem essas interações.

## Estatísticas

Os cartões usam o **GitHub Stats Extended**, sucessor indicado pelo projeto que aparecia no código original. Os contadores usam Shields.io. Eles consultam dados públicos e podem demorar para atualizar ou ficar indisponíveis por limites dos serviços. O cabeçalho, perfil, carrossel e estudos funcionam sem esses serviços. [Documentação e migração](https://github.com/stats-organization/github-stats-extended).

A distribuição de linguagens reflete o código dos repositórios analisados; não mede domínio profissional. Nenhum número foi inventado ou fixado no pacote.

## Créditos

Ícones de tecnologias e LinkedIn: [Devicon](https://github.com/devicons/devicon), licença MIT (incluída em CREDITOS.txt). Ícone SVG: [W3C, criado por Harvey Rayner](https://www.w3.org/Icons/SVG/), Creative Commons Attribution-NonCommercial-ShareAlike 2.5. Os nomes e marcas pertencem aos respectivos titulares. Ilustração e cartões vetoriais criados para este perfil, inspirados na referência enviada.
