# Acionamento_Motor_de_passo_54HC112
Circuito para lógica de acionamento de motor de passo com CIs 74LS86 (XOR), 54HC112 (flip-flop JK) e SN4HC00 (NAND)

## Introdução
O objetivo é projetar um circuito eletrônico que controla um motor de passo através de sinais de clock e direção, além de possuir um sinal de enable que liga ou desliga o acionamento do motor de passo. No projeto é utilizado portas lógicas XOR e XNOR e flip flops JK para gerar os sinais necessários.

## Tabela Verdade e Mapa de Karnaugh
Antes da realização da montagem do circuito, na qual será usado o CI ULN2003 como driver de potência, é preciso analisar a tabela verdade (T.V.) para se desenvolver uma lógica combinacional capaz de representar o funcionamento do circuito sequencial. Para essa etapa foram estabelecidas duas condições de trabalho:
1. Quando D = 0, a máquina de estados rotaciona no sentido horário.
2. Quando D = 1, a máquina de estados rotaciona no sentido anti-horário.

Partindo dessas condições foi possível elaborar a seguinte T.V:

<div align="center">
<img src ="https://github.com/Brenoaalencar/Acionamento_Motor_de_passo_54HC112/assets/72100554/3e9564e0-e44b-4354-bed8-ea13734d99b7" width="600px"/>
</div>

Visando obter a quantidade certa de portas lógicas  necessárias para representação do funcionamento descrito acima, foram desenvolvidos mapas de Karnaugh, progressivamente manipulado com intuito de determinar uma versão otimizada da lógica implementada na T.V. A seguir pode-se verificar um detalhamento desse processo.

<div align="center">
<img src ="https://github.com/Brenoaalencar/Acionamento_Motor_de_passo_54HC112/assets/72100554/c11dc40e-368e-4a6a-b8bd-b94d230d319f" width="400px"/>
</div>

<div align="center">
<img src ="https://github.com/Brenoaalencar/Acionamento_Motor_de_passo_54HC112/assets/72100554/f8439b96-cda4-4ea7-a550-a8cf2edd75d9" width="400px"/>
</div>

Feitas as simplificações, chega-se em quatro equações necessárias para a construção do circuito, são elas:
* Jb=AD'+A'D
* Kb=A'D'+AD
* Ja=D'B'+DB
* Ka=D'B+DB'

## Esquemático de ligações
Com base na análise lógica previamente elaborada, foi possível prosseguir com a representação do circuito por meio do esquema abaixo, composto por duas portas XOR, duas XNOR  e  dois flip flops JK, desenvolvido com o software Proteus.

<div align="center">
<img src ="https://github.com/Brenoaalencar/Acionamento_Motor_de_passo_54HC112/assets/72100554/312dd1af-3e95-4d09-8d9a-725b2cf4a633" width="700px"/>
</div>

## Montagem
Após análise da simulação e desenvolvimento das otimizações necessárias, é possível implementar a lógica por meio do circuito físico com o auxílio de uma protoboard. A representação da montagem elaborada está representada a seguir. Os componentes usados foram os circuitos integrados 74LS86 (XOR), 54HC112 (flip-flop), SN4HC00 (NAND) e ULN2003 (driver para acionamento do motor).

<div align="center">
<img src ="https://github.com/Brenoaalencar/Acionamento_Motor_de_passo_54HC112/assets/72100554/692f305d-9f3b-474c-8ad2-3e5ac86501cf" width="700px"/>
</div>
