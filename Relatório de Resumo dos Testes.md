# **Relatório de Resumo dos Testes**

## **1\. Objetivo**

Este documento apresenta o resumo dos resultados obtidos durante o ciclo de testes manuais realizado na aplicação de e-commerce.

O objetivo é consolidar os resultados da execução, apresentar os principais indicadores do ciclo, registrar os defeitos identificados e fornecer uma visão geral da qualidade observada durante os testes.

## **2\. Resumo da Execução**

O ciclo de testes contou com 25 casos de teste, abrangendo as principais funcionalidades da jornada de compra.

| Métrica | Resultado |
| :---- | :---- |
| Total de casos de teste | 25 |
| Casos executados | 25 |
| Passou | 18 |
| Falhou | 7 |
| Bloqueado | 0 |
| Não executado | 0 |
| Taxa de execução | 100% |

## **3\. Cobertura Funcional**

Os testes contemplaram os principais fluxos funcionais da aplicação:

| Funcionalidade | Casos de Teste | Cobertura |
| :---- | :---- | :---- |
| Autenticação | TC-01 e TC-02 | Coberta |
| Logout | TC-03 | Coberta |
| Exibição de produtos | TC-04 a TC-06 | Coberta |
| Ordenação | TC-07 | Coberta |
| Detalhes do produto | TC-08 | Coberta |
| Carrinho | TC-09 a TC-14 | Coberta |
| Checkout | TC-15 a TC-23 | Coberta |
| Geração de PDF | TC-24 | Coberta |
| Navegação | TC-25 | Coberta |

## **4\. Casos de Teste com Falha**

Os seguintes casos apresentaram resultado **FALHOU** durante a execução:

| ID | Funcionalidade | Resultado | Observação |
| :---- | :---- | :---- | :---- |
| TC-04 | Exibição de produtos | Falhou | Foram identificadas divergências nas informações apresentadas no catálogo  |
| TC-05 | Exibição de produtos | Falhou | Nome da Red T-Shirt apresenta divergência  |
| TC-06 | Exibição de produtos | Falhou | Descrição da mochila apresenta divergência  |
| TC-14 | Carrinho | Falhou | Checkout permitido com carrinho vazio  |
| TC-18 | Checkout | Falhou | First Name aceita entradas inválidas  |
| TC-19 | Checkout | Falhou | Last Name aceita entradas inválidas  |
| TC-20 | Checkout | Falhou | Zip Code aceita entradas inválidas  |

## **5\. Defeitos Identificados**

A análise dos resultados identificou **5 defeitos distintos**:

| ID | Área | Descrição |
| :---- | :---- | :---- |
| BUG-01 | Catálogo | Nome incorreto do item Red T-Shirt  |
| BUG-02 | Catálogo | Descrição incorreta do item Backpack |
| BUG-03 | Carrinho / Checkout | Checkout permitido com carrinho vazio  |
| BUG-04 | Checkout | First Name e Last Name aceitam entradas inválidas  |
| BUG-05 | Checkout | Zip Code aceita entradas inválidas  |

## **6\. Distribuição dos Resultados**

A execução apresentou a seguinte distribuição:

| Resultado | Quantidade | Percentual |
| :---- | :---- | :---- |
| Passou | 18 | 72% |
| Falhou | 7 | 28% |
| Bloqueado | 0 | 0% |
| Não executado | 0 | 0% |
| Total | 25 | 100% |

## 

## 

## **7\. Principais Observações**

Os principais problemas encontrados durante o ciclo de testes estão concentrados em duas áreas:

### **Catálogo de Produtos**

Foram identificadas divergências nas informações apresentadas para determinados produtos, incluindo nome e descrição.

### **Checkout**

Foram identificados problemas relacionados à validação dos dados informados pelo usuário e ao controle do fluxo de compra.

Também foi identificado um comportamento que permite prosseguir com o checkout mesmo quando o carrinho está vazio.

**8\. Conclusão**

O ciclo de testes foi concluído com **100% dos casos planejados executados**.

Dos 25 casos executados, 18 foram aprovados e 7 apresentaram falhas. A análise dessas falhas resultou na identificação de 5 defeitos distintos, documentados no Relatório de Bugs.

Os resultados demonstram que os principais fluxos funcionais da aplicação foram exercitados, porém foram identificados pontos de atenção relacionados à exibição de informações de produtos, validação de dados no checkout e controle do fluxo de compra.

Com base nos resultados obtidos, recomenda-se a correção e posterior reteste dos defeitos identificados antes de considerar essas funcionalidades totalmente validadas.

## **9\. Status do Ciclo**

**Status:** Concluído  
**Ciclo:** Ciclo 1  
**Tipo de teste:** Testes Manuais  
**Casos de teste:** 25  
**Casos executados:** 25  
**Taxa de execução:** 100%  
**Taxa de aprovação:** 72%  
**Casos com falha:** 7  
**Defeitos identificados:** 5

