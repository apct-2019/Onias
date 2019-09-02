# Layout e componentes de características distribuídas 

O Layout da placa diz respeito ao posicionamento e dimensão das trilhas e componentes que compõe o circuito. É a manifestação física do esquemático da placa.

Para este projeto, existem os seguintes pre-requisitos:
- Conector MicroRF e cabo para SMA
- Conversor DC/DC para células de lítio com saída para 7,4V 4A
- Conector Dados com SPI, I2C, GPIO (2 I/O)

Por se tratar de uma placa que deve operar com sinais de alta frequência, alguns cuidados adicionais devem ser tomados:

- Impedância das trilhas deve ser controlada
- A frequência do ripple dos níveis DC não pode causar interferência nos sinais AC

Dados esses dois cuidados, algumas conclusões podem ser tiradas: 

- Trabalharemos com impedâncias controladas o mais próximo possível de 50 ohms;
- Cada componente do circuito deve ter seu próprio conversor DC/DC, para que não causem interferência entre si;
- O circuito de conversão DC/DC deve ser apropriado para circuitos de RF

Abaixo um vídeo exemplificando como será a estratégia de desenvolvimento das placas:

[![X-Microwave's Modular RF System](https://img.youtube.com/vi/o7zYtF5dE3c/1.jpg)](https://www.youtube.com/watch?v=o7zYtF5dE3c "X-Microwave's Modular RF System")

Pode-se observar a modularidade de cada parte do circuito, podendo fazê-lo a medida que os componentes vão sendo selecionados.

Abaixo, serão dispostos os componentes cujo layout já foram feitos.

- LNA: TQP3M9019
Layout recomendado pelo fabricante:
![](LNA_datasheet.PNG)

Para frequência de operação na faixa 108 a 137 MHz, foram usados os valores 4.7nF e 100nF para os capacitores e 330pH para o indutor
![](LNA-sch.PNG)

Após o posiciomentos dos componentes, este ficou o layout do módulo do LNA:
![](LNA_3d_layout.PNG)








