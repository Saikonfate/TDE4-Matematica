# TDE4 - Matemática

Agrupamento (clustering) com **K-Means** aplicado ao conjunto de dados
[Travel Reviews](https://archive.ics.uci.edu/dataset/484/travel+reviews) (UCI, id 484).

## Integrantes

- Lia Costa Andrade
- José Daniel Macêdo Fechine
- Clara Sobreira Vidal
- Morya Samyak Arrais Benicio
- Michel Gomes Pinheiro
- Wesley Furtado Pessoa
- Ingrid Sampaio Angelim do Nascimento
- Maria Taliciane Pereira da Silva

## Etapas do notebook

1. **Carregamento dos dados** — download do dataset via `ucimlrepo` e inspeção inicial
   (variáveis, dimensões, tipos e valores ausentes).
2. **Pré-processamento** — remoção da coluna de identificação do usuário, tratamento de
   ausentes, renomeação dos 10 atributos (categorias de locais avaliados) e
   padronização com `StandardScaler` (média 0, desvio 1).
3. **Escolha de k** — curva do cotovelo (inércia `J(k)`) e silhueta média para
   `k = 1..10`, além do gráfico de silhueta por ponto.
4. **Modelo final** — K-Means com o `k` escolhido, centróides na escala original e
   visualização dos grupos em 2D via PCA.
5. **Análise de robustez** — comparação com/sem padronização (silhueta e ARI),
   contagem de pontos extremos (`|z| > 3`) e estabilidade entre sementes aleatórias.

## Como executar

```bash
pip install -r requirements.txt
jupyter notebook TDE4_Matematica.ipynb
```

Ou abra o notebook diretamente no Google Colab.
