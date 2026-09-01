**CASOS DE TESTE**  
saucedemo.com \- Testes Manuais  
v1.0 \- Autor: Matheus Ribeiro Modesto \- 08/08/2026

## 1.  Resumo dos casos de teste  
   

| ID | Título | Funcionalidade | Tipo de teste | Prioridade |
| :---- | :---- | :---- | :---- | :---- |
| TC-01 | Realizar login com usuário válido | Autenticação | Funcional / Smoke | **P1** |
| TC-02 | Realizar login com usuário inválido | Autenticação | Negativo | **P1** |
| TC-03 | Realizar logout do sistema | Logout | Funcional | **P2** |
| TC-04 | Exibir produtos corretamente no catálogo | Exibição de produtos | Funcional | **P1** |
| TC-05 | Exibir nome correto dos produtos | Exibição de produtos | Funcional | **P2** |
| TC-06 | Exibir descrição correta dos produtos | Exibição de produtos | Funcional | **P2** |
| TC-07 | Ordenar produtos usando filtros disponíveis | Ordenação | Funcional | **P2** |
| TC-08 | Acessar detalhes de um produto | Detalhes de produto | Funcional | **P2** |
| TC-09 | Adicionar produto ao carrinho | Carrinho | Funcional | **P1** |
| TC-10 | Remover produto do carrinho | Carrinho | Funcional | **P1** |
| TC-11 | Exibir produtos adicionados ao carrinho | Carrinho | Funcional | **P1** |
| TC-12 | Calcular corretamente valor do carrinho | Carrinho | Funcional | **P1** |
| TC-13 | Atualizar valor do carrinho após remoção de produto | Carrinho | Funcional | **P1** |
| TC-14 | Seguir para checkout com o carrinho vazio | Carrinho | Negativo | **P2** |
| TC-15 | Preencher campo First Name no Checkout | Checkout | Positivo | **P1** |
| TC-16 | Preencher campo Last Name no Checkout | Checkout | Positivo | **P1** |
| TC-17 | Preencher campo Zip Code no Checkout | Checkout | Positivo | **P1** |
| TC-18 | Validar entrada de números e caracteres especiais no campo First Name | Checkout | Negativo | **P1** |
| TC-19 | Validar entrada de números e caracteres no campo Last Name | Checkout | Negativo | **P1** |
| TC-20 | Validar entrada de letras e caracteres especiais no campo Zip Code | Checkout | Negativo | **P1** |
| TC-21 | Avançar para o resumo do pedido | Checkout | Funcional | **P1** |
| TC-22 | Finalizar pedido | Checkout | Funcional | **P1** |
| TC-23 | Exibir confirmação após finalizar pedido | Checkout | Funcional | **P1** |
| TC-24 | Gerar PDF do pedido | Contato | Funcional | **P3** |
| TC-25 | Retornar para Home após finalizar pedido | Navegação | Funcional | **P2** |

## 2.  Detalhamento dos casos de teste  
 


| TC-01: Realizar login com usuário válido |  |
| :---- | :---- |
| **Funcionalidade** | Autenticação |
| **Tipo de Teste** | Funcional / Smoke |
| **Tipo de Cenário** | Happy Path |
| **Prioridade** | **P1** |
| **Pré-condições** | Usuário deve possuir credenciais válidas e estar na página de login do sistema.  |
| **Passo a Passo** | Acessar a página de login \> Informar um usuário válido no campo de usuário \> Informar uma senha válida no campo de senha \> Clicar no botão Login \> Verificar a página apresentada após a autenticação.  |
| **Resultado esperado** | O sistema deve validar as credenciais informadas, autenticar o usuário com sucesso e redirecioná-lo para a página principal do catálogo de produtos.  |
| **Resultado obtido** | O login foi realizado com sucesso utilizando credenciais válidas, e o usuário foi redirecionado para o catálogo de produtos.  |
| **Massa de dados:** | Usuário: standard\_user \- Senha: secret\_sauce |

| TC-02: Realizar login com usuário inválido |  |
| :---- | :---- |
| **Funcionalidade** | Autenticação |
| **Tipo de Teste** | Negativo |
| **Tipo de Cenário** | Negativo |
| **Prioridade** | **P1** |
| **Pré-condições** | O tester deve estar na página de login e inserir dados invalidos de login e senha.   |
| **Passo a Passo** | Acessar a página de login \> Informar usuário inexistente \> Clicar no botão **Login** \> Observar o comportamento apresentado pelo sistema.  |
| **Resultado esperado** | O sistema deve impedir a autenticação do usuário inexistente e exibir uma mensagem informando que o usuário não possui permissão para realizar o login |
| **Resultado obtido** | O sistema impediu o acesso do usuário e apresentou uma mensagem informando que os dados são inválidos |
| **Massa de dados:** | Usuário: invalid\_user \- Senha: 123 |

| TC-03: Realizar logout do sistema |  |
| :---- | :---- |
| **Funcionalidade** | Logout |
| **Tipo de Teste** | Negativo |
| **Tipo de Cenário** | Negativo |
| **Prioridade** | **P2** |
| **Pré-condições** | Usuário deve estar autenticado no sistema e na página principal do catálogo de produtos.  |
| **Passo a Passo** | Realizar login utilizando credenciais válidas \> Localizar a opção **Logout** no menu do sistema \> Clicar em **Logout** \> Verificar a página apresentada após o encerramento da sessão.  |
| **Resultado esperado** | O sistema deve encerrar a sessão do usuário e redirecioná-lo para a página de login, impedindo o acesso às funcionalidades que exigem autenticação.  |
| **Resultado obtido** | A sessão do usuário foi encerrada com sucesso e o sistema redirecionou o usuário para a página de login.  |
| **Massa de dados:** | Usuário: standard\_user \- Senha: secret\_sauce |

| TC-04: Exibir produtos corretamente no catálogo |  |
| :---- | :---- |
| **Funcionalidade** | Exibição de produtos |
| **Tipo de Teste** | Funcional |
| **Tipo de Cenário** | Happy Path |
| **Prioridade** | **P1** |
| **Pré-condições** | Usuário deve estar autenticado no sistema e na página de produtos.  |
| **Passo a Passo** | Acessar a página de login \> Informar credenciais válidas \> Clicar no botão **Login** \> Acessar o catálogo de produtos \> Verificar os produtos apresentados na página.  |
| **Resultado esperado** | O sistema deve exibir corretamente os produtos disponíveis no catálogo, apresentando os itens de forma adequada e permitindo sua visualização pelo usuário.  |
| **Resultado obtido** | Os produtos foram exibidos corretamente no catálogo, permitindo sua visualização pelo usuário.   |
| **Massa de dados:** | Usuário: standard\_user \- Senha: secret\_sauce |

| TC-05: Exibir nome correto dos produtos |  |
| :---- | :---- |
| **Funcionalidade** | Exibição de produtos  |
| **Tipo de Teste** | Funcional |
| **Tipo de Cenário** | Happy Path |
| **Prioridade** | **P2** |
| **Pré-condições** | Usuário deve estar autenticado no sistema e na página de produtos. |
| **Passo a Passo** | Acessar a página de login \> Informar credenciais válidas \> Clicar no botão **Login** \> Acessar o catálogo de produtos \> Verificar o nome apresentado em cada produto \> Comparar os nomes exibidos com os nomes esperados.  |
| **Resultado esperado** | O sistema deve apresentar o nome correto de cada produto, sem alterações, erros de grafia ou informações divergentes dos dados cadastrados.  |
| **Resultado obtido** | Os nomes dos produtos foram apresentados corretamente, sem divergências em relação às informações esperadas.  |
| **Massa de dados:** | Usuário: standard\_user \- Senha: secret\_sauce |

| TC-06: Exibir descrição correta dos produtos |  |
| :---- | :---- |
| **Funcionalidade** | Exibição de produtos  |
| **Tipo de Teste** | Funcional |
| **Tipo de Cenário** | Happy Path |
| **Prioridade** | **P2** |
| **Pré-condições** | Usuário deve estar autenticado no sistema e na página de produtos. |
| **Passo a Passo** | Acessar a página de login \> Informar credenciais válidas \> Clicar no botão **Login** \> Acessar o catálogo de produtos \> Verificar a descrição apresentada em cada produto \> Comparar as descrições exibidas com as informações esperadas.  |
| **Resultado esperado** | O sistema deve apresentar a descrição correta de cada produto, com informações correspondentes ao produto exibido e sem divergências nos dados apresentados.  |
| **Resultado obtido** | As descrições dos produtos foram apresentadas corretamente, sem divergências em relação às informações esperadas.  |
| **Massa de dados:** | Usuário: standard\_user \- Senha: secret\_sauce |

| TC-07: Ordenar produtos usando filtros disponíveis |  |
| :---- | :---- |
| **Funcionalidade** | Ordenação |
| **Tipo de Teste** | Funcional |
| **Tipo de Cenário** | Fluxo alternativo |
| **Prioridade** | **P2** |
| **Pré-condições** | Usuário deve estar autenticado no sistema e na página de produtos. O catálogo deve possuir produtos disponíveis para ordenação.  |
| **Passo a Passo** | Acessar a página de login \> Informar credenciais válidas \> Clicar no botão **Login** \> Acessar o catálogo de produtos \> Localizar o campo de ordenação \> Selecionar uma das opções disponíveis \> Verificar a ordem dos produtos apresentada.  |
| **Resultado esperado** | O sistema deve reorganizar os produtos de acordo com o critério de ordenação selecionado pelo usuário.  |
| **Resultado obtido** | Os produtos foram reorganizados corretamente de acordo com o critério de ordenação selecionado.  |
| **Massa de dados:** | Usuário: standard\_user \- Senha: secret\_sauce |

| TC-08: Acessar detalhes de um produto |  |
| :---- | :---- |
| **Funcionalidade** | Detalhes do produto |
| **Tipo de Teste** | Funcional |
| **Tipo de Cenário** | Happy path |
| **Prioridade** | **P2** |
| **Pré-condições** | Usuário deve estar autenticado no sistema e na página de produtos. Deve haver pelo menos um produto disponível no catálogo.  |
| **Passo a Passo** | Acessar a página de login \> Informar credenciais válidas \> Clicar no botão **Login** \> Acessar o catálogo de produtos \> Selecionar um produto \> Clicar no produto para acessar seus detalhes \> Verificar as informações apresentadas.  |
| **Resultado esperado** | O sistema deve direcionar o usuário para a página de detalhes do produto selecionado e apresentar corretamente suas informações, como nome, descrição, preço e imagem.  |
| **Resultado obtido** | O sistema direcionou o usuário para os detalhes do produto selecionado, apresentando corretamente as informações disponíveis sobre o item.  |
| **Massa de dados:** | Usuário: standard\_user \- Senha: secret\_sauce |

| TC-09: Adicionar produto ao carrinho |  |
| :---- | :---- |
| **Funcionalidade** | Carrinho  |
| **Tipo de Teste** | Funcional |
| **Tipo de Cenário** | Happy path |
| **Prioridade** | **P1** |
| **Pré-condições** | Usuário deve estar autenticado no sistema e na página de produtos. Deve haver pelo menos um produto disponível no catálogo.  |
| **Passo a Passo** | Acessar a página de login \> Informar credenciais válidas \> Clicar no botão **Login** \> Selecionar um produto disponível \> Clicar no botão **Add to cart** \> Verificar o indicador do carrinho e a inclusão do produto.  |
| **Resultado esperado** | O sistema deve adicionar o produto selecionado ao carrinho e atualizar o indicador do carrinho, refletindo a quantidade de itens adicionados.  |
| **Resultado obtido** | O produto selecionado foi adicionado corretamente ao carrinho e o indicador do carrinho foi atualizado.  |
| **Massa de dados:** | Usuário: standard\_user \- Senha: secret\_sauce |

| TC-10: Remover produto do carrinho |  |
| :---- | :---- |
| **Funcionalidade** | Carrinho  |
| **Tipo de Teste** | Funcional |
| **Tipo de Cenário** | Fluxo alternativo |
| **Prioridade** | **P1** |
| **Pré-condições** | Usuário deve estar autenticado no sistema e possuir pelo menos um produto previamente adicionado ao carrinho.  |
| **Passo a Passo** | Acessar a página de login \> Informar credenciais válidas \> Clicar no botão **Login** \> Adicionar um produto ao carrinho \> Acessar o carrinho \> Localizar o produto adicionado \> Clicar no botão **Remove** \> Verificar o conteúdo do carrinho.  |
| **Resultado esperado** | O sistema deve remover o produto selecionado do carrinho e atualizar a quantidade de itens exibida no indicador do carrinho.  |
| **Resultado obtido** | O produto selecionado foi removido corretamente do carrinho e o indicador de quantidade de itens foi atualizado.  |
| **Massa de dados:** | Usuário: standard\_user \- Senha: secret\_sauce |

| TC-11: Exibir produtos adicionados ao carrinho |  |
| :---- | :---- |
| **Funcionalidade** | Carrinho  |
| **Tipo de Teste** | Funcional |
| **Tipo de Cenário** | Happy Path |
| **Prioridade** | **P1** |
| **Pré-condições** | Usuário deve estar autenticado no sistema e possuir pelo menos um produto adicionado ao carrinho.  |
| **Passo a Passo** | Acessar a página de login \> Informar credenciais válidas \> Clicar no botão **Login** \> Selecionar um produto \> Clicar no botão **Add to cart** \> Acessar o carrinho \> Verificar os produtos apresentados.  |
| **Resultado esperado** | O sistema deve apresentar no carrinho todos os produtos previamente adicionados pelo usuário, exibindo corretamente as informações correspondentes aos itens selecionados.  |
| **Resultado obtido** | O produto adicionado foi apresentado corretamente no carrinho, com as informações correspondentes ao item selecionado.  |
| **Massa de dados:** | Usuário: standard\_user \- Senha: secret\_sauce |

| TC-12: Calcular corretamente valor do carrinho |  |
| :---- | :---- |
| **Funcionalidade** | Carrinho  |
| **Tipo de Teste** | Funcional |
| **Tipo de Cenário** | Happy Path |
| **Prioridade** | **P1** |
| **Pré-condições** | Usuário deve estar autenticado no sistema e possuir pelo menos um produto adicionado ao carrinho.  |
| **Passo a Passo** | Acessar a página de login \> Informar credenciais válidas \> Clicar no botão **Login** \> Adicionar um ou mais produtos ao carrinho \> Acessar o carrinho \> Identificar os preços dos produtos adicionados \> Somar os valores dos produtos \> Comparar o valor calculado manualmente com o valor apresentado pelo sistema.  |
| **Resultado esperado** | O sistema deve apresentar o valor total do carrinho corretamente, correspondendo à soma dos preços dos produtos adicionados.  |
| **Resultado obtido** | O valor apresentado pelo sistema correspondeu corretamente à soma dos preços dos produtos adicionados ao carrinho.  |
| **Massa de dados:** | Usuário: standard\_user \- Senha: secret\_sauce |

| TC-13: Atualizar valor do carrinho após remoção de produto |  |
| :---- | :---- |
| **Funcionalidade** | Carrinho  |
| **Tipo de Teste** | Funcional |
| **Tipo de Cenário** | Fluxo Alternativo  |
| **Prioridade** | **P1** |
| **Pré-condições** | Usuário deve estar autenticado no sistema e possuir pelo menos dois produtos adicionados ao carrinho.  |
| **Passo a Passo** | Acessar a página de login \> Informar credenciais válidas \> Clicar no botão **Login** \> Adicionar dois ou mais produtos ao carrinho \> Acessar o carrinho \> Registrar o valor total apresentado \> Remover um dos produtos \> Verificar o novo valor total apresentado.  |
| **Resultado esperado** | O sistema deve remover o produto selecionado e atualizar o valor total do carrinho, subtraindo o valor correspondente ao produto removido.  |
| **Resultado obtido** | Após a remoção do produto, o valor total do carrinho foi atualizado corretamente, refletindo apenas os produtos restantes.  |
| **Massa de dados:** | Usuário: standard\_user \- Senha: secret\_sauce |

| TC-14: Seguir para checkout com o carrinho vazio |  |
| :---- | :---- |
| **Funcionalidade** | Carrinho |
| **Tipo de Teste** | Negativo |
| **Tipo de Cenário** | Negativo  |
| **Prioridade** | **P2** |
| **Pré-condições** | Usuário deve estar autenticado no sistema e não possuir nenhum produto adicionado ao carrinho.  |
| **Passo a Passo** | Acessar a página de login > Informar credenciais válidas > Clicar no botão Login > Acessar o carrinho > Verificar que não existem produtos adicionados > Tentar prosseguir para o Checkout > Observar o comportamento apresentado pelo sistema.  |
| **Resultado esperado** | O sistema deve impedir o avanço para o Checkout quando o carrinho estiver vazio e apresentar uma mensagem ou comportamento indicando que é necessário adicionar pelo menos um produto antes de prosseguir.  |
| **Resultado obtido** | Mesmo com o carrinho vazio, o sistema permite avançar para a finalização do pedido sem nenhum aviso ou mensagem de erro  |
| **Massa de dados:** | Usuário: standard\_user \- Senha: secret\_sauce |

| TC-15: Preencher campo First Name no Checkout  |  |
| :---- | :---- |
| **Funcionalidade** | Checkout |
| **Tipo de Teste** | Funcional |
| **Tipo de Cenário** | Positivo |
| **Prioridade** | **P1** |
| **Pré-condições** | Usuário deve estar autenticado e possuir pelo menos um produto adicionado ao carrinho. O usuário deve estar na etapa de informações do Checkout.  |
| **Passo a Passo** | Acessar a página de login \> Informar credenciais válidas \> Clicar no botão **Login** \> Adicionar um produto ao carrinho \> Acessar o carrinho \> Clicar em **Checkout** \> Informar um nome válido no campo **First Name** \> Verificar o valor inserido no campo.  |
| **Resultado esperado** | O sistema deve permitir o preenchimento do campo **First Name** com um nome válido e manter corretamente a informação inserida.  |
| **Resultado obtido** | O campo **First Name** aceitou o nome informado e manteve corretamente o valor inserido.  |
| **Massa de dados:** | Usuário: standard\_user \- Senha: secret\_sauce - First Name: Matheus |

| TC-16: Preencher campo Last Name no Checkout  |  |
| :---- | :---- |
| **Funcionalidade** | Checkout |
| **Tipo de Teste** | Funcional |
| **Tipo de Cenário** | Positivo |
| **Prioridade** | **P1** |
| **Pré-condições** | Usuário deve estar autenticado e possuir pelo menos um produto adicionado ao carrinho. O usuário deve estar na etapa de informações do Checkout.  |
| **Passo a Passo** | Acessar a página de login \> Informar credenciais válidas \> Clicar no botão **Login** \> Adicionar um produto ao carrinho \> Acessar o carrinho \> Clicar em **Checkout** \> Informar um sobrenome válido no campo **Last Name** \> Verificar o valor inserido no campo.  |
| **Resultado esperado** | O sistema deve permitir o preenchimento do campo **Last Name** com um sobrenome válido e manter corretamente a informação inserida.  |
| **Resultado obtido** | O campo **Last Name** aceitou o sobrenome informado e manteve corretamente o valor inserido.  |
| **Massa de dados:** | Usuário: standard\_user \- Senha: secret\_sauce - Last Name: Modesto |

| TC-17 — Preencher campo Zip Code no Checkout |  |
| :---- | :---- |
| **Funcionalidade** | Checkout |
| **Tipo de Teste** | Funcional |
| **Tipo de Cenário** | Positivo |
| **Prioridade** | **P1** |
| **Pré-condições** | Usuário deve estar autenticado e possuir pelo menos um produto adicionado ao carrinho. O usuário deve estar na etapa de informações do Checkout.  |
| **Passo a Passo** | Acessar a página de login \> Informar credenciais válidas \> Clicar no botão **Login** \> Adicionar um produto ao carrinho \> Acessar o carrinho \> Clicar em **Checkout** \> Informar um código postal válido no campo **Zip Code** \> Verificar o valor inserido no campo.  |
| **Resultado esperado** | O sistema deve permitir o preenchimento do campo **Zip Code** com um código postal válido e manter corretamente a informação inserida.  |
| **Resultado obtido** | O campo **Zip Code** aceitou o código postal informado e manteve corretamente o valor inserido.  |
| **Massa de dados:** | Usuário: standard\_user \- Senha: secret\_sauce - ZipCode 11111111 (fictício porém factível) |

| TC-18: Validar entrada de  números e caracteres especiais no campo First Name  |  |
| :---- | :---- |
| **Funcionalidade** | Checkout |
| **Tipo de Teste** | Negativo |
| **Tipo de Cenário** | Negativo |
| **Prioridade** | **P1** |
| **Pré-condições** | Usuário deve estar autenticado e possuir pelo menos um produto adicionado ao carrinho. O usuário deve estar na etapa de informações do Checkout.  |
| **Passo a Passo** |Acessar a página de login > Informar credenciais válidas > Clicar no botão Login > Adicionar um produto ao carrinho > Acessar o carrinho > Clicar em Checkout > Informar um valor inválido no campo First Name > Preencher os demais campos obrigatórios com dados válidos > Tentar avançar para a próxima etapa > Observar o comportamento apresentado pelo sistema.  |
| **Resultado esperado** | O sistema deve identificar a entrada inválida no campo **First Name**, impedir o avanço do Checkout e apresentar uma mensagem de validação adequada ao usuário.  |
| **Resultado obtido** | O sistema permite avanço para finalização de compra.  |
| **Massa de dados:** | Usuário: standard\_user \- Senha: secret\_sauce - First Name: 123|

| TC-19: Validar entrada de números e caracteres especiais no campo Last Name  |  |
| :---- | :---- |
| **Funcionalidade** | Checkout |
| **Tipo de Teste** | Negativo |
| **Tipo de Cenário** | Negativo |
| **Prioridade** | **P1** |
| **Pré-condições** | Usuário deve estar autenticado e possuir pelo menos um produto adicionado ao carrinho. O usuário deve estar na etapa de informações do Checkout.  |
| **Passo a Passo** | Acessar a página de login \> Informar credenciais válidas \> Clicar no botão **Login** \> Adicionar um produto ao carrinho \> Acessar o carrinho \> Clicar em **Checkout** \> Informar um valor inválido no campo **Last Name** \> Preencher os demais campos obrigatórios com dados válidos \> Tentar avançar para a próxima etapa \> Observar o comportamento apresentado pelo sistema.  |
| **Resultado esperado** | O sistema deve identificar a entrada inválida no campo **Last Name**, impedir o avanço do Checkout e apresentar uma mensagem de validação adequada ao usuário.  |
| **Resultado obtido** | O sistema permite avanço para finalização de compra.  |
| **Massa de dados:** | Usuário: standard\_user \- Senha: secret\_sauce - Last Name: 4 |

| TC-20: Validar entrada de letras e caracteres especiais no campo Zip Code  |  |
| :---- | :---- |
| **Funcionalidade** | Checkout |
| **Tipo de Teste** | Negativo |
| **Tipo de Cenário** | Negativo |
| **Prioridade** | **P1** |
| **Pré-condições** | Usuário deve estar autenticado e possuir pelo menos um produto adicionado ao carrinho. O usuário deve estar na etapa de informações do Checkout.  |
| **Passo a Passo** | Acessar a página de login \> Informar credenciais válidas \> Clicar no botão **Login** \> Adicionar um produto ao carrinho \> Acessar o carrinho \> Clicar em **Checkout** \> Informar um valor inválido no campo **Zip Code** \> Preencher os demais campos obrigatórios com dados válidos \> Tentar avançar para a próxima etapa \> Observar o comportamento apresentado pelo sistema.  |
| **Resultado esperado** | O sistema deve identificar a entrada inválida no campo **Zip Code**, impedir o avanço do Checkout e apresentar uma mensagem de validação adequada ao usuário.  |
| **Resultado obtido** | O sistema permite avanço para finalização de compra.  |
| **Massa de dados:** | Usuário: standard\_user \- Senha: secret\_sauce - ZipCode - asdsa|

| TC-21:Avançar para o resumo do pedido  |  |
| :---- | :---- |
| **Funcionalidade** | Checkout |
| **Tipo de Teste** | Funcional |
| **Tipo de Cenário** | Happy Path |
| **Prioridade** | **P1** |
| **Pré-condições** | Usuário deve estar autenticado, possuir pelo menos um produto no carrinho e estar na etapa de informações do Checkout. Os campos obrigatórios devem estar preenchidos com dados válidos.  |
| **Passo a Passo** | Acessar a página de login \> Informar credenciais válidas \> Clicar no botão **Login** \> Adicionar um produto ao carrinho \> Acessar o carrinho \> Clicar em **Checkout** \> Preencher os campos **First Name**, **Last Name** e **Zip Code** com dados válidos \> Clicar no botão **Continue** \> Verificar a página apresentada.  |
| **Resultado esperado** | O sistema deve validar os dados informados e direcionar o usuário para a página de resumo do pedido, apresentando corretamente os produtos e valores da compra.  |
| **Resultado obtido** | O sistema validou os dados informados e direcionou o usuário corretamente para a página de resumo do pedido, apresentando as informações da compra.  |
| **Massa de dados:** | Usuário: standard\_user \- Senha: secret\_sauce |

| TC-22: Finalizar pedido  |  |
| :---- | :---- |
| **Funcionalidade** | Checkout |
| **Tipo de Teste** | Funcional |
| **Tipo de Cenário** | Happy Path |
| **Prioridade** | **P1** |
| **Pré-condições** | Usuário deve estar autenticado, possuir pelo menos um produto no carrinho e estar na página de resumo do pedido. Os dados do Checkout devem ter sido preenchidos corretamente.  |
| **Passo a Passo** | Acessar a página de login \> Informar credenciais válidas \> Clicar no botão **Login** \> Adicionar um produto ao carrinho \> Acessar o carrinho \> Clicar em **Checkout** \> Preencher os campos **First Name**, **Last Name** e **Zip Code** com dados válidos \> Clicar no botão **Continue** \> Verificar o resumo do pedido \> Clicar no botão **Finish** \> Observar o comportamento apresentado pelo sistema.  |
| **Resultado esperado** | O sistema deve processar a finalização do pedido com sucesso e direcionar o usuário para a página de confirmação da compra.  |
| **Resultado obtido** | O pedido foi finalizado com sucesso e o sistema direcionou o usuário para a página de confirmação da compra.  |
| **Massa de dados:** | Usuário: standard\_user \- Senha: secret\_sauce |

| TC-23: Exibir confirmação após finalizar pedido  |  |
| :---- | :---- |
| **Funcionalidade** | Checkout |
| **Tipo de Teste** | Funcional |
| **Tipo de Cenário** | Happy Path |
| **Prioridade** | **P1** |
| **Pré-condições** | Usuário deve estar autenticado e possuir um pedido finalizado com sucesso. O usuário deve estar na página apresentada após a finalização do pedido.  |
| **Passo a Passo** | Acessar a página de login \> Informar credenciais válidas \> Clicar no botão **Login** \> Adicionar um produto ao carrinho \> Acessar o carrinho \> Clicar em **Checkout** \> Preencher os campos **First Name**, **Last Name** e **Zip Code** com dados válidos \> Clicar no botão **Continue** \> Verificar o resumo do pedido \> Clicar no botão **Finish** \> Verificar a mensagem e as informações apresentadas após a finalização.  |
| **Resultado esperado** | O sistema deve apresentar uma página de confirmação informando que o pedido foi concluído com sucesso e apresentar as informações correspondentes à finalização da compra.  |
| **Resultado obtido** | O sistema apresentou corretamente a página de confirmação após a finalização do pedido, informando que a compra foi concluída com sucesso.  |
| **Massa de dados:** | Usuário: standard\_user \- Senha: secret\_sauce |

| TC-24: Gerar PDF do pedido |  |
| :---- | :---- |
| **Funcionalidade** | Contato  |
| **Tipo de Teste** | Funcional |
| **Tipo de Cenário** | Happy Path |
| **Prioridade** | **P3** |
| **Pré-condições** | Usuário deve estar autenticado e possuir um pedido finalizado com sucesso. O usuário deve estar na página de confirmação do pedido.  |
| **Passo a Passo** | Acessar a página de login \> Informar credenciais válidas \> Clicar no botão **Login** \> Adicionar um produto ao carrinho \> Acessar o carrinho \> Clicar em **Checkout** \> Preencher os campos **First Name**, **Last Name** e **Zip Code** com dados válidos \> Clicar no botão **Continue** \> Clicar no botão **Finish** \> Acessar a opção de geração do PDF do pedido \> Solicitar a geração do documento \> Verificar o arquivo gerado.  |
| **Resultado esperado** | O sistema deve gerar o PDF do pedido com sucesso, contendo as informações correspondentes à compra realizada.  |
| **Resultado obtido** | O PDF do pedido foi gerado com sucesso e apresentou as informações correspondentes à compra realizada.  |
| **Massa de dados:** | Usuário: standard\_user \- Senha: secret\_sauce |

| TC-25: Retornar para Home após finalizar pedido  |  |
| :---- | :---- |
| **Funcionalidade** | Navegação |
| **Tipo de Teste** | Funcional |
| **Tipo de Cenário** | Happy Path |
| **Prioridade** | **P2** |
| **Pré-condições** | Usuário deve estar autenticado e possuir um pedido finalizado com sucesso. O usuário deve estar na página de confirmação do pedido.  |
| **Passo a Passo** | Acessar a página de login \> Informar credenciais válidas \> Clicar no botão **Login** \> Adicionar um produto ao carrinho \> Acessar o carrinho \> Clicar em **Checkout** \> Preencher os campos **First Name**, **Last Name** e **Zip Code** com dados válidos \> Clicar no botão **Continue** \> Clicar no botão **Finish** \> Clicar na opção **Back Home** \> Verificar a página apresentada.  |
| **Resultado esperado** | O sistema deve direcionar o usuário de volta para a página inicial do catálogo de produtos após clicar em **Back Home**.  |
| **Resultado obtido** | O sistema direcionou o usuário corretamente para a página inicial do catálogo de produtos.  |
| **Massa de dados:** | Usuário: standard\_user \- Senha: secret\_sauce |

