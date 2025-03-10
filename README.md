# 📌 Projeto de Extensão - Aula Introdutória sobre Microcontroladores

## 📖 Descrição
Este projeto faz parte de uma atividade de extensão com o objetivo de oferecer uma aula introdutória sobre microcontroladores para a proprietária de um salão de beleza. Durante a aula, será apresentada uma simulação prática no Tinkercad para demonstrar como os microcontroladores podem ser utilizados para solucionar um problema real do estabelecimento.

## 🎯 Objetivo
Ensinar os conceitos básicos de microcontroladores e demonstrar, por meio de uma simulação no Tinkercad, como um sistema automatizado pode auxiliar na melhoria do atendimento do salão de beleza. A solução proposta envolve um sistema de campainha acionado por um botão para alertar a proprietária quando um cliente chega ao estabelecimento.

## 🛠 Componentes Utilizados na Simulação
- **Microcontrolador** (Arduino Uno)
- **Botão** (para representar o acionamento da campainha)
- **Buzzer** (para emitir o som da campainha)
- **LED** (para sinalizar visualmente a chegada do cliente)
- **Resistor de 10kΩ** (para o botão)

## 🔧 Funcionamento do Sistema
1. O cliente aperta um botão na entrada do salão.
2. O microcontrolador detecta o acionamento e ativa um **buzzer**, emitindo um som característico de campainha.
3. Simultaneamente, um **LED** acende para reforçar a notificação visualmente.
4. Após alguns segundos, o buzzer desliga e o LED apaga, aguardando uma nova chamada.

## 💻 Código Fonte (Arduino)
```c
const int botao = 2;
const int buzzer = 3;
const int led = 4;

void setup() {
    pinMode(botao, INPUT_PULLUP);
    pinMode(buzzer, OUTPUT);
    pinMode(led, OUTPUT);
}

void loop() {
    if (digitalRead(botao) == LOW) {
        digitalWrite(led, HIGH);
        tone(buzzer, 1000); // Som da campainha
        delay(1000);
        noTone(buzzer);
        digitalWrite(led, LOW);
        delay(2000); // Pequena pausa antes de permitir novo acionamento
    }
}
```

## 🖥 Como Acessar a Simulação
A simulação do projeto foi realizada na plataforma [Tinkercad](https://www.tinkercad.com/). Para visualizar e testar o circuito:
1. Acesse o link: [**(inserir link da simulação aqui)**]
2. Clique em "Start Simulation" para ver o funcionamento do sistema.

## 📢 Conclusão
Essa atividade de extensão proporcionou uma experiência prática sobre o uso de microcontroladores para resolver problemas cotidianos. A proprietária do salão pôde aprender conceitos básicos e visualizar, por meio da simulação, como um sistema simples pode melhorar o atendimento do seu estabelecimento.

---
🛠 **Desenvolvido como parte do projeto de extensão da disciplina de Programação de Microcontroladores.**

