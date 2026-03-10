🇺🇸 [English](README.md) | 🇧🇷 Português

# Irrigador Automático com Arduino

Um projeto prático de automação onde as participantes constroem um sistema que monitora a umidade do solo e irriga plantas automaticamente.

Este projeto foi desenvolvido durante um encontro prático da **Connect Byte** e introduz conceitos de sensores analógicos e controle de atuadores (bombas d'água).

---

## Visão geral

Neste projeto, as participantes constroem um sistema inteligente que detecta quando uma planta precisa de água utilizando um sensor de umidade de solo.

O Arduino processa os dados do sensor e, se o solo estiver seco, aciona uma mini bomba d'água através de um módulo relé.

Este projeto apresenta conceitos fundamentais como:
- Leitura de sensores analógicos
- Uso de módulos relé para controle de carga externa
- Estruturas condicionais (if/else) na programação
- Automação básica de processos

---

## Objetivos de aprendizado

Ao concluir este projeto, as participantes aprendem:
- Como coletar dados do ambiente usando sensores
- A diferença entre sinais analógicos e digitais
- Como isolar e controlar circuitos de maior potência (bomba) usando relés
- Lógica de calibração de sensores no código

---

## Circuito

Conecte os componentes conforme mostrado no diagrama (disponível na pasta assets).

![Circuito](./assets/componentes.png)

**Ligação básica:**
- Sensor de Umidade → Pino A0 (Analógico)
- Módulo → Pino 7 (Digital)
- Bomba d'água → Conectada à saída do Relé e fonte externa

---

## Ambiente de desenvolvimento

Este projeto foi desenvolvido utilizando **Visual Studio Code**.

Ferramentas utilizadas:
- Visual Studio Code
- Extensão Arduino / PlatformIO
- Arduino Framework

---

## Código

O código de exemplo está disponível na pasta `code`.

Arquivo principal:
`code/irrigador.ino`

---

## Como funciona

O Arduino lê constantemente o valor analógico do sensor de umidade. Quando o solo seca, a resistência aumenta e o valor lido ultrapassa o limite definido (setpoint).

Ao detectar o solo seco, o Arduino envia um sinal para o Rel