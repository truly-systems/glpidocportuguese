Níveis de escalonamento
==================

Os níves de escalonamento podem ser definidos dentro de um SLA. Cada nível aciona ações automáticas para a resolução do ticket tão rapidamente quanto possível. Um nível é acionado antes ou depois da data de vencimento do SLA de acordo com o tempo definido.

    Por exemplo, um dia antes do prazo, o ticket é atribuído ao suporte nível e sua prioridade passa a alta.

Os níveis de escalonamento podem ser condicionados por critérios de acionamento. Independentemente, os níveis serão acionados se os critérios forem definidos, eles serão checados antes da aplicação dos níveis de escalonamento.

     Por exemplo, se um dia antes da data de vencimento você desejar enviar um lembrete para o administrador e o ticket estiver no estado de *Novo*, deve ser definido como critério  `Status é Novo`.


As diversas abas
----------------------

-   **Aba "Critérios"**
    Permite adicionar um novo critério e lista os critérios já definidos para esse nível de escalonamento.

-   **Aba "Ações"**
    Permite adicionar uma ação que será executada se o critério definido for atendido.
    Ela também lista as ações já definidas para este.

-   **[Aba "Histórico"](index.php?pt/As_diversas_abas/Aba_Historico.md)**
     O histórico é visualizado a partir da guia *Histórico*

-   **[Aba "Depuração"](index.php?pt/As_diversas_abas/Aba_Depuracao.md)**
    Apenas se estiver conectado no modo Depuração.

-   **[Aba "Todas"](index.php?pt/As_diversass_abas/Aba_Todas.md)**
     Para um item, todas as informações são exibidas em uma página.


As diversas ações
-----------------------
-   **Adicionando um novo nível de escalonamento]**
    Essa ação será feita via guia *Níveis de escalonamento* de um SLA

------
**Tópico principal :** [SLA](index.php?pt/08_Modulo_Configuracao/05_Sla/01_Sla.md "Administrando os SLA")

**Tópico principal :** [Módulo Configuração](index.php?pt/08_Modulo_Configuracao/01_Modulo_Configuracao.md "Módulo Configuração da GLPI")