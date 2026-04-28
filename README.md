🩺 CarePlus Health Tracker IoT


📌 Descrição do Projeto

Este projeto consiste na simulação de um dispositivo vestível (Health Tracker) utilizando o microcontrolador ESP32. O sistema coleta dados de saúde simulados e os envia em tempo real por meio do protocolo MQTT para uma plataforma de processamento (Node-RED).

A solução representa uma aplicação de **Edge Computing**, onde os dados são coletados na borda (dispositivo IoT) e transmitidos para uma camada de processamento.



🎯 Objetivo.

Desenvolver um sistema IoT capaz de:

* Coletar dados de saúde simulados
* Processar dados no dispositivo (Edge)
* Enviar informações em tempo real via MQTT
* Integrar com uma plataforma de visualização (Node-RED)



🛠️ Tecnologias Utilizadas

* ESP32 (simulado no Wokwi)
* Sensor DHT22 (temperatura e umidade)
* Potenciômetro (simulação de batimentos cardíacos)
* Botão (simulação de passos)
* MQTT (broker público HiveMQ)
* Node-RED (executado na nuvem via FlowFuse)
* Arduino IDE (C/C++)



🧱 Arquitetura da Solução

A arquitetura do sistema segue o modelo de IoT em camadas:


[ESP32 + Sensores] → MQTT → [Broker HiveMQ] → [Node-RED (FlowFuse)] → [Processamento / Debug]



📡 Fluxo de Comunicação

O ESP32 coleta os dados dos sensores e publica em tempo real no seguinte tópico MQTT:

careplus/healthtracker/esp32_001



📦 Estrutura do Payload MQTT

{
  "deviceId": "healthtracker_001",
  "type": "HealthTracker",
  "temperature": 24,
  "humidity": 40,
  "heartRate": 60,
  "steps": 1,
  "timestamp": 12059
}



⚙️ Funcionamento do Sistema

📍 Dispositivo (ESP32)

* Lê temperatura e umidade via DHT22
* Simula batimentos cardíacos com potenciômetro
* Simula passos com botão
* Envia dados a cada 3 segundos via MQTT

📍 Comunicação

* Utiliza protocolo MQTT
* Broker público: HiveMQ
* Comunicação em tempo real

📍 Plataforma (Node-RED)

* Consome os dados do tópico MQTT
* Converte JSON
* Exibe no painel de debug



▶️ Como Executar o Projeto

🔹 Simulação no Wokwi

1. Abra o projeto no Wokwi
2. Clique em **Run**
3. Observe os dados sendo enviados via MQTT no console

🔹 Node-RED (FlowFuse)

1. O fluxo está disponível em `node-red-flow.json`
2. O Node-RED consome o tópico MQTT:
careplus/healthtracker/esp32_001
3. Os dados são exibidos no painel de debug em tempo real



📁 Estrutura do Repositório

README.md  
sketch.ino  
diagram.json  
node-red-flow.json  
circuito-wokwi.png  
fluxo-node-red.png  
debug-node-red.png  



📷 Evidências do Projeto

Circuito no Wokwi

<img width="442" height="320" alt="image" src="https://github.com/user-attachments/assets/838ee9b0-3afb-4beb-96e0-a86076ce6726" />




Fluxo no Node-RED
*(adicionar imagem aqui)*


Recebimento de dados (Debug)
*(adicionar imagem aqui)*



📊 Resultados Obtidos

* Envio de dados em tempo real funcionando ✔️
* Integração com MQTT realizada ✔️
* Consumo dos dados no Node-RED ✔️
* Simulação completa de dispositivo IoT ✔️



🎯 Conclusão

O projeto demonstra com sucesso a implementação de uma solução IoT para monitoramento de saúde, utilizando comunicação em tempo real via MQTT e processamento em uma plataforma externa (Node-RED).

A abordagem evidencia conceitos importantes como:

* Edge Computing
* Comunicação assíncrona
* Integração de sistemas IoT
* Processamento de dados em tempo real



🔗 Links

* Simulação Wokwi: *(adicione aqui seu link público)*
* Repositório GitHub: *(link do próprio repositório)*

