Preparando para a atualização
=======================

Antes da atualização em si deve preparar e sistema de arquivos.

Preparação do sistema
----------------------

O processo de atualização exige provisoriamente mais recursos do sistema. Se o banco de dados GLPI é grande, é conveniente aumentar os valores de memória \ limite e tempo limite no arquivo de configuração php.ini do servidor web.

Preparação dos arquivos
------------------------

No servidor, deslocar todos o diretório da GLPI para um diretório temporário, exceto o diretório de arquivos (pasta onde os documentos são armazenados).

Se a atualização da GLPI for feita a partir de uma versão inferior a 0.68,alguns diretórios terão seus nomes modificados. Por isso é necessário copiar seu conteúdo:

~~~~ {.codeblock}
ancien_GLPI/docs/ -> nouveau_glpi/files
ancien_GLPI/backup/dump -> nouveau_GLPI/files/_dumps
~~~~

**Tópico principal:** [Atualização da GLPI](../glpi/admin_upgrade.html "É necessário atualizar regularmente a aplicação para se beneficiar das correções de segurança e novos recursos.")
