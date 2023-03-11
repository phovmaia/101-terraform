# O que é Infraestrutura como Código? (IaC)

Nosso primeiro passo nesse 101 de terraform, tem que ser entender a base dele, que é
Infraestrutura como Código (IaC). Segundo Yevgeniy Brikman, a ideia por trás do IaC é
que você escreva e execute código para definir deployar, atualizar e destruir sua
infraestrutura.
Sou novo na área de TI mas fica muito claro que nesse momento da linha do tempo das
tecnologias passa a existir uma nova visão de operação dentro de infraestrutura, tendo
em vista a adoção desse novo midset, e temos que falar dessa palavra *operação*, pois é
a visão Ops de *DevOps*. Não adianta termos um cargo de DevOps Engineer se não aplicamos
DevOps como cultura e filosofia.

Visualizando essa mudança é possível entender que um aspecto chave do mundo DevOps
é com que possamos gerenciar quase tudo como código, e isso inclui muitos recursos como:
servers, databases, load balancers, firewalls, DNS entries, etc.

E o terraform? Cade? Bora lá, existem muitas ferramentas para gerenciar nossos recursos
como código e cada uma delas tem suas vantagens e desvantagens, além de utilizarem de
abordagens diferentes. Vamos falar um pouco sobre elas.

## ad hoc scripts

Apesar de ser uma abordagem simples e uma das mais conhecidadas, eu demorei um bom tempo
para entender o porque desse nome mas definitivamente não fiz o básico, procurar o
significado de 'ad hoc', que nada mais é que destinado a essa finalidade.
Então é simples, você escreve um script para fazer o que precisa e executa ele, let's go
<details open>
<summary class="summary">script ad hoc</summary>
Nesse exemplo vamos instalar o apache e o php, clonar um repositório do github e
iniciar o serviço do apache.

```
apt-get update
apt-get install \\
    -y \
    php \
    apache 2
git clone \
    github.com/foo/bar \
    var/www/html/app
service apache2 start
```

</details>

Interessante, agora podemos executar +/- 7 linhas de comando apenas com nosso script.
Então, quando Diretor X. da aquele salve e pede para você criar um sevidor apache, já
está tudo pronto, basta executar o script e pronto, mas e se precisar criar 10 servidores?
20? 100? 1000? 10000? 100000? 1000000? 10000000? 100000000? 1000000000? 10000000000?
Aí já não é mais tão simples, e aí de cara já conseguimos imaginar onde está o problema...
Os scripts ad hoc são bem diretos e legíveis mas difíceis de manter, difíceis de reutilizar
e inviáveis de se escalar.

## ferramentas de

Aqui a gente começa a escutar vários nomes do mercado, como chef, puppet e ansible
(sim, existem várias outras). Essas ferramentas são destinadas para gerenciar a
