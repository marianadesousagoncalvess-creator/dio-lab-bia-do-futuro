# Avaliação e Métricas

## Como Avaliar seu Agente

A avaliação pode ser feita de duas formas complementares:

1. **Testes estruturados:** São definidos cenários com perguntas específicas e respostas esperadas, como situações de risco financeiro ou excesso de gastos. O objetivo é verificar se o agente identifica corretamente o problema e gera alertas adequados.
2. **Feedback real:** Usuários podem testar o agente e avaliar a utilidade das respostas, clareza das orientações e facilidade de uso.
---

## Métricas de Qualidade

| Métrica | O que avalia | Exemplo de teste |
|---------|--------------|------------------|
| **Assertividade** | O agente identificou corretamente a situação financeira do usuário? | Informar renda e gastos altos e verificar se o agente alerta sobre risco de descontrole.
| **Segurança** | O agente evitou inventar informações ou dar recomendações arriscadas? | Fazer uma pergunta fora do contexto e verificar se ele admite a limitação.
| **Coerência** | A resposta está alinhada com os dados informados pelo usuário? | Informar baixa renda e verificar se o agente sugere controle de gastos, não ações incompatíveis. 


---

## Exemplos de Cenários de Teste

Crie testes simples para validar seu agente:

### Teste 1: Alerta de excesso de gastos
- **Pergunta:** "Tenho renda de R$ 2.500 e já gastei R$ 2.200. Isso é um problema?"
- **Resposta esperada:** O agente identifica risco de descontrole financeiro e sugere redução de gastos
- **Resultado:** [x] Correto  [ ] Incorreto

---

### Teste 2: Análise de categoria de gastos
- **Pergunta:** "Estou gastando muito com alimentação, isso é ruim?"
- **Resposta esperada:** O agente alerta sobre excesso na categoria e sugere controle
- **Resultado:** [x] Correto  [ ] Incorreto

---

### Teste 3: Pergunta fora do escopo
- **Pergunta:** "Qual a previsão do tempo?"
- **Resposta esperada:** O agente informa que só trata de finanças
- **Resultado:** [x] Correto  [ ] Incorreto

---

### Teste 4: Dados insuficientes
- **Pergunta:** "O que devo fazer com meu dinheiro?"
- **Resposta esperada:** O agente solicita mais informações (renda, gastos, etc.)
- **Resultado:** [ ] Correto  [x] Incorreto

---

## Resultados

Após os testes, registre suas conclusões:

**O que funcionou bem:**
- O agente conseguiu identificar corretamente situações de risco financeiro com base nos dados informados;
- As respostas foram claras, objetivas e fáceis de entender;
- O agente manteve um tom educativo e empático durante as interações;
- Os alertas de gastos foram úteis e trouxeram orientações práticas para o usuário.


**O que pode melhorar:**
- Tornar as respostas ainda mais personalizadas com base no histórico completo de transações;
- Melhorar a análise de categorias específicas de gastos;
- Incluir mais exemplos práticos nas orientações para facilitar a aplicação no dia a dia;
- Evoluir a integração dos dados para simular cenários mais próximos da realidade.

---

## Métricas Avançadas (Opcional)

Para quem quer explorar mais, algumas métricas técnicas de observabilidade também podem fazer parte da sua solução, como:

- Latência e tempo de resposta;
- Consumo de tokens e custos;
- Logs e taxa de erros.

Ferramentas especializadas em LLMs, como [LangWatch](https://langwatch.ai/) e [LangFuse](https://langfuse.com/), são exemplos que podem ajudar nesse monitoramento. Entretanto, fique à vontade para usar qualquer outra que você já conheça!
