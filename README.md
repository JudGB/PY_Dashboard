# PY_Dashboard (Projeto de Estudos)

Este repositório contém um script em Python desenvolvido para a criação de um **painel de análise de dados educacionais (Dashboard de Turma)**. O projeto foi estruturado a partir de um notebook do Google Colab e convertido para um script executável, com o objetivo de consolidar conceitos de manipulação de dados e geração de gráficos estatísticos.

## Sobre o Projeto e Metodologia

Este projeto foi construído **exclusivamente para fins didáticos e de estudo**. A construção deste dashboard foi realizada com o **auxílio do professor de programação**, que guiou o desenvolvimento apresentando o passo a passo da lógica. 

A metodologia aplicada consistiu em entender profundamente o que cada bloco de código executava, permitindo compreender a transição entre a extração de dados brutos e a exibição de indicadores consolidados de uma turma de alunos.

## Demonstração Visual dos Gráficos

<p align="center">
  <img src="https://github.com/JudGB/PY_Dashboard/blob/main/assets/Imagens/img01dash.png" alt="Quantidade de Alunos por Situação" width="400" />
</p>

<p align="center">
  <img src="https://github.com/JudGB/PY_Dashboard/blob/main/assets/Imagens/img02dash.png" alt="Distribuição das Notas Finais" width="500" />
</p>

## Tecnologias e Bibliotecas Utilizadas

O ecossistema de análise de dados utilizado neste estudo foi composto por:

* **Python 3:** Linguagem base para a construção de toda a lógica e funções.
* **Pandas:** Biblioteca fundamental usada para carregar o arquivo CSV, tratar strings, filtrar registros e calcular métricas estatísticas de maneira otimizada.
* **Matplotlib:** Ferramenta responsável pela renderização visual dos gráficos de barras, histogramas e relatórios horizontais.
* **Gdown:** Biblioteca utilizada para automatizar o download seguro do banco de dados direto de um link compartilhado no Google Drive.
* **Google colab:** Ferramenta aonde foi feito o passo a passo e finalização do código

## O Que Foi Visto e Compreendido

O desenvolvimento passo a passo permitiu o domínio prático sobre os seguintes tópicos de engenharia e análise de dados:

* **ETL (Extração, Transformação e Carga):** Captura automática do arquivo `alunos.csv`, seguido pela higienização completa dos dados.
* **Padronização de Strings:** Criação de funções personalizadas utilizando `.str.strip()`, `.str.lower()` e encadeamento de `.str.replace()` para remover acentos e substituir espaços por *underscores* (`_`) nos cabeçalhos.
* **Tratamento de Tipos de Dados:** Conversão de strings de texto para valores numéricos usando `pd.to_numeric()` com tratamento de erros (`errors="coerce"`).
* **Lógica de Negócio Dinâmica:** Aplicação de funções `lambda` combinadas com `.apply()` para julgar e classificar a situação do aluno (Aprovado/Reprovado) com base na somatória das notas.
* **Análise Temporal e Extremos:** Uso de `pd.to_datetime()` para manipular campos de datas de nascimento, permitindo rastrear o aluno mais velho (`.idxmin()`) e o mais novo (`.idxmax()`) junto com suas respectivas notas.


## Estrutura de Arquivos

Abaixo está o mapeamento do arquivo estruturado no repositório:

```text
├── imagens/                                             # Gráficos exportados do painel
└── dashboradjudson_gabriel_ferreira_dos_santospy.py     # Script principal com a lógica do Dashboard
```

## Como Executar o Projeto Localmente

Para rodar este painel estatístico na sua máquina, siga os passos abaixo:

1. **Clone o repositório:**
   ```bash
   git clone https://github.com/JudGB/PY_Dashboard
   ```

2. **Acesse a pasta do projeto:**
   ```bash
   cd PY_Dashboard
   ```

3. **Instale as dependências necessárias:**
   ```bash
   pip install pandas matplotlib gdown
   ```

4. **Execute o script:**
   ```bash
   python dashboradjudson_gabriel_ferreira_dos_santospy.py
   ```

## Considerações Finais

Este projeto faz parte do portfólio de aprendizado de **Judson Gabriel**. O desenvolvimento supervisionado foi uma etapa fundamental para fixar boas práticas de programação estruturada, criação de funções limpas e documentação com *docstrings* em Python.
