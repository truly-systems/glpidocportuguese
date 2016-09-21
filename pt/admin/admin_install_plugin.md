Instalação e atualização dos plugins
======================================

Adicionar e fazer a manutenção das extensões (plugins) da GLPI

ATENÇÃO :

Antes de instalar um plugin, veja [Backup
GLPI](admin_backup.html "Realizar um backup completo da GLPI.").

Download de um plugin
---------------------

Abaixo estão disponíveis os links para o catálogo de plugins da GLPI e a possibilidade de composição dos mesmos :

-   [Catálogo dos plugins.](http://plugins.glpi-project.org/)
-   [Compor os plugins.
    ](https://forge.indepnet.net/projects/show/plugins)

Note-se que um plugin pode ter várias versões, cada versão é na maior parte do tempo específico para uma determinada versão do GLPI.
Certifique-se de selecionar o arquivo correto para download !

Instalação de um plugin
-------------------

Uma vez que é feito o download de um plugin, a instalação ocorre em duas etapas principais : o processamento dos arquivos do plugin, e sua instalação a partir da interface.

Importante : É preciso ter permissão registrada para configuração e os perfis(Campos **Configuração** e **Perfis** a partir da aba
**Administração/Configuração** na configuração de um perfil).

-   **Processamento dos arquivos.**

    Os plugins são compactados no formato GZIP. O primeiro passo é descompactar o arquivo. Ele deve então transferir os arquivos para a pasta *plugins* localizada no diretório principal da GLPI
    (*Exemplo : /var/www/mon\_glpi/plugins/*).

    Importante : Deve-se manter o nome da pasta que você criou no diretório *plugins* ! Deve ser exatamente o mesmo nome especificado no arquivo.

-   **Instalação de um plugin a partir da interface.**
    Uma vez que o arquivo foi alterado, o plugin aparecerá na página de configuração de plugins.  Pode-se consultar o número da versão e os autores do plugin. Isso ocorre por  conta da **Instalação** e da **Ativação**.
    -   A instalação vai criar as possíveis tabelas no banco de dados.
    -   A ativação irá tornar o plugin acessível aos usuários.

    Importante: No entanto, se um plugin não aparecer após a mudança, verifique a versão da GLPI.

Atualização de um plugin
-----------------------

A atualização de um plugin é realizada através da remoção física (*Atenção : não confundir com **Desinstalação de um plugin***) da versão anterior e instalação da nova. Remova completamente apenas a pasta correspondente do plugin e consulte a seção de instalação do plugin para um novo processo.

Importante : Após a atualização da GLPI todos os plugins são desativados, então é preciso reativá-los!

Desinstalação de um plugin
----------------------

A desinstalação de um plugin é realizada a partir da configuração dos plugins. Clique em **Desinstalação**.


**Tópico principal :** [Realização das operações de manutenção](../glpi/admin.html "Operações de manutenção da GLPI")
