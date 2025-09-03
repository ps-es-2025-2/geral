# 🚗 Simulação de Transcrição – Entrevista WhatsApp

**Contexto:**  
A entrevista é conduzida por Pedro (estudante de Engenharia de Software) com Carlos (gerente de um estacionamento de grande porte). O objetivo é levantar requisitos para um **aplicativo de controle de estacionamento**.

---

### 🗨️ Conversa

**Pedro (Aluno):**  
Olá, Carlos! Obrigado por topar conversar comigo. Gostaria de entender melhor como funciona a operação do seu estacionamento e o que você espera de um aplicativo.

**Carlos (Gerente):**  
Oi, Pedro! Sem problemas. Olha, a gente tem um fluxo muito grande de carros todos os dias. Tudo ainda é anotado no papel: placa, horário de entrada, vaga. Isso atrasa muito e gera erros.

---

**Pedro:**  
Entendo. Então o app ajudaria a automatizar esses registros, certo?

**Carlos:**  
Exatamente! Quero que os atendentes registrem o carro na entrada (check-in), o sistema já sugira uma vaga disponível e depois faça o check-out com cálculo automático do valor.

---

**Pedro:**  
Você gostaria que o aplicativo também mostrasse a localização da vaga para os atendentes?

**Carlos:**  
Sim, seria ótimo! Assim o cliente pode ser direcionado direto para a vaga. O app também pode mostrar um mapa simples do estacionamento.

---

**Pedro:**  
Sobre o preço: vocês trabalham com tarifa por hora ou minuto?

**Carlos:**  
Por minuto. Gostaria que o sistema calculasse o total automaticamente com base no tempo de permanência.

---

**Pedro:**  
E sobre a placa do carro, você gostaria que ela fosse registrada manualmente ou por foto (OCR)?

**Carlos:**  
No começo pode ser manual, mas seria bom deixar preparado para leitura automática de placas futuramente.

---

**Pedro:**  
Legal. Gostaria de um histórico dos carros que já passaram pelo estacionamento?

**Carlos:**  
Sim, isso é essencial. Quero saber a frequência dos clientes, horários de pico, tempo médio de permanência.

---

**Pedro:**  
E sobre o pagamento, deseja que seja feito via app ou no caixa?

**Carlos:**  
Por enquanto, só no caixa. Mas quero ter relatórios automáticos para saber o faturamento diário.

---

**Pedro:**  
Perfeito. E quem vai usar o app? Atendentes, gerentes ou clientes também?

**Carlos:**  
Nesta primeira versão, só atendentes e gerência. Depois podemos criar uma versão para cliente reservar vaga, mas não é prioridade agora.

---

**Pedro:**  
Entendido. Gostaria de ter alertas, como quando o estacionamento está quase cheio?

**Carlos:**  
Sim, isso ajuda muito!

---

**Pedro:**  
Ótimo. Para resumir, quais seriam as prioridades para o MVP?

**Carlos:**  
1. Registro de entrada (check-in) e saída (check-out) de veículos.  
2. Cálculo automático do valor com base no tempo.  
3. Controle de vagas disponíveis e ocupadas.  
4. Registro da placa do veículo.  
5. Relatórios básicos (faturamento, tempo médio, ocupação).  

Depois podemos pensar em leitura de placas automática, pagamento via app e reservas.

---

**Pedro:**  
Excelente, Carlos! Com essas informações já conseguimos modelar o sistema. Muito obrigado!

**Carlos:**  
Obrigado você! Quero ver esse sistema funcionando logo. 🚀

