# **Relatório de Bugs**

## **1\. Objetivo**

Este documento apresenta os defeitos identificados durante a execução dos casos de teste da aplicação de e-commerce.

Os bugs foram registrados a partir das falhas observadas durante o ciclo de testes e relacionados aos respectivos casos de teste e evidências de execução.

## **2\. Resumo dos Defeitos**

Durante a execução dos 25 casos de teste, foram identificados 7 casos com falha. Após a análise dos resultados, foram identificados 5 defeitos distintos.

| ID | Título | Casos Relacionados | Funcionalidade | Status |
| :---- | :---- | :---- | :---- | :---- |
| BUG-01 | Nome incorreto da Camisa Vermelha no catálogo | TC-04 / TC-05 | Exibição de produtos | Aberto |
| BUG-02 | Descrição incorreta de produto no catálogo | TC-04 / TC-06 | Exibição de produtos | Aberto |
| BUG-03 | Checkout permitido com carrinho vazio | TC-14 | Carrinho / Checkout | Aberto |
| BUG-04 | Campos First Name e Last Name aceitam entradas inválidas  | TC-18 / TC-19 | Checkout | Aberto |
| BUG-05 | Campo Zip Code aceita entradas inválidas  | TC-20 | Checkout | Aberto |

| 25 Total de Casos | 18 Passou | 7 Falhou | 0 Bloaqueado | 100% % Executado |
| :---: | :---: | :---: | :---: | :---: |

**3\. Detalhamento dos Defeitos**

| BUG-01: Nome incorreto no item “Red T-Shirt” no catálogo |  |
| :---- | :---- |
| **Casos de teste:** | TC-04 / TC-05 |
| **Funcionalidade** | Exibição de produtos |
| **Status** | Aberto |
| **Severidade** | Baixa |
| **Prioridade** | **P2** |
| **Passo a Passo para reprodução do bug**  | 1\. Acessar o catálogo de produtos. 2\. Localizar o produto Red T-Shirt. 3\. Verificar o nome apresentado para o produto. |

| BUG-02: Descrição incorreta do item “Backpack” |  |
| :---- | :---- |
| **Casos de teste:** | TC-04 / TC-06 |
| **Funcionalidade** | Exibição de produtos |
| **Status** | Aberto |
| **Severidade** | Baixa |
| **Prioridade** | **P2** |
| **Passo a Passo para reprodução do bug** | 1\. Acessar o catálogo de produtos. 2\. Localizar o produto em questão. 3\. Verificar a descrição apresentada para p produto.  |

| BUG-03: Checkout permitido com carrinho vazio |  |
| :---- | :---- |
| **Casos de teste:** | TC-14 |
| **Funcionalidade** | Carrinho / Checkout |
| **Status** | Aberto |
| **Severidade** | Média |
| **Prioridade** | **P2** |
| **Passo a Passo para reprodução do bug** | 1\. Acessar o carrinho. 2.Garantir que não existam produtos adicionados. 3.Tentar prosseguir para o checkout. 4.Observar o comportamento apresentado pelo sistema.  |

| BUG-04: Campos First Name e Last Name aceitam entradas inválidas |  |
| :---- | :---- |
| **Casos de teste:** | TC-18 / TC-19 |
| **Funcionalidade** | Checkout |
| **Status** | Aberto |
| **Severidade** | Alta |
| **Prioridade** | **P1** |
| **Passo a Passo para reprodução do bug** | 1.Acessar a etapa de preenchimento das informações do checkout. 2.Informar números e/ou caracteres especiais no campo First Name. 3.Informar números e/ou caracteres especiais no campo Last Name. 4.Observar o comportamento apresentado pelo sistema.  |

| BUG-05: Campo Zip Code aceita entradas inválidas |  |
| :---- | :---- |
| **Casos de teste:** | TC-20 |
| **Funcionalidade** | Checkout |
| **Status** | Aberto |
| **Severidade** | Alta |
| **Prioridade** | **P1** |
| **Passo a Passo para reprodução do bug** | 1.Acessar a etapa de preenchimento das informações do checkout. 2.Localizar o campo Zip Code. 3.Informar letras e/ou caracteres especiais. 4.Observar o comportamento apresentado pelo sistema.  |

## **8\. Considerações**

Os defeitos registrados neste documento foram consolidados a partir dos resultados da execução dos casos de teste.

Embora 7 casos de teste tenham apresentado falhas, a análise dos resultados identificou 5 defeitos distintos, uma vez que alguns casos de teste validam diferentes aspectos de um mesmo comportamento.

A relação entre casos de teste, resultados e defeitos permite manter a rastreabilidade durante o ciclo de testes.

