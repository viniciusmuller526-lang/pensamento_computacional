#Crux Sacra Sit Mihi Lux

Você foi contratado para desenvolver a lógica de um sistema automatizado utilizado em uma máquina industrial que realiza um processo contínuo, como mistura ou aquecimento.
O operador controla o sistema por meio de um botão de iniciar. Além disso, o sistema possui dois potenciômetros que influenciam diretamente seu funcionamento.
O primeiro potenciômetro será utilizado para definir o tempo de execução do processo. Esse valor varia de 0 a 1023 e deve ser interpretado pelo sistema como um tempo entre 1 e 10 segundos, em que valores menores representam tempos mais curtos e valores maiores representam tempos mais longos.
Ao pressionar o botão iniciar, o sistema deve ler o valor do potenciômetro de tempo e iniciar o processo. Durante esse período, o LED amarelo deve permanecer aceso, indicando que o processo está em execução. Após o tempo definido, o processo deve encerrar automaticamente, apagando o LED amarelo e acendendo o LED verde, indicando que o ciclo foi finalizado.
Quando o sistema estiver parado, antes de iniciar um novo ciclo, o LED vermelho deve permanecer aceso.
O segundo potenciômetro será utilizado para ajustar a intensidade do processo. Essa intensidade deve ser representada por três LEDs adicionais: um LED aceso indica intensidade baixa, dois LEDs acesos indicam intensidade média e três LEDs acesos indicam intensidade alta.
Durante a execução do processo, o sistema deve indicar a intensidade configurada no momento do início do ciclo. Caso o operador altere os potenciômetros durante a execução, a alteração só será considerada em um novo ciclo.


1) Identifique as entradas e saídas do sistema 
2) Apresente todos os componentes do sistema e para que eles servem
3) Apresente as regras de funcionamento a serem implementadas
4) Explique como você utilizaria estruturas if para controlar o sistema

1R:
As entradas seriam o botão e os dois potenciômetros, e as saídas seriam os LEDs.

2R:
Botão: ele servirá como o imput responsável por iniciar o ciclo.

Potenciômetro de tempo: servirá para ditar o tempo que o LED amarelo (que representa que o processo está em execução) ficará ligado, quanto maior o nível do potenciômetro, mais tempo esse led fiará ligado.

Potenciômetro de intensidade: servirá para ditar a intensidade do processo, indicado por trẽs LEDs. Quanto maior o nível do potenciômetro, mais LEDs acenderão.
LEDs de ciclo: três LEDs, um vermelho, indicando que o processo está parado, um amarelo, que indica que o processo está em execução, e um verde que indica que o processo foi concluído.
LEDs de intensidade: três leds vermelhos, indicando se a intensidade do processo é baixa, média ou alta.

3R:
Regra 1: o processo será iniciado ao apertar o botão.
Regra 2: ao iniciar o processo, o sistema deve ler o valor respectivo dos dois potenciômetros e usá-los como base para o comportamento dos LEDs respectivos.
Regra 3: mesmo que o valor dos potenciômetros seja alterado, o sistema apenas deve usar os valores que recebeu quando o botão foi apertado.

4R:

//If para iniciar processo

if botao == 1:
  iniciar processo

//If para controlar o tempo do processo

If do potenciometro de tempo mapear(A3, 0 a 1023, 1 a 10):
  led amarelo fica mais ou menos tempo acesso com base no imput

//If para controlar o ritmo do trabalho

Ler valor do potenciômetro

  if < 255:
    acender 1 LED

  if > 255 and if < 700:
    acender 2 LEDs

  if > 700:
    acener 3LEDs
  
