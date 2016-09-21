Administrando os computadores
=====================

Dans la fiche d'un ordinateur, on trouve un certain nombre d'informations concernant le système d'exploitation (nom, version, service pack, numéro de série, product ID), les caractéristiques générales (fabricant, modèle, type, numéro de série), les informations de gestion (responsable technique, statut, localisation) et les usagers du poste (connus ou non dans GLPI).

D'autres champs sont informatifs, comme **Rede** (type de connexion au poste), et la **source de la mise à jour** qui est un intitulé indiquant d'où proviennent les mises à jour d'un poste (oui/non, Windows update, yum, apt, etc).

***Observações :***
*- No caso do uso da GLPI juntamente com uma ferramenta de inventário, informações diferentes sobre a importação também estarão disponíveis.*
*- Um computador pode ser tanto um servidor, um desktop ou um laptop. Para diferenciar, é possível usar o campo tipo
.*

**[Gerenciamento os modelos](index.php?pt/As_diversas_acoes/Administrando_os_modelos.md)**

As diversas abas
----------------------
-   **[Aba "Componentes"](index.php?pt/As_diversas_abas/Aba_Componentes.md)**
     Gerenciamento de componentes nos computadores

-   **Aba "Volumes"**
     Gerenciamento dos volumes nos computadores

    Un volume lié à un ordinateur est caractérisé par son nom, la partition physique, son point de montage et son système de fichiers ainsi que sa taille.

    Il est également possible de définir la taille restant libre sur le volume.

    ***Observação :*** *No caso da utilização de uma ferramenta de inventários de terceiros, essas informações podem ser automaticamente importadas e atualizadas.

-   **Aba "Softwares"**
     Gerenciamento dos softwares instalados nos computadores.

    Estas são classificadas por categorias e são caracterizados por seu nome e versão e o status.

    Se uma licença está associada com o uso deste software no computador, as informações serão apresentadas.

    Para instalar um software, selecione seu nome na lista drop-down e sua versão.

    ***Observaçõess :***
    *- O menu drop-down lista o software disponível na entidade.*
    *- A lista dos softwares disponíveis podem ser definidas na gestão de softwares. Veja [*Gerenciamento de softwares *](inventorio_software.html "Os softwares são gerenciados a partir do menu Parque > Softwares").*

    Para atribuir uma licença a esse computador, selecione o software e a licença desejada na lista drop-down.


-   **[Aba "Conexões"](index.php?pt/As_diversas_abas/Aba_Conexoes.md)**
     Gerenciamento das conexões

-   **[Aba "Portas de rede"](index.php?pt/As_diversas_abas/Aba_Portas_de_Rede.md)**
     Gerenciamento das portas de rede para os itens do inventário

-   **[Aba "Gestão"](index.php?pt/As_diversas_abas/Aba_Gestao.md)**
    Gerenciando as informações financeiras e administrativas

-   **[Aba "Contratos"](index.php?pt/As_diversas_abas/Aba_Contratos.md)**
    Gerenciando os contratos associados

-   **[Aba "Documentos"](index.php?pt/As_diversas_abas/Aba_Documentos.md)**

-   **Aba "Máquinas virtuais"**
    Dans cet onglet, on retrouve toutes les machines virtuelles associées à un hôte de virtualisation (host) ou l'hôte sur lequel une machine virtuelle est installée. Les informations disponibles pour une machine virtuelle associée sont son nom, son système de virtualisation, son modèle de virtualisation, l'état de la machine virtuelle, la mémoire allouée ainsi que le nom de la machine physique(hôte) et le nombre de processeurs logiques.

    GLPI réalise actuellement la liaison entre un hôte et une machine virtuelle en se basant sur l'identifiant unique (uuid). Dans certains cas, il arrive que l'uuid soit différent au sein de la machine physique et virtuelle, la liaison est alors impossible.

   Le seul moyen d'associer manuellement une machine virtuelle à une machine physique est d'attribuer à la machine virtuelle déclarée sur l'hôte et à la machine virtuelle dans GLPI un uuid identique.

   ***Observação :** En cas d'utilisation d'un outil d'inventaire tiers, ces informations peuvent être automatiquement importées et mises à jour.*

-   **[Aba "Tickets"](index.php?pt/As_diversas_abas/Aba_Tickets.md)**

-   **[Aba "Problemas"](index.php?pt/As_diversas_abas/Aba_Problemas.md)**

-  **[Aba "Links"](index.php?pt/As_diversas_abas/Aba_Links.md)**
     Para alguns itens, links externos são administrados a partir do menu ***Links externos***

-   **[Aba "Anotações"](index.php?pt/commontabs/As_diversas_abas/Aba_Anotacoes.md)**

-   **[Aba "Reservas"](index.php?pt/As_diversas_abas/Aba_Reservas.md)**
     Gestão des reservar para um objeto do inventário

-   **[Aba "Histórico"](index.php?pt/As_diversas_abas/Aba_Historico.md)**
     O histórico é visualizado a partir da guia *Histórico*

-   **[Aba "Depuração"](index.php?pt/As_diversas_abas/Aba_Depuracao.md)**
    Apenas se estiver conectado no modo de Depuração.

-   **[Aba "Todas"](index.php?pt/As_diversas_abas/Aba_Todas.md)**
     Para um item, todas as informações são exibidas em uma única página.

As diversas ações
-----------------------
-   **[Adicionando um computador](index.php?pt/As_diversas_acoes/Criando_um_novo_objeto.md)**
-   **[Visualizando um computador](index.php?pt/As_diversas_acoes/Visualizando_um_objeto.md)**
-   **[Modificando um computador](index.php?pt/As_diversas_acoes/Modificando_um_objeto.md)**
-   **[Excluindo um computador](index.php?pt/As_diversas_acoes/Excluindo_um_objeto.md)**
-   **[Associando um documento a um monitor](index.php?pt/As_diversas_acoes/Lier_un_document_à_un_objet.md)**
-   **[Associando um contrato a um monitor](index.php?pt/As_diversas_acoes/Lier_un_contrat_à_un_objet.md)**
-   **[Transferindo un monitor para outra entidade](index.php?pt/As_diversas_acoes/Transferindo_um_objeto.md)**
-   **Instalação de um software licenciado em um computador**
    A partir da aba *Softwares*, ajouter une licence en choisissant le nom du logiciel suivi du nom de la licence.
    Depuis les actions de masse du tableau récapitulatif, choisissez **Instalação**.
    ***Atenção*** : un logiciel ne peut être installé que si sa licence possède une version d'achat et/ou d'utilisation.

------------
**Tópico princiapl :** [Módulo Parque](index.php?pt/03_Modulo_Parque/01_Module_Parque.md "Módulo Parque da GLPI")
