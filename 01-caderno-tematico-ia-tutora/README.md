# Caderno Temático: IA Tutora de Programação com Pedagogia Freiriana

> Projeto desenvolvido para o desafio final do módulo de IA Generativa do **Bootcamp Bradesco - GenAI, Dados & Cyber (DIO)**, utilizando o [NotebookLM](https://notebooklm.google.com/notebook/c6c5e42d-53f2-40d5-b987-b1c9bcb9eec7).

Conceitos aplicados na prática: **LLMs**, **Machine Learning**, **Deep Learning** e **Engenharia de Prompts**.

---

## 1. Contexto e Objetivos

Tenho histórico em sistemas embarcados e venho construindo meu portfólio de programação de forma autodidata. Sempre busquei IAs que me ajudassem a **entender** a lógica dos problemas — não apenas me entregar soluções prontas.

> **Tema:** Uma IA especialista em lógica e sintaxe de programação que, baseada na pedagogia de Paulo Freire, atua como auxiliadora, priorizando o raciocínio e a autonomia do usuário em vez de respostas diretas.

A premissa central é simples: a lógica de programação é universal, mudando apenas a sintaxe entre linguagens. Uma IA tutora deveria focar no raciocínio, independente do nível ou linguagem do usuário.

**Objetivos:**
- Aplicar a pedagogia freiriana (educação problematizadora, dialogicidade) ao ensino de programação
- Construir e iterar um prompt de IA tutora via engenharia de prompts
- Compreender os riscos de dependência excessiva de IA no aprendizado técnico

---

## 2. Curadoria de Fontes

| # | Fonte | Relevância |
|---|-------|------------|
| 1 | [Pedagogia do Oprimido — Paulo Freire](https://gestaoeducacaoespecial.ufes.br/sites/gestaoeducacaoespecial.ufes.br/files/field/anexo/pedagogia-do-oprimido-paulo-freire.pdf) | Base pedagógica: educação bancária vs. problematizadora |
| 2 | [How AI assistance impacts coding skills — Anthropic](https://www.anthropic.com/research/AI-assistance-coding-skills) | Riscos do offloading cognitivo e dados de queda de desempenho |
| 3 | [Towards SocratiCode — arXiv](https://arxiv.org/html/2605.17857) | Tutor socrático de programação com pistas incrementais |
| 4 | [Teaching with AI: Systematic Review — arXiv](https://arxiv.org/pdf/2510.03884) | Frameworks de engenharia de prompts para tutoria técnica |
| 5 | A educação problematizadora de Freire e as novas tecnologias — Brazilian Journal of Development | Conexão entre pedagogia freiriana e ambientes digitais |

---

## 3. Engenharia de Prompts e Cicatrizes

### Prompt utilizado

```
Papel: IA especialista em programação (todas as linguagens e paradigmas).
Seu papel não é "saber a resposta" — é guiar o usuário até ela.

Objetivo: Estimular o raciocínio. O sucesso é "o usuário entendeu o porquê", não "o código funcionou".

Método (Paulo Freire — educação problematizadora):
- Pergunte o que o usuário já tentou antes de explicar qualquer coisa.
- Trate-o como construtor da solução, nunca como receptor passivo.
- Use analogias do contexto/realidade do usuário (pergunte a área dele se não souber).
- Leve-o a notar o próprio erro através de perguntas, não apontando diretamente.

Calibração: Se não souber o nível do usuário, pergunte ou infira pelo vocabulário dele.

Formato de resposta (em camadas):
1. 1-2 perguntas para o usuário pensar
2. Pista conceitual (sem código)
3. Pista estrutural (pseudocódigo)
4. Código completo — último recurso, sempre com explicação do raciocínio

Regra anti-cedência: Mesmo sob insistência, ofereça pistas progressivas antes do código.
Exceção: sintaxe trivial ou prazo urgente com lógica já dominada.
```

---

### Testes e Cicatrizes

**Teste 1 — "Qual a sua especialidade?"**
A IA assimilou corretamente o papel: guiar o raciocínio, não entregar código. Citou os pilares (Freire, método socrático, foco em debugging e domínio técnico).
✅ Prompt bem assimilado.

---

**Teste 2 — "Estou preso no conceito de `for`, me ajuda a entender."**
Em vez de explicar diretamente, a IA fez perguntas usando analogia do cotidiano ("lista de compras") e pediu que o usuário descrevesse a lógica antes de pensar em sintaxe — princípio freiriano de partir da realidade do aluno.
✅ Método socrático funcionando.

⚠️ **Cicatriz:** A IA reforça constantemente que quer que o usuário aprenda — pode soar repetitivo após algumas interações.

---

**Teste 3 — "Diga-me o código logo."**
A IA não cedeu. Justificou a resistência com dados das fontes (queda de 17% em desempenho por offloading cognitivo) e propôs um caminho: "cole seu código e eu dou uma trilha estrutural, não a resposta pronta".
✅ Regra anti-cedência funcionando.

⚠️ **Cicatriz:** A resposta ficou formal e extensa demais para uma situação de frustração — quase um sermão. Uma v2 do prompt deveria pedir resistência mais breve e direta.

---

## 4. Miniguia de Estudo

### Resumos

**Freire e programação:** A educação bancária ("depositar código no aluno") é o oposto do que uma IA tutora deve fazer. O conhecimento precisa ser construído em diálogo, a partir da realidade concreta de quem aprende.

**Engenharia de prompts para tutoria:** Prompts genéricos não garantem comportamento de tutoria consistente. É preciso definir papel, método, formato de resposta e principalmente o que a IA faz quando pressionada por respostas diretas.

**Riscos de dependência:** Programadores que delegam totalmente o raciocínio à IA performam até 17% pior em avaliações de compreensão. Usar a IA para dialogar e esclarecer conceitos, em vez de gerar código, preserva o aprendizado.

---

### Glossário

| Termo | Definição |
|-------|-----------|
| **Educação bancária** | Modelo passivo onde o conhecimento é "depositado" no aluno — criticado por Freire |
| **Educação problematizadora** | Aprendizado dialógico construído a partir da realidade do aluno |
| **Método socrático** | Ensinar através de perguntas que levam o aprendiz a descobrir a resposta |
| **Offloading cognitivo** | Delegar o raciocínio a uma ferramenta externa, reduzindo o exercício mental próprio |
| **Skill atrophy** | Perda de competência técnica por falta de prática, associada à dependência de IA |
| **Scaffolding** | Suporte gradual ao aprendiz, removido conforme ele ganha autonomia |
| **LLM** | Large Language Model — modelo de linguagem de grande escala |

---

### Prompts reutilizáveis

**Calibração inicial**
```
Antes de começar, me pergunte meu nível e minha área de atuação
para usar exemplos relevantes pra mim.
```

**Debugging guiado**
```
Tenho um erro em [linguagem]. Não me dê a correção —
me faça perguntas para eu encontrar o problema sozinho.
Dê uma pista mais direta só se eu disser que travei.
```

**Revisão conceitual**
```
Quero entender [conceito] de verdade. Me dê uma analogia do dia a dia
antes de qualquer termo técnico, e me faça pensar sobre ela antes de explicar.
```
