Configurando os controles
========================

GLPI dispose d'un mécanisme permettant de réaliser des contrôles avant l'insertion en base de données d'un objet.

Cette fonctionnalité permet de rendre l'ajout ou la mise à jour d'un objet d'inventaire impossible si un autre possède déjà une valeur identique. Ce mécanisme s'applique sur les ajouts manuels, mais aussi
sur l'import depuis une source externe comme depuis un outil d'inventaire.

As diversas abas
----------------------
-   **Onglet "Unicité des champs"**
     L'unicité est définie par un nom, un type d'objet sur lequel elle se rapporte, une liste de champs ainsi que les actions en découlant (refus d'injection en base, envoi de notification). 
     Le champ sous-entité permet d'indiquer si les critères d'unicité s'appliquent à tout GLPI ou
seulement à l'entité dans laquelle l'unicité est créée.

     Il faut noter que la sélection de plusieurs champs vérifie l'unicité du n-uplet et non chaque champ individuellement.

     Pour un ordinateur, le critère d'unicité global est le numéro de série. 
     Si l'on tente d'enregistrer, quelque soit l'entité un autre ayant le même numéro de série, l'insertion est refusée et un message d'erreur indique l'élément déjà présent en base. Par contre, si un utilisateur insère un ordinateur sans numéro de série, alors aucune vérification sur l'unicité ne sera effectuée.

     Les critères ajoutés dans les listes noires seront ignorer lors du calcul d'unicité. Voir [Configurer les intitulés](index.php?pt/08_Modulo_Configuracao/02_Titulos/03_Titulo_Geral.md "A parte Geral dos Títulos")
.
-   **Aba "Duplicata"**
    Este guia lista todos os valores correspondentes aos critérios que atualmente estão duplicados na base da GLPI, possivelmente, para cada link para o perfil do objeto.

-   **[Aba "Histórico"](index.php?pt/As_diversas_abas/Aba_Historico.md)**
     O histórico é visualizado a partir da aba *Histórico*

-   **[Aba "Depuração"](index.php?pt/As_diversas_abas/Aba_Depuracao.md)**
    Apenas se estiver conectado no modo de depuração.

-   **[Aba "Todas"](index.php?pt/As_diversas_abas/Aba_Todas.md)**
     Para um item, todas as informações são exibidas em uma única página.

--------
**Tópico principal :** [Módulo Configuração](index.php?pt/08_Modulo_Configuracao/01_Modulo_Configuration.md "Módulo Configuração da GLPI")

