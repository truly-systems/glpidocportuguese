Aba Parque
===========

A aba parque permite definir os parâmetros gerais a respeito da parte do inventário da aplicação.

Parque
----------------
![image](docs/image/configparc.png)

- **Ativação das informações financeiras e administrativas por padrão** : aplicável a todos os itens do inventário.

- **Categoria de softwares excluídos pelas regras do dicionário** : é possível alterar automaticamente a categoria softwares excluindo do dicionário. Devido a padronização eles são automaticamente reposicionados na categoria FUSION.

- **Início do ano fiscal** :  utilizado na parte Gestão

- **Campos automáticos (marcados por *)** : para criar um modelo, você pode adicionar os campos gerados automaticamente a partir de um modelo (por exemplo : o nome do material, o número do inventário). A incrementação desse valores nesse campos são feitas por enteidade ou de maneira global.

- **Restringindo a gestão dos monitores** :
- **Restringindo a gestão dos periféricos** :
- **Restringindo a gestão dos telefones** :
- **Restringindo a gestão das impressoras** :
Ao criar manualmente um hardware, o usuário precisa escolher o tipo de gestão (unitário ou global).
    exemplo :  uma impressora compartilhada por muitos usuários, o monitor está conectado a um interruptor de tela
Posteriormente, um material administrado de maneira unitário pode passar sob o modo de gestão glocal. É possível restringir o tipo de gestão por materiais.


![image](docs/image/configtransfert.png)

- **Modelo para transferência automática para computadores em outra entidade** : GLPI permite também de transferir um computador para outra entidade se um dos critérios utilizados para atribuir uma entidade for modificado.
Se a opção Modelo para transferência automática do computador através de uma outra entidade indicar um modelo existente, a cada atualização de um computador a partir da ferramenta de um inventário, o motor de regras da atribuição das entidades será reproduzido. Se a entidade resultante for diferente da entidade do computador, ela será transferida.


![image](docs/image/configpc.png)

A interface com uma ferramenta de inventário possibilita o inventário automatizado de hardware. Esta interface é possível através de um plugin.

- **Ao conectar ou atualizar** : ao se conectar diretamente a um computador com um elemento gerido de maneira unitária, é possível atribuir as informações recuperadas do computador
- **Ao desconectar** : quando se desconectar, é possível apagar as informações.
Essas funcionalidades não são ativadas por padrão e dizem respeito a todos os itens de inventário que os campos de uso, usuário, grupo e local que são recuperados através do agente de inventário e o campo de statis que você define.

   Exemplo : durante a primeira subida do invenstário pode-se definir se o monitor conectado ao computador terá o status de produção. Em caso de se desconectar ele terá o status Disponível

-----
**Tópico principal :** [Configurando os parâmetros centrais](index.php?pt/08_Modulo_Configuracao/06_Geral/01_Configurando_os_parametros_centrais.md)