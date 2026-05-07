# 🔧 Arduino PWM Controller

## Índice
1. [Introdução ao PWM](#introdução-ao-pwm)
2. [Componentes necessários](#componentes-necessários)
3. [Esquemático](#esquemático)
4. [Código-fonte](#código-fonte)
5. [Instruções de montagem](#instruções-de-montagem)
6. [Funcionamento do projeto](#funcionamento-do-projeto)

---

## Introdução ao PWM
PWM (Pulse Width Modulation) é uma técnica que controla a velocidade do motor variando o tempo em que o sinal fica ligado. Quanto maior esse tempo, maior a velocidade.

---

## Componentes necessários
- Arduino UNO
- Driver L293D
- Motor DC
- Botão (push-button)
- Resistor 10kΩ
- Fonte 5V

---

## Esquemático
O esquemático completo está disponível em `schematics/pwm_controller_schematic.pdf`

---

## Código-fonte
O código está em `src/main.cpp`. Possui duas funções:
- **`setup()`** → configura os pinos e inicia o motor na velocidade 1
- **`loop()`** → aguarda o botão e avança o nível de velocidade

---

## Instruções de montagem
1. Conecte o pino 9 do Arduino ao EN1 do L293D
2. Conecte OUT1 e OUT2 do L293D ao motor
3. Conecte o botão ao pino 2 com resistor de 10kΩ no GND
4. Alimente o L293D com 5V externo

---

## Funcionamento do projeto
Cada clique no botão aumenta a velocidade do motor:

| Clique | PWM | Velocidade |
|--------|-----|-----------|
| 1º | 64 | 25% |
| 2º | 128 | 50% |
| 3º | 192 | 75% |
| 4º | 254 | 100% |
| 5º | 64 | 🔄 Reinicia |