Gerenciamento de relatórios
==================

GLPI permite a geração de um certo número de relatórios :

-   **Relatório padrão** : Este relatório registra os materiais presentes no parque classificados por tipo.
    Para computaodores, a triagem é feita por sistema operacional.

-   **Por contrato** : Contrato de manutenção de hardware com um terceiro.
    É possível obter uma declaração detalhada por tipo de material e data de compra. A seleção múltipla é permitida.
    Para adicionar um tipo, basta clicar na área em branco e escolher o novo tipo. O princípio é o mesmo para adicionar uma data.
    A tabela lista por tipo de objeto, nome, se está na cesta ou não, sua entidade, sua localização, as datas de compra e validade, o tipo de contrato e as datas de início e final de contrato.

-   **Por ano** : Relatar sob o mesmo princípio que o relatório anterior, mas também listar o contrato sem equipamentos.

-   **Informações financeiras e administrativas do material** : Resumo das informações financeiras para os computadores, as impressoras, os equipamentos de rede, os monitores, os periféricos os telefones.
    É possível obter um relatório para um determinado período.
    A tabela lista por tipo de objeto, nome, entidade, o seu valor, seu valor contábil, o seu TCO, suas datas de compra, comissionamento e validade da garantia.
    Um resumo incluindo o valor total e valor contábil líquido é proposto por tipo de objeto e para todos os objetos.

-   **Outras informações financeiras e administrativas** :
Relatar sob o mesmo princípio que o relatório anterior, mas para cartuchos, licenças e suprimentos.

-   **Relatório de rede** : 3 relatórios podem ser realizados : por localização, por tipo de hardware de rede ou entrada de rede.
![image](docs/image/Rapport-reseau.png)

-   **Empréstimo** : Resumo das reservas atuais, passadas ou as que estão para vir para um determinado usuário.

-   **Relatório sobre status** : Resumo por tipo de  aparelho de status diferente.

Un plugin pode adicionar vários relatórios na GLPI. Esse plugin : **Relatórios adicionais** está disponível na [elaborar plugins](https://forge.indepnet.net/projects/plugins).

--------
**Tópico principal :** [Modulo Ferramentas](index.php?pt/06_Modulo_Ferramentas/01_Modulo_Ferramentas.md "O módulo Ferramentas permite ao usuário administrar as anotações, conhecimento básicos, gerar anotações, reservas, bem como gerar o relatório")