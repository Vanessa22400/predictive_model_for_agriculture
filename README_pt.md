# Recomendação de Colheitas com Aprendizado de Máquina

Este projeto investiga como características do solo influenciam a escolha ideal de cultura agrícola.
A partir de um conjunto de dados contendo níveis de Nitrogênio (N), Fósforo (P), Potássio (K) e pH, o objetivo é identificar qual dessas variáveis, isoladamente, possui maior poder preditivo na recomendação de culturas.

O foco está em **clareza, interpretabilidade e geração de insights práticos**, servindo como uma análise inicial sólida para decisões agrícolas e para estudos exploratórios em Ciência de Dados.

### 1. Objetivo do Projeto

Entender qual característica do solo mais contribui para prever a cultura recomendada.
Para isso, cada variável é avaliada de forma independente usando um modelo simples de **Logistic Regression**.

### 2. Sobre o Conjunto de Dados

O arquivo `soil_measures.csv` contém:

* N — Nitrogênio
* P — Fósforo
* K — Potássio
* pH — Acidez/Alcalinidade
* Crop — Colheita recomendada

Cada linha corresponde a uma amostra de solo com sua respectiva recomendação.

### 3. Metodologia

O projeto segue um fluxo objetivo e claro:

1. Análise exploratória das variáveis (EDA)
2. Visualização das distribuições e correlações
3. Separação dos dados em treino e teste
4. Treinamento de modelos, usando uma variável por vez
5. Comparação de acurácia entre as variáveis
6. Identificação da variável individual mais preditiva

Esse processo evidencia boas práticas e organização — ideal para um primeiro projeto de portfólio.

### 4. Resultados

Após testar cada variável separadamente em modelos de Logistic Regression:

**Potássio (K)** apresentou a maior acurácia entre todos os atributos.

Embora o modelo seja propositalmente simples, o resultado indica que níveis de K carregam um sinal preditivo relevante para recomendar culturas adequadas.

Esse tipo de insight pode orientar decisões relacionadas a manejo do solo, planejamento agrícola ou análises mais avançadas em estudos futuros.


### 5. Próximos Passos (Sugestões)

* Testar modelos mais robustos (Random Forest, XGBoost)
* Avaliar combinações de variáveis
* Criar pipelines de pré-processamento
* Explorar métricas além da acurácia quando fizer sentido
