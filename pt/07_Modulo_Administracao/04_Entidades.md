Administrando as entidades
=======================

A noção de entidade é uma noção chave na GLPI. Elle peut s'apparenter à la notion de hierarquia, de service au sein d'une administration d'une entreprise ou d'un système d'information.
Elle permet d'isoler des ensembles organisés de manière hiérarchique dans une instance unique de GLPI (une seule installation de GLPI). Le terme choisi est volontairement neutre, afin de pouvoir s'adapter à chaque système d'information. Une seule instance de GLPI composée de plusieurs entités permet la consolidation des données et des règles communes.
L'utilisation des entités permet un cloisonnement relativement étanche entre les unités organisationnelles. Dans les cas où ce cloisonnement étanche n'est pas souhaité, il est préférable d'utiliser les fonctionnalités offertes par les groupes.
La segmentation en entités peut avoir plusieurs finalités : isoler le parc informatique de chaque service afin de limiter la vision du parc à certains groupes ou utilisateurs ; isoler le parc informatique de différents clients, reproduire la hiérarchie existante au sein de votre annuaire informatique (LDAP, Active Directory)... Cette notion est très intéressante pour une entreprise dont la gestion est hiérarchique et où les personnes doivent avoir une vision du parc dépendant de leur appartenance à un service.

Une fois plusieurs entités créées dans GLPI, l'inventaire de votre parc, les utilisateurs, les profils ou encore le service d'assistance devient fonction des entités. Autrement dit, on peut affecter un ordinateur à une entité, déclarer un ticket sur une entité, créer des profils, gérer des habilitations spécifiques à chaque entité. L'affectation automatique des utilisateurs et des matériels est possible grâce au paramétrage de règles.

On considère la hiérarchie suivante :

              EM
        |------|------|
       EA            EB
      |   |        |    |
    EA1   EA2     EB1   EB2


L'entité mère (EM, ou nativement appelée Entité Racine dans GLPI) possède deux filiales (EA et EB) qui possèdent à leur tour deux départements chacune (EA1, EA2, EB1 et EB2). Chaque entité possède une vision de son parc et des entités qui lui sont affiliées.

-   EM a une vision de son parc et de toutes les entités.
-   EA a une vision de son parc et de EA1 et EA2.
-   EA1 ne voit que son parc.

Un utilisateur peut être rattaché à plusieurs entités avec des droits différents. Ces droits peuvent être conservés sur les entités filles ou non. Pour reprendre l'exemple précédent, un utilisateur ne pourra déclarer un ticket qu'au sein de son service, se rapportant uniquement au matériel qui lui est rattaché ou à un matériel de son service (une imprimante, un écran...).

Inversement, un utilisateur disposant d'habilitations plus étendues pourra consulter l'ensemble des matériels, tickets ou autres objets. Et ce, sur toutes les entités sur lesquels ses droits sont applicables.

Par défaut, GLPI s'installe avec une entité générique, appelée Entité Racine. Il est donc mono-entité. Cette entité peut être renommée simplement en modifiant le non de celle-ci.

Les fonctionnements peuvent être amenés à varier d'une entité à une autre. C'est pour cela que les entités possèdent une administration déléguée (droit *Entités* dans le profil). Cette délégation doit être attribuée à un nombre très restreint d'utilisateurs qui auront en charge la gestion complète de l'entité.

Dans le cadre d'une utilisation de GLPI en multi-entités, la gestion de certains paramètres de configuration peut s'effectuer différemment pour chaque entité (§).

As diversas guias
----------------------

-   **Guia "Entidades"**
    Permet d'ajouter une sous-entité à l'entité sélectionnée et liste les sous-entités existantes. 

-   **Guia "Adresse"**
    Regroupe les informations administrative de l'entité (endereço, telefone, fax, e-mail...). 

-   **Guia "Informations avancées" §**
    Regroupe les données d'identification technique de l'entité : celles en rapport avec les règles génériques d'affectation à l'entité et celles concernant l'interface de recherche des utilisateurs. Ces données seront utilisés par les règles pour l'affectation automatique à cette entité (matériel si couplage avec un agent d'inventaire, utilisateur ou groupe si liaison avec un annuaire LDAP, ticket si création autorisé via un collecteur de courriel) ainsi que pour l'import et la synchronisation des utilisateurs issus d'un annuaire lDAP. 

    Afin de donner à un administrateur d'une entité la possibilité d'importer ses utilisateurs d'un annuaire LDAP, il est nécessaire de préciser certains paramètres : l'annuaire associé à l'entité et le
filtre de recherche. Ce dernier n'est important que si la définition d'une entité se fait par l'ajout d'une restriction sur le filtre LDAP. Il est également possible de définir le domaine de messagerie spécifique à l'entité qui peut être utilisé pour affecter les utilisateurs à cette entité.

    Trois options sont disponibles pour l'utilisation des règles d'affectation génériques à l'entité : le TAG provenant de l'outil d'inventaire, l'information LDAP représentant l'entité (par exemple le
DN de l'entité, voir Attribuer des habilitations à un utilisateur),
et le domaine de messagerie associé à celle-ci.

-   **Guia "Notificacoes" §**
    Le paramétrage des notifications se fait par entité.
    Cet onglet regroupe deux tableaux :
    - les options globales pour toutes les notifications issues de GLPI :
      le courriel de l'administrateur (sera le courriel expéditeur des mails issus de GLPI), le nom de l'administrateur, le préfixe pour le sujet des notifications (GLPI par défaut si vide), l'adresse de réponse (voir [configuration des suivis par courriels](index.php?pt/08_Modulo_Configuracao/04_Notificacoes/02_Configuracao_des_suivis_par_courriels.md)) et la signature.

      Pour chaque entité vous pouvez définir le délai appliqué pour l'envoi des notifications. Celui-ci permet par exemple dans le cas de modifications multiples rapides d'un ticket de n'envoyer qu'une seule notification.

      Vous pouvez également définir si le suivi par mail d'un acteur est défini à Oui ou Non.

    - les options de déclenchement des alertes pour les cartouches, consommables, contrats, informations financières, licences, réservations et tickets.
      > Important : Chaque option d'alerte est associée à une action automatique. Si l'action est désactivée par l'administrateur de GLPI, aucune notification ne sera envoyée.

    Si vous ne souhaitez pas affiner les notifications par entité, vous pouvez définir ces paramétrages au niveau de l'entité racine. Dans chaque entité sera alors pris par défaut les valeurs de l'entité parente (valeurs définies indiquées en vert).

-   **Guia "Assistência" §**
    Cet onglet est visible si vous avez les droits de lire ou modifier les paramètres de l'entité dans votre profil. Il regroupe les paramétrages de l'entité qui seront appliqués principalement aux tickets :
    - **Gabarit de ticket :** à chaque création d'un ticket, le gabarit sélectionné sera appliqué ;
    - **Calendrier :** indique le calendrier par défaut utilisable dans l'entité. Ce calendrier sert à calculer les temps d'attente des tickets et le décalage des dates d'échéance. Il sera par exemple pré-sélectionné lors de la création d'un SLA ; 
    - **Type par défaut pour les tickets :** type prédéfini lors de la création d'un ticket (très utile en cas de création de ticket via collecteur de courriels) ;
    - **Affectation automatique des tickets :** permet d'assigner automatiquement un ticket ;
      - *basée sur le matériel puis sur la catégorie :* uniquement si le ticket comporte un élément associé et que cet élément comporte un responsable ou un groupe technique. Dans ce cas, le ticket sera automatiquement affecté à ce technicien et/ou ce groupe technique à la sélection de l'élément associé. 
         Si ces champs sont vides mais que le ticket a une catégorie de définie, le responsable ou le groupe technique seront cherchés dans cette catégorie.
      - *basée sur la catégorie puis sur le matériel :* uniquement si une catégorie est définie dans le ticket et que cette catégorie comporte un responsable ou un groupe technique. Dans ce cas, le ticket sera automatiquement affecté à ce technicien et/ou ce groupe technique à la sélection de la catégorie.
        Si ces champs sont vides mais que le ticket a un élément associé de défini, le responsable ou le groupe technique seront cherchés dans cet élément.
    - **Clôture automatique des tickets résolus après :** permet de réaliser une clôture dite "administrative". Si cette clôture est paramétrée à *immédiatement*, dès que le ticket sera résolu il sera automatiquement clos, ce qui bloquera l'approbation de la solution par le demandeur.
      Cette clôture est réalisée via une action automatique qui doit être active.
    - **Configuração de l'enquête de satisfaction :** cette enquête peut être interne (formulaire de satisfaction de GLPI) ou gérée par à un système tiers.
      Pour chaque entité, vous pouvez donc définir quand l'enquête doit être lancée (délais à compter de la clôture d'un ticket) ainsi que le taux d'enquête à générer.
      Afin d'éviter que les anciens tickets ne soit concernés lors de l'activation de l'enquête de satisfaction, un champ *"Pour les tickets clos après"* prend la valeur de la date d'activation pour savoir quels doivent être les tickets concernés. De même, si vous décidez de reprendre les enquêtes après une période de désactivation, il faut penser à modifier ce champ pour exclure les vieux tickets.
      Pour les enquêtes externes, vous pouvez générer automatiquement à partir de balises l'adresse web pour accéder à l'enquête. Les balises disponibles sont :
      - [TICKET_ID] : id du ticket
      - [TICKET_NAME] : nom du ticket
      - [TICKET_CREATEDATE] : date de création du ticket
      - [TICKET_SOLVEDATE] : date de résolution du ticket
      - [REQUESTTYPE_ID] : id de la source de la demande
      - [REQUESTTYPE_NAME] : nom de la source de la demande (téléphone, helpdesk,...)
      - [ITEMTYPE] : type du matériel associé au ticket (ordinateur, imprimante,...)
      - [ITEM_ID] : id du matériel associé au ticket
      - [ITEM_NAME] : nom du matériel associé au ticket
      - [TICKET_PRIORITY] : priorité du ticket
      - [TICKETCATEGORY_ID] : id de la catégorie du ticket
      - [TICKETCATEGORY_NAME] : nom de la catégorie du ticket
      - [TICKETTYPE_ID] => type du ticket
      - [TICKETTYPE_NAME] => nom du type de ticket (gestion des incidents ou demandes de services)
      - [SOLUTIONTYPE_ID] => id du type de solution
      - [SOLUTIONTYPE_NAME] => nom de la solution
      - [SLA_ID] => id du sla associé au ticket
      - [SLA_NAME] => nom du sla associé au ticket
      - [SLALEVEL_ID] => id du niveau de sla
      - [SLALEVEL_NAME] = nom du niveau de sla

-   **Guia "Parque" §**
    Cet onglet propose la configuration de la gestion des différentes dates présentes dans les informations administratives et financières. 
    Les actions automatiques possibles sont :
    - le remplissage au passage du matériel dans un statut particulier ;
    - le remplissage par copie d'une autre date ;
    - aucune gestion automatique.

    L'option *Entité de création des logiciels* permet de rediriger la création des logiciels vers une autre entité se trouvant dans un niveau supérieur de la hiérarchie. Cette fonctionnalité s'applique sur la totalité des logiciels de l'entité ; si vous désirez choisir la redirection uniquement pour certains logiciel, vous pouvez utiliser le [dictionnaire des logiciels](index.php?fr/07_Module_Administration/05_Dictionnaires.md).

-   **Guia "Usuários"**
    Essa guia possibilita adicionar um usuário a esse entidade un utilisateur à cette entité tout en lui affectant un profil, récursif ou non. Il liste également, par profil, les utilisateurs de cette entité.

-   **Guia "Regras" §**
    Essa guia possibilita a criação de regras :
    - d'habilitations applicables à des utilisateurs ;
    - d'assignation de tickets ouverts par courriel. 
    Si vous avez besoin de baser ces règles sur des critères, il faut ouvrir la nouvelle règle créée pour définir ces critères.
    Sont également listés les règles déjà applicables à cette entité.

-   **[Guia "Documentos"](index.php?pt/As_diversas_guias/Guia_Documentos.md)**

-   **[Guia "Anotações"](index.php?pt/As_diversas_guias/Guia_Anotacoes.md)**

-   **[Guia "Histórico"](index.php?pt/As_diversas_guias/Guia_Historico.md)**

-   **[Guia "Todas"](index.php?pt/As_diversas_guias/Guia_Todas.md)**
     Para um item, todas as informações les informations sont affichées sur une seule page.


As diversas ações
-----------------------
-   **[Adicionando uma entidade](index.php?pt/As_diversas_acoes/Criando_um_novo_objeto.md)**
-   **[Visualizando uma entidade](index.php?pt/As_diversas_acoes/Visualizando_um_objeto.md)**
-   **[Alterando uma entidade](index.php?pt/Les_différentes_actions/Alterando_um_objeto.md)**
-   **[Excluindo uma entidade](index.php?pt/As_diversas_acoes/Excluindo_um_objeto.md)**
-   **[Vinculando um documento a uma entidade](index.php?pt/As_diversas_acoes/Guia_Itens.md)**

--------
**Tópico principal :** [Administrando os controles de acesso](../glpi/access_control_intro.html "Essa parte descrever como administrar o sistema de controle de acesso que possibilita que cada usuário tenha acesso a um contexto de utilização específica.")

**Tópico principal :** [Módulo Administração](index.php?pt/07_Modulo_Administracao/01_Modulo_Administracao.md "O módulo Administração possibilita gerenciar os usuários, grupos, entidades, perfis, regras, dicionários e fornece ferramentas para a manutenção da aplicação")
