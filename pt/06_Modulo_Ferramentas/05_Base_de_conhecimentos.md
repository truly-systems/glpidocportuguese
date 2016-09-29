Administrando a base de conhecimentos
==============================

A base de conhecimento atende a dois objetivos principais :

-   O primeiro está centralizado nos conhecimentos internos das diversas técnicas ;
-   O segundo fornece aos usuários informações (FAQ público) que lhes permitam resolver problemas simples.

Somente elementos de FAQ públicos são visíveis para os usuários da interface simplificada. Os elementos que não são definidos como parte do FAQ público são visíveis somente dentro do console central para técnicos, por exemplo.

A navegação dentro da base de conhecimento pode ser feita de 2 maneiras diferentes: :

-   Realizando uma pesquisa global na aba *Pesquisa* ;
-   Navegando dentro das categorias na aba *Browse*.

A aba *Gerenciar*, visível com base no perfil do usuário, permite gerenciar artigos escritos e artigos inéditos.

É necessário selecionar cada item na base de conhecimento ou FAQ um ou mais alvos. O ou os alvos correspondem as entidades, perfis, grupos ou usuários que podem consultar o artigo. Enquanto o alvo não for selecionado para um artigo, ele será visível apenas pelo seu editor.
O artigo é considerado "inétidot" e aparece na tabela "documentos não publicados" a partir da home page da base de conhecimento.

Por padrão, os itens não podem ser traduzidos em várias línguas. Esta funcionalidade pode ser ativada (veja [a configuração geral](index.php?pt/08_Modulo_Configuracao/06_Générale/02_Configuration_Générale.md "Essa aba permite personalizar a aparência geral da aplicação.")).

É possível associar um ou mais documentos aos artigos da base de conhecimento.

***Observação :** Um artigo pode se tornar visível durante um determinado período, definindo a data de início e data final*

>ATENÇÃO :
>Os itens que não serão visualizados poder ser definidos no estilo pre-format(`<pre>` HTML). 
>As tags como `<VirtualHost>` são inseridas e visualizadas.
>Para tags ficarem visíveis no texto vocÊ pode mudar para o modo HTML, onde todos os elementos são visíveis.
>Seu navegador também pode alterar dinamicamente o conteúdo (alteração de quebra, adicionar tags) em uma edição.

É possível criar categorias e sub-categorias com o intuito de organizar a navegação (veja [Configurando os títulos ](index.php?pt/08_Modulo_Configuracao/02_Titulos/01_Titulos.md "Os títulos são configurados a partir do menu Configuração > Títulos")).
O usuário pode utilizar vários modos de busca e navegar através da base de conhecimentos através de 3 abas diferentes :

-   **Busca :** é a aba padrão. Apresenta os artigos mais recentes, os mais populares e as últimas alterações. Também permite que seja feito pesquisas na base dos conhecimentos.
-   **Browser :** permite a navegação.
-   **Gerenciar :** essa aba é acessível aos administradores da base de conhecimentos. Dependendo dos direitos do usuário, ele pode acessar rapidamente seus ou qualquer artigo não publicado e todos os seus artigos.

***Observação :** O mecanismo de pesquisa da base de conhecimento permite utilizar um certo número de operações para pesquisas complexas serem mais efetivas : `+ - ~ < > * ” ” ()`.*

*- `+` Le mot doit être présent ;
- `-` Le mot ne doit pas être présent ;
- `*` Opérateur de troncature à positionner en suffixe ;
- `" "` Une phrase entre guillemets double (") est recherchée littéralement, telle qu'elle a été saisie ;
- `< >` permet de définir une préférence sur l'ordre des éléments recherchés ;
- `()` agrégateur utile pour l'utilisation de < et >.*

    Exemplos :

    - falha impressora
       -> Pesquisar as linhas que contenham pelo menos uma dessas palavras.
    - +falha +impressora
       -> Pesquisar as linhas que contenham essas duas palavras.
    - +e-mail thunderbird
       -> Pesquisas as linhas que contenha a palavra *e-mail*,
          mas classificar linhas que contenham *thunderbird*.
    - +courriel -outlook
       -> Pesquisas as linhas que contenham *e-mail* e não *outlook*.
    - * +courriel +(>thunderbird <outlook)
      -> Pesquisar as linhas que contenham as palavras *e-mail* e *thunderbird*,
                                                    ou *e-mail* e *outlook* (não importa qual a ordem), 
         mas classificar *e-mail thunderbird* mais do que *e-mail outlook*.
    - open*
       -> Encontrar palavras como *openoffice*, *openwriter*, *openbar* ou *openphp*.
    - "openoffice"
       -> Pesquisar linhas que contenham exatamente a frase *openoffice*

As diferentes abas
----------------------

- **Aba "Base de conhecimentos"**
  Essa aba exibe uma tabela relacionada ao artigo com título, categoria.
  São listados tema, conteúdo, nome do editor, datas de criação e última modificação, o número de vezes que o artigo foi lido e se faz ou não parte do FAQ.
  Se um artigo não foi publicado, aparece em vermelho.


-   **Aba "Target"**
    Um artigo é considerado pessoal por padrão. Consequentemente, é visível somente por seu autor.

    Para um item torna-se visível para outros usuários, é necessário selecionar um ou mais "alvos". O ou os alvos correspondem as entidades, perfis, grupos ou usuários que podem visualizar a anotação.

    Essa aba permite adicionar um novo alvo ao listar aqueles já definidos


- **Aba "Editar"
  Essa guia permite, de acordo com suas autorizações, modificar ou excluir um item.


- **[Aba "Documentos"](index.php?pt/As_diversas_abas/Aba_Documentos.md)**
    É possível associar um ou mais documentos a uma anotação

- **[Aba "Todas"](index.php?pt/As_diversas_abas/Aba_Todas.md)**
     Para um item, todas as informações são exibidas em uma página.


As diversas ações
-----------------------
-   **[Adicionar um artigo](index.php?pt/As_diversas_acoes/Criando_um_novo_objeto.md)**
-   **Alterar um artigo**
    A modificaçã é feita a partir da aba *Editar*.
-   **Excluir um artigo**
    A exclusão é feita a partir da aba *Editar*. Tendo em conta que a base de conhecimento não é Lixeira, uma mensagem pede para confirmar a sua remoção permanente
-   **[Vinculando um documento a um artigo](index.php?pt/As_diversas_acoes/Linkando_um_documento_a_um_objeto.md)**
-   **Fazer um artigo público**
    Basta adicionar um destino para o artigo.
-   **publicar um artigo em um determinado período**
    Basta adicionar uma data de início e uma data final para o nível visibilidade

----------------
**Tópico principal :** [Módulo Ferramentas](index.php?pt/06_Module_Outils/01_Module_Outils.md "Le module Outils permet aux utilisateurs de gérer les notes, la base de connaissance, les réservations ainsi que de générer des rapports")