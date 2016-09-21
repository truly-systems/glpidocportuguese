Administrando os contratos
==================

Os contratos referem-se a acordos entre terceiros. 	Itens de inventário podem ser associado a um contrato. Este recurso permite cobrir todo o contrato realizado como empréstimos, contratos de manutenção...

Um contrato inclui vários tipos de informação :

-   as informações gerais (nome, tipo, número) ;
-   des informations temporelles (date de début, durée, périodicité, heures d'intervention). Les plages horaires sont intéressantes dans le cadre d'un contrat de maintenance ou d'infogérance par exemple ;
-   des informations comptables (reconduction, durée de préavis, périodicité de facturation).

Il est possible d'être alerté par courriel sur différents éléments du contrat (fin, préavis, fin de période...).

**[Gérer les gabarits](index.php?fr/Les_différentes_actions/Gérer_les_gabarits.md)**

Description des champs
----------------------
-   **Type de contrat** : par défaut, aucun type de contrat n'est renseigné. Il faut au préalable les renseigner dans la configuration des intitulés. Voir [Configurer les intitulés](index.php?fr/08_Module_Configuration/02_Intitulés/01_Intitulés.md "Les intitulés se configurent depuis le menu Configuration > Intitulés") ;
-   **Numéro**: cette information n'est pertinente que si le numéro de contrat est identique à celui utilisé au sein des autres services de la société ;
-   **Date de début** : à ne pas confondre avec la date d'enregistrement du contrat dans GLPI. Tous les calculs de périodicité sur le contrat sont donc fonction de cette date ;
-   **Durée initiale du contrat** : si ce champ et la date de début sont renseignés, la date de fin de contrat apparaitra (en rouge si la date a expirée) ;
-   **Préavis** : ce champ peut servir également au déclenchement des notifications d'alerte ;
-   **Numéro comptable** : pour permettre un rapprochement avec le logiciel comptable de la société ;
-   **Périodicité du contrat** : c'est la durée à laquelle la reconduction du contrat est possible (*Exemple : Un contrat d'abonnement téléphonique d'une durée de 24 mois renouvelable au bout de 12 mois*) ;
-   **Périodicité de facturation** :
-   **Type de reconduction** : *Tacite* (le contrat est reconductible automatiquement d'une période à une autre si aucune des parties ne manifeste sa volonté de le rompre) ou *Expresse* (nécessite l'accord des deux parties pour la reconduction du contrat) ;
-   **Nombre max d'éléments** : la valeur choisie dans ce champ bloquera ou non l'ajout de nouvel éléments attachés à ce contrat ;
-   **Heures d'intervention** : Les plages horaires d'intervention correspondent aux horaires d'intervention couvert par le contrat. Il est possible d'y distinguer les samedis et les jours chômés.

Les différents onglets
----------------------
-   **Onglet "Coûts"**
    Les éléments de coûts peuvent être saisi indépendamment (coût initial, coût avenant...).
    Chaque élément peut être lié à un budget différent (voir [Gérer les budgets](index.php?fr/05_Module_Gestion/02_Budgets.md "Les budgets sont gérés depuis le menu Gestion > Budgets")).
    Sous la possibilité d'ajout de nouveaux coûts, un tableau récapitule les coûts déja enregistrés ainsi que le coût total pour ce contrat.

-   **[Onglet "Fournisseurs"](index.php?fr/Les_différents_onglets/Onglet_Fournisseurs.md)**
    Gérer les informations financières et administratives

-   **[Onglet "Eléments"](index.php?fr/Les_différents_onglets/Onglet_Eléments.md)**
    Cet onglet permet d'ajouter et de visualiser les éléments attachés à ce contrat.
    
-   **[Onglet "Documents"](index.php?fr/Les_différents_onglets/Onglet_Documents.md)**

-   **[Onglet "Liens"](index.php?fr/Les_différents_onglets/Onglet_Liens.md)**
     Pour certains éléments, les liens externes se gèrent depuis le menu ***Liens externes***

-   **[Onglet "Notes"](index.php?fr/Les_différents_onglets/Onglet_Notes.md)**

-   **[Onglet "Historique"](index.php?fr/Les_différents_onglets/Onglet_Historique.md)**
     L'historique est visualisé depuis l'onglet *Historique*

-   **[Onglet "Debug"](index.php?fr/Les_différents_onglets/Onglet_Debug.md)**
    Uniquement si vous êtes connecté en mode Debug.

-   **[Onglet "Tous"](index.php?fr/Les_différents_onglets/Onglet_Tous.md)**
     Pour un élément, toutes les informations sont affichées sur une seule page.


Les différentes actions
-----------------------
-   **[Ajouter un contrat](index.php?fr/Les_différentes_actions/Créer_un_nouvel_objet.md)**
-   **[Voir un contrat](index.php?fr/Les_différentes_actions/Visualiser_un_objet.md)**
-   **[Modifier un contrat](index.php?fr/Les_différentes_actions/Modifier_un_objet.md)**
-   **[Supprimer un contrat](index.php?fr/Les_différentes_actions/Supprimer_un_objet.md)**
-   **[Associer un document à un contrat](index.php?pt/As_diversas_acoes/Lier_un_document_à_un_objet.md)**
-   **[Transférer un contrat vers une autre entité](index.php?pt/As_diversas_acoes/Transférer_un_objet.md)**
-   **Paramétrer les alertes sur les contrats**
    Il est possible de recevoir des notifications pour prévenir d'événements tels que la fin du contrat.
    Dans le cas ou la reconduction du contrat serait expresse, il peut être intéressant d'être alerté à la date du préavis. Pour les contrats périodiques il est également possible d'être alerté à la
    fin de chaque période ou préavis de période.
    Ceci est configurable par entité dans le menu **Configuração > Notificações** pour définir les modèles et destinataires utilisés et dans le menu **Configuração > Entidade** para ativar ou desativar essa funcionalidade, définir les valeurs par défaut et une anticipation de l'envoi de la notification si besoin.

--------
**Tópico principal :** [Módulo Gestão](index.php?pt/05_Modulo_Gestao/01_Modulo_Gestao.md "O módulo Gestão possibilita aos usuários administrar os contatos, fornecedores, orçamentos , os contatos e os documentos")
