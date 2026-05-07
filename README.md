# 🔧 Arduino PWM Controller

Controle de velocidade de motor DC com Arduino UNO e driver L293D.

---

## ⚡ Como funciona

O projeto usa **PWM** (Pulse Width Modulation) para controlar a velocidade de um motor DC.  
Cada vez que o botão é pressionado, a velocidade aumenta um nível.

| Clique | Velocidade | PWM |
|--------|-----------|-----|
| 1º | 25% | 64 |
| 2º | 50% | 128 |
| 3º | 75% | 192 |
| 4º | 100% | 254 |
| 5º | 🔄 Reinicia | 64 |

---

## 📄 Código (`src/main.cpp`)

O código possui duas funções principais:

- **`setup()`** → configura os pinos e inicia o motor na primeira velocidade
- **`loop()`** → fica aguardando o botão ser pressionado e avança o nível de velocidade

---

## 🔌 Esquemático (`schematics/`)

| Componente | Conexão |
|------------|---------|
| Arduino pino 9 | EN1 do L293D (PWM) |
| Arduino pino 2 | Botão |
| L293D OUT1/OUT2 | Motor DC |
| BAT1 5V | Alimentação do motor |

---

## 🧰 Componentes

- Arduino UNO
- Driver L293D
- Motor DC
- Botão (push-button)
- Resistor 10kΩ
- Fonte 5V