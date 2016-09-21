Aba Sistema
==============

Essa guia permite visualizar um resumo das informações sobre as capacidade do servidor web e definir as informações de log e erros do registro assim como a política de aplicação de senhas.

![image](docs/image/sytemConfig.png)

- **Níveis de log** : cada evento interno interno da aplicação é registrado nos logs que são visíveis na seção [Administração > Log](index.php?pt/07_Modulo_Administracao/10_Log.md). Nessa guia, é possível reduzir o grau de prolixidade desses logs.

- **Marcadores em arquivos (SQL, e-mail, ação automática ...)** : é possível registrar alguns eventos adicionais em arquivos (SQL, notificações, ação automática). Esses arquivos estão disponíves em files/_log.

- **Número máximo de ações automáticas simultâneas (execução CLI)** : quando as ações automáticas são definidas, é possível determinar que estas irão ser realizadas por um sistema externo a GLPI (CLI). Padronizadamente ele executa essas ações uma a uma. É possível aumentar o número de execuções lançadas simultaneamente.

- **Replicar MySQL** : no caso de se utilizar uma réplica MySQL, uma vez ativada, um novo guia é adicionada à interface.

![image](docs/image/systemMdp.png)

Uma política de senha pode ser implementada para obter informações ou bloquear. Os critérios utilizados são o comprimento da senha, a presença ou ausência de números, letras minúsculas, maiúsculas e símbolos.

![image](docs/image/systemMaintenance.png)

Um modo de manutenção é ativado para permitir uma operação técnica como uma atualização, por exemplo. Uma mensagem de manutenção é configurável. No modo manutenção, você ainda pode acessar via GLPI `index.php?skipMaintenance=1`.

![image](docs/image/systemProxy.png)

No caso da utilização de um proxy, é necessário indicar as informações das últimas configurações para permitir à GLPI que verifique se há versões mais recentes.

![image](docs/image/systemInfo.png)

Siga a lista de todas as informações necessárias na tela da GLPI para relatar o mau funcionamento para a equipe de desenvolvimento GLPI. Basta copiar/colar o texto no fórum: o formato já é suportado.

-----
**Tópico principal :** [Configurando as definições centrais](index.php?pt/08_Module_Configuracao/06_Geral/01_Configurando_as_definicoes_centrais.md)
