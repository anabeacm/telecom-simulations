# telecom-simulations

1. O que é uma variável aleatória?
- Uma variável aleatória é uma regra ou função que associa os resultados de um evento incerto a números reais.
    - Ela é "aleatória" porque você não sabe o valor exato antes de acontecer, mas conhece os valores possíveis.

2. O que significam média e variância?
- Esses dois números resumem o comportamento de um conjunto de dados ou de uma distribuição:
- Média: Valor esperado ou a tendência central;
- Variância: Medida de dispersão.
- Variância baixa: Os dados estão todos muito espremidos perto da média.
- Variância alta: Os dados estão muito espalhados.

3. O que significa uma distribuição normal (Gaussiana)?
- Modelo matemático em formato de sino que descreve como os valores de uma variável aleatória se distribuem quando o acaso está envolvido.
- Definida por sua média e sua variância: A média determina onde fica o topo do sino; A variância determina o quão "largo" ou "fino" o sino é.
- **Uma propriedade fundamental dela é a simetria:** Os valores têm a mesma chance de cair um pouco acima ou um pouco abaixo da média.

4. O que faz a função randn()?
- Gera números aleatórios que seguem uma Distribuição Normal Padrão — ou seja, uma Gaussiana especial com:
- Média = 0
- Variância = 1 (e desvio padrão = 1)
- Toda vez que você chama randn(), ela sorteia um número seguindo essas regras exatas.

5. Por que aparecem valores positivos e negativos no randn()?
- Como a função randn() usa uma distribuição com média igual a 0 e é simétrica:
- Cerca de 50% dos números sorteados serão maiores que 0 (positivos) e cerca de 50% dos números sorteados serão menores que 0 (negativos).
- Como a variância é 1, a imensa maioria dos valores vai cair no intervalo entre -3 e +3. *Valores como 0.12, -0.85 e 1.4 são muito comuns, enquanto valores como 4.5 ou -5.0 são extremamente raros*.