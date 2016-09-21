Administrando os softwares
===================

GLPI possibilita a gestão dos softwares, de suas versões e licenças (que podem estar associadas ou não às versões).

Um software é padronizadamente associado a uma entidade: isso quer dizer que gaverão muitos softwares com base na existência de entidades. Executar um software visível pelas sub-entidade permite fazer uma administração mais fina.

A gestão financeira é efetuada ao nível das licenças, enquanto que o presente modelo de  software é usado apenas para as licenças que lhe são associadas.

Os softwares podem ser importados automaticamente a partir de uma ferramenta do inventário e nesse caso um dicionário pode ser usado para filtrar dados (veja [Configuração dos dicionários de dados](index.php?pt/07_Modulo_Administracao/06_Dicionarios.md "Os dicionários são gerenciados a partir do menu  Administração > Dictionários")).

Alguns campos são específicos para o registro do software :
- **Atualização** é um dado informativo, a partir da qual nenhum tratamento é realizado e indica que o software é uma atualização de outra versão.
- **Categoria** possibilita agrupamentos em uma lista de software de um computador.
- **Anexando um ticket** define a visibilidade do software na lista "Hardware" de um ticket.

**Boas práticas:**

1.  Crie o software
2.  Crie as versões
3.  Crie as licenças

***Sugestão :*** no modo multi-entidades, a lista dos softwares pode ser longa, em parte devido as duplicatas (1 software por entidade). Uma gestão mais detalhada dos softwares, licenças e versões pode agrupar os softwars idênticos na mesma entidade (veja aba *Agrupamento* acima), puis à rendre récursif les éléments qui peuvent l'être.

**[Administrando os modelos](index.php?pt/As_diversas_acoes/Administrando_os_modelos.md)**

As diversas abas
----------------------
-   **Aba "Versões"**
    Princípios e gestão das versões de software em GLPI

     Uma versão de  um software pode ser instalado em um computador.
     Veja também guia *Instalações* abaixo.

     A vista principal lista o número da versão instalada.

     ** Campos específicos: **
     - ** ** Nome: corresponde ao número da versão;
     - ** ** Status: recomendações ITIL, que acompanha o DSL (biblioteca de armazenamento de versões autorizadas);
     - ** ** Sistema operacional: o sistema operacional que está executando esta versão do software;
     - ** ** Serviço: número de instalações de versão;
     - ** Comentários **.


-   **[Aba "Licenças"](index.php?pt/03_Modulo_Parque/04_Softwares/Aba_Licencas.md)**
   Princípios e gestão de licenças de software em GLPI


- ** Guia "Instalações **
    Princípios e gestão das instalações de software em GLPI.

    Instalação do software em um post é exibido através de uma versão (ver *Versões* guia acima) e disponível na forma de software (lista de computadores com pelo menos uma versão instalada) por um versão (computadores com a versão instalada) ou, finalmente, no registro do computador (lista de versões de software instaladas, classificado por categorias).

   ***Observações :***
   - A coluna licença é cumprida quando a licença é atribuída ao computador afetadoé.
   - A tela inicial de diversas categorias depende das preferências do usuário. Veja [Administrando as preferências](index.php?pt/02_Primeiros_passos_com_GLPI/03_Utilizacao_GLPI/04_Administrando_as_preferencias.md").

   2 opções estão disponíveis na lista de um instalações de software do computador. Acima da lista, **Instalar ** manualmente uma versão do software no computador (requer que você selecione o software e a versão): Se houver uma licença associada a ele a "Versão de uso" de licença é preenchido automaticamente.

    ** ** Para Desinstalar uma versão deste software, usar o sistema de ações de massa: selecione as versões que quer excluir e escolha ***Excluir Definitivamente**.

  Você pode adicionar uma nova licença associado a esse computador. O sistema permite que ações de massa, através da ação **Instalar**, instalar versões para o uso de licenças selecionadas

-   **[Aba "Gestão"](index.php?pt/As_diversas_abas/Aba_Gestao.md)**
    Administrando as informações financeiras e administrativas

-   **[Aba "Contratos"](index.php?pt/As_diversas_abas/Aba_Contratos.md)**
    Administrando os contratos associados

-   **[Aba "Documentos"](index.php?pt/As_diversas_abas/Aba_Documentos.md)**

-   **[Aba "Tickets"](index.php?pt/As_diversas_abas/Aba_Tickets.md)**

-   **[Aba "Problemas"](index.php?pt/As_diversas_abas/Aba_Problemas.md)**

-  **[Aba "Links"](index.php?pt/As_diversas_abas/Aba_Links.md)**
     Para certos itens, os links externos são gerados a partir do menu ***Links externos***

-   **[Aba "Anotações"](index.php?pt/As_diversas_abas/Aba_Anotacoes.md)**

-   **[Aba "Reservas"](index.php?pt/Les_différents_onglets/Aba_Reservas.md)**
     Administração das reservas para um onjeto do inventário

-   **[Aba "Histórico"](index.php?pt/As_diversas_abas/Aba_Historico.md)**
     O histórico é visualizado a partir da aba *Histórico*

-   **Aba "Consolidação"**
    Como combinar homônimos de software na sub-entidades.

    ***Observação :** Esta opção só está disponível para a plataforma multi-entidade.*

    Possibilita combinar os softwares das entidades filhas na entidade mãe.

    ***Como realizar um reagrupamento:***

    1.  Se o software não existe na entidade principal  :
         Criar um software cujo nome é idêntico ao nome do software nas sub entidades;
     2. Abra o software plug-principal;
     3. Ative a recursividade (sub-entidades Sim superior direito);
     Uma nova guia "Reagrupamento" aparece depois na guia "Histórico".
     4. Abra a guia;
     A lista mostra as entidades secundárias do software com o mesmo nome.
     5. Selecione as linhas desejadas e confirme a consolidação.

    > ATENÇÃO : Essa operação é irreversível.

    ***Efeitos da consolidação :***

    -   s licenças estão vinculada ao software original, mas permanecem nas sub-entidades originais;
     - As versões são mesclados (duplicado com a entidade-mãe);
     - O software antigo é movido para o lixo;

     *** Nota ** Ao usar um inventário ferramenta de terceiros, lembre-se: *
     * - Esvaziar o lixo no final do grupo (se não restaurar o software de sincronização se nova versão) *
     * - Para atribuir o mesmo fabricante do novo software (sincronização verificando o nome do fabricante, um novo software seria criado)

-   **[Aba "Depuração"](index.php?pt/As_diversas_abas/Aba_Depuracao.md)**
    Apenas se você estiver conectado no modo de Depuração.

-   **[Aba "Todas"](index.php?pt/As_diversas_abas/Aba_Todas.md)**
     Para um item, todas as informações são exibidas em uma única página.


As diversas ações
-----------------------
-   **[Adicionando um software](index.php?pt/As_diversas_acoes/Criando_um_novo_objeto.md)**
-   **[Visualizando um software](index.php?pt/As_diversas_acoes/Visualiser_un_objet.md)**
-   **[Alterando um software](index.php?pr/As_diversas_acoes/Alterando_um_objeto.md)**
-   **[Excluindo um software](index.php?pr/As_diversas_acoes/Excluindo_um_objeto.md)**
-   **[Vinculando um documento a um software](index.php?pr/As_diversas_acoes/Linkando_un_documento_a_un_objeto.md)**
-   **[Vinculando um contrato a um software](index.php?pr/As_diversas_acoes/Linkando_um_contrato_a_um_objeto.md)**
-   **[Transferindo um software para outra entidade](index.php?pt/As_diversas_acoes/Transferindo_um_objeto.md)**
-   **Adicionando uma versão a um software**
    Veja aba *Versões* acima
-   **[Administrando as licenças](index.php?pt/03_Modulo_Parque/Aba_Softwares/Aba_Licencas.md)**
    A partir do menu ***Parque > Softwares*** clique sobre o nome da licença na guia *Licenças*.

-------
**Tópico principal :** [Módulo Parque](index.php?pt/03_Modulo_Parque/01_Modulo_Parque.md "Módulo Parque da GLPI")
