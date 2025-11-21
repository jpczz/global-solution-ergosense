# ErgoSense – Monitor Inteligente de Ergonomia e Bem-Estar

## 📌 1. Visão Geral

O **ErgoSense** é um sistema IoT desenvolvido com ESP32 que monitora ergonomia e bem-estar em ambientes de trabalho híbridos ou home office.  
Ele utiliza sensores para acompanhar:

- **Postura** (distância da pessoa até a mesa)  
- **Iluminação do ambiente**  
- **Temperatura e umidade**  
- **Tempo contínuo de trabalho**

Quando detecta algo fora do ideal, o sistema:

- acende um **LED**  
- emite alerta no **buzzer**  
- mostra a mensagem no **display OLED**  
- envia um **JSON via MQTT** para a nuvem  

O projeto demonstra como *Physical Computing*, IoT e IoB podem melhorar saúde, produtividade e qualidade de vida no **futuro do trabalho**.

---

## 📌 2. Contexto – Futuro do Trabalho

Com o aumento do trabalho remoto e híbrido, profissionais passam longas horas em posições inadequadas e em ambientes mal preparados (pouca luz, alta temperatura, ausência de pausas).  
Esse cenário afeta:

- saúde física  
- saúde mental  
- produtividade  
- qualidade de vida  
- taxas de afastamento  

O futuro do trabalho exige ambientes **inteligentes**, capazes de agir proativamente para melhorar o bem-estar humano.

---

## 📌 3. Problema

Hoje, a maioria das pessoas trabalha:

- sem monitoramento de postura  
- sem controle de ambiente (temperatura, umidade, iluminação)  
- sem lembretes de pausas  
- sem feedback em tempo real  

Isso gera:

- dores musculares  
- fadiga visual  
- queda de produtividade  
- risco de LER/DORT  
- estresse e cansaço  

As empresas não têm ferramentas simples e acessíveis que monitorem ergonomia **em tempo real**.

---

## 📌 4. Objetivo da Solução

Criar um sistema IoT capaz de:

- detectar postura inadequada  
- monitorar conforto térmico e luminosidade  
- emitir alertas imediatos  
- sugerir pausas inteligentes  
- enviar dados para a nuvem via MQTT  
- permitir monitoramento remoto via dashboards  

O foco é promover **saúde, bem-estar e produtividade** dentro da temática *Futuro do Trabalho*.

---

## 📌 5. Persona e Cenário de Uso

**Persona:**  
**Ana**, 29 anos, analista de marketing, trabalha em modelo híbrido. Passa horas no computador e sofre com dores nas costas e cansaço visual.

**Cenário de uso:**  
O ErgoSense fica na mesa da Ana monitorando:

- distância (postura)  
- temperatura  
- umidade  
- luz ambiente  
- tempo sentado  

Quando algo sai do ideal:

- LED acende  
- buzzer toca  
- display exibe alerta  
- dados são enviados para a nuvem via MQTT  

---

## 📌 6. Conexão com o Futuro do Trabalho

O ErgoSense está 100% alinhado às tendências:

- ambientes inteligentes  
- IoT e IoB aplicados ao comportamento humano  
- saúde e ergonomia como parte da produtividade  
- automação e monitoramento contínuo  
- decisões baseadas em dados  

Ele demonstra, na prática, como Physical Computing transforma o ambiente de trabalho em um espaço mais **seguro, saudável e eficiente**.

---

## 📌 7. Arquitetura da Solução

### 🧩 7.1 Componentes Utilizados

| Componente | Função |
|-----------|--------|
| ESP32 DevKit V1 | Microcontrolador principal |
| HC-SR04 | Medição de postura pela distância |
| DHT22 | Temperatura e umidade |
| LDR (sensor de luz) | Iluminação ambiente |
| LED | Alerta visual |
| Buzzer | Alerta sonoro |
| OLED SSD1306 | Exibição das mensagens |

---

### 🧩 7.2 Pinagem

| Componente | Pino | ESP32 |
|-----------|------|--------|
| HC-SR04 TRIG | → | D4 |
| HC-SR04 ECHO | → | D5 |
| HC-SR04 VCC | → | 3V3 |
| HC-SR04 GND | → | GND |
| DHT22 DATA | → | D15 |
| OLED SDA | → | D21 |
| OLED SCL | → | D22 |
| LED | → | D2 (via resistor 220Ω) |
| Buzzer | → | D18 |
| LDR AO | → | D34 |
| LDR VCC | → | 3V3 |
| LDR GND | → | GND |

---

## 📌 8. Lógica de Funcionamento

1. **Leitura contínua dos sensores**  
   - distância  
   - temperatura/umidade  
   - luminosidade  
   - tempo sentado  

2. **Processamento**  
   - distância baixa → postura ruim  
   - luz baixa → alerta  
   - temperatura alta → alerta  
   - 45 min sentado → pausa necessária  

3. **Ações do sistema**  
   - LED acende  
   - buzzer toca  
   - display mostra a mensagem  
   - JSON enviado via MQTT  

4. **Exemplos de alertas:**  
   - “Ajuste a postura!”  
   - “Pouca luz!”  
   - “Muito quente!”  
   - “Hora da pausa!”

---

## 📌 9. Comunicação MQTT

### 🔌 9.1 Configuração

- **Broker:** `broker.hivemq.com`  
- **Porta:** `1883`  
- **ID do cliente:** `ErgoSenseDevice`  
- **Tópico publicado:**  

ergosense/dados

---

### 🔌 9.2 Payload JSON enviado pelo ESP32

A cada 5 segundos, o dispositivo envia:

json
{
  "postura": "boa",
  "distancia_cm": 400.0,
  "temperatura_c": 24.0,
  "umidade_pct": 40.0,
  "luz_raw": 1001,
  "tempo_sentado_min": 0,
  "alerta": "Pouca luz!"
}

Campos:

postura – “boa” ou “ruim”

distancia_cm – distância medida

temperatura_c – temperatura ambiente

umidade_pct – umidade

luz_raw – leitura do LDR

tempo_sentado_min – tempo contínuo trabalhando

alerta – mensagem exibida no display

Esse JSON pode alimentar:

dashboards (Grafana, Node-RED)

bancos de dados

aplicações empresariais

📌 10. Tecnologias Utilizadas

ESP32 DevKit V1

C/C++ (Arduino)

Wokwi (simulação)

MQTT

HiveMQ

Sensores físicos (HC-SR04, DHT22, LDR)

Atuadores (LED, buzzer, display OLED)

Git / GitHub

📌 11. Como Executar
▶ 11.1 Pelo Wokwi

Abrir o projeto:
👉 <COLE AQUI o link do seu Wokwi público>

Arquivos principais:

sketch.ino

diagram.json

libraries.txt

Clique em Run (play)

Abra o Serial Monitor para ver:

leituras

alertas

JSON MQTT sendo enviado

Interaja com os sensores:

clique no ultrassônico e altere a distância

aumente temperatura no DHT22

mexa na iluminação do LDR

veja LED / buzzer / display reagindo

📌 12. Estrutura do Repositório

/
├── sketch.ino
├── diagram.json
├── libraries.txt
├── README.md
└── /docs
    ├── circuito.png
    └── oled.png

📌 13. Impacto e Relevância

O ErgoSense mostra como IoT + IoB + Physical Computing podem criar ambientes de trabalho inteligentes.

Benefícios:

prevenção de dores e lesões

aumento de produtividade

bem-estar físico e mental

redução de afastamentos

tomada de decisão baseada em dados

É uma solução acessível, escalável e totalmente alinhada ao Futuro do Trabalho.

📌 14. Link da Simulação

https://wokwi.com/projects/448264856204439553

📌 15. Autor

João Pedro Chizzolini de Freitas - RM553172
FIAP – Global Solution – Physical Computing (IoT & IoB)

