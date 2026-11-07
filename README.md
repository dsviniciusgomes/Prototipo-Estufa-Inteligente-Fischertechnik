# Prototipo-Estufa-Inteligente-Fischertechnik  
O projeto ilustra, de forma prática, como a integração entre sensores e atuadores permite criar soluções automatizadas para o controle das condições ambientais de uma estufa.

## Resumo
Um LED simula a incidência de luz solar, enquanto um fototransistor identifica a luminosidade do ambiente. Quando a luz é detectada, o sistema aciona um motor que abre a cortina, permitindo a entrada do vento para circulação de ar e refrescar o ambiente. Quando a luminosidade deixa de ser identificada, o motor é acionado novamente para fechar a persiana.

![Rascunho do projeto](imagens/rascunho%20projeto.png)

## Observações
*O foco deste projeto está na lógica de funcionamento, no código e na configuração dos componentes de hardware. A montagem física da estufa, incluindo vigas, eixo de rotação e engrenagens, não é detalhada neste documento. Na seção "Estrutura", são apresentadas orientações e referências para auxiliar na construção dessa estrutura.

**O projeto foi desenvolvido com os componentes Fischertechnik disponíveis. Como não tínhamos um sensor de temperatura, optamos pelo uso do fototransistor para simular o controle da luminosidade. Ressaltamos que, em uma estufa inteligente real, o monitoramento da temperatura também é essencial.

## O que o protótipo faz?
O programa desenvolvido no Robo Pro Coding, quando está em execução, atribui a uma variável chamada "estado" o valor inicial 0, semanticamente, signfica que a cortina está abaixada. Após isso, o programa entra em looping infinito e alterna o valor da variável "estado" para 1 se for capturado luminosidade, o que signfica que a cortina está levantada.

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

## Software necessário

- Robo Pro Coding: [Windows](https://apps.microsoft.com/store/detail/robo-pro-coding/9MXPK52R734C?hl=de-de&gl=de&activetab=pivot%3Aoverviewtab), [MAC/iOS](https://apps.apple.com/us/app/robo-pro-coding/id1569643514), [Linux](https://update.fischertechnik-cloud.com/repository/ft-roboprocoding-public/ft-roboprocoding-linux-STABLE.zip), [Android](https://play.google.com/store/apps/details?id=eu.beemo.roboprocoding&pli=1)

## Drivers/Utilitários

Pode ser que seja necessário instalar drivers para conexão USB com notebook/computador pessoal.

- [Driver USB para Windows 32 bits (MSI, 6 MB)](https://www.fischertechnik.de/-/media/fischertechnik/fite/service/downloads/robotics/usbdriverwin32.ashx)
- [Driver USB para Windows 64 bits (MSI, 6 MB)](https://www.fischertechnik.de/-/media/fischertechnik/fite/service/downloads/robotics/usbdriverwin64.ashx)
- [Driver USB (ZIP, 11 MB)](https://www.fischertechnik.de/-/media/fischertechnik/fite/service/downloads/robotics/bt-smart-controller/document/usbdriverbtsmart-all-ft-controller-2017-06-16.ashx)

## Estrutura

A imagem do rascunho apresenta uma estrutura retangular construída com peças de montagem da Coleção Brink Robótica, inspirada no livro Ensino Fundamental – 4º ano, página 50 (Projeto Estufa), ISBN nº 978-65-87758-01-5.

Recomenda-se a leitura do material como referência, especialmente para compreender a montagem do eixo de rotação. Entretanto, não é obrigatório reproduzir o mesmo formato de estrutura, sendo livre a escolha da montagem, desde que os componentes estejam devidamente conectados e o código esteja em execução.

⚠️Atenção: o eixo de rotação conectado ao motor deve possuir um pedaço de plástico fixado, funcionando como um mecanismo de enrolamento para permitir a subida e a descida da cortina. 

Adaptamos também uma peça [(código - 035059)](https://www.fischertechnik.de/en/products/spare-parts/other/35059-x-strut-106-yellow) fixando na parte inferior ao fim da persiana de plástico para realizar uma força peso e facilitar a descida/subida da cortina.

![Eixo e plastico](imagens/eixo-plastico.jpeg)

## Orientações

