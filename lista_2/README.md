# Machine Learning
Projetos desenvolvidos na disciplina de APRENDIZAGEM DE MÁQUINA E MINERAÇÃO DE DADOS, na UFRN, semestre 2020.6

## Questões desenvolvidas
### Questão 2
Utilize redes neurais perceptron de múltiplas camadas para aproximar as funções abaixo. Para o caso dos itens b e c apresente um gráfico com a curva da função analítica e a curva da função aproximada pela rede neural. Apresente também a curva do erro médio de treinamento com relação ao número de épocas e a curva do erro médio com o conjunto de validação. Procure definir para cada função a arquitetura da rede neural perceptron, isto é, o número de entradas, o número de neurônios em cada camada e o número de neurônios camada de saída.

a) ![equation1](http://www.sciweavers.org/tex2img.php?eq=f%28x_%7B1%7D%2C%20x_%7B2%7D%2C%20x_%7B3%7D%29%20%3D%20x_%7B1%7D%20%5Coplus%20x_%7B2%7D%20%5Coplus%20x_%7B3%7D&bc=White&fc=Black&im=jpg&fs=12&ff=arev&edit=0)

b) ![equation2](https://bit.ly/2TN5PTJ)

c) ![equation3](http://www.sciweavers.org/tex2img.php?eq=f%28%5Cmathbf%7Bx%7D%29%20%3D%20x_%7B1%7D%5E2%20%2B%20x_%7B2%7D%5E2%20%2B%202x_%7B1%7Dx_%7B2%7D%5Ctext%7Bcos%7D%28%5Cpi%20x_%7B1%7Dx_%7B2%7D%29%20%2B%20x_%7B1%7D%20%2B%20x_%7B2%7D%20-%201%24%2C%20%24%5Cmid%20x_%7B1%7D%20%5Cmid%20%5Cleq%201%24%2C%20%24%5Cmid%20x_%7B2%7D%20%5Cmid%20%5Cleq%201&bc=White&fc=Black&im=jpg&fs=12&ff=arev&edit=0) 

### Questão 3
Considere o problema de classificação de padrões constituído por duas espirais intercaladas. A espiral 1 sendo a classe 1 e a espiral 2 sendo a classe 2. Gere os exemplos de treinamento usando as seguintes equações:

para espiral 1, ![equation4](http://www.sciweavers.org/tex2img.php?eq=%24x%20%3D%20%5Cdfrac%7B%5Ctheta%7D%7B4%7D%5Ctext%7Bcos%7D%5Ctheta%24%20%5Cquad%20%24y%20%3D%20%5Cdfrac%7B%5Ctheta%7D%7B4%7D%5Ctext%7Bsen%7D%5Ctheta%24%20%5Cquad%20%24%5Ctheta%20%5Cgeq%200%24&bc=White&fc=Black&im=jpg&fs=12&ff=arev&edit=0)

para espiral 2, ![equation5](http://www.sciweavers.org/tex2img.php?eq=%24x%20%3D%20%28%5Cdfrac%7B%5Ctheta%7D%7B4%7D%20%2B%200.8%29%5Ctext%7Bcos%7D%5Ctheta%24%20%5Cquad%20%24y%20%3D%20%28%5Cdfrac%7B%5Ctheta%7D%7B4%7D%20%2B%200.8%29%5Ctext%7Bsen%7D%5Ctheta%24%20%5Cquad%20%24%5Ctheta%20%5Cgeq%200%24&bc=White&fc=Black&im=jpg&fs=12&ff=arev&edit=0)

fazendo ![equation6](http://www.sciweavers.org/tex2img.php?eq=%24%5Ctheta%24&bc=White&fc=Black&im=jpg&fs=12&ff=arev&edit=0) assumir valores igualmente espaçados entre 0 e 20 radianos. Compare o desempenho das soluções com base na matriz de confusão. Pesquise e utilize uma rede convolutiva já treinada.

Solucione este problema considerando: 

a) Um rede perceptron de múltiplas camadas
b) Uma máquina de vetor de suporte (SVM)
c) Um comitê de máquinas

### Questão 4
Considere uma rede deep learning convolutiva (treinada) aplicada à classificação de padrões em imagens. A base de dados considerada é a CIFAR-10 (pesquise). A referida base de dados consiste de 60 mil imagens coloridas de 32x32 pixels, com 50 mil para treino e 10 mil para teste. As imagens estão divididas em 10 classes, a saber: avião, navio, caminhão, automóvel, sapo, pássaro, cachorro, gato, cavalo e cervo. Cada imagem possui apenas um dos objetos da classe de interesse, podendo estar parcialmente obstruído por outros objetos que não pertençam a esse conjunto. Apresente os resultados da classificação em uma matriz de confusão.

Obs. Pesquise e utilize uma rede convolutiva já treinada

### Questão 5

Utilize uma rede autoencoder, aplicada ao problema da redução de dimensionalidade (compressão/descompressão). Para isto considere a matriz de dados abaixo:

![equation7](https://bit.ly/3kYvZiA)
    
Obtenha uma compressão 5:3, isto é, comprima a matriz 5x5 para uma matriz 3x3. Obtenha a matriz descomprimida isto é ![equation8](http://www.sciweavers.org/tex2img.php?eq=%5Chat%7B%5Cmathbf%7BF%7D%7D&bc=White&fc=Black&im=jpg&fs=12&ff=arev&edit=0) e calcule a relação sinal ruído em dB, definida como:

![equantion9](http://www.sciweavers.org/tex2img.php?eq=%5Cdfrac%7BS%7D%7BN%7D%20%3D%2010%5Ctext%7Blog%7D_%7B10%7D%20%5Cbegin%7Bbmatrix%7D%5Cdfrac%7B%5Csum%5Climits%5E%7BN%7D_%7Bm%3D1%7D%5Csum%5Climits%5E%7BN%7D_%7Bn%3D1%7D%20f%5E2%28m%2Cn%29%7D%7B%5Csum%5Climits%5E%7BN%7D_%7Bm%3D1%7D%5Csum%5Climits%5E%7BN%7D_%7Bn%3D1%7D%20%5Cmid%20f%28m%2Cn%29%20-%20%5Chat%7Bf%7D%5E2%28m%2Cn%29%5Cmid%7D%5Cend%7Bbmatrix%7D&bc=White&fc=Black&im=jpg&fs=12&ff=arev&edit=0)

### Questão 6

Considere o problema de predição de uma série temporal definida como ![equation10](http://www.sciweavers.org/tex2img.php?eq=%24x%28n%29%20%3D%20v%28n%29%20%2B%20%5Cbeta%20v%28n-1%29v%28n-2%29%24&bc=White&fc=Black&im=jpg&fs=12&ff=arev&edit=0), com média zero e variância dada por ![equation11](http://www.sciweavers.org/tex2img.php?eq=%24%5Csigma_%7Bx%7D%5E2%20%3D%20%5Csigma_%7Bv%7D%5E2%20%2B%20%5Cbeta%5E2%5Csigma_%7Bv%7D%5E2%24&bc=White&fc=Black&im=jpg&fs=12&ff=arev&edit=0) onde ![equation12](https://bit.ly/3mQOKoj) é um ruído branco gaussiano, como variância unitária e ![equation13](http://www.sciweavers.org/tex2img.php?eq=%5Cbeta%20%3D%200.5&bc=White&fc=Black&im=jpg&fs=12&ff=arev&edit=0). Utilizando uma rede NARX estime ![equation14](http://www.sciweavers.org/tex2img.php?eq=x%28n%2B1%29%3Df%28x%28n%29%2C%20x%28n-1%29%2C%20x%28n-2%29%2C%20x%28n-3%29%2Cy%28n%29%2C%20y%28n-1%29%2C%20y%28n-2%29%29&bc=White&fc=Black&im=jpg&fs=12&ff=arev&edit=0). Esboce a curva da série e a curva de predição em função em função de n. Esboce também o erro de predição. Calcule a variância da predição e compare com a variância da série temporal. No treinamento utilize a estratégia da resposta forçada do professor. Isto é na estimativa de ![equation15](http://www.sciweavers.org/tex2img.php?eq=x%28n%2B1%29%3Df%28x%28n%29%2C%20x%28n-1%29%2C%20x%28n-2%29%2C%20x%28n-3%29%2Cd%28n%29%2C%20d%28n-1%29%2Cd%28n-2%29%29&bc=White&fc=Black&im=jpg&fs=12&ff=arev&edit=0). Onde ![equation16](http://www.sciweavers.org/tex2img.php?eq=%24d%28n%29%24&bc=White&fc=Black&im=jpg&fs=12&ff=arev&edit=0) é resposta desejada.
