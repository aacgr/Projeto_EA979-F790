## Processo moderno multi-frame

Nos últimos tempos, com a evolução dos *smartphones* e da qualidade da rede de internet, houve também a 
evolução das câmeras digitais: é possível gravar vídeos e tirar fotos de altíssima qualidade com apenas 
um aparelho celular. Um conceito fundamental no deselvolvimento das câmeras foi o de capturar e juntar 
vários frames, ao invés de capturar somente uma imagem, em busca de melhorar sua qualidade.

![Pipeline-image](./assets/pipeline-modern.jpg)

### Sensor da câmera

O sensor de uma câmera digital é composto por uma grade 2D de fotodiodos, responsáveis por converter fótons
em carga elétrica. Normalmente, cada fotodiodo corresponde a um pixel da imagem. Para criar imagens coloridas,
é necessário utilizar filtros de cores. Geralmente, esses filtros permitem que somente uma das três cores do 
grupo RGB sejam capturadas. O filtro mais comum é a matriz CFA, também conhecida como filtro de Bayer.

![Bayer-image](./assets/bayer.jpg)
![Sensor-image](./assets/camera-sensor.jpg)

### Controle de exposição

Exposição é a quantidade de luz que o sensor da câmera recebe. É de fundamental importância que 
isso seja bem regulado, já que pode gerar ruído, fazer com que a imagem fique borrada, entre outros.
O ajuste da exposição pode ser feito pela combinação da abertura da lente, ISO (ganho do sensor) e o
tempo de exposição. Contudo, como os celulares tem uma abertura de lente fixa, o controle geralmente é
feito através do tempo de exposição e do ganho do sensor, que podem ser controlados manualmente ou 
serem usados com a configuração padrão automaticamente.

### Alinhamento 

Consiste no processo de alinhar corretamente os diversos frames obtidos, em busca de obter uma
imagem de alta qualidade. 

### *Merge*

Faz com que os vários frames capturados se tornem um só. HDR+ foi um dos primeiros processos a serem 
sistribuídos comercialmente em larga escala. Ele mesclava, a partir de um frame de referência, pares de 
frames e os interpolava. O peso da interpolação dependia da quantidade de ruído esperada e a diferença
entre os parees, dando um peso maior a referência quando a diferença entre eles era muito grande e um
peso maior a mescla quando o ruído esperado era maior que a diferença. O produto final é um frame com 
filtro de Bayer e um bit de profundidade maior do que o esperado caso só um frame fosse capturado. 

## Referências

- https://www.cambridgeincolour.com/tutorials/camera-sensors.htm
- https://www.digitalcameraworld.com/tutorials/what-is-exposure
