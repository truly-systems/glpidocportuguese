Transferindo um item uma entidade para outra
============================================

Avec la notion d'entités vient la possibilité de définir des profils de transfert pour les mutations d'éléments entre entités.

Cette fonctionnalité permet notamment de passer d'un GLPI mono entité à un GLPI multi-entités en utilisant les transferts.

Comment faire un transfert :

1.  Utiliser un profil qui a le droit de faire des transferts (Administration > Profils > Administration --> Droit le Lecture sur Transférer) ;

2.  Configurer les actions faites par le transfert ([Administration > Règles --> **Transférer](index.php?fr/07_Module_Administration/05_Règles/01_Gérer_les_règles.md)) ;

3.  S'assurer que le profil qui va effectuer le transfert a une visibilité sur l'entité cédante et sur l'entité prenante (le plus simple est d'utiliser un profil récursif depuis l'entité racine) ;

4.  Se positionner sur l'Entité racine (Voir Tous) ;

5.  Depuis la liste des objets, sélectionner l'élément à transférer ;

6.  Choisir **Ajouter à la liste de transfert** et **Valider** ;

7.  Dans **Mode de transfert**, choisir un profil de configuration du transfert (créé en point 2) ;

8.  Sélectionner l'entité dans laquelle sera transféré l'élément ;

9.  Cliquer sur **Transférer** ;

10. Vérifier dans la nouvelle entité que le matériel s'y trouve bien.

***Remarque :** si un élément lié n'existe pas dans la nouvelle entité, il sera automatiquement créé si le profil de transfert demande de le conserver.
Exemple : transfert d'un ordinateur avec un fournisseur défini dans les informations financières. Si ce fournisseur n'existe que dans l'entité cédante, il sera créé dans l'entité prenante.
Par contre un fournisseur défini dans l'entité racine en récursif ne sera pas recréé.*

>Avertissement : Le lieu et le groupe seront à adapter pour la nouvelle entité.

---------
**Tópico principal :** [Administrando os computadores](index.php?pt/03_Modulo_Parque/02_Computadores.md "Os computadores são administrados a partir do menu Parque > Computadores")

**Tópico principal :** [Administrando os monitores](index.php?pt/03_Modulo_Parque/03_Monitores.md "Os monitres são gerenciandos a partir do menu Parque > Monitores")

**Tópico principal :** [Administrando os softwares](index.php?pt/03_Modulo_Parque/04_Softwares/01_Softwares.md "Os softwares são gerenciados a partir do menu Parque > Software")

**Tópico principal :** [Administrando os equipamentos de rede](index.php?pt/03_Modulo_Parque/05_Equipamentos_de_rede.md "Os equipamentos de rede são gerenciados a partir do menu Parque > Rede")

**Tópico principal :** [Administrando os periféricos](index.php?pt/03_Modulo_Parque/06_Perifericos.md "Os periféricos são administrandos a partir do menu Parque > Periféricoss")

**Tópico principal :** [Administrando as impressoras](index.php?pt/03_Module_Parque/07_Impressoras.md "As impressoras são geradas a partir do menu Parque > Impressoras")

**Tópico principal :** [Administrando os cartuchos](index.php?pt/03_Modulo_Parque/08_Cartuchos.md "Os cartuchos da GLPI, características e uso")

**Tópico principal :** [Administrando os consumíveis](index.php?pt/03_Modulo_Parque/09_Consumíveis.md "Os consumíveis são gerenciandos a partir do menu Parque > Consumíveis")

**Tópico principal :** [Administrando os telefones](index.php?pt/03_Modulo_Parque/10_Telefones.md "Os telefones são gerenciados a partir do menu Parque > Telefones ;")

**Tópico principal :** [Administrando os tickets](index.php?pt/04_Modulo_Assistencia/06_Tickets/03_Administando_os_tickets.md "Os tickets são gerenciados a partir do menu Assistência > Tickets")

**Tópico principal :** [Administrando os problemas](index.php?pt/04_Modulo_Assistencia/08_Problemas.md "Os problemas são gerenciados a partir do Assistência > Problemas")

**Tópico principal :** [Administrando os provedores](index.php?pt/05_Modulo_Gestao/03_Provedores.md "Os provedores são gerenciados a partir do menu Gestão > Provedores")

**Tópico principal :** [Administrando os contatos](index.php?pt/05_Modulo_Gestao/04_Contatos.md "Os contatos são gerenciados a partir do menu Gestão > Contatos")

**Tópico principal :** [Administrando os contratos](index.php?pt/05_Modulo_Gestao/05_Contratos.md "Os contratos são gerenciados a partir do menu Gestão > Contratos")

**Tópico principal :** [Administrando os documentos](index.php?pt/05_Modulo_Gestão/06_Documentos.md "Os documentos são gerenciados a partir do menu Gestão > Documentos")

**Tópico principal :** [Administrando os grupos](index.php?pt/07_Modulo_Administracao/03_Grupo.md "Os grupos são gerenciados a partir do menu Administração > Grupos")