# Aula 1 - Fundamentos

`x = np.random.randn(1000)`

Gera um vetor `numpy.ndarray` contendo 1000 amostras independentes provenientes de uma Distribuição Normal Padrão, cuja média teórica é 0 e a variância teórica é 1.

Em notação matemática:

\[
x \sim N(0,1)
\]

`print(x.mean())`

Calcula e exibe a média empírica das 1000 amostras geradas.

`print(x.var())`

Calcula e exibe a variância empírica das amostras.

`plt.hist(x, bins=40)`

Constrói um histograma, permitindo visualizar graficamente como os valores estão distribuídos.

- `x`: Conjunto de dados que será analisado.
- `bins=40`: Divide automaticamente a faixa de valores presentes em x em 40 intervalos (bins), contabilizando quantas amostras pertencem a cada intervalo.

Quanto maior o número de amostras, mais o histograma se aproxima da conhecida Curva de Gauss (Distribuição Normal).

# Definições

## Ruído

Qualquer perturbação aleatória e indesejada que se soma ao sinal útil durante sua transmissão, processamento ou recepção, degradando a qualidade da informação e dificultando sua recuperação pelo receptor.

Matematicamente:

\[
x(t)=s(t)+n(t)
\]

onde:

- s(t): sinal transmitido (informação útil);
- n(t): ruído;
- x(t): sinal recebido.

### Ruído Gaussiano

No modelo de ruído gaussiano, cada amostra do ruído segue uma Distribuição Normal.

Ou seja,

\[
n \sim N(0,\sigma^2)
\]

onde:

- Média = 0;
- Variância = \(\sigma^2\).

### Ruído Branco

Um **ruído branco** possui aproximadamente a mesma quantidade de energia (ou, mais precisamente, a mesma densidade espectral de potência) em todas as frequências de interesse.

Isso significa que nenhuma frequência é privilegiada em relação às demais.

---

## Ruído Colorido

Um **ruído colorido** apresenta distribuição de energia diferente ao longo das frequências.

Algumas frequências possuem mais energia do que outras, caracterizando uma preferência espectral.

---

# Atividade 1.1

## Objetivo

1. Gerar duas variáveis aleatórias gaussianas independentes;
2. Construir um vetor de números complexos normalizado;
3. Visualizar esse vetor utilizando um Scatter Plot (Gráfico de Dispersão).

## Construção do sinal complexo

A atividade utiliza:

```python
s = np.sqrt(1/2) * (x + 1j*y)
```

onde:

- x → Componente em fase;
- y → Componente em quadratura;
- 1j → Unidade imaginária do Python;
- √(1/2) → Fator de normalização utilizado para que a potência média do sinal seja igual a 1.

Assim, cada elemento de `s` é um número complexo da forma

\[
s = x + jy
\]

representando um ponto no plano complexo.


## Scatter Plot

Projeta cada número complexo no plano cartesiano:

- Eixo horizontal → Parte Real (In-Phase);
- Eixo vertical → Parte Imaginária (Quadrature).

Como:

- Ambas as componentes possuem média 0;
- Ambas possuem variância 1;
- Possuem a mesma dispersão;
- São independentes;

Nenhuma direção do plano é privilegiada.

Como consequência, a nuvem de pontos apresenta uma distribuição aproximadamente circular, centrada na origem.

## OBS:

A expressão

```python
np.sqrt(1/2) * (x + 1j*y)
```

Gera uma variável aleatória complexa circularmente simétrica, normalizada para potência média unitária, que nesse contexto da simulação, representa um ruído gaussiano complexo (AWGN).