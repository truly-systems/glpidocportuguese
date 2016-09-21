A interface padrão e a interface simplificada
==============================================

De acordo com as autorizações dadas, o usuário pode usa a **interface padrão** ou a **interface simplificada**.

A interface padrão
--------------------

Essa é a interface principal da aplicação. O conjunto de módulos está disponível.

Figura 1. Menu da interface padrão
![image](docs/image/interfaceStandard.png)

A homepage da **interface padrão** apresenta uma visão geral para acesso rápido dos ativos (chamadas, notas, agendas, contratos...).

É dividido em 4 modos de visualização :

-   **Pessoal** mostra chamados em aberto, recusados, em processo, aprovados (dos quais o usuário conectado for o requerente) ou aqueles em que houve interação do usuário como validador ou técnico (aguardando validação, em curso, em encerramento, pendente). Esse ponto de vista também oferece o cronograma e as avaliações disponíveis dos problemas atuais.
-   **De grupo** oferece as mesmas informações sobre as chamadas e os problemas que a pessoal, mas tendo como referência os grupos em que ele pertence. De acordo com o  perfil do usuário, ele terá acesso ou não aos chamados para os grupos em que é requerente. 

***Observação :*** *Para as visualizações Pessoal e de Grupo, somente seus displays exibirão suas tabelas contendo suas informações.*

-   **Global** fornece estatísticas sobre os chamados e os problemas de acordo com suas disponsições e seus contratos em função de sua data de validade. Elle propose également la vue des derniers ajouts d'objets dans GLPI. Próximo a configuração usada, novos chamados podem ser apresentados nessa guia.
-   **Feed RSS** oferece o conteúdo do RSS definido (veja [Gerenciamento do feed RSS](index.php?pt/06_Modulo_Ferramentass/04_Feed_RSS.md "Os feeds RSS são gerenciados a partir do menu Ferramentas > Feed RSS")).

Figura 2. Bem vindo ![image](docs/image/vuesStandard.png)

***Observação :*** *Duas mensagens de segurança podem ser exibidas quando o usuário faz o login pela primeira vez, apóis o procedimento de instalação.
A primeira mensagem solicitará alteração das senhas das contas criadas pelo padrão GLPI.
A segunda é para remover o diretório de instação glpi.

Figure 2. Segurança ![image](docs/image/messageAccueil.png)
Como pode perceber essas mensagens permanecem.*

Figura 3. Menu da interface padrão personalizada
![image](docs/image/GLPI-Interface%20personnalisee.png)

Interface présentée à un utilisateur utilisant l'interface padrão, mais n'ayant aucun droit de configuration et de consultation de l'inventaire. O nome de menus présents na barra de navigação
est ainsi limité.

A interface simplificada
----------------------

Essa interface é mais restrita. Ela é destinada a usuários com autorizações de uso muito restritas: helpdesk self-service. A quantidade de menus disponíveis é restrita. Na configuração padrão, um usuário pode, a partir dessa interface, apenas criar os tickets fazer as reservas, visualizar as anotações ou os feeds RSS publicados (ou criar as anotações ou feeds privados) e consultar as perguntas mais frequentes. A página inicial fornece o número de tickets de acordo com os seus status e os tópicos mais populares e mais recentes do FAQ.

Figura 4. Menu da interface simplificada
![image](docs/image/interfaceSimplifiee.png)

***Observação :*** *A escolha da interface padrão assim como a dos diversos módulos pode ser definida nos perfis. Veja [Administrando os perfis dos usuários](administrar_perfil.html "Na GLPI, administrar o perfil dos usuários é feito  partir do menu Administração > Perfis.").*

---------
**Tópico principal :** [Utilização GLPI](index.php?pt/02_Primeiros_passos_com_GLPI/03_Utilizacao_GLPI/01_Utilizacao_GLPI.md)
