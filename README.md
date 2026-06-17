Disciplina de Inteligência Artificial , Professor Munif , Unicesumar 2026

# Predição de Doenças Cardíacas Utilizando Inteligência Artificial

## Integrantes

* Nome do Aluno 1 - RA: 23403549-2

## Contextualização do tema escolhido

As doenças cardiovasculares estão entre as principais causas de morte no mundo. A utilização de técnicas de Inteligência Artificial pode auxiliar profissionais da saúde na identificação precoce de pacientes com maior probabilidade de desenvolver doenças cardíacas, contribuindo para diagnósticos mais rápidos e precisos.

## Problema

Dado um conjunto de características clínicas de pacientes, o objetivo deste trabalho é desenvolver modelos capazes de classificar se um indivíduo possui ou não doença cardíaca.

## Hipótese da equipe

A equipe acredita que diferentes algoritmos de Inteligência Artificial apresentarão desempenhos distintos na classificação dos pacientes. Espera-se que o modelo SVM obtenha melhores resultados preditivos, enquanto a Árvore de Decisão ofereça maior interpretabilidade.

## Descrição do dataset utilizado

Foi utilizado o Heart Disease Dataset, disponibilizado no Kaggle por John Smith e baseado no tradicional conjunto de dados de Cleveland da UCI Machine Learning Repository.

O conjunto de dados contém informações clínicas dos pacientes, incluindo idade, sexo, tipo de dor no peito, pressão arterial, colesterol, frequência cardíaca máxima, entre outras variáveis relevantes.

A variável alvo é denominada "target", em que:

* 0 = Sem doença cardíaca;
* 1 = Com doença cardíaca.

Antes do treinamento dos modelos, registros duplicados foram removidos para evitar vazamento de dados (data leakage) e garantir uma avaliação mais confiável dos algoritmos.

## Métodos de Inteligência Artificial utilizados

### Parte 1 – Árvore de Decisão

A Árvore de Decisão é um algoritmo supervisionado que constrói regras de decisão a partir dos atributos do conjunto de dados, permitindo interpretar facilmente o processo de classificação.

### Parte 2 – Máquina de Vetores de Suporte (SVM)

O SVM é um algoritmo supervisionado que busca encontrar um hiperplano capaz de separar as classes com a maior margem possível. Para este trabalho, foi utilizado o kernel RBF juntamente com a padronização dos atributos por meio do StandardScaler.

## Avaliação dos modelos

Os dados foram divididos em conjuntos de treinamento (80%) e teste (20%), utilizando estratificação das classes.

As métricas utilizadas para avaliação foram:

* Acurácia;
* Precisão;
* Recall;
* F1-score;
* Matriz de confusão.

### Resultados da Árvore de Decisão

* Acurácia: 72,13%

| Classe     | Precisão | Recall | F1-score |
| ---------- | -------- | ------ | -------- |
| Sem Doença | 0,69     | 0,71   | 0,70     |
| Com Doença | 0,75     | 0,73   | 0,74     |

(Inserir imagem da matriz de confusão da Árvore)

(Inserir imagem da árvore gerada)

### Resultados do SVM

* Acurácia: 77,05%

| Classe     | Precisão | Recall | F1-score |
| ---------- | -------- | ------ | -------- |
| Sem Doença | 0,77     | 0,71   | 0,74     |
| Com Doença | 0,77     | 0,82   | 0,79     |

(Inserir imagem da matriz de confusão do SVM)

## Comparação dos resultados

| Métrica               | Árvore de Decisão | SVM    |
| --------------------- | ----------------- | ------ |
| Acurácia              | 72,13%            | 77,05% |
| Precisão (Com Doença) | 75%               | 77%    |
| Recall (Com Doença)   | 73%               | 82%    |
| F1-score (Com Doença) | 74%               | 79%    |
| Falsos Negativos      | 9                 | 6      |

Observou-se que o SVM apresentou melhor desempenho geral, principalmente na identificação correta de pacientes com doença cardíaca, resultando em menor quantidade de falsos negativos.

## Conclusão

Os resultados demonstraram que ambos os modelos foram capazes de realizar a classificação dos pacientes. Entretanto, o SVM apresentou desempenho superior nas métricas avaliadas, especialmente no recall da classe positiva, aspecto relevante em aplicações médicas. Por outro lado, a Árvore de Decisão destacou-se pela interpretabilidade, permitindo compreender as regras utilizadas pelo modelo durante o processo de classificação.

Dessa forma, conclui-se que o SVM foi o modelo mais adequado para este conjunto de dados sob a perspectiva preditiva, enquanto a Árvore de Decisão mostrou-se útil para fins explicativos e de apoio à tomada de decisão.
