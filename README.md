# FarmTech Solutions - Análise e Previsão de Rendimento de Safras

Este repositório contém a solução desenvolvida pela nossa equipe para o projeto do Cap 1 - FarmTech na era da cloud computing, visando prever o rendimento agrícola com base em condições ambientais e identificar tendências e cenários discrepantes através de análise exploratória e técnicas de Machine Learning.

## Descrição do Projeto

O objetivo deste projeto é fornecer à fazenda de médio porte (aproximadamente 200 hectares) insights claros sobre o rendimento esperado das culturas com base em dados ambientais como precipitação, umidade e temperatura.

### Dados Utilizados

A análise foi feita com o arquivo `crop_yield.csv`, que contém as seguintes variáveis:

- **Cultura:** Tipo de produto agrícola cultivado.
- **Precipitação (mm dia 1):** Volume diário de chuva em milímetros.
- **Umidade específica a 2 metros (g/kg):** Quantidade de vapor de água no ar.
- **Umidade relativa a 2 metros (%):** Umidade relativa do ar.
- **Temperatura a 2 metros (ºC):** Temperatura ambiente a 2 metros acima do solo.
- **Rendimento:** Rendimento agrícola em toneladas por hectare.

## Metodologia

O projeto envolveu as seguintes etapas principais:

1. **Análise Exploratória de Dados (EDA)**
   - Visualização inicial dos dados
   - Identificação de correlações
   - Detecção de outliers e inconsistências

2. **Clusterização para Tendências**
   - Utilização de técnicas não supervisionadas para identificação de padrões de produtividade
   - Análise de clusters para detectar cenários atípicos

3. **Modelagem Preditiva**
   - Construção de cinco modelos preditivos utilizando diferentes algoritmos:
     - Regressão Linear
     - Árvores de Decisão
     - Random Forest
     - Gradient Boosting
     - XGBoost
   - Avaliação de desempenho com métricas adequadas para regressão (RMSE, MAE, R²)

## Como acessar os resultados

Para acessar o notebook com a análise completa e os códigos detalhados, clique no link abaixo:

[FarmTech_Analise_Rendimento_Agricola.ipynb](https://drive.google.com/file/d/1lOkDvWQjkGF1Er8G8vVfxy1QKdOorreU/view?usp=sharing)

## Pré-requisitos

- Python 3.x
- Bibliotecas: Pandas, NumPy, Matplotlib, Seaborn, Scikit-Learn

## Equipe

- Ana Kolodji 
- Fernando Segregio
- Mateus Conciani

## Instituição

Projeto desenvolvido para o curso de Tecnologias de Inteligência Artificial e Machine Learning da FIAP.

---

## Entrega 2: Hospedagem em Nuvem (AWS)

Nesta segunda etapa do projeto, iremos realizar a hospedagem da aplicação de Machine Learning em uma estrutura de computação em nuvem utilizando a AWS (Amazon Web Services). O objetivo é estimar custos e comparar opções para garantir desempenho e conformidade com restrições legais sobre armazenamento de dados.

### Metas da Entrega 2

1. Realizar uma estimativa de custos (On-Demand – 100%) para uma máquina Linux simples nas regiões:
   - São Paulo (BR)
   - Virgínia do Norte (EUA)

   Configurações da máquina:
   - 2 CPUs
   - 1 GiB de memória
   - Até 5 Gigabit de rede
   - 50 GB de armazenamento (HD)

2. Avaliar as opções levando em consideração a necessidade de acesso rápido aos dados dos sensores e restrições legais sobre armazenamento de dados no exterior.

### Resultado da Análise de Custos

[Estimativa de Custos com AWS](https://github.com/anakolodji/Farmtech_Analise_Rendimento_Agricola/blob/main/My%20Estimate1%20-%20Calculadora%20de%20Pre%C3%A7os%20da%20AWS.pdf)

| Região                  | Tipo de Instância | vCPUs | RAM  | Custo Mensal (USD) | Custo Anual (USD) |
|-------------------------|-------------------|-------|------|--------------------|-------------------|
| Virgínia do Norte (EUA) | t3.micro          | 2     | 1GiB | $3,80              | $45,60            |
| São Paulo (BR)          | t3.micro          | 2     | 1GiB | $6,13              | $73,56            |

Custo Total Anual (Região mais barata – EUA):

Aproximadamente $22,80 (12 meses x $1,90)

### Justificativa da Escolha

Embora o custo mensal seja mais barato na Virgínia do Norte (EUA), a melhor escolha é hospedar a solução na região de São Paulo (BR) por dois fatores essenciais:

Acesso rápido aos dados dos sensores:
Hospedar localmente garante latência reduzida e melhor desempenho em tempo real para coleta e processamento das informações dos sensores.

Restrições legais:
Em cenários com restrições legais que impedem o armazenamento de dados no exterior, hospedar no Brasil é obrigatório para conformidade regulatória.

Desta forma, a opção recomendada pelo seu grupo para esta entrega seria a instância t3.micro localizada na região São Paulo (BR), apesar do pequeno aumento nos custos, garantindo desempenho adequado e conformidade com exigências legais locais.

