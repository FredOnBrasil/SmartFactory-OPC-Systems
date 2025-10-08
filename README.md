<h1 align="center"> Documentação Smart Factory: OPC-Systems <br> Software House industrial. </h1>
<p align="center"> 
  
  <img src="https://github.com/MaysCroft/Situacao-de-Aprendizagem-6/blob/main/Imagens%20Smart%20Factory/00%20-%20Logo%20Smart%20Factory.png" height="500" width="700"/> 
</p>

<h3> Equipe responsável: <br> Marilene Araujo e Vinícius </h3>
<h3> Instrutor: Frederico Martins Aguiar </h3>

<hr>

<h2 align="center"> Introdução </h2>

A empresa SmartFactory OPC Systems está desenvolvendo uma solução para monitoramento e controle de uma planta piloto, utilizando o protocolo OPC UA como meio de comunicação entre dispositivos fisicos e aplicações desktop. <br>
O cliente solicitou que a aplicação seja capaz de:

- Coletar dados de sensores conectados a um Arduino (via Serial).
- Publicar os dados coletados em um Servidor OPC UA.
- Criar Clientes WPF independentes para cada grandeza medida.
- Permitir o acionamento remoto de dispositivos (motor, relé, servo).
- Versionar toda a documentação e o código no GitHub <br>

A turma deverá atuar como uma equipe única de desenvolvimento, simulando uma software house industrial dividida em squads de responsabilidade.

<hr>

<h2 align="center"> Responsabilidades das Squads </h2>

<h2> Squad 1: Documentação e Testes </h2>

<p align="justify">
  Squad composto pelos membros: <b>Marilene Araujo e Vinícius Gomes.</b> <br>
  Esta Squad garante a qualidade, rastreabilidade e manutenibilidade de todo o projeto. <br>
</p>

- Elaborar e manter toda a documentação técnica do projeto, incluindo:
    - Estrutura e arquitetura geral do sistema OPC UA.
    - Diagrama de blocos e fluxos de dados entre os módulos.      
,   - Configuração e uso das aplicações (Servidor, Clientes e Arduino).
- Criar e gerenciar o repositório GitHub da turma, garantindo versionamento adequado do código e da documentação.
- Definir e aplicar planos de teste funcionais e de integração:
  - Testar a comunicação Serial (Arduino ↔ Servidor).
  - Testar a comunicação OPC UA (Servidor ↔ Clientes).
  - Validar as funcionalidades de controle remoto (acionamento de motor, relé, servo).
- Registrar bugs, ajustes e melhorias necessárias.

<b> Dificuldades </b>
- Organização das informações coletadas;
- Planejamento no recebimento das informações.
- Controle da execução das squads.

<hr>

<h2> Squad 2: Arduino (Coleta de Dados) & Servidor OPC UA </h2>

<p align="justify"> 
  Squad composto pelos membros: <b> Alice Virginia, Danilo Santos, Luna Beatriz, Otávio Soares.</b> <br>
  Este squad é o responsável pela coleta de dados no nível do hardware e pela comunicação middleware, formando a base da arquitetura Cliente-Servidor do OPC UA.<br>  
</p>

- <b>Integração de Sensores: </b> Selecionar, calibrar e conectar os Sensores físicos (Ultrassônico (HC-SR04) e Umidade do Solo) ao Arduino.
- <b>Firmware do Arduino: </b> Desenvolver o código (Sketch) para que o Arduino faça a leitura das 2 grandezas de forma contínua e confiável.
- <b>Atuadores e Drives: </b> Ser responsável por transformar os comandos digitais recebidos pela rede (OPC UA) em ações físicas na planta piloto.
   - <b> Acionamento Remoto: </b> Cumprir o Requisito 4 do cliente: "Permitir o acionamento remoto de dispositivos (motor, relé, servo)".
   - <b> Drivers e Proteção: </b> Utilizar o Driver de Motor L298N para fornecer a corrente e voltagem necessárias aos atuadores, protegendo o Arduino no processo.
- <b> Comunicação de Saída: </b> Implementar a lógica para formatar os dados dos sensores e atuadores e enviá-los de forma serial para a próxima camada, o Servidor OPC UA, será o responsável por publicar esses dados no Address Space para os clientes.

<b> Pontos Importantes </b>
- As ligações positivo e negativo (5V e GND) identificadas em vermelho e preto para padronização

<b> Dificuldades </b>
- Montagem e ligação dos sensores a protoboard/arduino sendo posição correta de conexão do sensor

<h3 align="center"> Esquema de Montagem do Aduino </h3>

<p align="center"> Imagem </p>

<h3 align="center"> Montagem Protótipo </h3>

<p align="center"> Imagem </p>

<h3 align="center"> Código do Arduino Versão Inicial - V.1.0 </h3>

<p align="center"> Imagem </p>

<h3 align="center"> Código do Arduino Versão Final - V.2.0 </h3>

<p align="center"> Imagem </p>

<hr>

<h2> Squad 3: Clientes OPC UA </h2>

<p align="justify">
  Squad composto pelos membros: <b>Diulie Batista, Yhan, Nicolas Oliveira, Bruno Maia.</b> <br>
  Este Squad tem a responsabilidade de desenvolver as aplicações desktop independentes, essenciais para a visualização e controle de cada variável. <br>
</p>

- <b>Interface de Coleta:</b> Criar a aplicação WPF independentes integradas ao SDK OPC UA.
   - <b> Conexão e SDK OPC UA: </b> Integrar e configurar o SDK OPC UA Client na aplicação WPF para se conectar ao Servidor (Squad 02).
   - <b> Monitoramento via Subscription: </b> Implementar a lógica para assinar (subscribe) as variáveis (Nodes) do Servidor OPC UA, garantindo que os dados dos sensores sejam visualizados em tempo real no desktop.
   - <b> Acionamento Remoto (Escrita): </b> Criar a interface e o código para enviar comandos de escrita para o Servidor OPC UA, permitindo o acionamento remoto dos atuadores (motor, relé, servo).
   - <b> Gerenciamento de Conexão: </b> Implementar a lógica de reconexão automática ao Servidor OPC UA e o tratamento de falhas na leitura dos Nodes.

<h3 align="center"> Interface WPF Client </h3>

<p align="center"> 
  Idealização da primeira interface: <<br>
  imagem
</p>

<p align="center"> 
  Segunda interface mais intuitiva: <br>
  imagem
</p>

<p align="center"> 
 Tela com erro o a ser solucionado: <br>
  DESCRIÇÃO DO ERRO. <br>
  imagem 
</p>

<p align="center">
 Interface atual após a correção dos erros. <br>
 imagem
</p>
