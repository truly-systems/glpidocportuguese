
Uso do assistente de instalação on-line GLPI
====================================================

Para iniciar a instalação, direcionar o navegador  para a pasta raiz da GLPI :
[http://<ADRESSE\_GLPI\>](http://<ADRESSE_GLPI>).

Assim que se conectar a esse endereço, um passo a passo da instalação se iniciará.

Escolha o idioma
-----------------------------------------

A primeira etapa consiste na escolha do idioma em que a instalação será realizada.
Para instalar em "Português", selecione **Português** e confirme.

Licença
-------

A utilização da GLPI está sujeita a licença de utilização GNU General Public Licence. Essa licença está disponível para leitura.  Uma vez que a licença é lida e aceita, envie o formulário. Se este não for o caso, é impossível ter acesso aos seguintes passos

Iniciar instalação : Instalação ou atualização da GLPI
-------------------------------------------------------------

Clique em **Instalação**.

Etapa 0 : Verificar a compatibilidade de seu ambiente com a execução da GLPI
------------------------------------------------------------------------------------------

Este etapa irá garantir que o sistema satisfaz os pré-requisitos para a instalação. Se isso não acontecer, é impossível acessar os seguintes passos e uma mensagem de erro indicará as ações a tomar antes de tentar novamente.Se todas as verificações forem efetuadas,valide o formulário

Etapa 1 : Configuração da conexão da base de dados.
-------------------------------------------------------------

Os parâmetros de conexão ao banco de dados são solicitados.

-   **Servidor MySQL** : inserir o caminho de rede para o servidor, por exemplo : *localhost*, ou *mysql.domaine.tld* ;
-   **Usuário MySQL** : inserir o nome do usuário que tem a permissão para se conectar ao servidor MySQL
-   **Senha MySQL** : inserir a senha relacionada ao usuário e que foi definida previamente.

Uma vez que esses três campos forem preenchidos corretamente, valide o formulário. Se os parâmetros forem inválidos, uma mensagem de erro surgirá e srá necessário modificar as configurações de conexão e tentar novamente.

Etapa 2 : Criando ou escolha da base de dados e a sua utilização
-------------------------------------------------------------------------------

Uma vez que a conexão ao servidor MySQL for estabelizada, criar ou selecionar a base de dados destinada a acomodas os dados da aplicação GLPI e iniciar.

Duas possibilidades :

-   Um banco destinado a acomodar os dados da GLPI já existentes :

    Selecionar essa função na lista de bancos de dados exibidas.
    Validar para inicializar o banco de dados.

    > ATENÇÃO :
    O conteúdo do banco de dados selecionado será destruído quando inicializado.

-   Para criar um novo banco de dados para acomodar os dados da GLPI :

    Selecionar **Criando de um novo banco de dados**.
    Inserir o nome do novo banco de dados no campo de texto.
    Validar para criar o banco de dados.

    > Importante : Essa estapa precisa que o usuário tenha premissão para criar um novo banco.

Etapa 3 : Inicialização do banco de dados.
-----------------------------------------------

Esta etapa inicializa o banco de dados com valores padrão.
Em caso de erro, leia as informações com cuidado.

Etapa 4 : A instalação da GLPI está agora completa.
---------------------------------------------------------

Essa etapa apresenta um resumo dos procedimentos de instalação e lista as contas criadas pelos usuários. Leia atentamente essas informações e valide para manter a primeira conexão com a aplicação.

***Conselho :*** As contas dos usuários padrão são :

*glpi/glpi* para a conta do administrador

*tech/tech* para a conta do técnico

*normal/normal* para a conta normal

*post-only/postonly* para a conta post-only

> Atenção : Deve-se excluir ou modificar essas contas padrão por motivos de segurança. Verifique antes de excluir a conta para criar o perfil com um super-adm.

----------------------

**Tópico principal :** [Instalação da aplicação GLPI](index.php?pt/2_Primeiros_passos_com_GLPI/02_Implantacao_GLPI/03_Instalação_da_aplicacao.md)
