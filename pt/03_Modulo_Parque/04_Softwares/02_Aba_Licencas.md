Administrando as licenças
===================

A licença do software é um direito de usar esse software. Ele tem um número e campos específicos. O nome indica o nome comercial da licença. A versão de compra é comprado quando a versão de uso corresponde à versão do software realmente instalado. Ambas as versões podem ser totalmente diferente, mas deve refletir o existente.

2 versões de um software foram compradas, mas apenas um está realmente instalada.

Le type est la nature du droit d'utilisation. Le type OEM est le seul type configuré par défaut dans GLPI. Voir [Configurer les intitulés](index.php?fr/08_Module_Configuration/02_Intitulés/01_Intitulés.md "Les intitulés se configurent depuis le menu Configuration > Intitulés") pour définir les types.

Le nombre indique le volume d'installation qui pourra être fait avec cette licence. Cela peut être un nombre d'utilisateurs (licence flottante), un nombre d'installations (licence multiple), un nombre illimité (licence site), etc. Il est possible d'affecter la licence à un ou plusieurs ordinateurs correspondant. par exemple si la licence est de type OEM.

L'expiration est la date limite donnant droit d'utilisation de la licence. La dépassement de cette date peut déclencher une notification. Voir [Configuration des notifications](index.php?fr/08_Module_Configuration/04_Notifications/01_Configurer_les_notifications.md "Les notifications se configurent depuis le menu Configuration > Notifications ;").

***Conseil :*** Ceci est configurable par entité dans le menu ***Configuration > Notifications*** pour définir les modèles et destinataires utilisés et dans le menu ***Configuration > Entité*** pour activer ou non cette fonctionnalité, définir les valeurs par défaut et une anticipation de l'envoi de la notification si besoin.

***Remarque :** Les licences expirées ne comptent plus dans les totaux des licenses disponibles.*

Il est possible de lier des contrats à des licences (Voir [Gérer les contrats](index.php?fr/05_Module_Gestion/05_Contrats.md "Les contrats sont gérés depuis le menu Gestion > Contrats")).

***Remarque :** Lors de l'activation des informations financières d'une licence, les données sont initialisées avec les renseignements saisis dans les informations financières du logiciel (qui n'est qu'un modèle).*


As diversas abas
----------------------
-   **Onglet "Résumé"**
    Affiche un tableau listant le nombre d'ordinateurs utilisant cette licence
    ![image](docs/image/resumeLicence.png)


-   **Onglet "Ordinateurs"**
    Fournit un tableau listant les ordinateurs utilisant cette licence avec notamment, le nom de l'ordinateur, son numéro de série, son numéro d'inventaire, son lieu d'affectation, son statut, son groupe et son utilisateur.
    Des actions de masse sont proposées à ce niveau (si droit sur les ordinateurs), pour supprimer l'utilisation de cette licence sur l'ordinateur sélectionné ou pour affecter une autre licence du même logiciel à cet ordinateur (action Déplacer).

-   **[Aba "Gestão"](index.php?pt/As_diversas_abas/Aba_Gestao.md)**
    Administrando as informações financeiras e administrativas

-   **[Aba "Contratos"](index.php?pt/As_diversas_abas/Aba_Contratos.md)**
    Administrando os contratos associados

-   **[Aba "Documentos"](index.php?pt/As_diversas_abas/Aba_Documentos.md)**

-   **[Aba "Histórico"](index.php?pt/As_diversas_abas/Aba_Historico.md)**
    O histórico é visualizado a partir da aba *Histórico*

-   **[Aba "Depuração"](index.php?pt/As_diversas_abas/Aba_Debupuracao.md)**
    Uniquement si vous êtes connecté en mode Debug.

-   **[Aba "Todas"](index.php?pt/As_diversas_abas/Aba_Todas.md)**
     Pour un élément, toutes les informations sont affichées sur une seule page.

As diversas ações
-----------------------
- **Visualiser le détail d'une licence d'un logiciel**
  Depuis le menu **Parc > Logiciels** cliquer sur le nom de la licence dans l'onglet *Licences*.
- **Supprimer l'utilisation d'une licence par un ordinateur**
  Voir onglet *Ordinateurs* ci-dessus
  [Voir onglet *Logiciels* d'un ordinateur](index.php?fr/03_Module_Parc/04_Logiciels/01_Logiciels.md)
- **[Associer un document à une licence](index.php?fr/Les_différentes_actions/Lier_un_document_à_un_objet.md)**
- **[Associer un contrat à une licence](index.php?fr/Les_différentes_actions/Lier_un_contrat_à_un_objet.md)**

-------
**Sujet parent :** [Module Parc](index.php?fr/03_Module_Parc/01_Module_Parc.md "Module Parc de GLPI")
**Sujet parent :** [Onglet Logiciels](index.php?fr/03_Module_Parc/04_Logiciels/01_Logiciels.md "Gestion des logiciels")
