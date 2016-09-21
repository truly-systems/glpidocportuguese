Administrando os grupos
=======================

É possível adicionar, editar, apagar os grupos, fazer buscas e exportação.

Os grupos podem ser definidos em forma de árvore para facilitar a navegação e busca.

    Exemplo :
    Direção > Departamento > Serviço
    ou
    Suporte N3 > Rede > LAN

Os grupos reúnem diversas funções :
- *habilidades* (por exemplo técnicos de rede, ou administradores de banco de dados) para helpdesk,
- *agrupamentos organizacionais* (por exemplo todos os computadores do serviço de gestão ou contabilidade) mas também *de pessoas para notificar*.

Les options disponibles permettant de régler ces comportements sont :
- **Visible dans un ticket** (groupe demandeur et/ou attribution à ce groupe) ; 
- **Peut être notifié** (destinataire de notifications) ;
- **Peut être superviseur** (uniquement pour un [projet](index.php?fr/06_Module_Outils/02_Projets/01_Projets.md "voir gérer les projets")) ;
- **Peut contenir** (matériel et/ou utilisateurs).

Dans la fiche des matériels, 2 notions de groupes sont disponibles :
*groupe technique*, qui indique quel groupe de personnes a la charge du matériel (équivalent pour un groupe du responsable technique), et groupe qui indique à quel *groupe* de matériels celui-ci appartient.

***Observação :** le groupe technique peut permettre l'auto-attribution d'un ticket à un groupe de techniciens. Voir les catégories de tickets dans le chapitre [Configurer les intitulés](index.php?pt/08_Modulo_Configuracao/07_Intitulés/01_Intitulés.md "Les intitulés se configurent depuis le menu Configuration > Intitulés").
De la même manière, il peut être utilisé dans les [Règles métier pour les tickets](index.php?fr/07_Module_Administration/05_Règles/04_Règles_métier_pour_les_tickets.md "Lors de la création d'un ticket, un mécanisme permet de modifier les attributs du ticket de manière automatique.").*

***Astuce*** : si toutes les options sont à *non*, le groupe n'apparaîtra dans aucune liste de sélection. Cela peut être utile pour un groupe supprimé et conservé pour l'historique. C'est aussi utile pour ajouter des groupes vides dans l'arborescence.

Un groupe peut avoir ou plusieurs superviseurs, notion utilisable ensuite pour les notifications, par exemple pour envoyer un courriel au(x) superviseur(s) du groupe à l'ouverture d'un ticket. Voir [Notifications](index.php?fr/08_Module_Configuration/04_Notifications/01_Configurer_les_notifications.md "Une notification est l'association d'un événement pour un type donné avec un modèle. Une liste destinataire est créée à cet effet.").

Un mécanisme de **délégation** permet à un utilisateur de déclarer des incidents non pas pour lui mais pour un des membres de ce groupe.

    Exemple : 
    une secrétaire qui déclare les incidents pour les personnes de la direction.

Les notions de délégation et de superviseur se paramètres dans l'onglet "Utilisateurs" (voir ci-dessous).

L'association d'un utilisateur à un groupe est soit statique, c'est-à-dire réalisée à l'aide de l'interface de GLPI, soit dynamique quand celle-ci est déduite automatiquement de l'annuaire LPAP.

Un groupe est attaché à l'entité dans laquelle il est créé et peut ensuite être visible dans les sous-entités.

Depuis la liste des groupes, vous pouvez importer un groupe depuis un annuaire LDAP via ![image](docs/image/addUserLdap.png) si l'authentification externe est utilisée et que vous avez le droit "Mise à jour auth et sync" dans votre profil. L'affectation des utilisateurs dans les groupes sera automatique.index.php?fr/07_Module_Administration/07_Profils/01_Profils.md
Si plusieurs annuaires sont configurés, le choix de l'un d'entre eux est proposé, sinon le formulaire de recherche est directement accessible. En fonction des modalités de recherche des groupes (voir [Authentifier des utilisateurs à partir d'annuaires LDAP](config_auth_ldap.html "L'interface de GLPI avec les annuaires LDAP se configure depuis le menu Configuration > Authentification > Annuaire LDAP.")), un **filtre de recherche dans les groupes** et/ou **un filtre de recherche des utilisateurs** apparaissent : ceux-ci permettent d'affiner la liste affichée et prête à être importée. Si GLPI est utilisé en multi-entités, il est nécessaire de sélectionner l'entité de destination du groupe, ainsi que sa visibilité dans les sous-entités.

***Remarque :** l'import des groupes ne peut pas être filtré par entité. De plus, aucune fonction de synchronisation des groupes est disponible. Le seul moyen de rafraîchir la liste des membres d'un groupe depuis un annuaire est de resynchroniser les utilisateurs (voir [Importer des utilisateurs depuis une source externe](index.php?fr/07_Module_Administration/02_Utilisateurs/02_Importer_des_utilisateurs.md)).

> Important : dans le cas d'une migration depuis une version inférieure à GLPI 0.80, toute liaison manuelle réalisée préalablement sur un groupe provenant de l'annuaire LDAP sera perdue.


Les différents onglets
----------------------

-   **Onglet "Sous-groupes"**
    Permet d'ajouter un sous-groupe au groupe sélectionné et liste les sous-groupes existants. 
 
-   **[Aba "Itens utilizados"](index.php?pt/As_diversas_abas/Aba_Itens.md)**
    Liste les éléments pour lesquels le champ *Groupe* correspond à ce groupe. 
    La recherche peut être étendue ou sous-groupes ainsi qu'aux membres du groupe (champ *Utilisateur* de l'objet).

-   **[Aba "Itens gerados"](index.php?pt/As_diversas_abas/Aba_Itens.md)**
    Liste les éléments pour lesquels le champ *Groupe Technique* correspond à ce groupe.
     La recherche peut être étendue ou sous-groupes ainsi qu'aux membres du groupe (champ *Responsable technique* de l'objet).


-   **Aba "Liaison annuaire LDAP**
    Cet onglet n'apparait que si vous avez le droit "Mise à jour auth et sync" dans votre profil. Il regroupe les informations permettant à GLPI de retrouver le groupe et ses utilisateurs dans l'annuaire LDAP. 


-   **Aba "Usuários**
    Cet onglet permet d'ajouter un utilisateur à ce groupe en définissant s'il est *délégataire* et/ou *superviseur* de ce groupe.
    Il liste également les utilisateurs de ce groupe avec recherche possible via critère (délégataire ou superviseur) et également dans les sous-groupe du groupe courant.

-   **Aba "Notificações"**
    Liste des notifications pour lesquelles ce groupe est destinataire ou le superviseur de ce groupe.
    ![image](docs/image/notifGroupe.png)]


-   **[Aba "Tickets criados"](index.php?pt/As_diversas_abas/Aba_Tickets.md)**
    Liste les tickets dans lesquels le groupe est demandeur.


-   **[Aba "Histórico"](index.php?pt/As_diversas_abas/Aba_Historico.md)**


-   **[Aba "Todas"](index.php?pt/As_diversas_abas/Aba_Todas.md)**
     Pour un élément, toutes les informations sont affichées sur une seule page.


As diversas ações
-----------------------
-   **[Ajouter un groupe](index.php?pt/Les_différentes_actions/Créer_un_nouvel_objet.md)**
-   **[Voir un groupe](index.php?pt/As_diversas_acoes/Visualiser_un_objet.md)**
-   **[Modifier un groupe](index.php?pt/As_diversas_acoes/Modifier_un_objet.md)**
-   **[Excluindo um grupo](index.php?pt/As_diversas_acoes/Excluindo_um_objeto.md)**
-   **[Associando um item a um grupo](index.php?pt/As_diversas_acoes/Guia_Itens.md)**
-   **[Associando um ticket a um grupo](index.php?pt/As_diversas_acoes/Guia_Tickets.md)**
-   **[Transferência de um grupo para outra entidade](index.php?pt/As_diversas_acoes/Transferindo_um_objeto.md)**

--------
**Tópico principal :** [Administrando os controles de acesso](../glpi/access_control_intro.html "Essa parte descrever como administrar o sistema de controle de acesso que possibilita que cada usuário tenha acesso a um contexto de utilização específica.")

**Tópico principal :** [Módulo Administração](index.php?pt/07_Modulo_Administracao/01_Modulo_Administracao.md "O módulo Administração possibilita gerenciar os usuários, grupos, entidades, perfis, regras, dicionários e fornece ferramentas para a manutenção da aplicação").