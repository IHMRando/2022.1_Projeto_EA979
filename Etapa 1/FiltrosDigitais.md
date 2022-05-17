## Filtros Digitais
Os filtros são nada mais que transformações pixel a pixel da imagem, que dependem do valor do próprio pixel e dos seus respectivos vizinhos. Na filtragem espacial as classificações mais comuns são passa-baixa, passa-alta e passa-banda, no entanto, o filtro passa-banda é utilizado apenas em alguns processos específicos que não cabem no contexto do projeto, logo, não falaremos dele.

### Filtro Passa-baixa
É um filtro que permite a passagem de sinais de baixa frequência e atenua os sinais de alta frequência. A suavização é a característica principal deste filtro, que pode ser de três tipos: Ideal, Butterworth e Gaussiano. O que diferencia um do outro é a função utilizada na máscara, no entanto, não me aprofundarei neste tópico.

### Filtro Passa-alta
É um filtro que permite a passagem somente de sinais de alta frequência, atenuando os sinais de baixa frequência. A nitidez é fundamentalmente uma operação desse filtro que, como o passa-baixa, também pode ser dividido em Ideal, Butterworth e Gaussiano. Todos esses filtros de passa-alta são usualmente representados por sua relação com os passa-baixa, onde sua função de transferência é igual a 1 menos a função de transferência do respectivo filtro passa-baixa.

**Figura 1: Aplicação dos filtros com diferentes parâmetros em uma imagem médica**
![FilterExamples](https://mipav.cit.nih.gov/pubwiki/images/4/4d/FreqFilterExamples.jpg)
