Administrando as anotações pessoais ou públicas
=========================================

Esse módulo permite a administração das anotações, sua duração, seu status e se deve aparecer no cronograma. Uma anotação corresponde a uma informação pessoal ou pública.

As anotações inseridas aparecem na página inicial de GLPI ou no planejamento.

É possível estabelecer uma data de início e data final da publicação para cada anotação.
Se a data de início não for mencionada, a anotação será visível até a data final.
Se a data final não for mencionada, a anotação estará permanentemente visível a partir da data de início.

Adicionando uma anotação na agenda possibilita que ela apareça no planejamento dos outros usuários interessados: a dos usuários para uma anotação pessoal, os cronogramas de todos os usuários no caso de uma anotação púlica. Uma anotação agendada não é excluída após as datas de validade.

***Observação :** Você pode definir um aviso para a anotação antes do seu início, definindo um intervalo de tempo para o aviso. As notificações devem ser habilitadas para ele (veja em [Configurando as notificações](index.php?pt/08_Modulo_Configuracao/04_Notificacoes/01_Configurando_as_notificacoes.md "As notificações são configuradas a partir do menu Configuração > Notificações ;")).*


As diferentes guias
----------------------

-   **[Guia "Documentos"](index.php?pt/As_diferentes_guias/Guia_Documentos.md)**
    É possível associar um ou mais documentos para uma anotação.


-   **Guia "Destino"**
    Uma anotação é considerada pessoal por conta do padrão. Consequentemente, ela é visível apenas para quem a redigiu.

    Para que uma nota se torne visível para outros usuários (anotação pública), é necessário selecionar um ou mais destinos. O ou os destinos correspondentes são entidades, perfis, grupos ou usuários que podem visualizar a anotação.

    Uma anotação pública é visível para os usuários vinculados a um perfil autorizado a ler anotações públicas.

-   **[Guia "Todas"](index.php?pt/As_diferentes_guias/Guia_Todas.md)**
    Para um item, todas as informações são exibidas em uma única página.


As diferentes ações
-----------------------
-   **[Adicionar uma anotação](index.php?pt/As_diferentes_acoes/Criar_um_novo_objeto.md)**
-   **[Alterar uma anotação](index.php?pt/As_diferentes_acoes/Alterar_um_objeto.md)**
-   **[Eliminar uma anotação](index.php?pt/As_diferentes_acoes/Remover_um_objeto.md)**
-   **[Associar um documento a uma anotação](index.php?pt/As_diferentes_acoes/Linkar_um_documento_a_um_objeto.md)**
-   **Crie uma anotação pública**
    Basta adicionar um destino para sua anotação.
-   **publicar uma anotação durante um determinado período**
    Basta adicionar uma data de início e uma data final para o nível de visibilidade.

-----------
**Tópico principal :** [Modulo Ferramentas](index.php?pt/06_Modulo_Ferramentas/01_Modulo_Ferramentas.md "O módulo Ferramentas possibilita aos usuários administrar as anotações, la base de connaissance, les réservations ainsi que de générer dos relatórios")