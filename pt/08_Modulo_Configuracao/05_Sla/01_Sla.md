Configurando os SLAs
===================

Um SLA (Service Level Agreement ou acordo de nível de serviço service) é a formalização de um contrato negociado entre o ServiceDesk e o cliente definindo o nível de serviço esperado e, portanto, o tempo máximo para resolver um incidente ou solicitação (D+1, H+4...).

Os SLAs são associados aos tickets através de mecanismos de regras dos tickets (veja [Regras de negócio para os tickets](index.php?pt/07_Modulo_Administracao/05_Regras/04_Regras_de_negócio_para_os_tickets.md "Ao criar um bilhete, um mecanismo usado para alterar os atributos do ticket de meneira automática.")).
A associação do SLA com ticket permite o cálculo automático da sua data de vencimento. Muitos SLAs podem ser definidos e atribuídos de acordo com critérios específicos.

    Por exemplo, o SLA 1 será afetado se o bilhete for atribuído a uma categoria específica e SLA 2 para outras categorias.

>ATENÇÃO :
>- Se um SLA é atribuído manualmente à a abertura do ticket (pelo usuário ou através de um modelo de ticket), regras de negócio não pode redefini-lo.
>- Um SLA pode ser afetado posteriormente. Na atribuição da mesma, ela será completamente reproduzido e as ações associadas aos níveis de escalonamento anteriores serão executadas.

Um agenda pode ser associado com um SLA (veja [Configurando os títulos](index.php?pt/08_Modulp_Configuracao/02_Titulos/01_Titulos.md "Os títulos são configurados a partir do menu Configuração > Títulos")).
Pelo padrão, nenhuma agenda está associada e os cálculos são feitos em uma base de trabalho de 7 dias em 7 e 24 horas em 24. Também é possível utilizar a agenda associada com o ticket (isto é, a da entidade a qual está vinculada o ticket).

>Importante : Se a resolução de tempo máximo é expresso em dias, todos os cálculos serão em dias (D + 1, d + 4, por exemplo), tendo em conta o calendário para determinar a semana. Se a resolução de tempo máximo é expresso em horas ou minutos, os cálculos serão feitos depois tendo em conta as horas de abertura

    Por exemplo para um SLA H+4 com um cronograma que define os horários de abertura das 8h às 18h, um ticket aberto às 16h terá uma data de vencimento no dia seguinte às 10h.

A aprovação do ticket no status pendente deixa SLA em dormência. Se o bilhete continua pendente por 3 horas, por exemplo, a data de vencimento será adiada 3 horas.

As diversas abas
----------------------

-   **[Aba "Níveis de escalonamento"](index.php?pt/08_Modulo_Configuracao/05_Sla/02_Niveis_de_escalonamento.md)**
    Permite adicionar um novo nível de escalonamento a esse SLA e lista os diferentes níveis já definidos com com seus critérios e ações.
    ![image](docs/image/NiveauSla.png)
    Para alterar um nível basta clicar sobre o seu nome.


-   **Aba "Regras"**
    Lista as regras de negócio relacionadas a esse SLA.

-   **[Aba "Tickets"](index.php?pt/As_diversas_abas/Aba_Tickets.md)**
     Lista os bilhetes atribuídos a esse SLA.

-   **[Aba "Todas"](index.php?pt/As_diversas_abas/Aba_Todas.md)**
     Para um item, todas as informações são exibidas em uma única página.


As diversas ações
-----------------------
-   **[Adicionando um sla](index.php?pt/As_diversas_acoes/Criando_um_novo_objeto.md)**
-   **[Visualizando um sla](index.php?pt/As_diversas_acoes/Visualizando_um_objeto.md)**
-   **[Alterando um sla](index.php?pt/As_diversas_acoes/Alterando_um_objeto.md)**
-   **[Excluindo un sla](index.php?pt/As_diversas_acoes/Excluindo_um_objeto.md)**
-   **Adicionar um nível de escalonamento**
    Essa ação é feita via guia *Níveis de escalonamentos*



------
**Tópico principal :** [Módulo Configuração](index.php?pt/08_Modulo_Configuracao/01_Modulo_Configuracao.md "Módulo Configuração da GLPI")