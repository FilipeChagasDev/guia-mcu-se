---
description: Filipe Chagas Ferraz
cover: .gitbook/assets/Home_Electronics_Lab.jpg
coverY: -303.32984293193715
---

# Guia de Projetos em Microcontroladores e Sistemas Embarcados - Introdução

## Introdução

Este é um pequeno guia de implementação de projetos direcionado aos alunos das disciplinas de **Microcontroladores** e **Sistemas Embarcados** dos cursos de **Engenharia de Computação** e **Engenharia de Controle e Automação** da **Universidade Federal de Mato Grosso (UFMT).** No entanto, mesmo os leitores que não estão cursando estas disciplinas, ou sequer estudam na UFMT, podem tirar proveito desta leitura. Neste guia, algumas orientações sobre a implementação de pequenos projetos de sistemas microcontrolados serão dadas. Dentre elas, algumas orientações gerais (que valem para todos os projetos), e algumas de projeto específico, seguindo uma pequena lista de projetos sugeridos.&#x20;

### Sobre o Autor

Sou **Filipe Chagas Ferraz**. Atualmente (setembro de 2022) sou monitor da disciplina de **Microcontroladores**, ministrada pelo professor **Jésus Franco Bueno.** No semestre que antecedeu o atual, fui monitor da disciplina de **Sistemas Embarcados**. Sou graduando do curso de **Engenharia de Computação** da **UFMT-VG**, com poucos meses restantes até a conclusão deste. Também fui monitor das disciplinas de **Algoritmos e Programação de Computadores (2018)** e **Sistemas Operacionais (2020).** Vocês podem ver projetos _open-source_ de minha autoria e se conectar comigo através dos seguintes _links_:

**GitHub:** [https://github.com/FilipeChagasDev](https://github.com/FilipeChagasDev)

**LinkedIn:** [https://www.linkedin.com/in/filipe-chagas-16a9371b8](https://www.linkedin.com/in/filipe-chagas-16a9371b8)

**Email:** filipe.ferraz0@gmail.com

<mark style="color:green;">**Sugestões para melhorar este guia são sempre bem-vindas.**</mark>

## Orientações gerais

### Cuidado com o tempo!

Tendo em vista que os projetos devem estar concluídos antes do fim do semestre, recomendo a escolha de projetos simples. Mesmo os alunos que querem se destacar com projetos elaborados e desafiadores devem escolher um escopo sucinto e não muito difícil de implementar. O tempo até a data de apresentação do projeto é curto e não é seguro se aventurar com projetos difíceis. No entanto, isto não quer dizer que você não deve se desafiar um pouco. **Escolha um projeto que seja simples, mas que não seja simples demais.** Faça algo que reflita uma aplicação prática e que, a longo prazo, possa se tornar um projeto de alto nível, passível à publicação em um periódico nacional ou internacional, ou até mesmo ao uso prático dentro de uma industria. Consulte o professor da disciplina antes de iniciar o desenvolvimento do projeto, e sinta-se à vontade para tirar dúvidas comigo e/ou me pedir ajuda para implementar o projeto.&#x20;

### Antes de "por a mão na massa", pense sobre como o projeto será feito

O primeiro passo que você deve dar no desenvolvimento do seu projeto é organizar uma pequena reunião com sua equipe e discutir sobre como o projeto será feito. Pense sobre os requisitos do projeto, os componentes que serão usados, os _softwares_ e _middlewares_ que serão usados, os custos, a carga de trabalho necessária; faça desenhos, diagramas, plantas... Faça isto para dar um norte sólido aos integrantes do grupo e também para prever os problemas que podem surgir. Ou seja: **pense em tudo, inclusive em tudo que pode dar errado**, e fique preparado para resolver os problemas a tempo de apresentar o projeto.

Algumas questões sobre as quais você deve pensar:

* Quais materiais você precisará para montar o projeto? Quanto custam esses materiais? Onde você irá comprar? Quanto tempo levarão para chegar?
* De que forma você irá montar a parte elétrica do projeto? Vai usar _protoboard_, placa ilhada, ou vai confeccionar sua própria PCB?
  * Caso pretenda usar _protoboard_: você sabe que _protoboards_ são bem problemáticas, não? Elas possuem quantidades consideráveis de capacitâncias parasitas, pois são compostas por extensos condutores paralelos e próximos uns aos outros; são altamente suscetíveis a mal-contatos, pois não fixam bem os componentes; e são verdadeiras antenas de interferência eletromagnética, deixando os circuitos extremamente ruidosos e instáveis. Seu projeto será resistente aos problemas da _protoboard_?&#x20;
  * Caso pretenda usar placa ilhada: tem equipamentos de soldagem, como estanho, esponja vegetal e ferro de solda? Sabe soldar?&#x20;
  * Caso pretenda confeccionar sua própria PCB: conhece o processo de confecção de PCBs caseiras? Sabe onde comprar os materiais necessários? Sabe usar os _softwares_ de _design_? Sabe soldar² ? Nem pense em usar serviços de fabricação de PCB sob demanda, como JLCPCB e PCBWay, em seu projeto da disciplina! Esses serviços são (muito) caros e demoram meses para entregar.&#x20;
* Qual microcontrolador você irá usar no projeto? Há kits/placas de desenvolvimento para este microcontrolador no mercado local? O microcontrolador tem memória o suficiente para comportar o _firmware_ do projeto? O microcontrolador tem as entradas e saídas necessárias para conectar os periféricos do projeto? Tem certeza que o dispositivo que você escolheu é mesmo um microcontrolador (ou será que é um [**SoC**](https://pt.wikipedia.org/wiki/System-on-a-chip)) ?
* Quais grandezas físicas do ambiente você precisará aferir? Quais sensores você irá usar? Esses sensores estão disponíveis no mercado local? Como esses sensores se comunicam com o microcontrolador? Com relação à programação, há bibliotecas para esses sensores? Essas bibliotecas são compatíveis com a plataforma que você pretende usar? De que forma os dados de cada sensor são "entregues" pela biblioteca, e que processamentos você deve aplicar sobre estes dados?
* Caso seu projeto seja eletromecânico: que tipo de motores você irá usar? qual é o torque mínimo que cada motor deve ter? Como você fará a estrutura do projeto?
* Qual fonte de energia você usará em seu projeto? Essa fonte é capaz de fornecer a potência necessária para todos os componentes mesmo nos momentos de maior consumo?
* Alguém já fez algum projeto semelhante ou igual ao seu? Se sim, quais desafios essa pessoa teve?

## Tópicos importantes para estudar

### Prioritários

Este são os conhecimentos que você precisa adquirir para trabalhar bem com microcontroladores e desenvolver sistemas embarcados:

* Análise de circuitos elétricos simples, com resistores, capacitores, indutores e diodos;
* Arquiteturas de microprocessadores modernos (Ex: ARM, RISC-V, Xtensa);
* Famílias de microcontroladores modernos (Ex: AVR, STM8, STM32, LPC);
* Recursos de microcontroladores (Ex: GPIOs, ADCs, DACs, interrupções, _timers_ de uso geral_, watchdog timers,_ DMA)_;_
* Programação embarcada em C e um pouco de C++;
* Protocolos de comunicação serial (Ex: UART, I2C, SPI);
* Interpretação de _datasheets_ e manuais.

### Secundários

Estes são alguns dos diversos conhecimentos que agregam muito à área, mas que pertencem a outras disciplinas e podem ser adquiridos com experiência de trabalho:

* Sistemas operacionais _real-time_ (Ex: FreeRTOS, MBED);
* Fontes lineares e chaveadas, simples e simétricas;
* Componentes eletrônicos um pouco mais avançados: diodos _zener_, diodos _schottky_, transistores bipolares de junção (BJTs), transistores de efeito de campo (FETs), amplificadores operacionais, etc;
* Filtros analógicos ativos e passivos;
* Conceitos de análise de sinais digitais: amostragem, teorema de Nyquist-Shannon, filtros IIR e FIR, transformada de Fourier rápida (FFT), etc;
* Sistemas de controle lineares e inteligentes (Ex: PID, Fuzzy, MPC);
* Para projetos eletromecânicos: máquinas elétricas e mecânica dos sólidos;
* Para IoT: protocolos de rede TCP/IP (Ex: HTTP, MQTT, TCP, UDP, IP, Ethernet) e Linux embarcado;
* Para industria: protocolos de redes industriais (Ex: CAN, Modbus, Profibus, Profinet), instrumentação industrial e controladores lógicos programáveis (CLPs);
* Programação em MATLAB e Python.
