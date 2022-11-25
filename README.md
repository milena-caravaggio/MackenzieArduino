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

Clicar no botão Advanced, add o topico exclusivo mackenzie20504039/#

<img width="444" alt="image" src="https://user-images.githubusercontent.com/48251038/204029002-1089b9f0-5cbe-46f4-9c97-469010660988.png">

em seguida clique no botão de canectar

<img width="508" alt="image" src="https://user-images.githubusercontent.com/48251038/204029296-71c93bc7-af3f-4a0a-bde2-9c41eb0bddd7.png">

Após conectar, volte ao projeto no worki e execute

<img width="381" alt="image" src="https://user-images.githubusercontent.com/48251038/204029390-b0c7542c-c2d3-4a5b-bf0c-a272435ef07b.png">

Após alguns segundo é conectado ao mqtt-explorer, onde podemos ver o histórico de temperatura e umidade do ar.

<img width="510" alt="image" src="https://user-images.githubusercontent.com/48251038/204029530-e09a1546-7b0f-44d1-93c1-7f23baa0e24b.png">

Agora precisar fazer a comunicação com o node-red, baixe o programa no link 

https://nodered.org/

Importante! sega o passo a passo para instalçao e execução.





