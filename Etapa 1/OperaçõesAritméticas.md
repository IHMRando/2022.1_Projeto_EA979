## Adição de Imagens
Ao somar N imagens que se situam no intervalo 0-255, o output resulta em um intervalo N x 0-255.
Logo, para que a imagem possa ser mostrada em um monitor de 8 bits, alguma forma de compressão é necessária
(geralmente isso é feito ao dividir a imagem resultante por N, o que volta ao intervalo 0-255).
Portanto, a adição pode ser vista como uma média aritmética entre as imagens.

Uma de suas aplicações é a **redução de ruído**: ao somar diferentes bandas espectrais da mesma imagem, uma média aritmética é feita e os ruídos que havia em uma banda
e não em outras é eliminado.

Outra aplicação é a **combinação de resultados de outros tipos de processamentos**. Um exemplo é a adição de uma imagem original à uma versão sua já filtrada para realce de bordas.

## Subtração de Imagens
Serva para realçar pequenas diferenças espectrais entre duas bandas. O intervalo gerado é -255 a +255 e, para consertar, adicionamos 255 ao resultado e dividimos por 2.
Ao subtrair imagens com contrastes diferentes seus histogramas não coincidem em termos de média e desvio padrão, o que faz com que a imagem resultante tenda à imagem
com maior contraste. A solução seria aplicar um aumento de contraste adequado a ambas as imagens, antes da subtração,
para equalizar a média e o desvio-padrão de seus histogramas. 
