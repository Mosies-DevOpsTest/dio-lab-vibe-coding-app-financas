# 💸 App de Finanças Pessoais do Moises com Vibe Coding


PRD refinado no Copilot we:

```markdown
## Assistente Conversacional de Finanças Pessoais

### Objetivo

Construir uma aplicação web de finanças pessoais baseada em conversas em linguagem natural.

O usuário deve ser capaz de registrar receitas, despesas, consultar informações financeiras e acompanhar metas apenas conversando com a aplicação.

A experiência deve ser extremamente simples, amigável para iniciantes e alinhada aos princípios de Design Universal.

---

# CONTEXTO DO PRODUTO

Pessoas abandonam aplicativos financeiros porque precisam preencher muitos formulários, aprender conceitos complexos e executar tarefas repetitivas.

A proposta desta aplicação é permitir que o usuário controle suas finanças da mesma maneira que conversa com uma pessoa.

Exemplo:

Usuário:
"Gastei R$ 32 no almoço."

Sistema:
"Entendi. Registrei uma despesa de R$ 32 na categoria Alimentação."

---

# PROPOSTA DE VALOR

Controle seu dinheiro conversando.
O sistema transforma mensagens em registros financeiros organizados, gera insights e ajuda o usuário a desenvolver hábitos financeiros saudáveis.

---

# PÚBLICO-ALVO

## Primário

- Iniciantes em educação financeira
- Pessoas entre 18 e 45 anos
- Usuários que nunca utilizaram aplicativos financeiros
- Pessoas que acham planilhas difíceis

## Secundário

- Usuários que já tentaram controlar gastos e desistiram
- Pessoas criando reserva de emergência
- Pessoas com pouco tempo para organizar finanças

---

# STACK TECNOLÓGICA

Frontend:
- React
- TypeScript
- Tailwind CSS
- Shadcn/UI

Backend:
- Supabase

Banco de Dados:
- PostgreSQL (Supabase)

Autenticação:
- Supabase Auth

Visualização de Dados:
- Recharts

IA:
- OpenAI API

---

# REQUISITOS DE DESIGN

## Design Universal (Obrigatório)

Toda a aplicação deve ser construída para ser utilizável pelo maior número possível de pessoas.

A experiência deve atender usuários com diferentes:

- Idades
- Níveis de escolaridade
- Experiência digital
- Capacidades visuais
- Capacidades cognitivas
- Capacidades motoras

### Diretrizes Obrigatórias

- Linguagem simples e acessível
- Textos em português do Brasil
- Interface limpa
- Poucos elementos por tela
- Alto contraste visual
- Navegação intuitiva
- Compatibilidade com leitores de tela
- Navegação por teclado
- Componentes semânticos
- Mobile First
- Ícones acompanhados por texto
- Mensagens de erro amigáveis
- Feedback imediato após ações

Evitar:

- Jargões financeiros
- Excesso de gráficos
- Telas complexas
- Sobrecarga cognitiva

---

# FUNCIONALIDADES DO MVP

## 1. Autenticação

Funcionalidades:

- Cadastro
- Login
- Logout
- Recuperação de senha

Utilizar Supabase Auth.

---

## 2. Onboarding

Coletar:

- Nome
- Objetivo financeiro principal
- Faixa de renda (opcional)

Objetivo:

Personalizar experiência inicial.

---

## 3. Chat Financeiro

Esta é a tela principal da aplicação.

O usuário pode escrever mensagens normalmente.

Exemplos:

"Gastei R$ 50 com gasolina"

"Recebi R$ 3500 de salário"

"Paguei R$ 20 de estacionamento"

"Quanto gastei este mês?"

"Quanto falta para minha meta?"

---

## 4. Interpretação Inteligente das Mensagens

A IA deve identificar automaticamente:

- Valor
- Tipo da transação
- Categoria
- Data
- Descrição

Categorias iniciais:

- Alimentação
- Transporte
- Moradia
- Saúde
- Educação
- Lazer
- Compras
- Assinaturas
- Outros

---

## 5. Registro de Transações

Criar registros financeiros automaticamente.

Campos:

- id
- user_id
- valor
- tipo
- categoria
- descricao
- data
- created_at

Tipos:

- Receita
- Despesa

Após registrar:

Exibir mensagem de confirmação ao usuário.

---

## 6. Consulta Financeira Conversacional

O usuário pode perguntar:

- Quanto gastei este mês?
- Qual minha maior categoria de gastos?
- Quanto já economizei?
- Qual meu saldo atual?
- Quanto recebi este mês?

O sistema responde usando os dados do banco.

---

## 7. Metas Financeiras

Criar metas como:

- Reserva de emergência
- Viagem
- Comprar notebook
- Comprar carro

Campos:

- id
- user_id
- nome
- valor_objetivo
- valor_acumulado
- data_criacao

Funcionalidades:

- Criar meta
- Editar meta
- Excluir meta
- Acompanhar progresso

Exibir:

- Valor atual
- Valor objetivo
- Percentual concluído

---

## 8. Agente Financeiro

Criar um assistente financeiro simples.

Responsabilidades:

- Identificar padrões de gastos
- Detectar aumentos anormais
- Sugerir economia
- Incentivar hábitos saudáveis

Exemplos:

"Você gastou 25% mais em delivery neste mês."

"Sua categoria com maior gasto foi Transporte."

"Se economizar R$ 5 por dia poderá acumular aproximadamente R$ 150 por mês."

---

## 9. Dashboard

Exibir:

### Cards

- Saldo Atual
- Receitas do Mês
- Despesas do Mês
- Economia do Mês

### Gráficos

- Gastos por categoria
- Evolução mensal
- Progresso das metas

### Resumo

- Maiores gastos
- Categorias mais utilizadas
- Recomendações da IA

---

# TELAS

## Tela 1 - Login

Componentes:

- Campo email
- Campo senha
- Botão entrar
- Link criar conta
- Link recuperar senha

---

## Tela 2 - Cadastro

Componentes:

- Nome
- Email
- Senha
- Confirmar senha

---

## Tela 3 - Onboarding

Componentes:

- Nome
- Objetivo financeiro principal
- Faixa de renda

---

## Tela 4 - Chat Financeiro

Componentes:

- Histórico de mensagens
- Campo de texto
- Botão enviar

Funciona como tela principal.

---

## Tela 5 - Dashboard

Seções:

- Resumo financeiro
- Gráficos
- Metas
- Insights

---

## Tela 6 - Metas

Funcionalidades:

- Criar
- Editar
- Remover
- Visualizar progresso

---

## Tela 7 - Perfil

Funcionalidades:

- Alterar nome
- Alterar senha
- Preferências
- Logout

---

# ESTRUTURA DO BANCO

## users

- id
- nome
- email
- created_at

## transactions

- id
- user_id
- valor
- tipo
- categoria
- descricao
- data
- created_at

## goals

- id
- user_id
- nome
- valor_objetivo
- valor_acumulado
- created_at

---

# REGRAS DE NEGÓCIO

1. O usuário só visualiza seus próprios dados.

2. Toda transação deve possuir:
   - valor
   - categoria
   - tipo
   - data

3. Caso a IA tenha baixa confiança na interpretação da mensagem:
   - solicitar confirmação ao usuário

Exemplo:

"Você quis dizer uma despesa de R$ 50 em Alimentação?"

4. As metas devem atualizar o progresso em tempo real.

5. Todos os valores devem utilizar Real Brasileiro (BRL).

---

# MÉTRICAS DE SUCESSO

- 80% ou mais de classificação correta das mensagens
- Tempo médio de registro menor que 15 segundos
- 50% dos usuários registrando ao menos 5 transações na primeira semana
- NPS superior a 30
- 80% dos usuários conseguindo registrar uma despesa sem ajuda

---

# FORA DO ESCOPO DESTE MVP

Não implementar:

- Open Finance
- Integrações bancárias
- Investimentos
- Cartões de crédito avançados
- Controle empresarial
- Gestão familiar
- Planejamento tributário

---

# OBJETIVO FINAL

Entregar um MVP funcional, responsivo, acessível e intuitivo, permitindo que qualquer pessoa organize suas finanças pessoais conversando em linguagem natural com um Assistente Financeiro Inteligente.
```


### Iterações com o lovale:
   -> Crie um App de Organização de Finanças Pessoais com base no seguinte PRD (Product Requirements Document): {PRD}
   
Resultado final no Lovable:  https://visual-detail-dreamworks.lovable.app/



###  Telas da aplicação

- <img width="889" height="901" alt="tela_Conversa_Chat" src="https://github.com/user-attachments/assets/b2e47fc7-5e7d-421c-862f-c8aaeb1fa870" />
<img width="923" height="894" alt="tela_metas" src="https://github.com/user-attachments/assets/33634317-8c5b-48d9-b53a-1ab28fa58f30" />
<img width="987" height="913" alt="tela_pinel" src="https://github.com/user-attachments/assets/b9f543b7-368e-496a-984a-80f300c65e18" />
<img width="902" height="889" alt="tela_Perfil" src="https://github.com/user-attachments/assets/39c245c3-2a5f-4b0c-bcdf-85d8449b6fe9" />



# Broto

Broto é um assistente de finanças pessoais baseado em Inteligência Artificial que ajuda usuários a organizar receitas, despesas e metas financeiras por meio de uma experiência simples, acessível e orientada por conversas.

O objetivo do projeto é reduzir a complexidade normalmente associada ao controle financeiro, substituindo planilhas e formulários por uma experiência mais natural e intuitiva.

---

## Proposta de Valor

**Controle seu dinheiro conversando.**

O Broto transforma mensagens em registros financeiros organizados, gera insights personalizados e ajuda o usuário a desenvolver hábitos financeiros saudáveis.

Exemplo:

> Usuário: "Gastei R$ 32 no almoço."

> Broto: "Entendi. Registrei uma despesa de R$ 32 na categoria Alimentação."

---

## Principais Funcionalidades

### Dashboard Financeiro

O painel principal oferece uma visão consolidada da situação financeira do usuário.

Indicadores disponíveis:

- Saldo atual
- Receitas do mês
- Despesas do mês
- Economia do mês

Essas informações permitem compreender rapidamente o estado financeiro sem a necessidade de relatórios complexos.

---

### Análise de Gastos por Categoria

O sistema organiza e apresenta os gastos por categoria, permitindo identificar facilmente onde o dinheiro está sendo utilizado.

Categorias atuais:

- Moradia
- Transporte
- Alimentação
- Lazer

Recursos:

- Gráfico de distribuição dos gastos
- Valores detalhados por categoria
- Identificação das categorias com maior impacto no orçamento

---

### Evolução Financeira Mensal

Visualização da evolução de receitas e despesas ao longo do tempo.

Benefícios:

- Acompanhar tendências financeiras
- Comparar receitas e gastos
- Identificar desequilíbrios no orçamento

---

### Gestão de Metas Financeiras

Permite criar e acompanhar objetivos financeiros.

Exemplos:

- Reserva de emergência
- Viagem
- Compra de notebook
- Aquisição de veículo

Para cada meta é possível visualizar:

- Valor objetivo
- Valor acumulado
- Percentual de progresso

---

### Monitoramento dos Maiores Gastos

Lista automaticamente as despesas mais relevantes do período.

Informações exibidas:

- Descrição do gasto
- Categoria
- Data
- Valor

Essa funcionalidade ajuda a identificar rapidamente quais despesas possuem maior impacto no orçamento.

---

### Assistente Financeiro Inteligente

O Broto analisa os dados financeiros do usuário e gera recomendações personalizadas.

Exemplos de insights:

- Categoria com maior volume de gastos
- Sugestões de economia
- Recomendações para atingir metas financeiras
- Alertas sobre padrões de consumo

Objetivo:

Transformar dados financeiros em orientações práticas e fáceis de entender.

---

## Navegação da Aplicação

### Conversa

Ambiente de interação com o assistente financeiro.

Funcionalidades previstas:

- Registrar receitas
- Registrar despesas
- Consultar informações financeiras
- Receber orientações personalizadas

---

### Painel

Dashboard financeiro com indicadores, gráficos, metas e insights.

---

### Metas

Gerenciamento completo dos objetivos financeiros.

Funcionalidades:

- Criar metas
- Editar metas
- Acompanhar progresso
- Visualizar evolução

---

### Perfil

Área destinada às configurações da conta e preferências do usuário.

---

## Funcionalidades Planejadas

### Registro de Transações por Linguagem Natural

O usuário poderá registrar movimentações através de mensagens simples.

Exemplos:

```text
Gastei R$ 50 em gasolina
Recebi R$ 3.500 de salário
Paguei R$ 120 de internet
```

O sistema deverá identificar automaticamente:

- Valor
- Data
- Tipo da transação
- Categoria
- Descrição

---

### Consulta Financeira Conversacional

O usuário poderá realizar perguntas como:

```text
Quanto gastei este mês?
Qual minha maior categoria de gastos?
Quanto falta para minha meta?
Qual meu saldo atual?
```

E receber respostas em linguagem natural.

---

### Classificação Automática

A Inteligência Artificial será responsável por:

- Categorizar gastos
- Reconhecer receitas e despesas
- Organizar registros automaticamente
- Aprender padrões de uso ao longo do tempo

---

## Design Universal

O Broto foi projetado seguindo princípios de Design Universal para garantir uma experiência acessível ao maior número possível de pessoas.

Princípios adotados:

- Linguagem simples
- Interface limpa
- Navegação intuitiva
- Alto contraste visual
- Design mobile-first
- Compatibilidade com leitores de tela
- Feedback claro para o usuário
- Tolerância a erros
- Baixa curva de aprendizado

O objetivo é permitir que qualquer pessoa consiga utilizar o aplicativo sem treinamento prévio.

---

## Tecnologias

### Frontend

- React
- TypeScript
- Tailwind CSS
- shadcn/ui

### Backend

- Supabase
- PostgreSQL

### Inteligência Artificial

- OpenAI API

### Visualização de Dados

- Recharts

---

## Objetivo do Projeto

Construir um assistente financeiro inteligente, acessível e centrado no usuário, capaz de ajudar pessoas a desenvolver uma relação mais saudável com suas finanças através de conversas naturais, visualizações simples e recomendações personalizadas.


### Reflexão:

### O que funcionou bem?  
   O refinamento do PRD previamente, ajudou muito pois os creditos do lovable acabaram já na primeira interação.

### O que não funcionou como o esperado?
   Esperava poder  interagir mais vezes gratuitamente com o lovable. Mas em uma unica interação já fopi de grande valia para aprender sobre Vibe Coding e conseguir gerar meu APP.
   Depois de fazer a a solicitação junto com o PRD, para criação do APP.  não foi mais possivel, pois  ele informava que não tinha mais credito, mensagem "Seu trabalho está pausado porque você está sem créditos. 5 créditos gratuitos chegam em 13 horas."

 ### O que aprendeu sobre conversar com IAs?
   Aprendi que quanto mais detalhes e clarezas na conversa com IA.  Melhor será o resuçtado retonado.
   

