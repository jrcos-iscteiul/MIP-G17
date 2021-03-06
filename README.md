# MIP
Este repositório contém todos os ficheiros utilizados pelo Grupo 17 na 2ºParte do Projeto de MIP, nomeadamente:

- "Enunciado.pdf" -> ficheiro pdf referente ao enunciado do projeto proposto pelos professores.
- "G17.pdf" -> Relatório de trabalho que contem respostas às perguntas e clarificações sobre as opções tomadas pelo grupo.

- DIRETORIA "1.Descoberta":
  - "G17.xlsx" -> ficheiro excel utilizado na ferramenta "R" que contem os dados fornecidos utilizads na simulação de cenários
  - "G17.csv" -> ficheiro excel utilizado na ferramenta "Apromore" que contem os dados fornecidos utilizads na simulação de cenários
  - "DiscoveredModel.bpmn" -> modelo "bpmn" gerado pela ferramenta "apromore" utilizando o ficheiro excel como input de dados.
  - "G17 - Case Frequency.png" -> fotografia com imagem do processo descoberto no apromore.
  - "ImprovedModel.bpmn" -> modelo "bpmn" baseado no modelo "DiscoveredModel.bpmn", melhorado e organizado na ferramenta signavio.
  - "Ficha Mineração G17.pdf" -> ficheiro .pdf com a tabela preenchida para o log do grupo 17.

- DIRETORIA "2.Mineração do Processo":
  - "AssessDistributions.Rmd" -> ficheiro disponiblizado pelos professores de forma a transformar e analizar os dados disponiblizados no ficheiro excel.
  - "AssessDistributions.html" -> ficheiro "html" gerado a partir do output resultante do ficheiro "AssessDistributions.Rmd". Este ficheiro foi criado de forma a facilitar a leitra dos dados estatisticos gerados pelo ficheiro de transformação de dados.
  - "DiscoveredScenario.bpmn" -> ficheiro bpmn igual ao "ImprovedModel", mas com os dados preenchidos na ferramenta Bimp relativos à simulação« feita.
  - "DiscoveredSimulationLog.mxmml.gz" -> ficheiro mxmml com informações estatísticas geradas na simulação feita.

- DIRETORIA "3.Otimização dos Recursos do Proceso":
  - DIRETORIA "Graphics":
    - "Activity instances over time.pdf" -> ficheiro mxmml gerado no apromore contendo o conjunto das simulações relativamente às instâncias das atividades
    - "Case Duration.pdf" -> ficheiro mxmml gerado no apromore contendo o conjunto das simulações relativamente às durações dos casos das atividades
    - "Case Variants.pdf" -> ficheiro mxmml gerado no apromore contendo o conjunto das simulações relativamente às variantes dos casos
    - "Work-In-Progress (WIP).pdf" -> ficheiro mxmml gerado no apromore contendo o conjunto das simulações relativamente ao trabalho em progresso
  - "MinimalistScenario.bpmn" -> ficheiro bpmn representante do cenáro minimalista onde apenas é utilizado 1 recurso de cada role.
  - "MinimalistSimulationLog.mxml.gz" -> ficheiro mxml utilizado para as observações gráficas dos resultados estatisticos no cenario minimalista.
  - "OptimizedScenario.bpmn" -> ficheiro bpmn representante do cenáro otimizado onde o grupo alterou o valor dos recursos tempo e dinheiro dos valores para a simulação.
  - "OptimizedSimulationLog.mxml.gz" -> ficheiro mxml utilizado para as observações gráficas dos resultados estatisticos no cenario otimizado.
  - "WastefulScenario.bpmn" -> ficheiro bpmn representante do cenáro esbanjador onde apenas é utilizado 100 recursos humanos de cada role.
  - "WastefulSimulationLog.mxml.gz" -> ficheiro mxml utilizado para as observações gráficas dos resultados estatisticos no cenario esbanjador.

- DIRETORIA "4.Implementação do Processo":
  - DIRETORIA "delegate":
    - "ApresentarPlanoDelegate.java" -> ficheiro java calcula o preço total das reservas efetuadas e utiliza os serviços de fatura e apresentar plano de forma a mostrar em consola todas as reservas e preços.
    - "CalcularPrecoPromocionalDelegate.java" -> ficheiro java que calcula o preço final após a introdução de uma promoção por parte do cliente.
    - "DescontarPrecoDelegate.java" -> ficheiro java que calcula o preço final (desconto de 5%) se o cliente utilizar cartão como forma de pagamento.
    - "EmailTripPlanSummaryDelegate.java" -> ficheiro java que irá fazer o envio do email com a fatura e o registo do plano para o email do cliente.
  - DIRETORIA "jsonFiles":
    - "Aviao.json" -> ficheiro json do tipo "Domain-Entity" com informação da classe Aviao.
    - "Hotel.json" -> ficheiro json do tipo "Domain-Entity" com informação da classe Hotel.
    - "Carro.json" -> ficheiro json do tipo "Domain-Entity" com informação da classe Carro.
    - "Promocao.json" -> ficheiro json do tipo "Domain-Entity" com informação da classe Promocao.
    - "TripPlan.json" -> ficheiro json do tipo "Domain-Entity" com informação da classe TravelPlan.
    - "TripPlanProcess.json" -> ficheiro json do tipo "Process-Bind-Entity" com informação da classe TravelPlan de forma a ligar aos objetos e ao camunda.
    - "TripPlanStartForm.json" -> ficheiro json do tipo "Start-Form-Entity" com informação inicial da classe TravelPlan.
    - "DisponibilizarDadosCliente.json" -> ficheiro json do tipo "User-Task-Entity" onde o cliente irá disponibilizar os seus dados de cliente.
    - "DisponibilizarDadosPagamento.json" -> ficheiro json do tipo "User-Task-Entity" onde o cliente irá disponibilizar os seus dados de pagamento.
    - "IndicarMetodoPagamento.json" -> ficheiro json do tipo "User-Task-Entity" onde o cliente irá indicar o método de pagamento.
    - "IntroduzirCodigoPromocional.json" -> ficheiro json do tipo "User-Task-Entity" onde o cliente irá introduzir um código promocional.
    - "RegistarReservaAviao.json" -> ficheiro json do tipo "User-Task-Entity" onde o cliente irá fazer a reserva do voo.
    - "RegistarReservaHotel.json" -> ficheiro json do tipo "User-Task-Entity" onde o cliente irá fazer a reserva do hotel.
    - "RegistarReservaCarro.json" -> ficheiro json do tipo "User-Task-Entity" onde o cliente irá fazer a reserva do carro.
  - DIRETORIA "service":
    - "ApresentarPlanoService.java" -> ficheiro java que mostra na consola de comandos o plano e os preço das reservas efetuadas.
    - "AviaoFaturaService.java" -> ficheiro java que mostra na consola de comandos a informação e o preço da reserva do voo.
    - "CarroFaturaService.java" -> ficheiro java que mostra na consola de comandos a informação e o preço da reserva do carro.
    - "HotelFaturaService.java" -> ficheiro java que mostra na consola de comandos a informação e o preço da reserva do hotel.
  - DIRETORIA "template":
    - "fatura.html" -> ficheiro html representante do email enviado ao cliente com inforção do plano registado.
  - "tripPlan-jdl.jdl" -> ficheiro .jdl com representação em UML da base de dados utilizada no projeto.
  - "ImplementationModel.bpmn" -> ficheiro bpmn criado pelo grupo como processo base na criação da aplicação e implementação do modelo.

O grupo também criou um video de forma a explicar o modelo BPMN utilizado e demonstrando o sistema desenvolvido:
- Link Youtube -> "https://youtu.be/ingWg13LuB0".
