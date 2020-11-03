# Machine Learning
Projetos desenvolvidos na disciplina de APRENDIZAGEM DE MÁQUINA E MINERAÇÃO DE DADOS, na UFRN, semestre 2020.6

## Questões desenvolvidas
### Questão 2
Utilize redes neurais perceptron de múltiplas camadas para aproximar as funções abaixo. Para o caso dos itens b e c apresente um gráfico com a curva da função analítica e a curva da função aproximada pela rede neural. Apresente também a curva do erro médio de treinamento com relação ao número de épocas e a curva do erro médio com o conjunto de validação. Procure definir para cada função a arquitetura da rede neural perceptron, isto é, o número de entradas, o número de neurônios em cada camada e o número de neurônios camada de saída.

a) $f(x_{1}, x_{2}, x_{3}) = x_{1} \oplus x_{2} \oplus x_{3}$

b) $f(\mathbf{x}) = [\dfrac{\text{sen}(\pi\parallel\mathbf{x}\parallel)}{\pi\parallel\mathbf{x}\parallel}]$, $\mathbf{x} = \begin{bmatrix} x_{1} & x_{2}\end{bmatrix}^T$, $\mid x_{1} \mid \leq 10$ e $\mid x_{2} \mid \leq 10$

c) $f(\mathbf{x}) = x_{1}^2 + x_{2}^2 + 2x_{1}x_{2}\text{cos}(\pi x_{1}x_{2}) + x_{1} + x_{2} - 1$, $\mid x_{1} \mid \leq 1$, $\mid x_{2} \mid \leq 1$

### Questão 3
Considere o problema de classificação de padrões constituído por duas espirais intercaladas. A espiral 1 sendo a classe 1 e a espiral 2 sendo a classe 2. Gere os exemplos de treinamento usando as seguintes equações:

para espiral 1, $x = \dfrac{\theta}{4}\text{cos}\theta$ &nbsp;&nbsp;&nbsp;&nbsp; $y = \dfrac{\theta}{4}\text{sen}\theta$ &nbsp;&nbsp;&nbsp;&nbsp; $\theta \geq 0$

para espiral 2, $x = (\dfrac{\theta}{4} + 0.8)\text{cos}\theta$ &nbsp;&nbsp;&nbsp;&nbsp; $y = (\dfrac{\theta}{4} + 0.8)\text{sen}\theta$ &nbsp;&nbsp;&nbsp;&nbsp; $\theta \geq 0$

fazendo $\theta$ assumir valores igualmente espaçados entre 0 e 20 radianos. Compare o desempenho das soluções com base na matriz de confusão. Pesquise e utilize uma rede convolutiva já treinada.

Solucione este problema considerando: 

a) Um rede perceptron de múltiplas camadas
b) Uma máquina de vetor de suporte (SVM)
c) Um comitê de máquinas

### Questão 4
Considere uma rede deep learning convolutiva (treinada) aplicada à classificação de padrões em imagens. A base de dados considerada é a CIFAR-10 (pesquise). A referida base de dados consiste de 60 mil imagens coloridas de 32x32 pixels, com 50 mil para treino e 10 mil para teste. As imagens estão divididas em 10 classes, a saber: avião, navio, caminhão, automóvel, sapo, pássaro, cachorro, gato, cavalo e cervo. Cada imagem possui apenas um dos objetos da classe de interesse, podendo estar parcialmente obstruído por outros objetos que não pertençam a esse conjunto. Apresente os resultados da classificação em uma matriz de confusão.

Obs. Pesquise e utilize uma rede convolutiva já treinada

### Questão 5

Utilize uma rede autoencoder, aplicada ao problema da redução de dimensionalidade (compressão/descompressão). Para isto considere a matriz de dados abaixo:

$$\mathbf{F} = \begin{bmatrix} 0.9192 & 0.4677 & 0.1714 & 0.0703 & 0.1052 \\ 
0.7719 & 0.9291 & 0.3725 & 0.1238 & 0.0416 \\
0.0654 & 0.4459 & 0.9397 & 0.3263 & 0.3686 \\
0.4428 & 0.1433 & 0.1649 & 0.9601 & 0.4239 \\
0.07772 & 0.2053 & 0.2550 & 0.5177 & 0.9272 \end{bmatrix}$$
    
Obtenha uma compressão 5:3, isto é, comprima a matriz 5x5 para uma matriz 3x3. Obtenha a matriz descomprimida isto é $\hat{\mathbf{F}}$ e calcule a relação sinal ruído em dB, definida como:

$$\dfrac{S}{N} = 10\text{log}_{10} \begin{bmatrix}\dfrac{\sum\limits^{N}_{m=1}\sum\limits^{N}_{n=1} f^2(m,n)}{\sum\limits^{N}_{m=1}\sum\limits^{N}_{n=1} \mid f(m,n) - \hat{f}^2(m,n)\mid}\end{bmatrix}$$

### Questão 6

Considere o problema de predição de uma série temporal definida como $x(n) = v(n) + \beta v(n-1)v(n-2)$, com média zero e variância dada por $\sigma_{x}^2 = \sigma_{v}^2 + \beta^2\sigma_{v}^2$ onde $v(n)$ é um ruído branco gaussiano, como variância unitária e $\beta = 0.5$. Utilizando uma rede NARX estime $x(n+1)=f(x(n), x(n-1), x(n-2), x(n-3),y(n), y(n-1), y(n-2))$. Esboce a curva da série e a curva de predição em função em função de n. Esboce também o erro de predição. Calcule a variância da predição e compare com a variância da série temporal. No treinamento utilize a estratégia da resposta forçada do professor. Isto é na estimativa de $x(n+1)=f(x(n), x(n-1), x(n-2), x(n-3),d(n), d(n-1),d(n-2))$. Onde $d(n)$ é resposta desejada.
