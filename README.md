# Prototipo-Estufa-Inteligente-Fischertechnik  
O projeto ilustra, de forma prática, como a integração entre sensores e atuadores permite criar soluções automatizadas para o controle das condições ambientais de uma estufa.

## Resumo
Um LED simula a incidência de luz solar, enquanto um fototransistor identifica a luminosidade do ambiente. Quando a luz é detectada, o sistema aciona um motor que abre a cortina, permitindo a entrada do vento para circulação de ar e refrescar o ambiente. Quando a luminosidade deixa de ser identificada, o motor é acionado novamente para fechar a persiana.

![Rascunho do projeto](imagens/rascunho%20projeto.png)

## Observações
O projeto foi desenvolvido com os componentes Fischertechnik disponíveis. Como não tínhamos um sensor de temperatura, optamos pelo uso do fototransistor para simular o controle da luminosidade. Ressaltamos que, em uma estufa inteligente real, o monitoramento da temperatura também é essencial.

## O que o protótipo faz?
O programa desevolvido no Robo Pro Coding, quando está em execução, atribui a uma variável chamada "estado" o valor inicial 0, semânticamente, signfica que a cortina está abaixada. Após isso, o programa entra em looping infinito e alterna o valor da variável "estado" para 1 se for capturado luminosidade, o que signfica que a cortina está levantada.

Caso o fotransistor identifique luminosidade, aguarda 3 segundos e verifica se ainda está incidindo luz. Caso positivo, o motor é acionado no sentido horário girando o eixo de rotação durante 4 segundos a uma velocidade de 300 em unidades definidas no código. Após o tempo, o motor é parado. 

Caso o fotransistor não identifique luminosidade, aguarda 3 segundos e verifica se ainda não está incidindo luz. Caso positivo, o motor é acionado no sentido anti horário girando o eixo de rotação durante 4 segundos a uma velocidade de 300 em undiades definidas no código. Após o tempo, o motor é parado. 

## Componentes necessários

- BT Smart Controller - [código 161944](https://www.fischertechnik.de/en/products/spare-parts/electronics/161944-bt-smart-controller-red) (Qntd: 1) 
- Motor 9V - [código 137096](https://www.fischertechnik.de/en/products/spare-parts/electronics/137096-motor-xs-9v-black) (Qntd: 1)
- Fototransistor - [código 36134](https://www.fischertechnik.de/en/products/spare-parts/electronics/36134-photo-transistor-assembled-yellow)  (Qntd: 1)
- Suporte bateria - [código 135719](https://www.fischertechnik.de/en/products/spare-parts/electronics/135719-battery-holder-9v-red) (Qntd: 1)
- Cabo duplo - [código 203847](https://www.fischertechnik.de/en/products/spare-parts/203847-cable-bundle-stem-coding-pro) (Qntd: 3) 
- Pilha 9V (Qntd: 1) 
- Fonte de luz ou led para ligar/desligar na direção do Fototransistor (Qntd: 1)
- Notebook/Laptop/Computador (MAC, Windows ou Linux) ou celular/smartphone (Android ou iOS) (Qntd: 1) 
- Cabo usb para BT Smart Controller ou conexão bluetooth do Notebook/Smartphone (Qntd: 1) 