# 💸 App de Finanças Pessoais do Moises com Vibe Coding

## Sobre o Projeto

Este projeto foi desenvolvido como Desafio da DIO sobre Vibe Coding utilizando Microsoft Copilot e Lovable.

O objetivo foi explorar como a IA Generativa pode auxiliar na criação de produtos digitais, desde a definição dos requisitos até a geração de um MVP funcional a partir de um PRD (Product Requirements Document) detalhado.

---

# 1. Prompt Final (PRD)

O PRD abaixo foi refinado utilizando o Copilot Web e serviu como base para a geração da aplicação.

```mardown
# LOVABLE BUILD SPEC
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

# 2. Interação com a IA

Após o refinamento do PRD, foi realizada a seguinte solicitação ao Lovable:

```text
Crie um App de Organização de Finanças Pessoais com base no seguinte PRD (Product Requirements Document): {PRD}
```

## Resultado da Geração

Aplicação gerada:

https://visual-detail-dreamworks.lovable.app/

---

# 3. Evidências do Processo

## Tela de Conversa

![Tela Conversa](https://github.com/user-attachments/assets/b2e47fc7-5e7d-421c-862f-c8aaeb1fa870)

---

## Tela de Metas

![Tela Metas](https://github.com/user-attachments/assets/33634317-8c5b-48d9-b53a-1ab28fa58f30)

---

## Tela de Painel

![Tela Painel](https://github.com/user-attachments/assets/b9f543b7-368e-496a-984a-80f300c65e18)

---

## Tela de Perfil

![Tela Perfil](https://github.com/user-attachments/assets/39c245c3-2a5f-4b0c-bcdf-85d8449b6fe9)

---

# 4. Resumo da Aplicação

## Broto

Broto é um assistente de finanças pessoais baseado em Inteligência Artificial que ajuda usuários a organizar receitas, despesas e metas financeiras por meio de uma experiência simples, acessível e orientada por conversas.

O objetivo do projeto é reduzir a complexidade normalmente associada ao controle financeiro, substituindo planilhas e formulários por uma experiência mais natural e intuitiva.

### Proposta de Valor

**Controle seu dinheiro conversando.**

Exemplo:

> Usuário: "Gastei R$ 32 no almoço."

> Broto: "Entendi. Registrei uma despesa de R$ 32 na categoria Alimentação."

---

## Principais Funcionalidades

### Dashboard Financeiro

- Saldo atual
- Receitas do mês
- Despesas do mês
- Economia do mês

### Análise de Gastos por Categoria

- Gráfico de distribuição dos gastos
- Valores detalhados por categoria
- Identificação das categorias com maior impacto no orçamento

Categorias atuais:

- Moradia
- Transporte
- Alimentação
- Lazer

### Evolução Financeira Mensal

- Comparação entre receitas e despesas
- Acompanhamento da evolução financeira ao longo do tempo

### Gestão de Metas Financeiras

- Definição de objetivos financeiros
- Controle do valor acumulado
- Acompanhamento percentual do progresso

### Monitoramento dos Maiores Gastos

- Descrição do gasto
- Categoria
- Data
- Valor

### Assistente Financeiro Inteligente

- Recomendações automáticas
- Sugestões de economia
- Identificação de padrões de gastos

---

## Navegação da Aplicação

### Conversa

Permite:

- Registrar receitas
- Registrar despesas
- Consultar informações financeiras
- Receber orientações personalizadas

### Painel

Apresenta:

- Indicadores financeiros
- Gráficos
- Metas
- Insights

### Metas

Permite:

- Criar metas
- Editar metas
- Acompanhar progresso

### Perfil

Permite gerenciar:

- Preferências do usuário
- Configurações da conta

---

## Funcionalidades Planejadas

### Registro por Linguagem Natural

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

### Consulta Conversacional

Exemplos:

```text
Quanto gastei este mês?
Qual minha maior categoria de gastos?
Qual meu saldo atual?
Quanto falta para minha meta?
```

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
- Mobile First
- Compatibilidade com leitores de tela
- Feedback claro para o usuário
- Tolerância a erros
- Baixa curva de aprendizado

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

---

# 5. Reflexão Sobre o Processo

## O que funcionou bem?

O refinamento prévio do PRD ajudou significativamente na qualidade da aplicação gerada pelo Lovable.

Mesmo com apenas uma interação foi possível gerar um MVP funcional bastante próximo da visão inicial do produto.

---

## O que não funcionou como esperado?

A expectativa era realizar mais interações gratuitas dentro do Lovable.

Após a primeira geração da aplicação, os créditos gratuitos foram consumidos e a plataforma passou a exibir a mensagem:

> "Seu trabalho está pausado porque você está sem créditos. 5 créditos gratuitos chegam em 13 horas."

Apesar dessa limitação, a experiência foi suficiente para compreender melhor o fluxo de desenvolvimento assistido por IA.

---

## O que aprendi sobre conversar com IAs?

A principal lição foi que a qualidade do resultado está diretamente relacionada à qualidade do contexto fornecido.

Quanto mais detalhes, exemplos, restrições e clareza estiverem presentes na solicitação, maior tende a ser a aderência da resposta ao resultado esperado.

> Quanto melhor o prompt, melhor a resposta da IA.
