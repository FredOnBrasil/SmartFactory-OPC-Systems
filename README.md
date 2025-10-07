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
  Squad composto pelos membros: <b>Marilene Araujo e Vinícius.</b> <br>
  Esta Squad garante a qualidade, rastreabilidade e manutenibilidade de todo o projeto. <br>
</p>

1. Plano de Testes e Qualidade
- <b> Testes de Integração (Fim a Fim): </b> Elaborar e executar um plano de testes que cubra a jornada completa de um dado, desde a coleta do sensor (Arduino/Serial) até a sua publicação no Servidor OPC UA e a visualização no Cliente WPF. O teste de integração também deve cobrir o acionamento remoto de atuadores. 
- <b> Testes Unitários: </b>Focar na confiabilidade do código de baixo nível, como a correta leitura dos dados no Arduino  e o parsing (estruturação) dos dados para o Servidor OPC UA.  
- <b> Gerenciamento de Requisitos: </b> Manter o checklist de verificação dos 5 requisitos do cliente (Coletar Dados, Publicar OPC UA, Clientes WPF, Acionamento Remoto, Versionamento).
- <b>Documentação Técnica:</b> Compilar toda a documentação gerada pelos outros Squads (diagramas, código-fonte, configurações do OPC UA) em um repositório centralizado.

<b> Dificuldades </b>
- Organização das informações coletadas;
- Planejamento no recebimento das informações.

<hr>
