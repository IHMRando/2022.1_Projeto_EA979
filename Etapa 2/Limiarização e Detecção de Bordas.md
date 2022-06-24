## Limiarização
Este processo nada mais é que uma separação dos grupos de cinza de uma imagem. Isso é realizado determinando uma intensidade, chamada de limiar, que divide a imagem em grupos de pixels com intensidades semelhantes.

Para determinar o valor deste limiar é feito um histograma com as intensidades dos pixels da imagem e a quantidade de pixels com cada intensidade. Na limiarização global, objeto de estudo desta seção, apenas um limiar é escolhido e ele usualmente é escolhido como sendo o meio entre os vales.

**Figura 1: Segmentação de Imagem por Limiarização Global**
![ThresholdSegmentation](https://scipy-lectures.org/_images/sphx_glr_plot_threshold_001.png)

## Detecção de Bordas
