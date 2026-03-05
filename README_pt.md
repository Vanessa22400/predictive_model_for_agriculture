# Recomendação de Culturas com Machine Learning  
*Identificando qual variável do solo possui maior poder preditivo para recomendação de culturas utilizando modelos de machine learning interpretáveis.*

**Dataset:** 2.200 amostras de solo  
**Variáveis:** Nitrogênio (N), Fósforo (P), Potássio (K), pH  
**Técnica:** Modelos baseline de Regressão Logística (comparação usando uma variável por vez)  
**Principal Insight:** Potássio (K) apresenta o sinal preditivo mais forte para recomendação de culturas

---

## Contexto de Negócio

Escolher a cultura correta para cada tipo de solo é uma decisão essencial na agricultura. Os nutrientes presentes no solo influenciam diretamente o crescimento das plantas, o potencial de produtividade e a sustentabilidade da produção agrícola.

Agricultores e agrônomos normalmente utilizam diferentes medições do solo para determinar qual cultura é mais adequada para determinada área. No entanto, entender **qual variável do solo possui o maior poder preditivo** pode simplificar análises iniciais e melhorar o processo de tomada de decisão.

Este projeto explora como diferentes nutrientes do solo influenciam a escolha de culturas, avaliando o poder preditivo de cada variável individualmente. O objetivo não é apenas construir um modelo preditivo, mas também gerar **insights claros e interpretáveis sobre qual propriedade do solo possui maior importância estratégica**.

---

## Dataset

O dataset utilizado neste projeto (`soil_measures.csv`) contém medições do solo e a cultura recomendada para cada amostra.

Cada linha representa uma amostra de solo e inclui:

- **N:** nível de Nitrogênio  
- **P:** nível de Fósforo  
- **K:** nível de Potássio  
- **pH:** acidez ou alcalinidade do solo  
- **crop:** cultura recomendada (variável alvo)

Características do dataset:

- **2.200 amostras de solo**
- **4 variáveis numéricas**
- **22 categorias de culturas**

Alguns exemplos de culturas presentes no dataset:

- arroz
- milho
- grão-de-bico
- banana
- manga
- algodão
- café

---

## Problema

Qual medição do solo possui o maior poder preditivo para determinar a cultura mais adequada?

Responder essa pergunta ajuda a identificar qual nutriente do solo possui maior relevância na tomada de decisões iniciais sobre o plantio.

---

## Objetivos

- Compreender a distribuição das variáveis do solo
- Explorar relações entre medições do solo
- Treinar modelos baseline utilizando uma variável por vez
- Comparar o desempenho preditivo das variáveis
- Identificar qual variável possui maior poder preditivo
- Traduzir os resultados em insights aplicáveis à agricultura

---

## Metodologia

1. **Inspeção do Dataset**  
   Exploração inicial da estrutura do dataset, tipos de dados e estatísticas básicas.

2. **Análise Exploratória de Dados (EDA)**  
   Visualização da distribuição das variáveis do solo e análise de seus padrões.

3. **Análise de Correlação**  
   Avaliação das relações entre variáveis por meio de matriz de correlação e heatmap.

4. **Divisão Treino-Teste**  
   Separação dos dados em conjuntos de treinamento (80%) e teste (20%).

5. **Modelagem Baseline**  
   Treinamento de modelos de Regressão Logística utilizando **uma variável do solo por vez**.

6. **Comparação de Modelos**  
   Comparação das métricas de desempenho para identificar qual variável possui maior poder preditivo.

---

## Ferramentas e Tecnologias

- Python  
- Pandas  
- NumPy  
- Matplotlib  
- Seaborn  
- Scikit-learn  
- Regressão Logística  
- Train-test split  
- Métricas de avaliação de modelos  

---

## Principais Resultados da Análise Exploratória

### Distribuição das Variáveis do Solo

![Distribuição das Variáveis](Images/image1_Distribution_of_each_Feature.png)

**Figura:** Distribuição dos valores de Nitrogênio, Fósforo, Potássio e pH nas amostras de solo.

Observações:

- **Nitrogênio (N):** ampla variação indicando diferentes condições de fertilidade.
- **Fósforo (P):** distribuição mais concentrada em determinadas faixas.
- **Potássio (K):** grande dispersão de valores, sugerindo alta variabilidade entre amostras.
- **pH:** valores dentro de intervalos realistas para solos agrícolas.

---

### Correlação entre Variáveis do Solo

![Mapa de Correlação](Images/image2_Correlation_Heatmap_of_Features.png)

**Figura:** Matriz de correlação entre as variáveis do solo.

Observações:

- A maioria das variáveis apresenta **baixa correlação**, indicando que cada uma fornece informações relativamente independentes.
- Existe uma correlação moderada entre **Fósforo e Potássio**, mas ainda assim cada variável mantém contribuição própria.

Isso reforça a decisão de avaliar o poder preditivo de cada variável individualmente.

---

## Estratégia de Modelagem

Foi utilizado um modelo de **Regressão Logística** treinado utilizando **uma variável por vez**.

Essa abordagem permite comparar de forma clara qual variável do solo possui maior poder preditivo isoladamente.

As variáveis avaliadas foram:

- Nitrogênio (N)
- Fósforo (P)
- Potássio (K)
- pH

O desempenho foi avaliado utilizando **acurácia no conjunto de teste**.

---

## Desempenho dos Modelos

Acurácia obtida utilizando cada variável individualmente:

| Variável | Acurácia |
|------|------|
| Nitrogênio (N) | 0.143 |
| Fósforo (P) | 0.189 |
| Potássio (K) | **0.248** |
| pH | 0.098 |

Apesar da acurácia geral ser limitada devido à **natureza multiclasse do problema (22 culturas)**, a comparação revela claramente qual variável possui maior poder informativo.

O **Potássio (K)** apresentou o melhor desempenho quando utilizado isoladamente.

---

## Principais Insights

**Potássio é o preditor individual mais forte**  
Entre as variáveis analisadas, o potássio apresentou maior capacidade de diferenciar culturas.

**As variáveis do solo são relativamente independentes**  
A baixa correlação entre as medições indica que cada nutriente fornece informação distinta sobre o solo.

**Modelos simples também geram insights relevantes**  
Mesmo um modelo simples como regressão logística pode revelar padrões importantes sobre fatores que influenciam a escolha de culturas.

---

## Impacto Prático

Possíveis aplicações incluem:

**Suporte à decisão agrícola**  
Testes iniciais de solo focados em potássio podem fornecer sinais relevantes sobre a adequação de culturas.

**Planejamento de fertilização**  
Identificar nutrientes com maior influência pode ajudar na gestão de fertilizantes.

**Diagnóstico inicial de solo**  
Priorizar medições mais informativas pode tornar análises preliminares mais eficientes.

---

## Limitações

Algumas limitações devem ser consideradas:

- Apenas **quatro variáveis do solo** foram utilizadas
- Fatores ambientais importantes como **clima, precipitação ou temperatura** não foram incluídos
- O modelo foi simplificado para avaliar variáveis individualmente

Essas restrições reduzem o poder preditivo, mas permitem uma interpretação mais clara dos resultados.

---

## Próximos Passos

Possíveis melhorias para o projeto:

- Incluir variáveis ambientais adicionais (temperatura, umidade, precipitação)
- Treinar modelos utilizando **múltiplas variáveis simultaneamente**
- Testar modelos mais avançados como **Random Forest ou Gradient Boosting**
- Desenvolver um **dashboard interativo de recomendação de culturas**

---

## Estrutura do Repositório

```
.
├── data
├── notebooks
├── images
├── requirements.txt
└── README.md
```

---

## Conclusão

Este projeto demonstra como modelos simples de machine learning podem gerar insights relevantes a partir de dados agrícolas.

Ao comparar o poder preditivo de diferentes nutrientes do solo, a análise identificou **o potássio (K) como a variável mais informativa** para distinguir a adequação de culturas neste dataset.

Além da modelagem preditiva, o projeto destaca como análises exploratórias e modelos interpretáveis podem apoiar **decisões práticas no planejamento agrícola e na gestão do solo**.
