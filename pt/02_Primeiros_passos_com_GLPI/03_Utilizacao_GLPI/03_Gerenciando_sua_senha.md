Gerenciamento de senha
======================

O formulário para alteração de senha está na guia principal do menu ***Preferências***

É necessário digitar e confirmar sua senha antes da validação. O administador pode desativar essa funcionalidade. A área para alterar a senha não aparece nesse caso. Veja [Gerenciamento dos perfis dos usuários](gerenciamento_perfil.html "Na GLPI, gerenciamento do perfil pode ser feito a partir do menu Gerenciamento > Perfil.").

No caso do usuário ter perdido sua senha, é possível redefiní-la na página de login. O link estará visível somente se as notificações estiverem habilitadas (veja [Configuração é seguida de e-mails e alertas](config_notification_configuration.html "A configuração geral das notificações é feita em Configuração > Notificações > Configuração para e-mails e alertas;")).
Somente os usuários com um endereço de e-mail definido ao GLPI e não autenticado através de uma fonte externa (LDAP, servidor de e-mail...) podem utilizar essa funcionalidade. Uma vez que o pedido de modificação foi feito, o usuário recebe um e-mail fornecendo um link para redefinir sua senha.

As senhas devem seguir a política de segurança definida (veja [Guia do Sistema] (config_common_sysinfo.html "Essa guia possibilita exibição de um resumo de informações sobre as capacidades do servidor web e de definir as informações de registros e erros de registro assim como a política de aplicação de senhas.")).
É efetuado um controle em tempo real da senha digitada.

**Tópico princiapl :** [Utilização GLPI](index.php?pt/02_Primeiros_passos_com_GLPI/03_Utilizacao_GLPI/01_Utilizacao_GLPI.md)
