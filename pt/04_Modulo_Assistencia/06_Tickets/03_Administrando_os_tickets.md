Administrando os tickets
=================

Características e utilização dos tickets da GLPI

Gérer les incidents en conformité avec ITIL ou pas
--------------------------------------------------

Le module d'assistance de GLPI est conforme au guide de bonnes pratiques ITIL pour la partie Gestion des incidents et gestion des demandes de services : il intègre donc des notions comme l'impact, l'urgence d'un ticket, la matrice de calcul des priorités associées et une normalisation des statuts. Bien que l'outil soit conforme ITIL, il n'y aucune obligation pour suivre ces bonnes pratiques : chacun est libre d'implémenter la gestion des incidents qui correspond le mieux à ses besoins.

As estatísticas do tickets estão disponíveis em  (veja [Visualizando as estatísticas](index.php?pt/04_Modulo_Assistencia/11_Estatisticas.md "Os relatórios referentes aos tickets estão disponíveis no menu Assistência > Esatatíticas")).


Descrição dos diversaos campos
--------------------------------
- **Date d'ouverture** : date de création du ticket ;

- **Date d'échéance** : Date à laquelle le ticket doit être résolu ;

Ces 2 dates permettent de circonscrire l'incident ou la demande de service dans le temps. Un **SLA** peut également être associé à un ticket. Dans ce cas, le SLA ainsi que le prochain niveau d'escalade sont affichés (voir [Configurer les SLAs](index.php?pt/08_Modulo_Configuracao/05_Sla/01_Sla.md "Dans GLPI, administrer les SLAs pode ser feito a partir do menu Configuração > SLAs.")).

- **Par** : référence l'utilisateur GLPI qui a ouvert le ticket ;

- **Tipo** : permet de définir s'il s'agit d'une demande ou d'un incident ;

- **Categoria** permet de classer les demandes ou incidents suivant leur nature (une catégorie pouvant être associée uniquement à un seul type) ;

- **Status** statut attribué manuellement par le technicien ou dynamiquement suivant les actions effectuées (veja [Regras de gestão](index.php?pt/04_Modulo_Assistencia/04_Tickets/01_Regras_de_gestao.md) et [Matrice de cycle de vie](index.php?fr/04_Module_Assistance/05_Les_matrices_de_cycle_de_vie.md)) ;

- **Source de la demande** : canal utilisé pour créer les tickets (voir [Configurer les intitulés](index.php?fr/08_Module_Configuration/02_Intitulés/01_Intitulés.md "Les intitulés se configurent depuis le menu Configuration > Intitulés")) ;

- **Urgence** : indique l'importance donnée par le demandeur au ticket ;

- **Impact** : est celle jugée par le technicien ;

- **Priorité** : est l'importance du ticket calculée automatiquement suivant une matrice de calcul prédéfinie en tenant compte de l'impact et de l'urgence définis (Voir [Matrice de cycle de vie](index.php?fr/04_Module_Assistance/05_Les_matrices_de_cycle_de_vie.md) ;

- **Validation** : par défaut il est *non soumis à validation* ;

- **Élément** : liste les éléments associés à ce ticket. L'ajout d'un nouvel élément se fait via l'onglet *Elements*.

- **Lieu** : permet d'indiquer le lieu de l'intervention et n'a aucun lien avec le lieu de l'élément associé où le lieu du demandeur (cas d'un demandeur "nomade" avec un portable) ;

- **Les acteurs**
  Les acteurs concernés sont référencés dans le ticket, ce qui permet leur notification durant le cycle de vie du ticket (Voir [Définir les acteurs](index.php?fr/04_Module_Assistance/02_Définir_les_Acteurs.md)).

  Deux informations concernant les notifications apparaissent pour un utilisateur ou un fournisseur si les suivis par courriels ont été configurés (Voir [Configurer les notifications](index.php?fr/08_Module_Configuration/04_Notifications/01_Configurer_les_notifications.md "Les notifications se configurent depuis le menu Configuration > Notifications ;")) : l'activation du **suivi par courriel** pour ce ticket et le **courriel** utilisé. Celui-ci est pré-rempli par défaut avec la valeur présente et définie par défaut dans la fiche de l'utilisateur ou du fournisseur (s'il en a une) et peut être modifié dans la liste déroulante si besoin. Si aucun courriel n'est défini dans la fiche de l'utilisateur ou du fournisseur sélectionnée, elle peut être indiquée, uniquement pour ce ticket, dans la zone de texte.

  Dans le cadre d'une utilisation de GLPI multi-entités avec des techniciens ayant des habilitations sur plusieurs entités, il n'est pas nécessaire de changer l'entité courante pour déclarer un nouvel incident
dans une entité. Le cheminement de l'ouverture d'un nouveau ticket est le suivant : le technicien commence par sélectionner le demandeur et GLPI va déterminer les entités sur lesquelles celui-ci a des habilitations. 
  S'il n'en possède que sur une entité, alors le formulaire de création est mis à jour et le ticket sera déclaré dans l'entité correspondante.
  S'il en possède plusieurs une liste déroulante supplémentaire permet de sélectionner celle dans laquelle on veut affecter le ticket.

- **Titre**
  Si aucun titre n'est défini par l'utilisateur lors de la création du ticket, les 70 premiers caractères de la description sont utilisés pour définir le titre du ticket ;

- **Description** : obligatoire pour les raisons définies ci-dessus.

- **Tickets liés** : définit une relation entre les tickets. 
  Cette liaison peut être de 2 types :
  -   *Lié à* : ce n'est qu'une liaison simple qui n'a qu'un but informatif ;
  -   *Duplique* : c'est une duplication de ticket. A la résolution d'un des tickets, la même solution est définie sur les tickets dupliqués (qui sont donc automatiquement résolus).


Les différents onglets
----------------------
-   **Onglet "Suivis"**
    C'est l'onglet par défaut lors de la consultation d'un ticket, sauf si celui-ci est en attente d'approbation de solution. 
    Il permet l'ajout d'informations à un ticket existant, par exemple signaler que le demandeur a rappelé, que le ticket est en attente de la disponibilité du demandeur... 
    C'est l'élément permettant les échanges entre le demandeur et les personnes en charge de son ticket.

    Pour ajouter un suivi, cliquer sur **Ajouter un nouveau suivi** et saisir une description.

    Il est possible de choisir la source du suivi (Voir [Configurer les intitulés](index.php?fr/08_Module_Configuration/02_Intitulés/01_Intitulés.md "Les intitulés se configurent depuis le menu Configuration > Intitulés")).

    Un suivi peut être privé ou public. Un suivi privé n'est visible que des utilisateurs ayant le droit `Voir tous les suivis et tâches` (publics et privés) dans ses habilitations. Cela permet, par exemple, un échange entre techniciens sans que le demandeur ne puisse le voir.

    L'ajout, la modification ou la suppression d'un suivi dépend des droits définis dans le profil (voir [Administrer les profils d'utilisateurs](index.php?fr/07_Module_Administration/07_Profils/01_Profils.md "Dans GLPI, administrer les profils peut se faire à partir du menu Administration > Profils.")).


-   **[Onglet "Validation"](index.php?fr/Les_différents_onglets/Onglet_Validations.md)**


-   **[Aba "Tarefas"](index.php?pt/As_diversas_abas/Aba_Tarefas.md)**
    Une tâche est une action correspondant à une intervention technique liée à un ticket.


-   **[Aba "Solução"](index.php?pt/As_diversas_guias/Aba_Solucao.md)**
    Cet onglet solution permet la résolution du ticket par un technicien et l'approbation de la solution par le demandeur ou le rédacteur.
**Vos tickets à clore**.


-   **[Aba "Estatísticas"](index.php?pt/As_diveras_abas/Aba_Estatisticas.md)**


-   **[Aba "Custos](index.php?pt/As_diversas_abas/Aba_Custos.md)**
    Définition des coûts applicables à ce ticket.


-   **Aba tarefas do projeto**
    Liste les tâches d'un projet liées à ce ticket en indiquant, para cada tarefa, o nome do projeto, seu nome, seu tipo, seu status, a porcentagem concluída, as datas de início e fim previsto, a duração prevista e a duração real e o nome da tarefa principal.
    Você pode editar uma tarefa ou projeto clicando em seu nome.


-   **[Aba "Documentos"](index.php?pt/As_diversas_abas/Aba_Documentos.md)**


-   **[Aba "Itens"](index.php?pt/As_diversas_abas/Aba_Itens.md)**
    Possibilita vincular diversos itens ao ticket.


-   **[Aba "Problemas"](index.php?pt/As_diversas_abas/Aba_Problemas.md)**

-   **[Aba "Alterações"](index.php?pt/As_diversas_abass/Onglet_Changements.md)**
    Adicionando e visualizando as alterações associadas a esse ticket.

-   **[Onglet "Historique"](index.php?pt/As_diversas_abas/Aba_Historico.md)**
     O histórico é visualizado a partir da aba *Histórico*

-   **[Aba "Depuração"](index.php?pt/As_diversas_abas/Aba_Depuracao.md)**
    Apenas se estiver conectado no modo Depuração.

-   **[Aba "Todas"](index.php?pt/As_diversas_abas/Aba_Todas.md)**
     Para um item, todas as informações são exibidas em uma única página.


As diversas ações
-----------------------
-   **[Adicionando um ticket](index.php?pt/04_Modulo_Assistencia/05_Criando_um_ticket.md)**
-   **[Alterando um ticket](index.php?pt/As_diversas_acoes/Alterando_um_objeto.md)**
-   **[Supprimer un ticket](index.php?fr/Les_différentes_actions/Supprimer_un_objet.md)**
-   **[Associer un document à un ticket](index.php?fr/Les_différentes_actions/Lier_un_document_à_un_objet.md)**
-   **Lier des tickets entre eux**
    Cette action se réalise via le champ *Tickets liés* du formulaire
-   **[Transférer un ticket vers une autre entité](index.php?fr/Les_différentes_actions/Transférer_un_objet.md)**


--------
**Sujet parent :** [Le service d'assistance aux utilisateurs](index.php?fr/04_Module_Assistance/01_Module_Assistance.md "Le service d'Assistance aux utilisateurs de GLPI")
