Para ir mais longe
====================

As categorias
--------------

Uma categoria pode ser hierarquizada :
- selecionar uma categoria principal na primeiro aba via campo "Subordinado" ;
- adicionar uma categoria segundária desde a segunda aba (Categorias do ticket ou das tarefas).


- **As categorias dos tickets**

  Contrariamente a seu nome, as categorias dos tickets também são utilizados para os problemas e alterações.
  A gestão das categorias são acessíveis a partir do menu títulos : ***Configuração > Títulos > Categorias dos tickets***.

  ![image](docs/image/categorieTicket.png)

  Um grupo oficial e/ou um grupo técnico podem ser adicionados a essa categoria e irá ser usada para notificações.

  Você também pode atribuir uma categoria para a base de conhecimento para pesquisa. Isto irá registar a ação da solução de objecto (se desejado), nesta categoria.

  ***Exemplo :*** 
  - categoria do ticket : falha no disco rígido
  - campo de conhecimento básico da categoria : Falha > Computador
  Se a categoria "Falha no disco rígido" for selecionada no ticket, além de adicionar uma solução ao ticket nos conhecimentos básicos, ele será armazenado em "Falha > Computador".

Uma categoria pode ser invisível na interface simplificada (para reduzir a lista de categorias apresentadas para usuários finais).
 Também pode ser visível ou não para incidentes, solicitações, problemas ou mudanças.

  Finalmente, um modelo pode estar associado a essa categoria e será o responsável ao escolher a categoria no objeto. Esse modelo pode ser diferente entre os pediods e incidentes.


  A categorização facilita o tratamento de um objeto. Por exemplo, para um bilhete, dependendo da configuração desejada, o requerente pode indicar uma categoria, e a mudança técnica.

    É importante durante a implementação do Helpdesk, pensar na lista de categorias disponíveis : de fato, muitas visíveis para os usuários podem atrapalhar a entrada, enquanto poucas não irão beneficiar as necessidades adequadamente.

    As categorias dos tickets são um dos elementos que permites processar automaticamente a criação de um ticket (veja [Regras de negócios para os tickets](index.php?pt/7_Modulo_Administracao/05_Regras/04_Regras_de_negocios_para_os_tickets.md "Ao criar um ticket, um mecanismo permite modificar os atributos de maneira automática.")).


- **As categorias das tarefas**
  
  Elles servent à catégoriser les tâches pour faciliter leur traitement ou à des fins statistiques.

[As regras da programação](index.php?pt/04_Modulo_Assistencia/03_Définir_la_matrice_de_calcul_de_la_priorité.md)
------------------------

Configurer la matrice d'attribution des priorités en fonction de l'urgence et de l'impact : limiter les niveaux d'urgence et d'impact disponibles.

[Consulter et gérer les plannings](index.php?pt/04_Modulo_Assistencia/09_Planning.md)
------------------------
Suivez les tâches planifiées.

La notification par courrier électronique
-----------------------------------------
Les actions sur les tickets peuvent entrainer l'envoi de notification suivant un évènement déclencheur (création d'un ticket, réponse à enquête de satisfaction...).
Voir **configurer les notifications**.

[Les statistiques](index.php?fr/04_Module_Assistance/10_Statistiques.md)
------------------
Les rapports concernant les tickets, les problèmes ou les changements sont disponibles dans le menu ***Assistance > Statistiques***.

-------------
**Sujet parent :** [Le service d'assistance aux utilisateurs](index.php?fr/04_Module_Assistance/01_Module_Assistance.md "Le service d'Assistance aux utilisateurs de GLPI")
