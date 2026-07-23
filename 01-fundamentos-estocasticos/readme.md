1. x = np.random.randn(1000)
- Gera um conjunto (array) com 1.000 números aleatórios sorteados a partir de uma Distribuição Normal Padrão (média $0$ e variância $1$) e guarda todos dentro da variável x.

2. print(x.mean())
- Calcula e exibe na tela a média real dos 1000 números que foram gerados.

3. print(x.var())
- Calcula e exibe na tela a variância real desses 1000 números.

4. plt.hist(x, bins=40)
- Monta um histograma (um gráfico de barras que conta frequências) para você visualizar a distribuição dos dados de x.
    - x: São os dados que serão divididos e contados no gráfico.
    - bins=40: Divide a faixa de valores (que vai de mais ou menos $-3$ até $+3$) em 40 intervalos (colunas) verticais.
