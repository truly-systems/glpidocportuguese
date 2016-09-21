Administrando os controles de acesso
=================================

Esta seção descreve como administrar o sistema de controle de acesso que permite a cada usuário tenha acesso a um contexto de uso específico.

No GLPI cada usuário não tem acesso à mesma interface, nem a mesma funcionalidade. Para cada usuário, um contexto específico é determinado, que permite acesso a recursos e elementos de informação a que ele tem direito a acessar. O acesso de informações da identidade do usuário permite determinar suas autorizações.

Primeiramente, liga-se o GLPI a um sistema de gestão de identidade. O GLPI pode gerenciar localmente a autenticação e informações pessoais dos usuários. No entanto, o sistema de informação, muitas vezes inclui um sistema de gestão de identidade (diretório), e é preferível delegar autenticação para ele e para utilizar as informações contidas neste sistema externo. Essa questão é tratada no capítulo [Configurar o gerenciamento de identidade](config_auth.html "O modo como o GLPI gera a autenticação e as informações pessoais dos usuários são configuradas a partir do menu Configuração > Autenticação.").

A implantação cotidiana da ligação com o ou os repositórios de gerenciamento de identidade leva a criação e a supressão, a sincronização, a ativação e a desativação das contas dos usuários associados a seus dados pessoais. Essa questão é tratada no capítulo [Gerenciamento dos usuários](gerenciamento_usuário.html "No GLPI, o gerenciamento dos usuários pode ser feito a partir do menu Gerenciamento > Usuários.").

É possível associar os dados pessoais em grupos, orgãos e em perfis, que são os meios para determinar as circunstâncias de uso.

Os grupos possibilitam que os usuários se reunam com base em  habilidades semelhantes  ou unidades organizacionais. Essa questão é tratada no capítulo  [Gerenciamento de grupos](gerenciamento_grupo.html "No GLPI, gerenciar os grupos pode ser feito a partir do menu Gerenciamento > Grupos.").

Les entités permettent de segmenter le parc et de rassembler les
utilisateurs en services isolés les uns des autres. Essa questão é tratada no capítulo [Gerenciamento les
entités](administration_entity.html "No GLPI, gerenciamente les entités pode ser feito a partir do menu Gerenciamento > Entités.").

Os perfis décrivent les autorisations d'accès qui doivent être
accordées à leurs membros. Essa questão é tratada no capítulo
[Gerenciamento dos perfis dos usuários](administration_profile.html "Dans GLPI, administrer les profils peut se faire à partir du menu Administration > Profils.").

En dernier lieu, il faut administrer les habilitations : déterminer les
contextes d'utilisation et les attribuer aux utilisateurs. Ces outils
sont utilisés par les règles d'affectations d'habilitations pour
déterminer de manière dynamique les habilitations des utilisateurs.
Essa questão é tratada no capítulo [Attribuer des habilitations à un utilisateur](administration_rule_right.html "GLPI dispose d'un moteur d'habilitations dynamiques qui se base sur des sources externes d'authentification. Il est accessible depuis le menu Administration > Règles > Règles d'affectation d'entité et de droits.").

-   **[Configuração da gestão de identidade](../glpi/config_auth.html)**\
     La manière dont GLPI gère l'authentification et les informations
    personnelles des utilisateurs se configure depuis le menu
    Configuration \> Authentification .
-   **[Gerenciamento dos usuários](../glpi/administration_user.html)**\
     Dans GLPI, administrer les utilisateurs peut se faire à partir du
    menu Administration \> Utilisateurs .
-   **[Gerenciamento de grupos](../glpi/administration_group.html)**\
     Dans GLPI, administrer les groupes peut se faire à partir du menu
    Administration \> Groupes .
-   **[Administrer les entités](../glpi/administration_entity.html)**\
     Dans GLPI, administrer les entités pode ser feito a partir do menu
    Administration \> Entités .
-   **[Gerenciamento dos perfis dos usuários](../glpi/administration_profile.html)**\
     No GLPI, gerenciar os perfis pode ser feito a partir do menu
    Gerenciamento \> Perfis .
-   **[Attribuer des habilitations à un utilisateur](../glpi/administration_rule_right.html)**\
     GLPI dispose d'un moteur d'habilitations dynamiques qui se base sur
    des sources externes d'authentification. Il est accessible depuis le
    menu Administration \> Règles \> Règles d'affectation d'entité et de
    droits .

