Aba Validações
==================

Um objeto (ticket ou uma alteração) podem necessitar de validação, por exemplo, para evolução de um hardware, tal como uma mudança do computador ou no monitor. Esse pedido de validação só é possível se você tiver autorização em seu perfil.

Após clicar em **Enviar uma solicitação de validação**, deve-se digitar o tipo do validador (usuário ou grupo) e seu nome. Para os grupos também devem ser selecionados qual grupo receberá o pedido de validação (não são todos listados como tendo o direito de validar).

Para validar o pedido, o validador deve abrir a aba **Validação** do objeto, e em seguida clica na linha correspondente ao pedido de validação. Selecionar **Aceitar** ou **Recusar**. No caso da recusa é obrigatório o preenchimento de um comentário.

No caso de uma solicitação de validação múltipla, a porcentagem de validação é necessária. Três casos são possíveis :

- 0% : O primeiro usuário que aceita ou rejeita a validação  (Status global da validação).

- 50% : A maioria vence. Exemplo : 3 validações solicitadas, 2 recusadas implica na recusa do ticket.

- 100% : Todos os validadores devem validar ou rejeitar a validação para que o estado geral da validação seja alterado.

Validação para um ticket
-------------------------
Quando uma solicitação de validação é criada, o ticket toma o status ** ** validação pendente em seu campo **Validação**.

O pedido de validação pode também ser criado diretamente na abertura do ticket através da interface padrão ou um [regra da profissão](index.php?pt/07_Modulo_Administracao/05_Regras/04_Regras_da_profissao_para_os_tickets.md).


Para validar o pedido, o validador pode clicar no ticket na home da GLPI (aba **Exibição pessoal**, parte **Seus tickets para validação**), ou vá para o menu **Assistência > Ticket** e clique no ícone ![image](docs/image/menu_showall.png) que aparece no breadcrumb.


Validação para uma alteração
-----------------------------

***Observação:** A validação não é um processo de bloqueio, é apenas informativo. Mas se um técnico pode tratar uma mudança que está aguardando ser validade. No entanto, se o técnico muda o status para Aplicada, Aberta ou Fechada, ou que adiciona uma solução na alteração aguardando uma validação, um aviso será exibido.*


-------
**Tópico principal :** [Administrando os tickets](index.php?pt/04_Modulo_Assistencia/06_Tickets/03_Administrando_os_tickets.md "Os tickerts são gerenciados a partir do menu Assistência > Tickets")

**Tópico principal :** [Administrando as alterações](index.php?pt/04_Modulo_Assistencia/09_Alteracoes.md "As alterações são gerenciadas a partir do menu Assistência > Alterações")