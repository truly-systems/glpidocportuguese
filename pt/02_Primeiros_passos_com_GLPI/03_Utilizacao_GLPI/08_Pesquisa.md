Busca de informações na GLPI
=====================================

GLPI dispõe de um mecanismos de busca que permite a exibição de um conjunto de elementos que correspondem a determinados. As listas propostas são paginadas. A presente barra de navegação na parte superior e inferior da lista permite que você defina o número de itens exibidos por página e navegar entre as páginas

Um mecanismos de busca global também está disponível.

Estas listas de itens com dois apêndices apresenta: exportação e grandes mudanças.

Finalmente, um sistema completo de de favoritos permite que você salve buscas favoritas.

Efetuando uma busca básica
-------------------------------

A busca básica permite várias pesquisas parametrizadas e ordenadas em um tipo de inventário.

De acordo com os dados em que a pesquisa é feita, os seguintes operadores podem ser oferecidos: contém, é, não é, antes, depois.

A busca por datas permite especificar uma data (Especificar uma data) ou definir em relação a data atual (Atualmente, + ou - X hora(s), data(s), mês ou ano(s)). Também é possível especificar uma busca antes ou depois de uma determinada data, bem como os intervalos pré-definidos.

Pour les intitulés, il est possible de rechercher une valeur donnée (est). Si les intitulés peuvent être visibles dans les sous-entités, les choix *sous* et *pas sous* apparaissent.

    Chercher les ordinateurs possédant plus de 1024 Mio de mémoire et plus de 80% d'espace disque libre :

    - Mémoire (Mio)    contient    >1024 

    - ET (recherche simple) Volumes > Pourcentage libre    contient    >80 .

***Observação :*** Uma vez que os critérios forem definidos, a pesquisa é iniciada pressionando o botão Buscar.

Efetuando uma pesquisa com multi-critérios
--------------------------------------

A pesquisa multi-critérios pode refinar a pesquisa, levando-a a buscar outros tipos de objetos com a adição de critérios de pesquisa globais. Este tipo de pesquisa é obtida pela adição de critérios com o "+" com um triângulo vermelho no fundo.

    Chercher les ordinateurs possédant plus de 1024 Mio de mémoire et plus de 80% d'espace disque libre, attachés à un moniteur de 17 pouces et
    ayant le logiciel LibreOffice installé :

    -   Mémoire (Mio)    contient    >1024

    -   ET (recherche simple)    Volumes > Pourcentage libre    contient    >80
    -   ET (multi-critère) pour lesquels Moniteur > Taille      contient    17
    -   ET (multi-critère) pour lesquels Logiciels > Nom        contient    LibreOffice.

Itens da cesta
--------------------------

Alguns elementos da GLPI podem ser descartados. Para restauração ou exclução definitiva, clique no ícone da lixeira. Para retornar à exibição dos elementos ativos, clique novamente no ícone.

Efetuando uma busca avançada
-------------------------------

Exemplos de operadores de busca:

***NULL***
  ~ rechercher les enregistrements ayant tel champ vide avec un champ date : <nombre_de_mois ou >nombre_de_mois
  ~ rechercher les matériels avec un délai correspondant au nombre de     mois
  ~ rechercher les ordinateurs vieux de 5 ans : Date d'achat contient <-60.
 
***^123***
  ~ rechercher les enregistrements contenant 123 en début de champ.
   
  > Attention, il faut taper ^ puis la barre d'espace puis le premier caractère.

***^Windows***
  ~ rechercher les enregistrements contenant Windows 2000, Windows XP mais pas avec Windows.

***123$***
  ~ rechercher les enregistrements contenant 123 en fin de champ

***^123$***
  ~ rechercher les enregistrements contenant uniquement le texte 123.

***deux critères de recherche liés par l'opérateur AND NOT***
  ~ rechercher les enregistrements ne correspondant pas à un critère (différent de).

***Type = vide (pour tout sélectionner) AND NOT Type = Laptop***
  ~ rechercher tous les ordinateurs qui ne sont pas des laptop, c'est-à-dire Type différent de Laptop.
    Figure 1. Exemple de recherche "différent de"
    ![image](../image/searchexample.png)
[Année]-[Mois]-[Jour] (AAAA-MM-JJ)
  ~ rechercher par date
 
\\
  ~ Pour des questions de sécurité, l'opérateur \\ n'est pas utilisable.

Exporter le résultat d'une recherche
------------------------------------

L'export du résultat de la recherche aux formats pour tableur SLK ou CSV, ou au format PDF peut être réalisé sous deux formes différentes :
la *page courante* exporte uniquement les données affichées à l'écran (par exemple les 10 premiers résultats sur 200) alors que *toutes les pages* exporte l'ensemble des résultats de la recherche.

Le format SLK est exploitable par de nombreux tableurs. Les champs trop longs seront tronqués en cas d'utilisation d'un logiciel qui ne respecte pas totalement les standards. Il est préférable dans ce cas d'utiliser les exports au format CSV.

Si les données exportées en format CSV sont importées dans le logiciel Microsoft Excel, les caractères accentués peuvent ne pas s'afficher correctement. Ce logiciel semble rencontrer des difficultés avec les
données encodées en UTF-8.

Effectuer des actions massives
------------------------------

Un système d'actions massives est intégré au moteur de recherche. Il permet d'effectuer des modifications sur tous les éléments sélectionnés (**Mettre à la corbeille**, **Supprimer définitivement**, **Restaurer**,
**Connecter** / **Déconnecter**, **Installer**, **Mettre à jour des champs**, **Ajouter un document ou un contrat**, **Activer les informations financières et administratives**, **Transférer** ou **Synchroniser**). Pour l'utiliser il suffit de sélectionner les éléments pour lesquels on veut réaliser une action puis de cliquer sur le bouton **Actions** disponible en haut et en bas de la liste. Ensuite, une fois le type d'action sélectionné, des options sont éventuellement présentées, ainsi qu'un bouton de validation.

Les résultats des actions ainsi que des messages d'information sont présentés à la fin de l'exécution de l'ensemble des actions.

***Remarques :*** 
*- Vous trouverez dans les entêtes du tableau (en haut et en bas) une case à cocher vous permettant de sélectionner ou dé sélectionner tous les éléments de la liste.*
*- Un système d'actions similaire est disponible dans certaines listes présentes au sein des objets eux même.
  Le fonctionnement est identique à celui exposé ici.*


> ATTENTION :
> Le nombre d'éléments manipulables simultanément est limité par les valeurs de *max_input_vars* ou de *suhosin.post.max_vars* de votre configuration php. Vous pourrez donc avoir un message indiquant que les
modifications massives sont désactivées. Il vous suffit d'augmenter les valeurs de votre configuration PHP ou réduire le nombre d'éléments que vous afficher.

Recherche rapide
----------------

Figura 2. Campo de busca rápida
![image](../image/quicksearch.png)

Cet outil se trouvant en haut à droite de l'écran GLPI permet la recherche d'une chaîne de caractères simultanément sur les éléments suivants : Ordinateur, Moniteur, Logiciel, Matériel Réseau, Périphérique, Imprimantes, Téléphones, Contacts, Fournisseurs et Documents.

***Observação :*** *La recherche ne se fera que sur les champs affichés par défaut pour chacun des éléments cités ci-dessus.*

Os favoritos
-----------------

GLPI pode registrar de maneira pessoal ou pública as buscas que os usuários desejam manter e realizar novamente.

***Observações :***
*-  Les marques pages personnels peuvent être ordonnés en fonction des besoins de l'utilisateurs alors que les marques pages publics utilisent un tri automatique.*
*- La recherche doit au préalable être exécutée via le bouton **Rechercher** avant de pouvoir enregistrer le marque-page.*

Um bookmark público só pode ser alterado pela entidade na qual ele foi criado. Somente as pessoas com permissão escrita le droit d'écriture sur les marques-pages public sont habilités à en créer et à modifier ceux qui existent.

De plus un marque-page peut être défini comme marque-page par défaut, et sera donc chargé à chaque démarrage de GLPI. Rééditer le marque-page et le positionner à oui sur **Vue par défaut**.

Para alterar um bookmark (favorito), escolher o bookmark desejado e clicar no ícone **Modificar bookmark**
![image](../image/bookmark.png) depuis le deuxième fil d'ariane.

Si les gestionnaires de parc ont besoin de connaître régulièrement l'ensemble des machines tournant sous GNU/Linux avec plus de 512 Mio de mémoire, alors créer un marque-page public.

No caso do uso do GLPI por multi-entidades, para dispor aos usuários as solicitações pré-definidas, que não podem ser modificadas, é possível criar bookmarks (favoritos) públicos e visíveis para cada sub-entidades.

----------
**Tópico Principal :** [Utilização do GLPI](index.php?pt/02_Primeiros_passos_com_GLPI/03_Utilizacao_GLPI/01_Utilizacao_GLPI.md)
