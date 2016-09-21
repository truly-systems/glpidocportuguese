Administrando suas preferências
=====================

As preferências do usuários utilisateur podem ser modificadas através da guia *Preferências* no registro do usuário ou através do menu *Minhas prferências* situado no topo e à direta da interface, em qualquer página.

Cada usuário autenticado pode modificar suas prfêrenciass.

Guia Principal
----------------
 O usuário pode modificar as informações pessoais : sobrenome, nome, e-mail, números de telefone, local e idioma.

***Observação :** Alguns campos não são editáveis se eles provêm de um diretório LDAP.*

Pode-se adicionar endereços de e-mail e selecionar o endereço padrão, que será usado para enviar notificações.

Também pode-se especificar certas condutas padrão da aplicação, como o perfil e a entidade padrão selecionada quando se conectar a interface. Veja [Gerenciamento dos perfis dos usuários](index.php?pt/07_Modulo_Administracao/07_Perfis/01_Perfis.md) "Na GLPI, o gerenciamentos dos perfis pode ser feito à partir do menu Gerenciamento > Perfis.") e [Gerenciamento das entidades](index.php?pt/07_Modulo_Administracao/04_Entidades.md "Na GLPI, administrar as entidades pode ser feito a partir do menu Administração > Entidades.").
Pode-se desativas as notificações para as ações executadas.

O usuário pode optar por deixar o modo operação normal da aplicação :

-   No modo depuração, GLPI apresenta erros, todos os valores variáveis, consultas SQL... É útil ativar esse modo em caso de falha da aplicação. Um máximo de informações pode ser fornecida para os desenvolvedores do projeto GLPI. Esse modo também permite obter informações adicionais sobre os vários objetos em uma aba específica(notificações...).

Guia de Personalização
----------------------
Esse guia permite alterar as preferências gerais de exibição aplicadas a um determinado usuário. Essas opções substituem as definidas na configuração geral.

Para maiores explicações, veja [guia de personalização da configuração geral](index.php?pt/08_Modulo_Configuracao/06_Geral/03_Valeurs_par_défaut.md)


![image](docs/image/personnalisation.png)

***Observação** : para o número de resultados por página, o valor especificado aqui não pode exceder o valor máximo definido no visor de definições geral.*



![image](docs/image/pref-assistance.png)


![image](docs/image/pref-cle.png)

A seção **Chave de acesso remoto** permita recuperar a chave de segurança utilizada para acessar os fluxos privados da GLPI.
Atualmente os fluxos ICAL et WEBCAL são protegidos com chav de segurança que é integrada a url.

![image](docs/image/pref-duedate.png)

Personal view
----------------------

Se você tiver definido personal view em objetos, essa aba será visível.
Ela exclui os personal view para retornar ao global view.

-------
**Tópico Principal :** [Utilização do GLPI](index.php?pt/02_Primeiros_passos_com_GLPI/03_Utilizacao_GLPI/01_Utilizacao_GLPI.md)
