Utilizando o assistente de atualização
===================================

Atualização da GLPI

---------------------------

Para iniciar a atualização, direcione o navegador para a unidade base da GLPI :
[http://<ADRESSE\\_GLPI\\>](http://<ADRESSE_GLPI>).

Procedimento de atualização passo a passo.

Selecionar o idioma (Select your language)
-----------------------------------------

A primeira etapa consiste em escolher o idioma no qual a instalação irá ocorrer. Para uma instalação em \"Portugês\" selecione Portugês e confirme.

Licença
-------

O uso da GLPI está diretamente vinculado a aceitação da licença GNU (Licença Pública Geral). Essa licença está disponível para leitura. Uma vez lida e aceita, enviar o formulário.
Se isso não ocorrer é impossível acessar os passos seguintes.

Iniciar Instalação: A instalação ou atualização da GLPI
-------------------------------------------------------------

Clicar em Atualização.

Etapa 0 : Verificação da compatibilidade do local de instalação com a execução da GLPI
------------------------------------------------------------------------------------------

Esta etapa irá garantir que o sistema atende aos pré-requisitos para a instalação. Se isso não acontecer, é impossível acessar os seguintes passos e uma mensagem de erro indicará as ações a serem tomadas antes de tentar novamente. Se todas as verificações forem realizadas com sucesso, envie o formulário.

Etapa 1 : Configuração da conexão das bases de dados.
-------------------------------------------------------------

Essa etapa só é realizada se o arquivo de configuração(*config/config\\_db.php*) não estiver presente.

Os parâmetros de conexão com a base de dados são solicitados.

-   Servidor MySQL : informe o caminho de rede de acesso para o servidor. Por exemplo : localhost, ou mysql.domaine.tld ;
-   Usuário MySQL : digite o nome do usuário que tem permissão para se conectar no servidor MySQL. Por exemplo glpidbuser ;
-   Senha MySQL : digite a senha vinculada ao usuário definido anteriormente.

Uma vez que esses três campos forem preenchidos corretamente, valide o formulário. Se os parâmetros forem inválidos, uma mensagem de erro será exibida, modifique as configurações de conexão e tente novamente.

Etapa 2 : Selecionando o banco de dados
-----------------------------------------

Essa etapa só é realizada se o arquivo de configuração (config/config\\_db.php) não estiver presente.

Uma vez que a conexão com o servidor MySQL for estabilizada, deve-se escolher o banco de dados destinado a aplicação da GLPI e atualização.

Etapa 3 : Migração do banco de dados.
------------------------------------------

Essa etapa realiza a atualização da base dados. Em caso de erro, ler atentamente as informações. Dependendo da versão que a GLPI atualizar, um número de telas intermediárias será mostrado. Responda às perguntas com base na organização. O assistente de atualização, em seguida, se oferece para realizar a atualização do antigo conteúdo do banco de dados. Depois de clicar em Continue, uma barra de progresso é exibida na tela.

Importante : Dependendo do tamanho do banco de dados, esse processo pode ser muito longo (vários minutos ou horas em bases de vários gigabytes).Da mesma forma, é possível que a barra de progresso permanece algum tempo a 0% sem que isso seja um sintoma de mau funcionamento

Etapa 4 : A atualização está completa.
---------------------------------------------------------

Essa etapa fornece um resumo do processo de atualização.
Leia atentamente as informações e valide para se conectar a aplicação..

**Tópico principal :** [Atualização da
GLPI](../glpi/admin_upgrade.html \"É necessário atualizar regularmente a aplicação para se beneficiar das correções de segurança e novos recursos.\")
