<img align="center" width="300" src="https://vestibulandoansioso.com/wp-content/uploads/2014/09/Vestibular-Mackenzie-2015.jpg" />

### Este artigo descreve o projeto de Arduino com o objetivo de ser usado de forma inicial para ser um projeto versátil, onde consigamos adaptar para diversos tipos de situações ou usabilidades, se tornando base para outros projetos mais complexos. Exemplos: Monitoramento de temperatura e umidade de um ar condicionado, de um ventilador ou até mesmo um aparato onde recebemos atualizações sobre a umidade e temperatura via Whatsapp para pessoas que possuem problemas respiratórios. Sobre a construção do Hardware, utilizamos uma placa ESP32 (NodeMCU) que por sua vez tem acoplado um sensor DHT22 (sensor de umidade e temperatura). 

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

> Primeiro vamos utilizar o bloque que recebe informações e configurar com nosso topico exclusivo mackenzie20504039


![WhatsApp Image 2022-11-25 at 13 23 43 (2)](https://user-images.githubusercontent.com/48251038/204033141-c5487fc4-1370-45b5-bf8f-c9be3767a727.jpeg)
![cab39f25-616f-4272-9307-eda392e3c724](https://user-images.githubusercontent.com/48251038/204033153-3f9f6a99-227d-4949-b1af-de780bd6d2db.jpg)

> Depois vamos incluir a biblioteca do whatsApp para enviar mensgens

![WhatsApp Image 2022-11-25 at 13 25 02 (1)](https://user-images.githubusercontent.com/48251038/204033318-57fc7c45-c691-40a9-becc-45862d73704a.jpeg)

> siga o modelo, clique 2x no campo para abrir a configuração

![WhatsApp Image 2022-11-25 at 13 23 33](https://user-images.githubusercontent.com/48251038/204033664-55f1a7ef-cc97-485b-8327-6692d84670d9.jpeg)

> Manager palette

![WhatsApp Image 2022-11-25 at 13 25 13 (1)](https://user-images.githubusercontent.com/48251038/204033248-8984f678-3670-4596-8e8a-f05c85120848.jpeg)

![c80112cc-b5fe-4264-8a00-15f7f86faebd](https://user-images.githubusercontent.com/48251038/204033171-d0b78894-be3e-42e7-9d78-6cc2e04a08fc.jpg)



