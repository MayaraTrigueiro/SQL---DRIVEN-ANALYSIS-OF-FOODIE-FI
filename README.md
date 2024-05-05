# SQL - ANÁLISE DA DINÂMICA DE ASSINATURA DO FOODIE-FI

LINK PARA GOOGLE CONSOLE - BIGQUERY - PERGUNTAS E RESPOSTAS (SQL):
- https://console.cloud.google.com/bigquery?sq=203346039404:ae4749ef417e454e8ff4a745f5698d65

LINK PARA ANÁLISE COMPLETA: 
- https://medium.com/@mayaratrigueiro4/case-análise-da-dinâmica-de-assinatura-do-foodie-fi-ee87f879555f

**Introdução**

Análise de dados de uma empresa chamada Foodie-Fi que oferece serviços streaming de conteúdo de comida (Como se fosse uma Netflix, mas apenas com programas e conteúdos de comidas e cozinha). 
A empresa foi fundada em 2020 e iremos utilizar os dados disponíveis para analisar aceitação do serviço entre os assinantes, quais foram os planos mais contratados, como foi a movimentação dos planos entre os clientes (churn, downgrades e upgrades), entre outros questionamentos que possa nos dar uma perspectiva do passado e presente visando decisões e recomendações mais assertivas para a empresa.

**Dados disponíveis**

Duas tabelas: Planos e Assinaturas com dados de 01/01/2020 até 30/04/2021

* *Tabela 1: Planos* 

civil-medley-321018.datamarts.plans

Tabela mostra código, nome do plano e valor mensal do plano 

-> Plano 0: Clientes podem iniciar sua experiencia com 7 dias de acesso gratis.

-> Plano 1: Plano Basico: 9.99 - Clientes possuem acesso limitado ao conteúdo

-> Plano 2: Plano Pro Mensal: 19.90

-> Plano 3:Plano Pro Anual: 199

-> Plano 4 Quando clientes cancelam a assinatura do Foodie-Fi, eles migram para o plano Churn com o preço 0.

* *Tabela 2: Assinaturas*

civil-medley-321018.datamarts.subscriptions

Tabela mostra a data exata de quando o plano do cliente inicia. Clientes podem fazer upgrade, downgrade ou cancelar o plano. A data de inicio ira refletir sobre o plano mais recente do cliente. 
