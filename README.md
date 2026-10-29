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


Iterações com o lovale:
> Crie um App de Organização de Finanças Pessoais com base no seguinte PRD (Product Requirements Document): {PRD}


### 3. Entregando o Desafio na DIO

Finalize seu projeto criando um **repositório no GitHub** (pode ser um **fork** deste).  
No README do seu repositório, inclua:

- Seu **prompt final** (PRD);  
- Prints ou pequenos vídeos das interações com a IA;  
- Um resumo do que o seu **App de Finanças Pessoais** faz;  
- Uma breve **reflexão sobre o processo**:
  - O que funcionou bem?  
  - O que não funcionou como o esperado?
      SO fiz uma interação com o lovable. Coloquei o PRD, e ele depois de muito tempo deu a informação que não tinha credito  
  - O que aprendeu sobre conversar com IAs?

> [!TIP]
> Publique seu repositório e compartilhe o link na plataforma da DIO! Sua entrega é a prova de que você domina o raciocínio de Vibe Coding, mesmo sem escrever uma única linha de código.

## 💬 Conclusão

Vibe Coding é sobre clareza, curiosidade e criatividade, não sobre perfeição técnica. O verdadeiro objetivo aqui é aprender a pensar junto com a IA, transformando ideias em conceitos reais e enxergando a tecnologia como uma extensão do seu raciocínio criativo. Cada interação é um experimento, quanto mais clara for sua intenção, mais surpreendente será o resultado.

```

