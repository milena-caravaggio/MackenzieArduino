
<img width="353" alt="Captura de tela_20221125_144047" src="https://user-images.githubusercontent.com/48251038/204034679-3542ac63-56c5-48d5-9521-cb6466a561b2.png">


 ### Este artigo descreve o projeto de Arduino com o objetivo de ser usado de forma inicial para ser um projeto versátil, onde consigamos adaptar para diversos tipos de situações ou usabilidades, se tornando base para outros projetos mais complexos. Exemplos: Monitoramento de temperatura e umidade de um ar condicionado, de um ventilador ou até mesmo um aparato onde recebemos atualizações sobre a umidade e temperatura via Whatsapp para pessoas que possuem problemas respiratórios. Sobre a construção do Hardware, utilizamos uma placa ESP32 (NodeMCU) que por sua vez tem acoplado um sensor DHT22 (sensor de umidade e temperatura). 
 
 
 
< MATERIAIS E MÉTODOS

Essa primeira seção contará com a informação dos módulos/hardware que fora utilizado no projeto final.
Demais detalhes sobre o funcionamento individual de cada componente estão descritos abaixo:

Placa ESP32 (NodeMCU):

Figura 1: Placa ESP32

O ESP32 é uma placa de desenvolvimento com Wifi e Bluetooth, ideal para desenvolvimento de inúmeras aplicações IoT (Internet of Things ou Internet das Coisas). É adequado para dispositivos inteligentes domésticos, controle sem fio industrial, monitoramento sem fio.
Equipado com CPU Xtensa® Dual-Core 32-bit LX6, antena embutida, interface usb-serial CP2102, e regulador de tensão 3.3V AMS1117. A programação pode ser feita em LUA ou usando a IDE do Arduino através de um cabo micro-usb. Com 4 MB de memória flash, o ESP32 ESP-WROOM-32, é uma solução ideal para aplicativos IoT.


Sensor DHT22

Figura 2: Sensor DHT22

O Sensor de Temperatura e Umidade DHT22, também conhecido como Sensor AM2302, é um sensor que faz a medição da temperatura e da umidade com alta precisão, sendo que é permitido fazer leituras de temperaturas entre -40º a 80º Celsius e umidade entre 0 a 100%.
O DHT22 funciona através de um sensor capacitivo de umidade e um termistor para medir o ar circundante, todos enviando informações para um microcontrolador de 8 bits que responde com um sinal digital para outro microcontrolador, como Arduino ou Pic. Ele trabalha com tensão de 3,5 a 5,5V e possui um baixo consumo de corrente, por volta de 1mA a 1,5mA, sendo que em stand by é de 40µA a 50µA, sem contar que sua precisão para medição de umidade chega a aproximadamente 2% RH e a de temperatura é de mais ou menos 0,5°C, tendo um excelente custo benefício para estudantes, amantes e profissionais da área de eletrônica.


<img align="right" width="300" src="https://i2.wp.com/allhtaccess.info/wp-content/uploads/2018/03/programming.gif?fit=1281%2C716&ssl=1" />


⭐Link do projeto para o simulador worki

https://wokwi.com/projects/349305302851519058 

### Passo a passo para executar o projeto

Fazer o dawload do mqtt-explorer, que irá receber as informações do worki

http://mqtt-explorer.com/

### Configuraçãoes necessárias

<img width="506" alt="image" src="https://user-images.githubusercontent.com/48251038/204028861-088ba067-255b-4e90-a847-e9c71b55e30d.png">

> Clicar no botão Advanced, add o topico exclusivo mackenzie20504039/#

<img width="444" alt="image" src="https://user-images.githubusercontent.com/48251038/204029002-1089b9f0-5cbe-46f4-9c97-469010660988.png">

> Em seguida clique no botão de canectar

<img width="508" alt="image" src="https://user-images.githubusercontent.com/48251038/204029296-71c93bc7-af3f-4a0a-bde2-9c41eb0bddd7.png">

> Após conectar, volte ao projeto no worki e execute

<img width="381" alt="image" src="https://user-images.githubusercontent.com/48251038/204029390-b0c7542c-c2d3-4a5b-bf0c-a272435ef07b.png">

> Após alguns segundo é conectado ao mqtt-explorer, onde podemos ver o histórico de temperatura e umidade do ar.

<img width="510" alt="image" src="https://user-images.githubusercontent.com/48251038/204029530-e09a1546-7b0f-44d1-93c1-7f23baa0e24b.png">

> ### Agora precisar fazer a comunicação com o node-red, baixe o programa no link 

https://nodered.org/

# Importante! sega o passo a passo para instalçao e execução do node-red.

### Configuração do Node-red

> Primeiro vamos utilizar o node-red que recebe informações e configurar com nosso topico exclusivo mackenzie20504039


![WhatsApp Image 2022-11-25 at 13 23 43 (2)](https://user-images.githubusercontent.com/48251038/204033141-c5487fc4-1370-45b5-bf8f-c9be3767a727.jpeg)
![cab39f25-616f-4272-9307-eda392e3c724](https://user-images.githubusercontent.com/48251038/204033153-3f9f6a99-227d-4949-b1af-de780bd6d2db.jpg)

> Menu Manager palette

![WhatsApp Image 2022-11-25 at 13 25 13 (1)](https://user-images.githubusercontent.com/48251038/204033248-8984f678-3670-4596-8e8a-f05c85120848.jpeg)

> Depois vamos incluir a biblioteca do whatsApp para enviar mensgens

![WhatsApp Image 2022-11-25 at 13 25 02 (1)](https://user-images.githubusercontent.com/48251038/204033318-57fc7c45-c691-40a9-becc-45862d73704a.jpeg)

> siga o modelo, clique 2x no campo para abrir a configuração

![WhatsApp Image 2022-11-25 at 13 23 33](https://user-images.githubusercontent.com/48251038/204033664-55f1a7ef-cc97-485b-8327-6692d84670d9.jpeg)

![WhatsApp Image 2022-11-25 at 13 23 43 (3)](https://user-images.githubusercontent.com/48251038/204034000-6b9ec833-8802-4671-8f04-a15b1e696a8d.jpeg)


![c80112cc-b5fe-4264-8a00-15f7f86faebd](https://user-images.githubusercontent.com/48251038/204033171-d0b78894-be3e-42e7-9d78-6cc2e04a08fc.jpg)

> Ao clicar 2x no campo de mensagem whats App tem a configuração, vamos usar agora o CallMeBot para enviar as mensagens, seguir os passou e depois preencher as informações como API-KEY na configuração do node-res

https://www.callmebot.com/blog/free-api-whatsapp-messages/

> ##  ⭐ Depois de ter feito todas as etapas o projeto já esta pronto para realizar os testes.





