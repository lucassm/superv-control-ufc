# Supervisão e Controle de SEP

## Atividade Complementar 4

### Desenvolvimento de um simulador de comunicação entre IED de proteção e SCADA-LTS utilizando os protocolos modbus-TCP e DNP3

1. Com base nos dados de pontos analógicos e digitais coletados nos equipamentos presentes no pátio da SE UFC (6,0kV e 13,8kV) desenvolva um simulador em linguagem de programação Python que simule a comunicação em modbus entre os IEDs dessa subestação e seu sistema SCADA.

Para a implementação do simulador modbus utilize a biblioteca Python *PyModbusTCP* que possui ampla documentação e está disponível no GitHub no seguinte link: [https://github.com/sourceperl/pyModbusTCP](https://github.com/sourceperl/pyModbusTCP)

Considere que os seguintes IEDs têm comunicação modbus-TCP:
- IED do vão de entrada de linha (Disjuntor de 69,0 kV);
- IEDs do vão de transformação (Disjuntor de 69,0 kV);

Considere que os seguintes IEDs têm comunicação DNP3:
- IED da barra de 13,8kV (Disjuntor de 13,8 kV);
- IEDs de saída de alimentador (Religadores de saída de alimentador);

Os equipamentos a serem considerados de acordo com cada protocolo são:

- 01 Chave seccionadora de 69,0 kV (Vão de entrada)
- 01 Transformador de Corrente de 69,0 kV
- 01 Transformador de Potencial de 69,0 kV
- 01 Disjuntor de 69,0 kV
- 02 Chave seccionadora de 69,0 kV (Vão de transformação)
- 02 Transformadores de 69,0kV/13,8kV
