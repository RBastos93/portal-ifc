# Conecta IFC — Portal de Projetos Estudantis

Portal escolar que reúne, em um só lugar, os projetos, as notícias e os eventos
produzidos pela comunidade estudantil. Este repositório corresponde à **Versão 1
(HTML e CSS)** do projeto da disciplina de Desenvolvimento Web.

## Descrição do portal

O **Conecta IFC** é um portal com várias páginas dedicado a dar visibilidade aos
trabalhos desenvolvidos pelos estudantes. O conteúdo é organizado em quatro
grandes áreas — tecnologia, sustentabilidade, robótica e cultura — e distribuído
entre páginas de notícias, agenda de eventos, galeria de projetos e um espaço
para contato.

## Problema ou necessidade identificada

Muitos projetos interessantes desenvolvidos na escola acabam esquecidos após as
apresentações, pois não existe um espaço central para divulgá-los, registrar sua
memória e inspirar novas turmas. O portal resolve essa lacuna oferecendo um
lugar único, organizado e navegável para reunir e compartilhar essas produções.

## Público-alvo

- estudantes que desejam divulgar e conhecer projetos;
- professores que acompanham os trabalhos das turmas;
- novos alunos em busca de referências e clubes para participar;
- a comunidade escolar em geral, interessada nos eventos e notícias.

## Autoria

- **Nome completo do estudante:** _preencher com o seu nome completo_
- **Disciplina:** Desenvolvimento Web
- **Modalidade:** trabalho individual

## Páginas desenvolvidas

O portal possui cinco páginas HTML, todas conectadas por um menu de navegação
funcional presente no cabeçalho.

| Página          | Arquivo         | Descrição                                              |
| --------------- | --------------- | ------------------------------------------------------ |
| Início          | `index.html`    | Apresentação, áreas em destaque e resumo de novidades. |
| Notícias        | `noticias.html` | Notícia em destaque e lista de publicações recentes.   |
| Eventos         | `eventos.html`  | Agenda de feiras, oficinas e encontros da escola.      |
| Projetos        | `projetos.html` | Galeria de projetos organizada por categoria.          |
| Sobre e contato | `contato.html`  | Texto sobre o portal e formulário de contato.          |

### Mapa de páginas

```text
index.html (Início)
├── noticias.html (Notícias)
│   ├── Destaque da semana
│   └── Publicações recentes
├── eventos.html (Eventos)
│   ├── Próximos eventos
│   └── Como organizar um evento
├── projetos.html (Projetos)
│   ├── Tecnologia
│   ├── Sustentabilidade
│   └── Robótica
└── contato.html (Sobre e contato)
    ├── Sobre o portal
    └── Formulário de contato
```

Todas as páginas compartilham o mesmo cabeçalho, menu de navegação e rodapé,
garantindo uma navegação consistente. O menu permite ir de qualquer página para
qualquer outra.

### Wireframe / protótipo (estrutura das páginas)

O layout segue uma estrutura comum a todas as páginas, descrita abaixo em baixa
fidelidade:

```text
+------------------------------------------------------+
| HEADER: logo "Conecta IFC"        [menu de navegação] |
+------------------------------------------------------+
| MAIN                                                 |
|   Título da página + texto de introdução             |
|                                                      |
|   Seção 1: destaque / hero / conteúdo principal      |
|   Seção 2: grade de cards ou lista                   |
|   Seção 3: conteúdo em duas colunas (main + aside)   |
+------------------------------------------------------+
| FOOTER: sobre | navegação | contato                  |
+------------------------------------------------------+
```

Em telas menores, o menu, os cards e as colunas se reorganizam verticalmente
(veja a seção Responsividade).

## Identidade visual

- **Cores principais:** verde `#1f7a4d` (institucional) e dourado `#f2a900`
  (destaque), com neutros claros para o fundo e o texto.
- **Tipografia:** fontes do sistema (`Segoe UI` para o texto e `Trebuchet MS`
  para os títulos), garantindo boa legibilidade sem dependências externas.
- **Componentes:** cards, botões, listas de eventos e caixas laterais, todos com
  cantos arredondados e sombras suaves.
- As variáveis de cor, espaçamento e tipografia estão centralizadas em
  `:root`, dentro de `assets/css/global.css`.

## Tecnologias utilizadas

- **HTML5** semântico;
- **CSS3** (Flexbox, CSS Grid, variáveis, media queries);
- imagens vetoriais em **SVG** produzidas para o projeto;
- **Git** e **GitHub** para versionamento;
- **GitHub Pages** para publicação.

## Estrutura de arquivos

```text
portal-ifc/
├── index.html
├── noticias.html
├── eventos.html
├── projetos.html
├── contato.html
├── assets/
│   ├── css/
│   │   ├── reset.css
│   │   └── global.css
│   ├── js/
│   │   └── (arquivos da Versão 2)
│   └── images/
│       ├── hero-projetos.svg
│       ├── card-tecnologia.svg
│       ├── card-sustentabilidade.svg
│       ├── card-robotica.svg
│       ├── card-cultura.svg
│       └── noticia-destaque.svg
├── docs/
├── README.md
└── LICENSE
```

## Como executar o projeto

Por ser um site estático, não é necessário instalar dependências.

1. Clone o repositório:
   ```bash
   git clone https://github.com/usuario/portal-ifc.git
   ```
2. Abra a pasta do projeto no VS Code.
3. Abra o arquivo `index.html` diretamente no navegador **ou** utilize a
   extensão **Live Server** (clique com o botão direito em `index.html` e
   selecione **Open with Live Server**).

## Link da aplicação publicada

- **Versão 1:** _adicionar o link do GitHub Pages após a publicação_

Sugestão de URL: `https://usuario.github.io/portal-ifc/`

## Capturas de tela

> Adicione aqui as imagens do resultado após a publicação. Exemplo:
>
> ```markdown
> ![Página inicial do Conecta IFC](assets/images/screenshot-inicio.png)
> ```

## Funcionalidades planejadas para a Versão 2

A Versão 1 não utiliza JavaScript. As funcionalidades abaixo estão planejadas
para a **Versão 2** e serão implementadas em arquivo externo dentro de
`assets/js/`.

| Funcionalidade                | Página          | Elementos envolvidos                             | Ação do usuário                       | Comportamento esperado                                                       | Importância                                                                |
| ----------------------------- | --------------- | ------------------------------------------------ | ------------------------------------- | ---------------------------------------------------------------------------- | -------------------------------------------------------------------------- |
| Menu responsivo               | Todas           | Botão de menu (hambúrguer) e lista de navegação  | Tocar no botão do menu                | Exibir ou ocultar os links de navegação em telas pequenas                    | Melhora o uso do portal em celulares, onde o menu horizontal ocupa espaço. |
| Filtro de projetos            | `projetos.html` | Botões de categoria e cards de projeto           | Clicar em uma categoria               | Mostrar apenas os projetos da categoria escolhida e ocultar os demais        | Facilita encontrar projetos por área de interesse na galeria.              |
| Campo de pesquisa de projetos | `projetos.html` | Campo de texto e títulos dos cards               | Digitar um termo no campo de pesquisa | Exibir somente os projetos cujo título contém o termo digitado               | Agiliza a localização de um projeto específico entre vários.               |
| Validação do formulário       | `contato.html`  | Campos do formulário e área de mensagens de erro | Enviar o formulário                   | Verificar os campos obrigatórios e apresentar mensagens de orientação claras | Evita envios incompletos e orienta o usuário a corrigir os dados.          |
| Alternância de tema           | Todas           | Botão de tema e a raiz do documento              | Clicar no botão de tema claro/escuro  | Alternar entre os temas e salvar a preferência com `localStorage`            | Aumenta o conforto de leitura e demonstra o uso de armazenamento local.    |

Este planejamento poderá ser revisado durante o desenvolvimento; qualquer
alteração será atualizada nesta seção.

## Referências utilizadas

- [HTML — MDN Web Docs](https://developer.mozilla.org/pt-BR/docs/Web/HTML)
- [CSS — MDN Web Docs](https://developer.mozilla.org/pt-BR/docs/Web/CSS)
- [Guia de Flexbox — MDN Web Docs](https://developer.mozilla.org/pt-BR/docs/Web/CSS/CSS_flexible_box_layout)
- [Guia de Grid — MDN Web Docs](https://developer.mozilla.org/pt-BR/docs/Web/CSS/CSS_grid_layout)
- [GitHub Pages](https://pages.github.com/)

As imagens em SVG foram criadas especificamente para este projeto.

## Licença

Este projeto está licenciado sob os termos descritos no arquivo
[LICENSE](./LICENSE).
