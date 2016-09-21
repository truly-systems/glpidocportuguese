Pré-requisisitos do servidor web
========================

Características do servidor web necessárias para funcionamento da GLPI.

Servidor web
-----------

GLPI requer um servidor web que suporte PHP, como :

-   Apache 2 ou superior ([http://httpd.apache.org](http://httpd.apache.org)) ;
-   Microsoft IIS ([http://www.iis.net](http://www.iis.net)).

PHP
---

GLPI necessita de uma versão PHP 5.4 ou superior ([http://www.php.net](http://www.php.net)).

Extensões PHP obrigatórias
---------------------------

As extensão PHP seguintes são necessárias para o bom funcionamento da aplicação :

-   JSON : suporte do formato de dados estruturados JSON ;
-   Mbstring : gestão de cadeias de caracteres multi-bytes ;
-   MySQL : associação com banco de dados ;
-   Sessão : suporte das sessões dos usuários.

Extensões PHP facultativas, mas recomendadas
---------------------------------------------

As seguintes extensões são necessárias para funcionalidades opcionais da aplicação :

-   CLI : uso de PHP em linha de comando para ações automáticas ;
-   CURL : para a autentificação CAS ;
-   DOMXML : para a autentificação CAS ;
-   GD : geração de imagens ;
-   IMAP : uso de servidores de e-mail para reunir os tickets ou autenticação de usuário ;
-   LDAP : usando um diretório externo para a autenticação ;
-   OpenSSL : comunicação criptografada.

Configuração PHP
-----------------

O arquivo de configuração de php (*php.ini*) deve ser modificado para incluir as seguintes variáveis :

    memory_limit = 64M ; // Valor mínimo
    file_uploads = on ;
    max_execution_time = 600 ; // Recomendada, mas não obrigatória
    register_globals = off ;  // Recomendada, mas não obrigatória
    magic_quotes_sybase = off ;
    session.auto_start = off ;
    session.use_trans_sid = 0 ; // Recomendada, mas não obrigatória

----------------
**Tópico principal :**
[Pré-requisitos necessários para instalação da GLPI](index.php?pt/02_Primeiros_passos_com_GLPI/02_Implantacao_GLPI/02_Prerequisitos/01_Prerequisitos_necessarios.md)
