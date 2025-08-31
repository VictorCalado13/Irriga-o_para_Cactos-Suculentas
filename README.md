# Irrigação_para_Cactos-Suculentas
# 🌵 Sistema de Irrigação Automática para Cactos e Suculentas

Este projeto é um **sistema embarcado de irrigação automática**, programável, desenvolvido para o cuidado de cactos e suculentas.  
Ele utiliza um **ESP32-C3 Super Mini** para controlar uma **mini bomba de água RS-385 (12V)** por meio de um **módulo relé 5V 10A**, permitindo programar intervalos semanais ou diários de irrigação, ideal para viagens ou para quem busca praticidade.

---

## 🛠️ Componentes Utilizados
- **ESP32-C3 Super Mini** – Microcontrolador principal  
- **Módulo Relé 5V 10A** – Controle da bomba de água  
- **Mini bomba de água RS-385 (12V)** – Responsável pela irrigação  
- **Fonte 12V** – Alimentação da bomba de água  
- **Fonte USB ou 5V** – Alimentação do ESP32-C3  
- **Mangueiras e reservatório** – Para armazenamento e transporte da água  

---

## ⚙️ Funcionamento
1. O sistema é configurado para ativar a bomba em **intervalos programados** (ex.: 1x por semana).  
2. A bomba é acionada por **um tempo pré-definido** (ex.: 5 segundos), suficiente para a irrigação adequada de cactos e suculentas.  
3. Após a irrigação, o sistema retorna ao modo de espera até o próximo ciclo.  

> O intervalo e o tempo de acionamento podem ser ajustados diretamente no código para diferentes necessidades.

---

## 🚀 Como Usar
1. **Faça o upload do firmware** para o ESP32-C3 via Arduino IDE ou PlatformIO.  
2. **Conecte os componentes** de acordo com a tabela de ligação.  
3. **Alimente o sistema**:
   - ESP32-C3 com USB/5V  
   - Bomba com fonte 12V  
4. Pronto! O sistema irá executar o ciclo de irrigação conforme programado.

---

## 🔌 Esquema de Ligação

| Componente              | Pino no ESP32-C3   |
|------------------------|--------------------|
| Módulo Relé (IN)       | GPIO XX            |
| Módulo Relé (VCC/GND)  | 5V/GND             |
| Bomba RS-385 (12V)     | Saída do relé      |
| Fonte ESP32-C3         | USB ou 5V/GND      |

> **Atenção**: A bomba RS-385 deve ser alimentada com **12V** independente do ESP32. O relé apenas chaveia a energia.

---

## 📚 Dependências
- **Arduino Core para ESP32-C3**  
- Biblioteca `esp_sleep.h`
