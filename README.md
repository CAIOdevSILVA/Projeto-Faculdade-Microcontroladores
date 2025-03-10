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
int buzzer = 13; //variavel conectada a porta 13
int button = 2; //variavel conectada a porta 2
int led = 8; //variavel conectada a porta 8

void setup()
{
  pinMode(buzzer, OUTPUT); //buzzer como saida
  pinMode(button, INPUT); //botão como entrada
  pinMode(led, OUTPUT); // led como saida
}

void loop()
{
  int Swith_State = digitalRead(button); //pegando a estado do botão
  if (Swith_State==HIGH){ // Se o botão for pressionado o led ascende e o 
    					//buzzer emite o som da campainha
  	digitalWrite(buzzer, HIGH);
    digitalWrite(led, HIGH);
    
    tone(buzzer, 1100, 300); //Ding
    delay(300);
    
    tone(buzzer, 850, 500);// Dong
    delay(500);
  }
  else { // Caso contrário nada acontece
  	digitalWrite(buzzer, LOW);
    digitalWrite(led, LOW);
  }
}
```

## 🖥 Como Acessar a Simulação
A simulação do projeto foi realizada na plataforma [Tinkercad](https://www.tinkercad.com/). Para visualizar e testar o circuito:
1. Acesse o link: [[**(inserir link da simulação aqui)**](https://www.tinkercad.com/things/iaoKOQdVYf7-smooth-bigery-hillar/editel?returnTo=https%3A%2F%2Fwww.tinkercad.com%2Fdashboard&sharecode=Wvd1E2OtxCPRkmWTzBDJQKm0Azdlp_mNo7cadOaQ6w4)]
2. Clique em "Start Simulation" para ver o funcionamento do sistema.

📍 obs: Com esse link, você também poderá editar o projeto. Portanto, siga as instruções acima corretamente para evitar alterações indesejadas.

## 📢 Conclusão
Essa atividade de extensão proporcionou uma experiência prática sobre o uso de microcontroladores para resolver problemas cotidianos. A proprietária do salão pôde aprender conceitos básicos e visualizar, por meio da simulação, como um sistema simples pode melhorar o atendimento do seu estabelecimento.


