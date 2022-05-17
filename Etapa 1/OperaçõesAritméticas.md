## Operações Aritméticas
As seguintes operações são possíveis somente quando as imagens utilizadas possuem mesmas dimensões.

### Adição de Imagens
Ao somar N imagens que se situam no intervalo 0-255, o output resulta em um intervalo N x 0-255.
Logo, para que a imagem possa ser mostrada em um monitor de 8 bits, alguma forma de compressão é necessária
(geralmente isso é feito ao dividir a imagem resultante por N, o que volta ao intervalo 0-255).
Portanto, a adição pode ser vista como uma média aritmética entre as imagens.

Uma de suas aplicações é a **redução de ruído**: ao somar diferentes bandas espectrais da mesma imagem, uma média aritmética é feita e os ruídos que havia em uma banda
e não em outras é eliminado.

Outra aplicação é a **combinação de resultados de outros tipos de processamentos**. Um exemplo é a adição de uma imagem original à uma versão sua já filtrada para realce de bordas.

### Subtração de Imagens
Serva para realçar pequenas diferenças espectrais entre duas bandas. O intervalo gerado é -255 a +255 e, para consertar, adicionamos 255 ao resultado e dividimos por 2.
Ao subtrair imagens com contrastes diferentes seus histogramas não coincidem em termos de média e desvio padrão, o que faz com que a imagem resultante tenda à imagem
com maior contraste. A solução seria aplicar um aumento de contraste adequado a ambas as imagens, antes da subtração,
para equalizar a média e o desvio-padrão de seus histogramas. 

### Multiplicação de Imagens
Assim como na adição, a informação comum a ambas imagens é realçada, no entanto, ela requer uma compressão muito mais intensa que a adição, dado que a imagem resultante tem um intervalo 0-65025. A multiplicação é caracterizada pela correção de sombreamentos, mais especificamente na calibração do brilho. Além disso, também pode ser utilizada para fazer segmentação de imagens.

### Divisão de Imagens
Também chamada de razões de banda, é caracterizada pela correção de sombreamentos, sendo responsável pela normalização do brilho. A divisão serve para realçar as diferenças espectrais em um par de bandas, onde os extremos pretos e brancos representam as maiores diferenças em entre elas. Um problema prático que pode surgir é o ruído, visto que, como não aparece em ambas as imagens, é exagerado pela razão.

## Filtros Digitais
Os filtros são nada mais que transformações pixel a pixel da imagem, que dependem do valor do próprio pixel e dos seus respectivos vizinhos. Na filtragem espacial as classificações mais comuns são passa-baixa, passa-alta e passa-banda, no entanto, o filtro passa-banda é utilizado apenas em alguns processos específicos que não cabem no contexto do projeto, logo, não falaremos dele.

### Filtro Passa-baixa
É um filtro que permite a passagem de sinais de baixa frequência e atenua os sinais de alta frequência. A suavização é a característica principal deste filtro, que pode ser de três tipos: Ideal, Butterworth e Gaussiano. O que diferencia um do outro é a função utilizada na máscara, no entanto, não me aprofundarei neste tópico.

### Filtro Passa-alta
É um filtro que permite a passagem somente de sinais de alta frequência, atenuando os sinais de baixa frequência. A nitidez é fundamentalmente uma operação desse filtro que, como o passa-baixa, também pode ser dividido em Ideal, Butterworth e Gaussiano. Todos esses filtros de passa-alta são usualmente representados por sua relação com os passa-baixa, onde sua função de transferência é igual a 1 menos a função de transferência do respectivo filtro passa-baixa.

**Figura 1: Aplicação dos filtros com diferentes parâmetros em uma imagem médica**
![FilterExamples](https://mipav.cit.nih.gov/pubwiki/images/4/4d/FreqFilterExamples.jpg)
