# Objetivo
Contribuir para a melhoria da usabilidade e experiência (UX Design) e da interface visual (UI Design) dos sites de cursos criados através do SIGAA (e seus derivados, em outras instituições).

# Contexto de documentação
Essa documentação foi elaborada com base na experiência de contribuição para a manutenção do site institucional do [PPGCC](http://www.posgraduacao.ufrn.br/ppgcc) da UFRN, utilizando o SIGAA.

Caso as [instituições públicas brasileiras](http://www.portalcooperacao.info.ufrn.br/) que contrataram o uso desse sistema, tenham acesso a essa opção de ++Páginas Web++, provavelmente este repositório lhes será útil.

# Problemática / conclusão
No início das atividades de manutenção do front-end do site sistêmico (no SIGAA) do PPGCC, realizou-se uma consulta aos sites das demais unidades da instituição e percebeu-se que:
* quantidade considerável dos cursos não utilizam qualquer [página personalizada](Documentação nos Sistemas da UFRN).
* os cursos que utilizam a página personalizada, utilizam apenas [recursos comuns](#modo-visual).
* não foi encontrado curso que utiliza recursos de [personalização de página](#modo-codigo), com HTML estilizado.

# O gerador das Páginas de Curso
Atualmente, os sistemas SIG (na opção ++Páginas Web++) utilizam um editor de código web online do tipo [WYSIWYG](https://pt.wikipedia.org/wiki/WYSIWYG) chamado [TinyMCE](https://github.com/tinymce/tinymce), [open-source](https://github.com/tinymce/tinymce/blob/master/LICENSE.TXT) e ainda em desenvolvimento, sendo a versão utilizada nos sistemas SIG a [3.4.9](https://github.com/tinymce/tinymce/releases/tag/3.4.9), de 2012.

Considerando a linguagem visual padrão, aparentemente, esse editor é o mesmo utilizado em todos os sites de cursos, quando implementado pela instituição.

# Funcionamento do TinyMCE
## Documentação nos Sistemas da UFRN
Tomando por referência a [documentação](https://docs.info.ufrn.br/doku.php?id=suporte) do sistema SIG utilizado na UFRN, aparentemente, a plataforma do TinyMCE está disponível para todos os cursos que utilizam o sistema SIG, exceto os de ensino infantil, fundamental, médio e de extensão universitária.

Abaixo foram tabelados links para as documentações dos diferentes níveis de curso com a Página Web de Cursos disponível.

| Tipo de Curso | Seção "Apresentação" | Seção "Notícias do Portal Público" | Seção "Outras Opções / Seções Extras" |
| ------------- | -------------------- | ---------------------------------- | ------------------------------------- |
| Técnico Integrado | [ambos](https://docs.info.ufrn.br/doku.php?id=suporte:manuais:sigaa:integrado:curso:pagina_web:gerenciar_portais_publicos#alterar_detalhes) | [ambos](https://docs.info.ufrn.br/doku.php?id=suporte:manuais:sigaa:integrado:curso:pagina_web:gerenciar_portais_publicos#gerenciar_noticias) | [ambos](https://docs.info.ufrn.br/doku.php?id=suporte:manuais:sigaa:integrado:curso:pagina_web:gerenciar_portais_publicos#gerenciar_secoes_extras) |
| Técnico Subsequente | [movoV](https://docs.info.ufrn.br/doku.php?id=suporte:manuais:sigaa:tecnico:curso:pagina_web:gerenciar_portais_publicos#alterar_detalhes) | [ambos](https://docs.info.ufrn.br/doku.php?id=suporte:manuais:sigaa:tecnico:curso:pagina_web:gerenciar_portais_publicos#gerenciar_noticias) | [ambos](https://docs.info.ufrn.br/doku.php?id=suporte:manuais:sigaa:tecnico:curso:pagina_web:gerenciar_portais_publicos#gerenciar_secoes_extras) |
| Formação Complementar <td colspan=3> [Documentação com problemas](https://docs.info.ufrn.br/doku.php?id=suporte:manuais:sigaa:formacao_complementar:curso:pagina_web:gerenciar_portais_publicos) |
| Graduação | [ambos](https://docs.info.ufrn.br/doku.php?id=suporte:manuais:sigaa:portal_coordenador_graduacao:pagina_web:apresentacao_do_curso) | ambos: [cadastro](https://docs.info.ufrn.br/doku.php?id=suporte:manuais:sigaa:portal_coordenador_graduacao:pagina_web:noticias_do_portal_publico_do_curso:cadastrar) e [edição](https://docs.info.ufrn.br/doku.php?id=suporte:manuais:sigaa:portal_coordenador_graduacao:pagina_web:noticias_do_portal_publico_do_curso:alterar_remover) | ambos: [cadastro](https://docs.info.ufrn.br/doku.php?id=suporte:manuais:sigaa:portal_coordenador_graduacao:pagina_web:outras_opcoes_do_curso:cadastrar) e [edição](https://docs.info.ufrn.br/doku.php?id=suporte:manuais:sigaa:portal_coordenador_graduacao:pagina_web:outras_opcoes_do_curso:alterar_remover) |
| Lato-Sensu <td colspan=3> [Documentação não elaborada](https://docs.info.ufrn.br/doku.php?id=suporte:manuais:sigaa:portal_coordenador_lato_sensu:lista#aba_pagina_web) |
| Strictu Sensu | [ambos](https://docs.info.ufrn.br/doku.php?id=suporte:manuais:sigaa:portal_coordenador_stricto_sensu:pagina_web:apresentacao_do_programa) | ambos: [cadastro](https://docs.info.ufrn.br/doku.php?id=suporte:manuais:sigaa:portal_coordenador_stricto_sensu:pagina_web:noticias_do_portal_publico_do_programa:cadastrar) e [edição](https://docs.info.ufrn.br/doku.php?id=suporte:manuais:sigaa:portal_coordenador_stricto_sensu:pagina_web:noticias_do_portal_publico_do_programa:alterar_remover) | ambos: [cadastro](https://docs.info.ufrn.br/doku.php?id=suporte:manuais:sigaa:portal_coordenador_stricto_sensu:pagina_web:outras_opcoes_do_programa:cadastrar) e [edição](https://docs.info.ufrn.br/doku.php?id=suporte:manuais:sigaa:portal_coordenador_stricto_sensu:pagina_web:outras_opcoes_do_programa:alterar_remover) |

## Modos de edição
No contexto de utilização nos sistemas SIG, a interface de usuário do TinyMCE (versão 3.4.9) disponibiliza dois modos de edição (assim como alguns editores de código WYSIWYG), aqui denominados: o modo visual (_"modoV"_) e o modo código (_"modoC"_).

### Modo visual
Nesse modo, o conteúdo é inserido e estilizado diretamente na caixa de texto disponibilizada, na tela de [disponibilizada](https://docs.info.ufrn.br/doku.php?id=suporte:manuais:sigaa:portal_coordenador_stricto_sensu:pagina_web:outras_opcoes_do_programa:cadastrar).
Para utilizá-lo, não são necessários conhecimentos de programação web, bastando apenas noções básicas de processadores de texto (como o [LibreOffice Writer](https://en.wikipedia.org/wiki/LibreOffice_Writer), [Google Docs](https://en.wikipedia.org/wiki/Google_Docs), [Microsoft Word](https://en.wikipedia.org/wiki/Microsoft_Word)).

### Modo código
Nesse modo, o conteúdo é inserido em uma janela externa, a qual somente lerá código HTML. Para utilizá-lo são necessários conhecimentos de programação web ([HTML](https://en.wikipedia.org/wiki/HTML), [CSS](https://en.wikipedia.org/wiki/Cascading_Style_Sheets) e, dependendo da necessidade, [JS](https://en.wikipedia.org/wiki/JavaScript)).
O conteúdo inserido nesta janela será lido e interpretado pelo TinyMCE como código HTML, CSS e JS, tendo sua aparência demonstrada quando este for submetido (botão `Update`).
A tecnologia usada neste código deve ser compatível com os padrões web existentes na data [dessa versão do TinyMCE](#o-gerador-das-paginas-de-curso). Padrões referentes ao HTML5 (adotado pela W3C como recomendação em [2014](https://www.w3.org/TR/2014/REC-html5-20141028/)) e posteriores, por exemplo, não são compatíveis.

O conteúdo do código aqui inserido pode ser desenvolvido (em editor de código web adequado) considerando-se que está, em uma estrutura convencional de página HTML, dentro de um elemento `<div>`.
Somente o conteúdo dessa tag `<div>` da página que foi desenvolvida precisa ser inserido na janela do _Modo Código_ do TinyMCE.
Caso a `<div>` (que engloba o conteúdo HTML colado) também seja inserida, esta será renderizada pelo TinyMCE (na página final, ficará dentro da `<div id="conteudo">`).

## Parâmetros de publicação
No ambiente do [modo visual](#modo-visual) também é possível escolher, no formulário disponível, se a "Seção Extra" será apenas um link externo, marcando-se o botão de opção "Acesso Link Externo" (sim / não).
Além disso, pode-se escolher tanto o título da seção, quanto se ela será acessível por link inserido diretamente no menu "Outras Opções" do site publicado do curso _(marcando "Publicar: Sim")_ e por link _(o usuário clica em um link para esta "Seção Extra")_, ou se será acessível somente por link _(marcando "Publicar: Não)_.

## Inserção de Imagens
O uso de imagens no TinyMCE, na versão 3.4.9 instalada no SIGAA da UFRN, não comporta inserção direta no sistema (o usuário não tem a opção de carregar a imagem diretamente no sistema), independente do modo de edição usado da página ([visual](#modo-visual) ou [código](#codigo)). Há duas maneiras de usá-las.

### Imagens via URL
Nessa maneira, as imagens devem já estar upadas em outro local, sendo inseridas através de sua URL. É a maneira padrão de se trabalhar.

### Imagens via código
Nessa maneira, que só funciona utilizando-se o navegador Mozilla Firefox (dos testados), as imagens são inseridas em fluxo de clicar (no 'explorador de arquivos') e arrastar (para dentro da área de edição do modo visual).
Para utilização na página, pode-se tanto usar as opções de controle no _modo visual_ quanto no _modo código_, sendo que nesta última opção, será revelado que a imagem assim inserida, na verdade, está em formato de código (seu conteúdo será um elemento `<img>` com o atributo `src` com valor começando em `data:image/jpeg;base64,`), o que pode deixar o código da página toda bem grande.

## Estilização de página
Dos [modos comuns de se atribuir estilo a uma página web individual](https://stackoverflow.com/a/55436534), aparentemente, somente a solução de _CSS inline_ está disponível para uso no TinyMCE 3.4.9, utilizado atualmente nos sistemas da UFRN, por parte das secretarias de cursos. Testes foram feitos e somente esta maneira de uso de estilização teve êxito, apesar de ser a menos favorável a um código mais simples de se dar manutenção.

# Descrição da solução
Para uma experiência efetiva de um editor de código WYSIWYG ou algum CMS institucional, proporcionando não só o cumprimento da função comunicativa (utilitária), a função de proporcionar uma boa experiência de uso por vezes melhora a primeira.

Nesse sentido, este repositório organiza a experiência adquirida sobre a manutenção do front-end (interface web no lado cliente) de páginas web referentes a uma unidade administrativa (o PPGCC) da UFRN, em um contexto de limitação tecnológica.

*Suscintamente, trata-se de*: front-end de páginas web em [HTML 4.01 transitional](https://www.w3.org/TR/html4/), com _CSS inline_ e _JavaScript_.

As páginas aqui registradas documentam o trabalho realizado no PPGCC, mas também podem servir de modelo (_template_) para uso por outras unidades que utilizam páginas web nos sistemas SIG.

A criação desses templates (e o processo de descoberta da limitação tecnológica) demandou tempo considerável, o qual pode ser economizado por outras unidades universitárias, ao utilizá-los. 

# Aplicação / Uso
Para utilização desses templates, pode ser necessário que a unidade universitária tenha pessoal com familiaridade com programação web.
Especificamente, as seguintes habilidades são necessárias: HTML intermediário, CSS básico e JavaScript básico.

# Observação
A documentação dessa experiência não expressa a opinião da SINFO, unidade administrativa responsável por manter e atualizar os sistemas da UFRN.
