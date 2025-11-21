# ErgoSense – Monitor Inteligente de Ergonomia e Bem-Estar

## 1. Visão Geral

O **ErgoSense** é um sistema IoT desenvolvido com ESP32 que monitora ergonomia e bem-estar de profissionais em ambientes de trabalho híbridos ou home office. Utilizando sensores de distância, temperatura/umidade e luminosidade, o dispositivo identifica postura inadequada, condições ambientais desconfortáveis e excesso de tempo contínuo de trabalho.

A solução emite alertas locais (LED, buzzer, mensagens em display) e envia os dados para a nuvem via MQTT, permitindo monitoramento remoto e integração com dashboards. O projeto demonstra como a Internet das Coisas e o Physical Computing podem contribuir para um futuro do trabalho mais saudável, produtivo e sustentável.

---

## 2. Contexto – Futuro do Trabalho

No futuro do trabalho, especialmente com o crescimento do home office e dos modelos híbridos, milhões de profissionais passam horas sentados em frente ao computador, muitas vezes em ambientes improvisados e sem qualquer suporte ergonômico. Esse cenário aumenta o risco de dores nas costas, LER (Lesões por Esforços Repetitivos), fadiga visual, estresse e queda de produtividade.

Relatórios de saúde ocupacional mostram que problemas ergonômicos estão entre as principais causas de afastamento do trabalho e perda de desempenho. Ao mesmo tempo, empresas estão buscando soluções tecnológicas para cuidar melhor do bem-estar dos colaboradores, sem depender apenas de intervenções humanas pontuais.

---

## 3. Problema

**Problema identificado:**  
Profissionais em home office ou escritórios híbridos passam longos períodos em posições inadequadas, em ambientes pouco confortáveis (temperatura, iluminação) e sem gestão inteligente de pausas. Isso gera:

- queda de produtividade;
- aumento de dores musculoesqueléticas;
- maior risco de afastamentos;
- impacto direto na qualidade de vida e no bem-estar no trabalho.

Hoje, a maioria das empresas não possui ferramentas simples e acessíveis para monitorar, em tempo real, postura, condições do ambiente e tempo contínuo de trabalho dos colaboradores.

---

## 4. Objetivo da Solução

Desenvolver um sistema IoT, baseado em ESP32, capaz de:

- monitorar postura (distância do corpo em relação à mesa);
- monitorar temperatura e umidade do ambiente;
- monitorar nível de iluminação do local de trabalho;
- sugerir pausas inteligentes após longos períodos contínuos de atividade;
- enviar esses dados para a nuvem via MQTT, permitindo visualização em dashboards ou integração com outros sistemas empresariais.

O foco é **promover saúde, bem-estar e produtividade** no futuro do trabalho, usando tecnologias acessíveis e escaláveis.

---

## 5. Persona e Cenário de Uso

**Persona:**  
Ana, 29 anos, analista de marketing digital, trabalha em modelo híbrido. Em casa, ela usa uma mesa pequena, cadeira simples e passa de 6 a 8 horas por dia no computador. Frequentemente sente dores nas costas e cansaço visual, mas dificilmente lembra de fazer pausas ou ajustar a postura.

**Cenário de uso:**  
O dispositivo ErgoSense é colocado na mesa da Ana, apontado na direção da cadeira. Ele monitora:

- a distância da Ana em relação à mesa (indicando se ela está muito curvada);
- a temperatura e a umidade do ambiente (conforto térmico);
- o nível de iluminação (condições ideais para trabalho);
- o tempo que ela permanece em atividade sem pausas.

Quando algo sai dos parâmetros ideais (postura ruim, ambiente desconfortável, muito tempo sentada), o equipamento:

- acende um LED e/ou dispara um buzzer com um alerta suave;
- exibe mensagens no display (por exemplo: “Ajuste a postura”, “Faça uma pausa de 5 minutos”, “Ambiente quente, hidrate-se”);
- envia os dados via MQTT para um broker na nuvem, permitindo que um dashboard monitore a saúde ergonômica da Ana ao longo do dia.

---

## 6. Conexão com o Futuro do Trabalho

O futuro do trabalho combina modelos flexíveis (home office, coworking, escritórios híbridos) com alta exigência de produtividade e constante conexão digital. Nesse contexto, tecnologias de **Physical Computing**, como IoT e IoB (Internet of Behaviors), permitem que o ambiente de trabalho deixe de ser passivo e passe a ser **inteligente e proativo**.

O ErgoSense se encaixa diretamente nessa tendência, pois:

- utiliza sensores físicos para interpretar o comportamento humano (postura, permanência prolongada, condições do ambiente);
- aplica lógica embarcada para gerar feedback em tempo real (alertas locais e IoT);
- usa comunicação MQTT para integrar o comportamento do colaborador a plataformas digitais de saúde ocupacional e gestão de pessoas.

Assim, a solução demonstra, na prática, como o uso de IoT pode transformar saúde e bem-estar no trabalho, contribuindo para um futuro do trabalho mais humano, sustentável e inteligente.

---

## 7. Arquitetura da Solução (Visão Geral)

*(Esta seção será detalhada nos próximos passos: componentes, sensores, atuadores, MQTT, fluxo de dados, etc.)*

---

## 8. Tecnologias Utilizadas

- ESP32
- Sensores (distância, temperatura/umidade, luminosidade)
- Atuadores (LED, buzzer, display)
- Protocolo MQTT
- Wokwi (simulação)
- Git / GitHub

---

## 9. Como executar o projeto

*(Aqui você irá colocar: link do Wokwi, como rodar, bibliotecas usadas, etc. Vou te passar isso mais pra frente.)*

---

## 10. MQTT / HTTP

*(Aqui entraremos nos tópicos MQTT usados, payload em JSON, etc. Também vou te passar pronto em outro passo.)*
