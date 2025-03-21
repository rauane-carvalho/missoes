# Relatório da Missão 1.0: Acendendo um LED com Arduino

Este repositório contém o relatório e o código para a missão de acender um LED utilizando a plataforma TinkerCAD e uma placa Arduino Uno.

## Introdução

O objetivo deste projeto é demonstrar como acender e piscar um LED utilizando uma placa Arduino Uno, com diferentes períodos de tempo. O projeto foi desenvolvido na plataforma TinkerCAD, que permite a simulação de circuitos eletrônicos.

## Componentes Utilizados

- **TinkerCAD**: Plataforma de simulação de circuitos.
- **Arduino Uno**: Placa de prototipagem utilizada para controlar o LED.
- **LED**: Diodo emissor de luz.
- **Resistor**: Utilizado para limitar a corrente e proteger o LED.
- **Protoboard**: Placa de ensaio para montagem do circuito.

## Circuito

O circuito foi montado utilizando uma placa Arduino Uno e uma protoboard. O LED foi conectado ao pino 13 do Arduino, com um resistor em série para limitar a corrente. O terminal negativo (cátodo) do LED foi conectado ao GND (terra) do Arduino.

### Esquema do Circuito

- **GND** do Arduino conectado ao terminal negativo da protoboard.
- **5V** do Arduino conectado ao terminal positivo da protoboard.
- **Pino 13** do Arduino conectado ao terminal positivo (ânodo) do LED.
- **Resistor** conectado entre o pino 13 e o LED para limitar a corrente.

## Funcionamento do Circuito

O LED é controlado pelo pino 13 do Arduino, que é configurado como saída (`OUTPUT`). O código faz com que o LED pisque em três períodos diferentes, em um loop infinito.

### Código do Arduino

```cpp
void setup() {
  pinMode(13, OUTPUT);  // Define o pino 13 como saída
}

void loop() {
  digitalWrite(13, HIGH);  // Acende o LED
  delay(1000);             // Espera 1 segundo
  digitalWrite(13, LOW);   // Apaga o LED
  delay(1000);             // Espera 1 segundo

  digitalWrite(13, HIGH);  // Acende o LED
  delay(500);              // Espera 0.5 segundos
  digitalWrite(13, LOW);   // Apaga o LED
  delay(500);              // Espera 0.5 segundos

  digitalWrite(13, HIGH);  // Acende o LED
  delay(200);              // Espera 0.2 segundos
  digitalWrite(13, LOW);   // Apaga o LED
  delay(200);              // Espera 0.2 segundos
}
```

<h2 style = "color: green">Conclusão</h2>
Concluímos que para o funcionamento de um circuito em que um LED seja aceso é
necessário vários passos sem exceção, e feitos de maneira correta para que a LED seja
acesa e para que não ocorra erros ou danos.
