# **Plano de Testes**

## **1\. Informações do Documento**

* **Projeto:** Sauce Demo  
* **Versão:** 1.0  
* **Autor:** Matheus Modesto  
* **Data:** Agosto de 2026  
* **Status do Documento:** Aprovado

# **2\. Objetivos**

## **2.1 Objetivo Principal**

O objetivo deste Plano de Testes é definir a estratégia de testes para a aplicação web Sauce Demo nos dois navegadores mais utilizados (Google Chrome e Microsoft Edge). O principal objetivo é verificar se as funcionalidades essenciais da aplicação funcionam conforme o esperado, garantindo uma experiência de compra confiável e intuitiva para o usuário.

## **2.2 Visão Geral da Aplicação**

O Sauce Demo é uma aplicação web de e-commerce desenvolvida para fins de prática em testes de software. Ela permite que os usuários realizem login, naveguem pelos produtos disponíveis, adicionem e removam itens do carrinho, concluam o processo de checkout e efetuem logout.

**Nome da Aplicação:** Sauce Demo ([https://www.saucedemo.com](https://www.saucedemo.com))

**Ambiente:** Produção (Ambiente Público de Demonstração)

**Navegadores Alvo:** Google Chrome e Microsoft Edge

**Idioma da Interface:** Inglês

## **2.3 Funcionalidades no Escopo**

* **Autenticação:** Login com credenciais válidas e inválidas, validação de campos obrigatórios, validação de mensagens de erro e funcionalidade de logout.  
* **Catálogo de Produtos:** Exibição da lista de produtos, validação das informações dos produtos e ordenação dos itens.  
* **Checkout:** Validação do formulário de informações, validação de campos obrigatórios, conferência do resumo do pedido, conclusão da compra e validação da mensagem de confirmação.  
* **Navegação:** Navegação entre páginas, funcionamento do menu, botão **Continue Shopping** e comportamento dos botões de retorno.  
* **Interface do Usuário:** Visibilidade dos elementos e menus, consistência do layout das páginas e validação de rótulos e mensagens.  
* **Validação Funcional:** Cenários de fluxo principal (*Happy Path*), cenários negativos, validação de limites de entrada e validação das regras de negócio.

## **2.4 Fora do Escopo**

As seguintes atividades não fazem parte deste ciclo de testes:

* Testes de Segurança (avaliação de vulnerabilidades, ataques de autenticação, falhas de autorização, SQL Injection, Cross-Site Scripting (XSS) e testes de invasão).  
* Testes de API (validação das APIs de backend, payloads de requisição e resposta, tokens de autenticação e contratos de API).  
* Validação de Banco de Dados (integridade dos dados, persistência, consultas SQL e consistência do backend).  
* Testes de Responsividade para dispositivos móveis.  
* Testes de Localização e Internacionalização (idiomas, formatos regionais, moedas e traduções).  
* Testes de Automação.  
* Revisão de Código-Fonte.

# **3\. Tipos de Teste**

### **Teste Exploratório**

Identificar comportamentos inesperados, problemas de usabilidade ou defeitos por meio da exploração livre da aplicação, além dos casos de teste previamente definidos.

### **Teste Funcional**

Verificar se cada funcionalidade atende aos requisitos de negócio e ao comportamento esperado do sistema.

### **Teste de Usabilidade**

Avaliar a facilidade de uso da aplicação, sua navegação e a experiência geral do usuário, verificando se tarefas comuns podem ser concluídas de forma intuitiva e eficiente.

### **Teste Negativo**

Verificar se a aplicação trata corretamente dados inválidos e ações inesperadas do usuário, sem apresentar falhas ou comportamentos incorretos.

### **Teste Positivo**

Verificar se a aplicação se comporta corretamente quando recebe dados válidos e quando o usuário segue o fluxo esperado.

# **4\. Estratégia de Testes**

## **4.1 Abordagem**

A estratégia de testes combina casos de teste funcionais previamente definidos com testes exploratórios. Os testes roteirizados garantem uma validação consistente dos fluxos críticos de negócio, enquanto os testes exploratórios são utilizados para identificar comportamentos inesperados, problemas de usabilidade e casos de borda que podem não estar contemplados pelos casos de teste pré-definidos.

## **4.2 Técnicas de Projeto de Teste**

**Particionamento por Equivalência** – Reduz a quantidade de casos de teste mantendo uma cobertura adequada.

**Análise de Valor Limite** – Valida o comportamento do sistema nos limites mínimos e máximos de entrada.

**Teste de Tabela de Decisão** – Verifica regras de negócio com base em diferentes combinações de entradas.

**Teste de Transição de Estados** – Valida o comportamento do sistema durante mudanças de estado, como autenticação e fluxo de checkout.

**Adivinhação de Erros (Error Guessing)** – Identifica defeitos com base na experiência do testador e em erros comuns cometidos pelos usuários.

## **4.3 Prioridades dos Testes**

### **P1 – Alta**

Funcionalidades críticas que impactam diretamente o principal fluxo de negócio da aplicação. Defeitos devem ser corrigidos antes da liberação.

**Exemplos:** Login, adicionar produtos ao carrinho e finalizar a compra.

### **P2 – Média**

Funcionalidades importantes que afetam a usabilidade ou processos secundários, mas não impedem a jornada principal do usuário.

**Exemplos:** Alterar a quantidade de itens no carrinho e filtros de ordenação.

### **P3 – Baixa**

Funcionalidades de baixo impacto ou problemas visuais que pouco afetam a operação do sistema ou a experiência do usuário.

**Exemplos:** Tamanho de botões e ícones, links do rodapé.

## **4.4 Critérios de Entrada**

* Ambiente de testes disponível.  
* Casos de teste preparados.  
* Massa de dados disponível.  
* Plano de Testes aprovado.  
* Aplicação estável.

## **4.5 Critérios de Saída**

* Todos os casos de teste planejados foram executados.  
* Todos os casos de teste de alta prioridade (P1) foram aprovados.  
* Todos os defeitos críticos e bloqueadores foram documentados.  
* O relatório de execução dos testes foi concluído.  
* As evidências dos testes foram coletadas e anexadas.  
* Não existem defeitos bloqueadores pendentes.

# **5\. Ambiente de Testes e Ferramentas**

**Gerenciamento de Casos de Teste:** Google Sheets / Google Docs

**Gerenciamento de Defeitos:** Google Sheets / Google Docs

**Navegadores:** Google Chrome e Microsoft Edge

**Captura de Evidências:** Ferramenta de Captura de Tela do Windows e Xbox Game Bar para evidências em vídeo.

**Massa de Dados:** Fornecida pelo Sauce Demo

**Documentação e Controle:** GitHub

# **6\. Cronograma**

Como este é um projeto pessoal, não há um cronograma fixo para a execução dos testes. As atividades de teste continuarão até que todos os critérios de saída sejam atendidos.

# **7\. Entregáveis**

* Plano de Testes.  
* Casos de Teste Detalhados.  
* Relatório de Execução dos Testes.  
* Relatórios de Bugs.  
* Evidências dos Testes.  
* Relatório Final de Testes.

