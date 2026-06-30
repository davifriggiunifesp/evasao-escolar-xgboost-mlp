# Algoritmos de classificação no auxílio ao combate à evasão estudantil
Projeto da disciplina de Inteligência Artificial - UNIFESP

Comparação entre **XGBoost** e **Multilayer Perceptron (MLP)** para a predição de
evasão estudantil, em um problema de classificação relacionado à **ODS 4 (Educação de Qualidade)**.

## Projeto
A evasão estudantil é um desafio para alcançar uma educação de qualidade (ODS 4). O trabalho trata 
do problema com algoritmos de classificação (evadir, continuar, formar), e faz a comparação  entre 
dois modelos, o XGBoost, baseado em árvores de decisão e o Multilayer Perceptron (MLP), baseado em 
redes neurais, avaliando qual é superior para dados tabulares e suas razões.

## Base
[Predict Students' Dropout and Academic Success](https://archive.ics.uci.edu/dataset/697/predict+students+dropout+and+academic+success)
UCI Machine Learning Repository (4.424 instâncias, 36 variáveis, 3 classes). Licença CC BY 4.0.
A base é carregada automaticamente pelo notebook via a biblioteca `ucimlrepo`.

## Execução
1. Abra o notebook `codigos.ipynb` no Google Colab (há um botão "Open in Colab" no topo do arquivo)
   ou em um ambiente Jupyter local.
2. Se for rodar localmente, instale todas as dependências:
```
pip install -r requirements.txt
```
3. Execute as células de código na ordem

## Principais resultados
XGBoost: F1-macro = 0,706 ± 0,018 | Tempo médio = ~2,2 s          
MLP: F1-macro = 0,642 ± 0,019 | Tempo médio = ~9,1 s

Com 30 iterações com splits pareados, o XGBoost foi superior ao MLP em todas, com
desempenho superior e cerca de 4× mais rápido, o que condiz com a literatura sobre
a vantagem de modelos baseados em árvores em dados tabulares.
