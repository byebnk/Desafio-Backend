# Desafio técnico backend - Byebnk

Olá,

Estamos muito felizes que você deseja fazer parte do time da Byebnk. O teste abaixo é construido de
forma que você consiga demonstrar os seus conhecimentos em Django/DRF e investimentos. Ele consiste
em apenas 2 a 3 endpoints com regras de negócio bem específicas.

Se você não entende de investimentos, não se preocupe. Isso é algo que você pode aprender trabalhando
com a gente. As regras financeiras estão bem detalhadas nos requisitos obrigatórios, mas caso tenha
alguma dificuldade em entender, não tenha medo de perguntar. Isso não é um ponto negativo. Na Byebnk
valorizamos quem sabe utilizar todos os recursos disponíveis para entregar um excelente resultado.
Por outro lado, se você é o especialista em mercado de capitais, pode se aventurar desenvolvendo
alguns dos requisitos extras (opcionais).

Você pode organizar a API e o banco de dados da maneira que achar que faz mais sentido. Além disso,
sinta-se a vontade para adicionar ferramentas ou funcionalidades que ache relevante, porém não deixe
que isso impacte negativamente a qualidade dos requisitos obrigatórios.

Uma coisa muito importante na Byebnk são os testes. A complexidade e responsabilidade dos sistemas
são grandes e o que nos ajuda a manter tudo sobre controle são os testes automatizados. Você não
precisa testar cada mínimo detalhe do seu código, mas é importante que as principais regras de
negócio estejam testadas e demais condições que você achar relevante (as decisões são importantes:
vamos perguntar o porque você decidiu testar A e não B).

Lembre-se: Existem diversas formas de se desenvolver um sistema. Não estamos procurando a resposta
certa, mas sim uma explicação racional por trás de cada decisão tomada.

## Requisitos obrigatórios
Usando [Django](https://www.djangoproject.com/) e [Django REST framework](https://www.django-rest-framework.org/)
desenvolva uma API REST que permita usuários a gerenciar investimentos.

* Usuários devem ser capazes de cadastrar ativos
* Usuários devem ser capazes de fazer aplicações e resgates em um ativo
    * Aplicação é quando o usuário aporta dinheiro em um ativo
    * Resgate é quando o usuário retira dinheiro de um ativo
    * Aplicações e resgates são transacionais e imutáveis. Uma vez realizada não há como alterar.
    * Usuários podem fazer aplicações/resgate em ativos cadastrados por qualquer usuário
* Usuários devem ser capazes de visualizar o saldo da sua carteira de investimentos
    * Você pode decidir onde e como mostrar a informação
    * O saldo da carteira é o somatório de saldos investidos em cada um dos ativos
* Usuários não podem ver aplicações e resgates de outros usuários
* Usuários não podem ver o saldo da carteira de outros usuários
* A autenticação da API deve ser feita via token
    * Não é necessário desenvolver endpoints para criação/gerenciamento de usuários
* Os ativos devem conter no mínimo as informações abaixo:
    * Identificador - um identificador aleatório gerado automaticamente
    * Nome - uma denominação para este ativo
    * Modalidade - renda fixa, renda variável ou cripto
* As aplicações e resgates devem conter no mínimo as informações abaixo:
    * Identificador - um identificador aleatório gerado automaticamente
    * Ativo - O ativo ao qual a aplicação/resgate se refere
    * Quantidade - número de ativos que foram aplicados/resgatados
    * Preço unitário - preço unitário do ativo na aplicação/resgate
    * Endereço de IP - endereço de IP que solicitou a aplicação/resgate
    * Data de solicitação - a data em que a aplicação/resgate foi solicitada
* Testes
    * As funcionalidade principais devem estar com [testes](https://docs.djangoproject.com/en/3.1/topics/testing/) escritos
    * Você pode decidir quais os testes que mais agregam valor ao projeto
* O escopo do teste é somente a API REST
    * Você não precisa desenvolver frontend/formulários para o sistema
    * Você apenas precisa desenvolver os 2 a 3 endpoints REST necessários para a realização dos requisitos obrigatórios

## Requisitos extras (opcional)
* Permitir os usuários listar ativos por tipo (renda fixa, renda váriavel, cripto)
* Adicionar o preço de mercado de cada ativo e calcular o saldo de carteira utilizando ele
* Permitir os usuários visualizar o lucro/prejuízo realizado
* Expandir o sistema adicionando taxa de custódia, administração, tarifa de saque, etc...

## O que vamos avaliar (nesta ordem)
1. O cumprimento dos requisitos obrigatórios
2. A forma que o código está organizado
3. O domínio das funcionalidade do Django e DRF
4. A abordagem e abrangência dos testes do código
5. A simplicidade da solução
6. Aderência a [PEP 8](https://duckduckgo.com/?q=pep8)
7. A implementação de requisitos opcionais
8. A implementação de funcionalidades extras