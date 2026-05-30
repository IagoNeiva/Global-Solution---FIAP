# Global-Solution---FIAP
Integrantes: Iago Neiva - RM 570234; Kelly Stephanie RM 569044; Renan RM 570532


#  Mission Control AI

Sistema de monitoramento inteligente para missões espaciais experimentais utilizando **Python**, **Ollama** e **LLM local (Llama 3.2 1B)**.

O projeto combina regras determinísticas de avaliação de risco com Inteligência Artificial para gerar alertas operacionais e recomendações rápidas para o comandante da missão.

---

##  Objetivo

Simular um centro de controle de missão capaz de:

* Monitorar indicadores críticos da operação.
* Classificar riscos automaticamente.
* Identificar tendências da missão.
* Gerar relatórios operacionais.
* Utilizar IA para produzir análises consultivas em linguagem natural.

---

##  Indicadores Monitorados

O sistema avalia cinco áreas operacionais:

| Indicador                | Descrição                    |
| ------------------------ | ---------------------------- |
| Temperatura Interna      | Controle térmico da nave     |
| Comunicação              | Qualidade do link com a base |
| Energia                  | Nível da bateria             |
| Oxigênio                 | Sistema de suporte à vida    |
| Estabilidade Operacional | Integridade das operações    |

---

##  Classificação de Risco

Cada indicador recebe uma pontuação:

| Status  | Pontuação |
| ------- | --------- |
| NORMAL  | 0         |
| ATENÇÃO | 1         |
| CRÍTICO | 2         |

### Classificação Geral da Missão

| Pontuação Total | Resultado         |
| --------------- | ----------------- |
| 0 – 2           | MISSÃO ESTÁVEL    |
| 3 – 7           | MISSÃO EM ATENÇÃO |
| 8+              | MISSÃO CRÍTICA    |

---

##  Inteligência Artificial

O projeto utiliza:

* Ollama
* Llama 3.2 1B
* Prompt Engineering
* Few-Shot Learning

A IA recebe os indicadores do ciclo analisado e gera:

* Alertas operacionais
* Avaliação do impacto
* Recomendações técnicas
* Nível de prioridade

### Exemplo de Saída

```text
 ALERTA CRÍTICO

Status Geral:
• MISSÃO CRÍTICA

Sistemas Afetados:
• Comunicação: 28% → CRÍTICO
• Bateria: 19% → CRÍTICO

Impacto:
• Elevado risco de perda de controle operacional.

Recomendações:
• Restabelecer comunicação com a base.
• Ativar modo de economia máxima de energia.

Prioridade:
• MÁXIMA
```

---

##  Arquitetura do Projeto

```text
Dados da Missão
       │
       ▼
Regras de Classificação
(Python)
       │
       ▼
Pontuação de Risco
       │
       ▼
Prompt Dinâmico
       │
       ▼
Ollama + Llama 3.2
       │
       ▼
Análise Inteligente
       │
       ▼
Relatório Operacional
```

---

##  Estrutura

```text
Projeto/
│
├── IA_Missão_Espacial.ipynb
├── README.md
│
├── Sistema de classificação
│   ├── temperatura_interna()
│   ├── comunicacao_base()
│   ├── sistema_energia()
│   ├── suporte_oxigenio()
│   └── estabilidade_operacional()
│
├── IA
│   ├── chamar_IA()
│   └── consultar_ia()
│
└── Relatórios
    ├── Relatório por ciclo
    ├── Relatório final
    └── Tendência da missão
```

---

##  Instalação

### Instalar Ollama

```bash
curl -fsSL https://ollama.com/install.sh | sh
```

### Iniciar servidor

```python
import subprocess

subprocess.Popen(["ollama", "serve"])
```

### Baixar modelo

```bash
ollama pull llama3.2:1b
```

---

##  Execução

Execute o notebook:

```bash
IA_Missão_Espacial.ipynb
```

O sistema analisará cada ciclo da missão e poderá solicitar uma análise complementar da IA.

---

##  Funcionalidades

* Classificação automática de riscos.
* Relatórios por ciclo.
* Relatório consolidado da missão.
* Tendência de evolução da operação.
* Identificação da área mais afetada.
* Integração com IA local via Ollama.
* Geração de recomendações para tomada de decisão.

---

##  Aplicações

Este projeto demonstra conceitos de:

* Python
* Estruturas de dados
* Funções
* Lógica de decisão
* Sistemas especialistas
* Inteligência Artificial Generativa
* Engenharia de Prompt
* Few-Shot Learning
* Monitoramento de sistemas críticos
