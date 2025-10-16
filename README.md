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
    - Configuração e uso das aplicações (Servidor, Clientes e Arduino).
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
- Dificuldade na execução dos testes devido à indisponibilidade do build ou versão do programa necessária para a etapa.

<hr>

<h2> Squad 2: Arduino (Coleta de Dados) & Servidor OPC UA </h2>

<p align="justify"> 
  Squad composto pelos membros: <b> Alice Virginia, Danilo Santos, Luna Beatriz, Otávio Soares.</b> <br>
  Este squad é o responsável pela coleta de dados no nível do hardware e pela comunicação middleware, formando a base da arquitetura Cliente-Servidor do OPC UA.<br>  
</p>

- Desenvolver o Servidor OPC UA responsável por:
  - Coletar dados dos sensores conectados ao Arduino via porta Serial.
  - Converter e publicar esses dados como nós (nodes) OPC UA acessíveis aos clientes.
- Programar o Arduino para:
    - Ler sensores (temperatura, umidade, ultrassônico, infravermelho, etc.).
    - Controlar atuadores (motor, relé, servo).
    - Enviar os dados via Serial no formato adequado.
- Implementar o mapeamento entre variáveis físicas e variáveis OPC UA, garantindo atualização contínua e confiável dos dados.
- Garantir que o servidor aceite comandos OPC UA vindos dos clientes para acionar os atuadores remotamente.

<b> Pontos Importantes </b>
- As ligações positivo e negativo (5V e GND) identificadas em vermelho e preto para padronização

<b> Dificuldades </b>
- Montagem e ligação de Leds a protoboard/arduino;
- Montagem da ponte do Motor DC;
- Identificar a informação da Umidade do solo no Arduino;

 <hr>

<h3 align="center"> Esquema de Montagem do Arduino </h3>

<p align="center"> 
  <img src="https://raw.githubusercontent.com/MARILENE-384076/SmartFactory-OPC-Systems/main/Arquivos/Squad%2002/Imagens/Diagrama_Arduino.jpeg" alt="Diagrama_Arduino.jpeg" width="600" height="600"
</p>

<hr>

<h3 align="center"> Montagem Protótipo </h3>

<p align="center"> 
  <img src="https://raw.githubusercontent.com/MARILENE-384076/SmartFactory-OPC-Systems/main/Arquivos/Squad%2002/Imagens/Mont_Prototipo01.jpeg" alt="Montagem Prototipo 01.jpeg" width="600" height="600"/>
</p> 
<p align="center"> 
  <img src="https://raw.githubusercontent.com/MARILENE-384076/SmartFactory-OPC-Systems/main/Arquivos/Squad%2002/Imagens/Mont_Prototipo02.jpeg" alt="Montagem Prototipo 02.jpeg" width="600" height="600"/> 
</p> 
<p align="center">
  <img src="https://raw.githubusercontent.com/MARILENE-384076/SmartFactory-OPC-Systems/main/Arquivos/Squad%2002/Imagens/Mont_Prototipo03.jpeg" alt="Montagem Prototipo 03.jpeg" width="600" height="600"/>
</p> 

<hr>

<h3 align="center"> Código do Arduino </h3>

<p align="center"> <img src="https://raw.githubusercontent.com/MARILENE-384076/SmartFactory-OPC-Systems/main/Arquivos/Squad%2002/Imagens/Cod_Arduino_01.jpeg" alt="Código Servidor 01" width="900"/> </p> 
<p align="center"> <img src="https://raw.githubusercontent.com/MARILENE-384076/SmartFactory-OPC-Systems/main/Arquivos/Squad%2002/Imagens/Cod_Arduino_02.jpeg" alt="Código Servidor 02" width="900"/> </p>
<p align="center"> <img src="https://raw.githubusercontent.com/MARILENE-384076/SmartFactory-OPC-Systems/main/Arquivos/Squad%2002/Imagens/Cod_Arduino_03.jpeg" alt="Código Servidor 03" width="900"/> </p> 
<p align="center"> <img src="https://raw.githubusercontent.com/MARILENE-384076/SmartFactory-OPC-Systems/main/Arquivos/Squad%2002/Imagens/Cod_Arduino_04.jpeg" alt="Código Servidor 04" width="900"/> </p> 

<hr>

<h3 align="center"> Interface do Servidor </h3>

<p align="center"> 
  <img src="https://raw.githubusercontent.com/MARILENE-384076/SmartFactory-OPC-Systems/main/Arquivos/Squad%2002/Imagens/Interface_Servidor01.jpeg" alt="Interface Servidor 01"                  width="600" height="600"/> 
</p>

<hr>

<h3 align="center"> Código do Servidor </h3>

<p align="center"> 
  <img src="https://raw.githubusercontent.com/MARILENE-384076/SmartFactory-OPC-Systems/main/Arquivos/Squad%2002/Imagens/Cod_Servidor_1.jpeg" alt="Código Servidor 01" width="900" />
</p>
<p align="center"> 
  <img src="https://raw.githubusercontent.com/MARILENE-384076/SmartFactory-OPC-Systems/main/Arquivos/Squad%2002/Imagens/Cod_Servidor_2.jpeg" alt="Código Servidor 02" width="900" /> 
</p>
<p align="center">
  <img src="https://raw.githubusercontent.com/MARILENE-384076/SmartFactory-OPC-Systems/main/Arquivos/Squad%2002/Imagens/Cod_Servidor_3.jpeg" alt="Código Servidor 03" width="900" /> 
</p>

<hr>

<h2> Squad 3: Clientes OPC UA </h2>

<p align="justify">
  
  Squad composto pelos membros: <b>Diulie Batista, Yhan, Nicolas Oliveira, Bruno Maia.</b> <br>
  Este Squad tem a responsabilidade de desenvolver as aplicações Cliente WPF (desktop) independentes, que se conectam ao Servidor OPC UA, oferecendo visualização em tempo real dos        sensores e permitindo o envio de comandos remotos de controle para os atuadores. <br>
  
</p>

- Criar aplicações clientes WPF independentes para cada grandeza medida (por exemplo, um cliente para temperatura, outro para umidade, etc.).
- Implementar a interface gráfica (UI) para visualização dos dados em tempo real.
- Garantir que cada cliente consiga ler e escrever dados no servidor OPC UA (monitorar e também enviar comandos).
- Desenvolver recursos de controle remoto para dispositivos (acionamento de motor, servo, relé) via OPC UA.
- Realizar testes de desempenho e confiabilidade na comunicação cliente-servidor.

<hr>

<h2 align="center">Roteiro de Desenvolvimento Back-End e Interface (Squad 3)</h2>

<p align="center">
    O desenvolvimento do código para o **Simulador Smart Factory** (Back-End e Cliente WPF) seguiu o roteiro estratégico detalhado abaixo.
</p>

<p align="center">
  
    <strong>Acesse a Documentação repassada pelos membros do Grupo 3 :</strong>
    <br>
    <a href="https://github.com/MARILENE-384076/SmartFactory-OPC-Systems/blob/main/Arquivos/Squad%2003/squard%2003.docx" target="_blank" style="text-decoration: none; display: inline-block; padding: 10px 20px; margin-top: 10px; border-radius: 5px; background-color: #007bff; color: white; font-weight: bold;">
        <span style="font-size: 1.2em;">📖</span> Documentação Grupo 3 (Clique para ver)
    </a>
</p>

<hr>

<h3 align="center"> Interface WPF Client </h3>

<p align="center"> 
  
  Idealização da primeira interface: <br>  
  <p align="center">
    <img src="https://raw.githubusercontent.com/MARILENE-384076/SmartFactory-OPC-Systems/main/Arquivos/Squad%2003/Imagens/Interface_WPF01.jpeg" alt="Interface WPF - 01" /> </p>
  </p>

<hr>

<h3 align="center"> Segunda interface mais intuitiva: </h3>
 
  <p align="center"> 
    <img src="https://raw.githubusercontent.com/MARILENE-384076/SmartFactory-OPC-Systems/main/Arquivos/Squad%2003/Imagens/Interface_WPF_V02.jpeg" alt="Interface WPF - 02" /> 
  </p>
  <p align="center">
    <img src="https://raw.githubusercontent.com/MARILENE-384076/SmartFactory-OPC-Systems/main/Arquivos/Squad%2003/Imagens/Interface_WPF_V02.1.jpeg" alt="Interface WPF - 02" /> 
  </p>

<hr>

<h3 align="center"> Código WPF(C#) Front-End </h3>

<p align="center"> 
  <img src="https://raw.githubusercontent.com/MARILENE-384076/SmartFactory-OPC-Systems/main/Arquivos/Squad%2003/Imagens/Front_End_01.jpeg" alt="Front-End - 01" width="900" /> 
</p>
<p align="center"> 
  <img src="https://raw.githubusercontent.com/MARILENE-384076/SmartFactory-OPC-Systems/main/Arquivos/Squad%2003/Imagens/Front_End_02.jpeg" alt="Front-End - 02" width="900" /> 
</p>
<p align="center"> 
  <img src="https://raw.githubusercontent.com/MARILENE-384076/SmartFactory-OPC-Systems/main/Arquivos/Squad%2003/Imagens/Front_End_03.jpeg" alt="Front-End - 03" width="900" />
</p>

<hr>

<h3 align="center"> Código WPF(C#) Back-End </h3>

<p align="center">
  <img src="https://raw.githubusercontent.com/MARILENE-384076/SmartFactory-OPC-Systems/main/Arquivos/Squad%2003/Imagens/Back_End_01.jpeg" alt="Back-End - 01" width="900" /> 
</p>
<p align="center">
  <img src="https://raw.githubusercontent.com/MARILENE-384076/SmartFactory-OPC-Systems/main/Arquivos/Squad%2003/Imagens/Back_End_02.jpeg" alt="Back-End - 02" width="900" />
</p>
<p align="center"> 
  <img src="https://raw.githubusercontent.com/MARILENE-384076/SmartFactory-OPC-Systems/main/Arquivos/Squad%2003/Imagens/Back_End_03.jpeg" alt="Back-End - 03" width="900" />
</p>
<p align="center"> 
  <img src="https://raw.githubusercontent.com/MARILENE-384076/SmartFactory-OPC-Systems/main/Arquivos/Squad%2003/Imagens/Back_End_04.jpeg" alt="Back-End - 04" width="900" /> 
</p>

<hr>

<h2> Squad 4: Gêmeo Digital </h2>

<p align="justify">
  
  Squad composto pelos membros: <b>Lucas Aquino, Miguel Duarte, Erick.</b> <br>
  Este Squad tem a responsabilidade de desenvolver as aplicações desktop independentes, essenciais para a visualização e controle de cada variável. <br>
  
</p>

- Desenvolver um gêmeo digital (representação virtual da planta piloto), que reproduza em tempo real o comportamento dos sensores e atuadores.
- Criar uma interface 3D ou painel gráfico dinâmico que mostre:
  - Variação dos sensores.
  - Estado dos atuadores (ligado/desligado, posição, etc.).
- Integrar o gêmeo digital ao Servidor OPC UA para sincronizar dados reais e simulados.
- Implementar um modo de simulação offline, permitindo testar o sistema mesmo sem hardware físico.
- Colaborar com o grupo de clientes OPC UA para validar a atualização visual e interativa do ambiente virtual.
  
<hr>

<h2 align="center"> Sensores Utilizados </h2>

<div align="center">
  <table>
    <thead>
      <tr>
        <th> :computer: Sensor </th>
        <th> ✅ Nome do Sensor </th>
        <th> :bulb: Descrição </th>
      </tr>
    </thead>
    <tbody align="center">
      <tr>
        <td> <img src="https://github.com/MaysCroft/Situacao-de-Aprendizagem-6/blob/main/Imagens%20Smart%20Factory/01%20-%20Arduino.jpg" height="300" width="300" /> </td>
        <td><b> Arduíno UNO </b></td>
        <td> A placa microcontroladora (o "cérebro" do projeto) usada para carregar e executar o código que controla os sensores e atuadores do circuito. </td>
      </tr>
      <tr>
        <td> <img src="https://github.com/MaysCroft/Situacao-de-Aprendizagem-6/blob/main/Imagens%20Smart%20Factory/02%20-%20Sensor%20Ultrassonico%20HC-SR04.jpg" height="300"                              width="300"/> 
        </td>
        <td><b> HC-SR04 Ultrassônico </b></td>
        <td> O sensor mede o crescimento da planta por meio de ondas ultrassônicas, calculando o tempo de retorno do pulso sonoro refletido pela superfície da planta para determinar a               distância e acompanhar sua variação ao longo do tempo.
        </td>
      </tr>
      <tr>
        <td> 
          <img src="https://raw.githubusercontent.com/MARILENE-384076/SmartFactory-OPC-Systems/main/Arquivos/Squad%2002/Imagens/Sensor_Higrometro.jpg" alt="Sensor_Higrometro.jpg"                      height="300" width="300"/> 
        </td>
        <td><b> Sensor de Umidade do Solo - Higrômetro </b></td>
        <td> Mede a umidade do solo pela variação da condutividade elétrica entre as hastes, permitindo avaliar a irrigação e acionar o monitoramento automático das plantas.
     </td>
  </tr>     
      <tr>
        <td> <img src="https://raw.githubusercontent.com/MARILENE-384076/SmartFactory-OPC-Systems/main/Arquivos/Squad%2002/Imagens/Servo_Motor.jpeg" alt="Servo_Motor.jpg" height="300" width="300"/></td>
        <td><b> Servo Motor </b></td>
        <td> Atua como irrigador do solo para evolução da planta na estufa. </td>
      </tr>
      <tr>
        <td> <img src="https://raw.githubusercontent.com/MARILENE-384076/SmartFactory-OPC-Systems/main/Arquivos/Squad%2002/Imagens/Relé.jpeg" alt="Relé.jpg" height="300" width="300"/></td>
        <td><b> Relé </b></td>
        <td> Controla a iluminação dentro da estufa. </td>
      </tr>
      <tr>
        <td> <img src="https://raw.githubusercontent.com/MARILENE-384076/SmartFactory-OPC-Systems/main/Arquivos/Squad%2002/Imagens/Motor_DC.jpeg" alt="Motor_DC.jpg" height="300"                          width="300"/></td>
        <td><b> Motor DC</b></td>
        <td> Responsável por ventilar o ambiente. </td>
      </tr>
       <tr>
        <td> <img src="https://raw.githubusercontent.com/MARILENE-384076/SmartFactory-OPC-Systems/main/Arquivos/Squad%2002/Imagens/Ponte_Hl298N.jpeg" alt="Ponte_HL298N.jpg"                               height="300" width="300"/></td>
        <td><b> Ponte - HL298N </b></td>
        <td> Responsável por controlar o motor DC através da bateria. </td>
      </tr>
    </tbody>
  </table>
</div>

<hr>
