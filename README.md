# Boas vindas ao repositório do projeto TryBeer!

Você já usa o GitHub diariamente para desenvolver os exercícios, certo? Agora, para desenvolver os projetos, você deverá seguir as instruções a seguir. Fique atento a cada passo, e se tiver qualquer dúvida, nos envie por _Slack_! #vqv 🚀

Aqui você vai encontrar os detalhes de como estruturar o desenvolvimento do seu projeto a partir desse repositório, utilizando uma branch específica e um _Pull Request_ para colocar seus códigos.

## O que deverá ser desenvolvido

Esse será o projeto mais desafiador até agora! Você será responsável por criar uma aplicação de ponta a ponta!

Isso significa que a API, o banco de dados e o front-end serão escritos por você. 😁

O projeto em si é super divertido! Você vai criar uma plataforma de delivery de cerveja. 🍻

Para facilitar o entendimento, dá para dividirmos a aplicação em três partes:

- Front-end do **cliente**, onde nossos clientes vão comprar cerveja;

- Front-end do **admin**, onde o estabelecimento controlará os pedidos feitos;

- API, que será compartilhada entre cliente e admin.

O banco de dados utilizado será o `MySQL`!

Você pode acessar um protótipo do front-end [aqui](https://www.figma.com/file/tzP4txu6Uy0qCxVZWdWMBO/TryBeer?node-id=0%3A1).

Para servir arquivos estáticos como imagens no back-end, utilize o seguinte path:
`/back-end/public/`

##### ⚠️ Lembre-se de escrever testes unitários e sinta-se livre para alterar a UI. Contudo, respeite os atributos `data-testid`, pois eles serão usados na correção do projeto.

Você pode ler mais sobre os atributos que serão utilizados para testes [neste link](https://www.eduardopedroso.com.br/?p=494).

##### ⚠️ Para ver os comentários sobre cada componente, basta clicar no ícone de comentários no Figma (lado esquerdo superior).

![image](https://res.cloudinary.com/drdpedroso/image/upload/c_scale,w_400/v1575815877/Screenshot_2019-12-08_at_11.37.25_kzt7rl.png)

---

## Desenvolvimento

Esse repositório contém duas pastas, `back-end` e `front-end`, onde você deve desenvolver o front-end e o back-end da aplicação. Ambas as pastas contêm um projeto iniciado com as configurações básicas necessárias. Após clonar o projeto e instalar as dependências, sinta-se livre para escolher usar Redux ou ContextAPI + React Hooks. Saiba avaliar as vantagens/desvantagens de cada um na hora da escolha.

Para o banco de dados, você deverá utilizar o `MySQL`. Modele-o e disponibilize um script, na raiz do seu app, para que o seu projeto seja corrigido utilizando o banco de dados arquitetado por você! O nome do script deve ser `script.sql`.

##### Você também deve **escrever testes unitários que devem cobrir pelo menos 90% do projeto**. Na [documentação do Jest CLI](https://jestjs.io/docs/en/cli) é possível ver como essa cobertura é coletada.

Para que seu projeto seja corretamente avaliado, siga as orientações a seguir:

- Sua aplicação deve ter um admin padrão com o nome de usuário `tryber` e senha `123456`.

- Sua aplicação deve ter, no mínimo, os produtos abaixo cadastrados. O arquivo `images.tar.gz`, na raiz do projeto, contém imagens para estes produtos.

  - Skol Lata 250ml, R$ 2.20;
  - Heineken 600ml, R$ 7.50;
  - Antarctica Pilsen 300ml, R$ 2.49;
  - Brahma 600ml, R$ 7.50;
  - Skol 269ml, R$ 2.19;
  - Skol Beats Senses 313ml, R$ 4.49;
  - Becks 330ml, R$ 4.99;
  - Brahma Duplo Malte 350ml, R$ 2.79;
  - Becks 600ml, R$ 8.89;
  - Skol Beats Senses 269ml, R$ 3.57;
  - Stella Artois 275ml, R$ 3.49.

- O front-end deve ser iniciado com `npm start` na pasta `front-end` e escutar a porta `3000`. A API deve ser iniciada com `npm start` dentro da pasta `back-end` e escutar a porta `3001`.

- O uso de `localStorage` é necessário para que as informações não se percam caso o usuário atualize a página.

- No `localStorage` do navegador:

  - A chave `user` deve conter a seguinte estrutura:

    ```json
    {
      "name": "Taylor Swift",
      "email": "taylorswift@email.com",
      "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiIxMjM0NTY3ODkwIiwibmFtZSI6IkpvaG4(...)",
      "role": "client"
    }
    ```

  - Ao deslogar, remova completamente a chave `user` do `localStorage`.

## Requisitos do projeto

⚠️ Lembre-se de que o seu projeto só será avaliado se estiver passando pelos _checks_ do **CodeClimate** e se estiver, também, seguindo corretamente os padrões REST para rotas e MVC para o back-end. Além disso, você deve também disponibilizar um script contendo a criação do seu banco de dados, das tabelas e inserção de dados iniciais.

⚠️ A criação dos endpoints da API, a modelagem do banco e a estrutura geral do projeto é livre, desde que os requisitos especificados na seção `Requisitos Gerais` sejam cumpridos.

O intuito desse app é que uma pessoa possa pedir uma cerveja no aplicativo e outra pessoa possa aceitar esse pedido no **admin**.

##### O projeto sera composto por duas entregas, cada uma especificada abaixo com seus respectivos requisitos e o prazo decidido com a facilitação.

## Requisitos Entrega 1

##### Requisitos Gerais

1. Os `endpoints` da API devem ser criados utilizando o padrão REST;

2. O back-end deve utilizar o banco de dados `MySQL`;

3. O back-end deve ser construído seguindo o padrão arquitetural `MSC`;

4. Disponibilize um script SQL na raiz do projeto com comandos para a criação do banco de dados, das tabelas, inserção dos dados iniciais e criação do admin padrão. O script deve ser nomeado `script.sql`.

### 1 - Crie uma página de login

Esta tela possui o nome `Login` no protótipo.

5. Todos os elementos da tela devem respeitar os atributos descritos no protótipo;

6. A rota da tela deve ser `/login`;

7. A pessoa deve conseguir escrever seu email no input de email;

8. A pessoa deve conseguir escrever sua senha no input de senha;

9. O formulário só fica válido após um email válido e uma senha de, no mínimo, 6 números serem preenchidos. Um email válido possui a forma `<nome>@<domínio>`. Caso o formulário esteja inválido, o botão de submeter deve estar desativado. Caso contrário, deve estar ativado;

10. Após a submissão bem sucedida do formulário, o token que identifica o usuário recebido na resposta deve ser salvo no `localStorage`. Esse token deve ser utilizado para futuras requisições à API;

11. Após a submissão bem sucedida do formulário, se o usuário for do tipo `administrador`, a pessoa deve ser redirecionada para a página **Admin - Home**;

12. Após a submissão bem sucedida do formulário, se o usuário for do tipo `cliente`, a pessoa deve ser redirecionada para a página **Cliente - Produtos**;

13. Deve existir um botão para o usuário se registrar com o texto `"Ainda não tenho conta"`. Ao ser clicado, a pessoa deve ser redirecionada para a página **Registro**.

DATA TEST ID
URL - /login
Campo email                - data-testid="email-input"
campo senha                - data-testid="password-input"
botao entrar               - data-testid="signin-btn"
link ainda nao tenho conta - data-testid="no-account-btn"

### Página de Login:

**[Será validado que é possível acessar a home]**

**[Será validado que a tela login contém os atributos descritos no protótipo]**

**[Será validado que não é possível fazer login com um email inválido]**

**[Será validado que não é possível fazer login com uma senha em branco]**

**[Será validado que não é possível fazer login com uma senha com menos de 6 caracteres]**

**[Será validado que é possível fazer login com um cliente e ser redirecionado para tela de cliente]**

**[Será validado que é possível fazer login com um admin e ser redirecionado para tela de admin]**

**[Será validado que é possível clicar no botão "Ainda não tenho conta" e ser redirecionado para tela de registro]**

### 2 - Crie uma página de registro de usuários

Esta tela possui o nome `Registro` no protótipo.

14. Todos os elementos devem respeitar os atributos descritos no protótipo;

15. A rota da tela deve ser `/register`;

16. A tela deve mostrar um formulário com os seguintes campos:

    - **nome** - deve conter, no mínimo, 12 letras, sem números ou caracteres especiais;

    - **email** - deve conter um email válido. Um email válido possui o formato `<nome>@<domínio>`;

    - **senha** - composta por, no mínimo, 6 números;

    - **quero vender** - um checkbox opcional, desmarcado por padrão.

17. Caso a opção `Quero vender` esteja marcada, o usuário deve ser cadastrado com um papel de **admin**. Caso contrário, será um **client**;

18. Caso os dados inseridos no formulário sejam inválidos, o botão de submeter deve estar desativado. Caso contrário, deve estar ativado;

19. Caso a opção `Quero vender` esteja marcada, ao clicar no botão `"Cadastrar"`, a pessoa deve ser redirecionada para a página **Admin - Home**. Caso contrario, deve ser redirecionada para a página de **Cliente - Produtos**.

DATA TEST ID

Campo nome            - data-testid="signup-name"
Campo email           - data-testid="signup-email"
Campo password        - data-testid="signup-password"
Checkbox quero vender - data-testid="signup-seller"
Botão de cadastrar    - data-testid="signup-btn"

### Página de Registro 

**[Será validado que é possível acessar a tela de registro]**

**[Será validado que contém os atributos descritos no protótipo]**

**[Será validado que não é possível fazer o registro com um nome com caracteres especiais]**

**[Será validado que não é possível fazer o registro com um nome com menos de 12 letras]**

**[Será validado que não é possível fazer o registro com um nome com números]**

**[Será validado que não é possível fazer login com um email inválido]**

**[Será validado que não é possível fazer login com um email já existente]**

**[Será validado que não é possível fazer login com uma senha em branco]**

**[Será validado que não é possível fazer login com uma senha com menos de 6 caracteres]**

**[Será validado que é possível fazer cadastro de um admin com sucesso e ser redirecionado para tela do admin]**

**[Será validado que é possível fazer cadastro de um cliente com sucesso e ser redirecionado para tela do cliente]**

## Cliente 

### Menu superior 

### 3 - Crie o menu top e o menu side bar

20. Todos os elementos devem respeitar os atributos descritos no protótipo para o menu superior;

21. O menu superior deve sempre ser exibido em todas as telas;

22. O título correspondente à tela em que o usuário se encontra deve ser mostrado, confome protótipos;

23. Deve haver um ícone do tipo "hambúrguer" no canto superior esquerdo do menu superior. Quando clicado, caso o menu lateral esteja oculto, deve ser mostrado. Caso contrário, o menu lateral deve ser escondido.

24. Todos os elementos devem respeitar os atributos descritos no protótipo para o menu lateral;

25. Deve conter quatro itens: `"Produtos"`, `"Meus pedidos"`, `"Meu Perfil"` e `"Sair"`;

26. Ao clicar no item `"Produtos"`, a pessoa deve ser redirecionada para a tela **Cliente - Produtos**;

27. Ao clicar no item `"Meus pedidos"`, a pessoa deve ser redirecionada para a tela **Cliente - Meus Pedidos**;

28. Ao clicar no item `"Meu Perfil"`, a pessoa deve ser redirecionada para tela **Cliente - Meu Perfil**;

29. Ao clicar no item `"Sair"`, a pessoa deve ser redirecionada para a tela **Login** e ser deslogada.

### Menu superior 

side-bar - class="side-menu-container"
titulo - data-testid="top-title"
Botão Hamburguer - data-testid="top-hamburguer"

### Menu lateral

botao produtos     - data-testid="side-menu-item-products"
botao meus pedidos - data-testid="side-menu-item-my-orders"
botao meu perfil   - data-testid="side-menu-item-my-profile"
botao sair         - data-testid="side-menu-item-logout"
o componente sidebar deve ter a seguinte classe = ".side-menu-container"

**[Será validado que os atributos do top menu devem ser mostrados confome protótipos]**

**[Será validado que ao clicar no componente hamburguer o sidebar deve ficar visível]**

**[Será validado que os atributos do side menu devem ser mostrados confome protótipos]**

**[Será validado que ao clicar no botão "produtos" será redirecionado para tela de produtos]**

**[Será validado que ao clicar no botão "meus pedidos" será redirecionado para tela de meus pedidos]**

**[Será validado que ao clicar no botão "meu perfil" será redirecionado para tela de meu perfil]**

**[Será validado que ao clicar no botão sair será redirecionado para tela home]**

### 4 - Criar tela de perfil do cliente

Esta tela possui o nome `Cliente - Meu Pefil` no protótipo.

30. Todos os elementos devem respeitar os atributos descritos no protótipo;

31. A rota da tela deve ser `/profile`;

32. Deve ter dois campos de texto: um para o `email` e o outro para o `nome`. Apenas o `nome` pode ser alterado. Dessa forma, o campo `email` deve ser `read-only`;

33. Deve ter um botão `"Salvar"`". Caso o usuário tenha editado o nome, o botão deve ser habilitado. Caso contrário, o botão deve estar desabilitado;

34. Ao clicar no botão `"Salvar"`, uma requisição deve ser feita à API e o nome da pessoa deve ser atualizado no banco de dados;

35. Ao entrar na tela, se o usuário não estiver logado, deve ser redirecionado para a tela **Login**.

input name   - data-testid="profile-name-input"
input email  - data-testid="profile-email-input"
botao salvar - data-testid="profile-save-btn"
title        - data-testid="top-title"

### Tela de perfil

**[Será validado que é possível acessar a tela de perfil do cliente]**

**[Será validado que contém os atributos descritos no protótipo]**

**[Será validado que campo email está como readonly]**

**[Será validado que o botão salvar fique desabilitado caso não altere o nome]**

**[Será validado que o botão salvar fique habilitado caso altere o nome]**

**[Será validado que é possível alterar o nome com sucesso]**

### 5 - Criar Tela de Produtos

Esta tela possui o nome `Cliente - Produtos` no protótipo.

36. Todos os elementos devem respeitar os atributos descritos no protótipo para a tela de produtos;

37. A rota da tela deve ser `/products`;

38. Nessa tela, os produtos devem ser organizados em "cards", e deve haver um card para cada produto;

39. Os cards devem conter os seguintes dados do produto:

    - Foto;

    - Nome do produto;

    - Preço unitário;

    - Quantidade atual inserida no carrinho;

    - Botão de adicionar (`+`) e de remover (`-`) uma unidade do produto no carrinho.

40. Ao clicar no botão `+`, a quantidade do produto deve aumentar em 1;

41. Ao clicar no botão `-`, a quantidade do produto deve diminuir em 1, limitado a 0;

43. Caso a pessoa atualize o browser, o carrinho deve ser mantido;

43. O preço unitário deve seguir o padrão `R$ 00,00`;

44. Quando a quantidade mostrada no card do produto chegar a 0, o produto deve ser removido do carrinho;

45. Deve ter um botão `"Ver carrinho"`. Esse botão também deve exibir o **valor total** dos produtos no carrinho;

46. O **valor total** mostrado no botão `"Ver carrinho"` deve ser alterado dinamicamente, ou seja, ao adicionar ou remover um produto no carrinho, o valor total deve ser atualizado;

47. Ao clicar no botão `"Ver carrinho"`, a pessoa deve ser redirecionada para a página **Cliente - Checkout**.

48. Ao entrar na tela, se o usuário não estiver logado, deve ser redirecionado para a tela **Login**.

card de um elemento - class="product-card"
garantir que o id mude de um produto para o outro em ordem crescente sendo o primeiro produto comecando por 0

valor do produto - data-testid="0-product-price"
imagem do produto - data-testid="0-product-img"
nome do produto - data-testid="0-product-name"
botao mais - data-testid="0-product-plus"
botao menos - data-testid="0-product-minus"
quantidade do produto - data-testid="1-product-qtd"
botao ver carrinho - data-testid="checkout-bottom-btn"
valor carrinho - data-testid="checkout-bottom-btn-value"

### Tela de produtos

**[Será validado que existe um produto na tela de produtos]**

**[Será validado que existe todos os produtos na tela de produtos]**

**[Será validado que é possíve clicar no botão "+" e atualizar o produto para 1]**

**[Será validado que é possível clicar no botão "-"e atualizar o produto para 0]**

**[Será validado que não é possível clicar no botão "-" e atualizar o produto para menor que zero]**

**[Será validado que é possível visualizar o botão "ver carrinho"]**

**[Será validado que é possível atualizar o valor do carrinho ao adicionar um produto]**

**[Será validado que é possível atualizar o valor do carrinho ao remover um produto]**

**[Será validado que ao atualizar a tela continuará na tela de produtos e carrinho com o mesmo valor]**

**[Será validado que é possível adicionar um produto e clicar no botão "ver carrinho" e ser redirecionado para tela de carrinho]**

**[Será validado que não o botão ver carrinho fique desabilitado caso não adicione nenhum produto]**

**[Será validado que não é possível acessar a tela de produtos sem estar logado e será redirecionado para tela de login]**

---

## Requisitos Entrega 2

##### Requisitos Gerais
<!-- VERIFICAR SE VALE -->
49. A cobertura de testes unitários deve ser de, no mínimo, 90%;

### 6 - Criar Tela de Checkout

Esta tela possui o nome `Cliente - Checkout` no protótipo.

50. Todos os elementos devem respeitar os atributos descritos no protótipo para a tela;

51. A rota da tela deve ser `/checkout`;

52. Caso a pessoa atualize o browser, o carrinho deve ser mantido;

53. Deve ter uma lista dos produtos selecionados com a seguinte estrutura: `quantidade do produto -- nome do produto -- valor total do produto`, sendo o valor total calculado por **quantidade * preço unitário**;

54. Ao lado de cada produto deve haver um botão que, quando clicado, exclui este produto do carrinho;

55. Abaixo da lista, mostre o **valor total do pedido**, no seguinte formato: `Total: R$ 0,00`. O valor total do pedido é calculado a partir da **soma de todos os valores totais dos produtos**;

56. Deve existir um formulário para a pessoa digitar o endereço de entrega dos produtos. O formulário deve conter dois campos de texto: um para a **rua** e o outro para o **número da casa**;

57. Deve ter um botão `"Finalizar Pedido"`. O botão deve estar habilitado **apenas** se o valor total do pedido for **maior que zero** e o endereço de entrega estiver preenchido;

58. Ao clicar em "`Finalizar pedido`", caso a operação dê certo, uma mensagem de sucesso deve ser exibida e a pessoa deve ser redirecionada para a página **Cliente - Produtos**. Caso contrário, deve ser exibido uma mensagem de erro;

59. Quando um pedido for finalizado, o carrinho deve ser esvaziado;

60. Ao entrar na tela, se o usuário não estiver logado, deve ser redirecionado para a tela **Login**.


titulo - data-testid="top-title"
quantidade do produto - data-testid="0-product-qtd-input"
nome do produto - data-testid="0-product-name"
valor do produto - data-testid="0-product-total-value"
valor unitario  - data-testid="0-product-unit-price"
botao de remover produto - data-testid="0-removal-button"
valor total - data-testid="order-total-value"
input da rua - data-testid="checkout-street-input"
numero da casa - data-testid="checkout-house-number-input"
botao finalizar pedido - data-testid="checkout-finish-btn"
mensagem de sucesso - Compra realizada com sucesso!
excluir todos os produtos aparece essa mensagem - Não há produtos no carrinho

### Tela de Checkout

**[Será validado que é possível acessar a tela de checkout]**

**[Será validado que contém atributos descritos no protótipo]**

**[Será validado que é possível ver que o produto tem quantidade, nome e valor total do produto]**

**[Será validado que é possível a lista mostrar o valor total do carrinho]**

**[Será validado que é possível fazer refresh da tela e os dados continuarem na tela]**

**[Será validado que é possível excluir um produto no checkout]**

**[Será validado que é possível o botão finalizar pedido ficar habilitado apenas quando tiver produto maior que zero e rua e numero preenchidos]**

**[Será validado que é possível fazer a compra de um produto e ao finalizar ver a mensagem de sucesso e ser redirecionado para tela de produtos]**

**[Será validado que não é possível acessar o checkout sem estar logado e será redirecionado para tela de login]**

### 7 - Criar Tela de Meus Pedidos

Esta tela possui o nome `Cliente - Meus Pedidos` no protótipo.

61. Todos os elementos devem respeitar os atributos descritos no protótipo para a tela de meus pedidos;

62. A rota da tela deve ser `/orders`;

63. Deve conter uma lista de cards, onde cada card é um pedido. Cada card deve conter as seguintes informações: `número do pedido`, `data de realização` e `valor total do pedido`. Para a data de realização do pedido, mostre apenas o dia e o mês;

64. A listagem deve mostrar os pedidos ordenados por id;

65. Ao clicar no card, a pessoa deve ser redirecionada para a página **Cliente - Detalhes do Pedido**.

66. Ao entrar na tela, se o usuário não estiver logado, deve ser redirecionado para a tela **Login**.

data-testid="top-title"
numero do pedido - data-testid="0-order-number"
data do pedido - data-testid="0-order-date"
valor do pedido - data-testid="0-order-total-value"
cards - data-testid="0-order-card-container"

### Tela de Meus Pedidos

**[Será validado que é possível acessar a tela de meus pedidos]**

**[Será validado que contém os atributos descritos no protótipo]**

**[Será validado que é possível ver que o produto tem quantidade, nome, valor total e a data da compra]**

**[Será validado que é possível clicar no card e ser redirecionado para tela do detalhe do produto]**

**[Será validado que não é possível acessar a tela de meus pedidos sem estar logado e será redirecionado para tela de login]**

<!--  -->

### 8 - Criar Tela de Detalhes Pedidos

Esta tela possui o nome `Cliente - Detalhes de Pedido` no protótipo.

67. Todos os elementos devem respeitar os atributos descritos no protótipo para a tela de detalhes do pedido;

68. A rota da página deve ser `/orders/:numero-do-pedido`;

69. Mostre o `número do pedido` e a `data de realização`. Para a data de realização do pedido, mostre apenas o dia e o mês;

70. Deve ter uma lista dos produtos selecionados com a seguinte estrutura: `quantidade do produto -- nome do produto -- valor total do produto`. Sendo o valor total calculado por **quantidade * preço unitário**;

71. Abaixo da lista, mostre o `valor total do pedido`. O valor total do pedido é calculado a partir da **soma de todos os valores totais dos produtos**.

72. Ao entrar na tela, se o usuário não estiver logado, deve ser redirecionado para a tela **Login**.

titulo - data-testid="top-title" - Detalhes de Pedido
numero do pedido - data-testid="order-number" - Pedido 1
data do pedido - data-testid="order-date" - 03/09
quantidade do produto - data-testid="0-product-qtd" - 1
nome do produto - data-testid="0-product-name" - Skol Lata 250ml
valor do produto - data-testid="0-product-total-value" - R$ 2,20
valor total da compra - data-testid="order-total-value" - Total: R$ 2,20
url - http://localhost:3000/orders/1

### Tela de detalhes de pedido

**[Será validado que é possível acessar a tela do detalhe do pedido]**

**[Será validado que contém os atributos descritos no protótipo]**

**[Será validado que é possível ver que tem numero do pedido e a data da compra]**

**[Será validado que é possível ver que o produto tem quantidade, nome e valor total do produto]**

**[Será validado que é possível ver o valor total do pedido]**

**[Será validado que não é possível acessar a tela de meus pedidos sem estar logado e será redirecionado para tela de login]**

## Administrador

### 9 - Criar menu side bar para Administrador

73. Todos os elementos devem respeitar os atributos descritos no protótipo para o menu lateral;

74. Deve conter três itens: `"Pedidos"`", `"Perfil"`" e "`Sair`";

75. Ao clicar no item `"Pedidos"`, a pessoa deve ser redirecionada para a tela **Admin - Home**;

76. Ao clicar no item `"Perfil"`, a pessoa deve ser redirecionada para tela **Admin - Perfil**;

77. Ao clicar no item `"Sair"`, a pessoa deve ser redirecionada para a tela **Login** e ser deslogada.

url http://localhost:3000/admin/orders

side bar - class - admin-side-bar-container

botao meus pedidos - data-testid="side-menu-item-orders"
botao meu perfil - data-testid="side-menu-item-profile"
botao logout - data-testid="side-menu-item-logout"

### Menu lateral Administrador

**[Será validado que o sidebar devem ser mostrados, conforme protótipos]**

**[Será validado que ao clicar no menu meus pedidos será redirecionado para tela de meus pedidos']**

**[Será validado que ao clicar no menu meus perfil será redirecionado para tela de meus perfil]**

**[Será validado que ao clicar no menu sair será redirecionado para tela home]**

### 10 - Criar tela de perfil de Administrador

Esta tela possui o nome `Admin - Perfil` no protótipo.

78. Todos os elementos devem respeitar os atributos descritos no protótipo para a tela de perfil;

79. A rota da página deve ser `/admin/profile`;

80. Mostrar o `email` e o `nome` do usuário. Não permita que o usuário edite os dados;

81. Ao entrar na tela, se o usuário não estiver logado, deve ser redirecionado para a tela **Login**.

texto - Perfil
url - `/admin/profile`
campo email - data-testid="profile-email"
campo nome - data-testid="profile-name"

### Tela de perfil Administrador

**[Será validado que é possível acessar a tela do perfil do administrador]**

**[Será validado que a tela de perfil contém os atributos descritos no protótipo]**

**[Será validado que a tela de perfil contém o email e nome do administrador]**

**[Será validado que não é possível acessar a tela sem estar autenticado e ser redirecionado para tela de login]**

### 11 - Criar tela de pedidos de admin

Esta tela possui o nome `Admin - Pedidos` no protótipo.

82. Todos os elementos devem respeitar os atributos descritos no protótipo para a tela de pedidos;

83. A rota da página deve ser `/admin/orders`;

84. Essa tela deve mostrar todos os pedidos feitos;

85. Os pedidos pendentes devem ter o label `Pendentes`, ao passo que os pedidos entregues devem ter o label `Entregue`;

86. Pedidos pendentes devem ser listados antes dos pedidos entregues

87. Os "cards" dos pedidos devem conter as informações:

    - Número do pedido;

    - Endereço para entrega;

    - Valor total do pedido.

88. Ao clicar em qualquer parte do card do pedido, a pessoa deve ser redirecionada para a tela `Admin - Detalhe de Pedido`.

numero do pedido - data-testid="0-order-number"
endereco do pedido - data-testid="0-order-address"
valor total do pedido - data-testid="0-order-total-value"
status - data-testid="0-order-status"

### Tela de Pedidos

**[Será validado que é possível acessar a tela do pedidos do administrador]**

**[Será validado que a tela de pedidos contém os atributos descritos no protótipo]**

**[Será validado que os dados do card estão corretos]**

**[Será validado que é possível clicar no card do produto e ser redirecionado para tela de detalhes do produto]**

### 12 - Criar tela de Detalhes de admin

Essa página corresponde às páginas `Admin - Detalhes de Pedido - Pendente` e `Admin - Detalhes de Pedido - Entregue` no protótipo.

89. Todos os elementos devem respeitar os atributos descritos no protótipo para a tela de detalhes do pedido;

90. A rota da página deve ser `/admin/orders/:id`;

91. No cabeçalho, mostre o `número do pedido` e o `status` atual - Pendente ou Entregue;

92. Deve ter uma listagem com os produtos do pedido, onde cada linha deve conter:

    - Quantidade;

    - Nome do produto;

    - Valor total do produto.

93. O `preço total` do produto é calculado usando **quantidade * preço unitário**;

94. Mostre também o `valor total do pedido`. O valor total do pedido é calculado a partir da **soma de todos os valores totais dos produtos**;

95. Caso o status do pedido seja **pendente**, um botão para marcar o pedido como entregue deve ser exibido. Caso contrário, não exiba o botão;

96. Ao clicar no botão `"Marcar pedido como entregue"`, o status desse pedido deve mudar para `Entregue` e o botão deve desaparecer.

numero do pedido - data-testid="order-number"
nome do pedido - data-testid="0-product-name"
valor tota do produto - data-testid="0-product-total-value"
valor unitario - data-testid="order-unit-price"
valor total do pedido - data-testid="order-total-value"

### Tela de Detalhes de Pedido

**[]**
**[]**
**[]**
**[]**
**[]**

### Bônus

### 13 - Cobertura de testes unitários

97. Escreva testes unitários com cobertura de, no mínimo, 90%, considerando front-end e back-end;

---

## Instruções para entregar seu projeto:

### ANTES DE COMEÇAR A DESENVOLVER:

1. Clone o repositório

- `git clone git@github.com:tryber/trybeer-project.git`.
- Entre na pasta do repositório que você acabou de clonar:
  - `cd trybeer-project`

2. Instale as dependências do front-end e do back-end

- Instale as dependências do front-end e inicie o servidor
  - `cd front-end`
  - `npm install`
  - `npm start` (uma nova página deve abrir no seu navegador com um texto simples)
- Instale as dependências do back-end
  - `cd back-end`
  - `npm install`

3. Crie uma branch a partir da branch `master`

- Verifique que você está na branch `master`
  - Exemplo: `git branch`
- Se não estiver, mude para a branch `master`
  - Exemplo: `git checkout master`
- Agora, crie uma branch onde você vai guardar os `commits` do seu projeto
  - Você deve criar uma branch no seguinte formato: `nome-de-usuário-nome-do-projeto`
  - Exemplo: `git checkout -b joaozinho-trybeer`

5. Adicione as mudanças ao _stage_ do Git e faça um `commit`

- Verifique que as mudanças ainda não estão no _stage_
  - Exemplo: `git status` (deve aparecer listada a pasta _components_ em vermelho)
- Adicione o novo arquivo ao _stage_ do Git
  - Exemplo:
    - `git add .` (adicionando todas as mudanças - _que estavam em vermelho_ - ao stage do Git)
    - `git status` (deve aparecer listado o arquivo _components/Header.jsx_ em verde)
- Faça o `commit` inicial
  - Exemplo:
    - `git commit -m 'iniciando o projeto'` (fazendo o primeiro commit)
    - `git status` (deve aparecer uma mensagem tipo _nothing to commit_ )

6. Adicione a sua branch com o novo `commit` ao repositório remoto

- Usando o exemplo anterior: `git push -u origin joaozinho-trybeer`

7. Crie um novo `Pull Request` _(PR)_

- Vá até a página de _Pull Requests_ do [repositório no GitHub](https://github.com/tryber/trybeer-project/pulls)
- Clique no botão verde _"New pull request"_
- Clique na caixa de seleção _"Compare"_ e escolha a sua branch **com atenção**
- Clique no botão verde _"Create pull request"_
- Adicione uma descrição para o _Pull Request_ e clique no botão verde _"Create pull request"_
- **Não se preocupe em preencher mais nada por enquanto!**
- Volte até a [página de _Pull Requests_ do repositório](https://github.com/tryber/trybeer-project/pulls) e confira que o seu _Pull Request_ está criado

---

### DURANTE O DESENVOLVIMENTO

- ⚠ **LEMBRE-SE DE CRIAR TODOS OS ARQUIVOS DENTRO DA PASTA COM O SEU NOME** ⚠

* Faça `commits` das alterações que você fizer no código regularmente

* Lembre-se de sempre após um (ou alguns) `commits` atualizar o repositório remoto

* Os comandos que você utilizará com mais frequência são:
  1. `git status` _(para verificar o que está em vermelho - fora do stage - e o que está em verde - no stage)_
  2. `git add` _(para adicionar arquivos ao stage do Git)_
  3. `git commit` _(para criar um commit com os arquivos que estão no stage do Git)_
  4. `git push -u nome-da-branch` _(para enviar o commit para o repositório remoto na primeira vez que fizer o `push` de uma nova branch)_
  5. `git push` _(para enviar o commit para o repositório remoto após o passo anterior)_

---

### DEPOIS DE TERMINAR O DESENVOLVIMENTO

Para **"entregar"** seu projeto, siga os passos a seguir:

- Vá até a página **DO SEU** _Pull Request_, adicione a label de _"code-review"_ e marque seus colegas
  - No menu à direita, clique no _link_ **"Labels"** e escolha a _label_ **code-review**
  - No menu à direita, clique no _link_ **"Assignees"** e escolha **o seu usuário**
  - No menu à direita, clique no _link_ **"Reviewers"** e digite `students`, selecione o time `tryber/students-sd-01`

Se ainda houver alguma dúvida sobre como entregar seu projeto, [aqui tem um video explicativo](https://vimeo.com/362189205).

---

### REVISANDO UM PULL REQUEST

⚠⚠⚠

À medida que você e os outros alunos forem entregando os projetos, vocês serão alertados **via Slack** para também fazer a revisão dos _Pull Requests_ dos seus colegas. Fiquem atentos às mensagens do _"Pull Reminders"_ no _Slack_!

Os monitores também farão a revisão de todos os projetos, e irão avaliar tanto o seu _Pull Request_, quanto as revisões que você fizer nos _Pull Requests_ dos seus colegas!!!

Use o material que você já viu sobre [Code Review](https://course.betrybe.com/real-life-engineer/code-review/) para te ajudar a revisar os projetos que chegaram para você.
