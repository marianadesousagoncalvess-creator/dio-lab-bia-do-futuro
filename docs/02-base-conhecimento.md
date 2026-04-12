# Base de Conhecimento

## Dados Utilizados

Descreva se usou os arquivos da pasta `data`, por exemplo:

| Arquivo | Formato | Utilização no agente |
|---------|---------|---------------------|
| `dados_usuario.json` | JSON | Armazena renda mensal, gastos fixos e objetivos financeiros do usuário |
| `transacoes.csv` | CSV | Registra gastos diários para análise de padrão de consumo |
| `categorias_gastos.json` | JSON | Define categorias como alimentação, transporte, lazer e seus limites |
| `regras_financeiras.json` | JSON | Contém regras como percentual máximo de gastos e critérios para geração de alertas |


---

## Adaptações nos Dados

> Você modificou ou expandiu os dados mockados? Descreva aqui.

Os dados utilizados no projeto foram adaptados para representar um cenário real de controle financeiro pessoal.

---

## Estratégia de Integração

### Como os dados são carregados?
> Descreva como seu agente acessa a base de conhecimento.

Os dados em JSON e CSV são carregados no início da interação e utilizados como base para análise do agente. Essas informações são incluídas no contexto do processamento, permitindo que a IA gere alertas e recomendações com base nos dados do usuário.

### Como os dados são usados no prompt?
> Os dados vão no system prompt? São consultados dinamicamente?

Os dados do usuário são incluídos dinamicamente no contexto do prompt, permitindo que a IA analise as informações antes de gerar a resposta.

---

## Exemplo de Contexto Montado

> Mostre um exemplo de como os dados são formatados para o agente.

```
Dados do Cliente:
- Nome: João Silva
- Perfil: Moderado
- Saldo disponível: R$ 5.000

Últimas transações:
- 01/11: Supermercado - R$ 450
- 03/11: Streaming - R$ 55
...
```
