# [terraform-101](github.com/phovmaia/terraform-101) - 101 de terraform

Este repo "baseado" no livro Terraform Up and Running do Yevgeniy Brikman, também
conhecido como @brikis98 e também co-funder do terragrunt. O livro tem um repo no
github com os exemplos usados no livro, <https://github.com/brikis98/terraform-up-and-running-code>.
Juntando minhas experiências com terraform e a experiência que tive com o livro vamos
criar um 101 de terraform para quem está começando.

## Intro

Para podermos fazer um 101 de terraform precisamos entender alguns conceitos e definir
qual será nossa caminhada aqui, então vamos lá.

Primeiro vamos entender *Infrastructure as Code (IaC)*, que é a base do terraform. Segundo
Yevgeniy Brikman, a ideia por trás do IaC é que você escreva e execute código para definir
deployar, atualizar e destruir sua infraestrutura.
Sou novo na área de TI mas é muito claro que aqui passa a existir uma nova visão de
operação com a adoção desse novo midset, e temos que falar dessa de operação, pois é
a visão de *DevOps*. Não adianta termos um cargo de DevOps Engineer se não aplicamos
DevOps como cultura e filosofia.

Tendo essa visão nova, podemos começar a entender que um aspecto chave do mundo DevOps
é com que possamos gerenciar quase tudo como código, e isso inclui muitos recursos como:
servers, databases, load balancers, firewalls, DNS entries, etc.

E o terraform? Cade? Bora lá, existem muitas ferramentas para gerenciar nossos recursos
como código e cada uma delas tem suas vantagens e desvantagens, além de utilizarem de
abordagens diferentes. Vamos falar um pouco sobre elas.
