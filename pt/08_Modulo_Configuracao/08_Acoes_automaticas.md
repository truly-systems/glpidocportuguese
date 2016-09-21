Configurando as ações automáticas
===================================

A ação automática **watcher** é uma ação que monitora a execução correta de outras ações automáticas. Se em um deles é encontrado em erro, uma notificação será enviadoa. Isso requer que o e-mail seja habilitado (veja [Configurando as notificacoes](index.php?pt/08_Modulo_Configuracao/04_Notificacoes/01_Configurando_as_notificacoes.md)")) ; destinatários podem ser configurados na notificação **Crontask Watcher** (veja [Gerenciando as notificações para entidade](index.php?pt/08_Modulo_Configuracao/04_Notificacoes/04_Notificacoes.md)).


As diversas abas
----------------------
-   **Ação automática**

    Para cada ação, é possível configurar:

    -   **A frequência da execução ** ;

    -   **O status** : permite desativar a ação ;

    -   **O modo de execução** :
        - GLPI : desencadeada pela navegação do usuário (por padrão durante a instalação padrão)
        - CLI  : mais robusto e estável, mas requer configuração do sistema ;

    -   **Os cronogramas de execução** : possibilita desativas certos tratamentos durante à noite, por exemplo ;

    -   **O tempo em dias da conservação dos diários** (de uma ação automática) : que são armazenados na base de dados.

    A interface também permite que você reconfigure a data de execução e forçar manualmente execução.

    Algumas ações automáticas podem ter parâmetros específicos, tais como e-mails, como o máximo de e-mails para enviar de cada vez.
    Da mesma forma plugins podem definir suas próprias ações automáticas.


-   **Estatísticas**
   Exibe informações sobre como executar esta tarefa (número de execuções, data, duração mínima, máxima, média e total)

-   **Diários**
    Lista as últimas execuções seguindo o parâmetro na guia *Ação automática* (veja acima).
    Um link na data de assinatura permite que os detalhes de uma implementação específica..


As diversas ações
-----------------------
-  **Desativação de uma ação automática** : alterar o status para Desativado
-  **Desbloquear uma ação automática** : em alguns casos, um caso automático pode ser bloqueado (ex. parar do banco de dados para backup enquanto a ação automática que controla repetições está ativa). Neste caso, basta clicar na cruz para a direita da palavra "execução"

-   **[Iniciar as ações automáticas a partir da linha de comando](../glpi/config_crontaskcli.html)**\
     O planejador de tarefas da GLPI pode ser chamado de manira externa, a partir da linha de comando, executando o arquivo front/cron.php.


--------
**Tópico principal :** [Módulo Configuração](index.php?pt/08_Modulo_Configuracao/01_Modulo_Configuracao.md "Módulo Configuração da GLPI")