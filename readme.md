# SISTEMA DE COMPARTILHAMENTO DE VIAGENS:

Este é um sistema simplificado de compartilhamento de viagens escrito em Python. Ele permite a criação de veículos (carros e motos), motoristas e passageiros, e a realização de corridas.


## REQUISITOS
Python 3.10.10.

## Módulos
Veículos: contém a definição das classes Carro e Moto.
Pessoas: contém a definição das classes Motorista_Cadastro e Passageiro.
Corrida: contém a definição da classe Corrida.
## Como executar
Criem um ambiente virtual na pasta onde deseja executar os mósdulos do projeto, execute o MÓDULO principal.py com o comando:

`

python main.py
`
## COMO USAR:

Crie instâncias de Carro ou Moto (no módulo main.py já há alguns objetos criados.)
Crie instâncias de Motorista_Cadastro (no módulo main.py já há alguns objetos criados.)
Obs*: Você não poderá criar objetos das classes Carro e Motorista que já existam gravados no arquivo .json que é a base de dados, quando reiniciar o script main.py é necesssário deletar o arquivo ou criar objetos com atributos diferentes daqueles já gravados no arquivo.
Crie uma instância de Passageiro.
Chame a função iniciar_corrida_passageiro para iniciar uma corrida.
Use a função relatorio_passageiro para obter o relatório de corridas de um passageiro.
Use a função consultar_corridas_motorista para obter o relatório de corridas de um motorista.
Caso tenha criado um ambiente virtual lembre de ativar.
Se estiver executando pelo terminal e queira encerrar a excecução envie ` ctrl + c ` para encerrar.

## CONTRIBUIÇÕES:
As contribuições são bem-vindas! Por favor, faça um fork deste repositório e crie uma pull request se você tem algo a acrescentar.

## ESTRUTURA DO PROJETO:

Para facilitar o desenvolvimento e o manejo do software, o mesmo é divido em 5 MÓDULOs diferentes, sendo eles:
	
### MÓDULO MAIN: MÓDULO que contem a criação dos objetos, tratativa das exceções e a chamada dos relatórios. Para a execução do projeto deve-se executar esse MÓDULO.

### MÓDULO PESSOAS: MÓDULO que contém a Classe abstrata Pessoa, Classe concreta Passageiro, Classe concreta Motorista_Cadastro, Classe concreta Motorista_Corrida, conforme explicações abaixo:
    a)	Classe Pessoa: Classe abstrata para definir atributos e métodos comuns aos passageiros e motoristas.
    i)	Classe Passageiro: Classe concreta para armazenar atributos dos passageiros e ter métodos de informações e solicitação de corrida, método que cria relatório de corridas e valores pagos, conforme abaixo:
    1.	iniciar_corrida_passageiro: Método para o passageiro pedir corrida. Instancia um objeto de corrida, em corrida é localizado um motorista conforme critério, que é chamado para responder, a resposta retorna em 'chamada'.
    2.	dados_passageiro_corrida: Método que devolve dicionário com dados do passageiro.
    3.	relatorio_passageiro: Método que devolve o relatório das corridas realizadas do passageiro com base no CPF informado.
    ii)	Classe Motorista_Cadastro: Classe concreta para cadastrar e armazenar os dados dos motoristas em banco de dados Json.
    iii)	Classe Motorista_Corrida: Classe concreta para aceitar ou rejeitar a corrida pelo Motorista.
    1.	aceitar_corrida: Método para aceitar ou rejeitar a corrida pelo Motorista.
    2.	_dados_motorista_corrida: Relatório com todos os dados gerais para usar no relatório de corridas.

### MÓDULO VEÍCULOS: MÓDULO que contém a Classe abstrata Veículo, Classe concreta Carro e Classe concreta Moto, conforme explicações abaixo:
    a)	Classe Veículo: Classe abstrata que define a construção das Classes Carro e Moto.
    i)	Classe Carro: Classe concreta para reunir dados sobre os carros.
    ii)	Classe Moto: Classe concreta para reunir dados sobre as motos.

### MÓDULO PAGAMENTO: MÓDULO que contém a Classe concreta Pagamento, conforme explicação abaixo:
    a)	Classe Pagamento: Classe concreta para calcular os valores das corridas conforme tipo da corrida e condições de pagamento.
    1.	valores_corrida: Método para calcular os valores bases, descontos conforme método de pagamento e valor final.

### MÓDULO CORRIDA: MÓDULO que contém a Classe Corrida e os métodos abaixo: 
    a)	Classe Corrida: Classe que armazena dados dos passageiros, das corridas e processa informações entre as classes envolvidas.
    	iniciar_corrida: Método para o Passageiro iniciar uma corrida e chamar o aceite do Motorista.
    	valores: Processar o valor da Corrida
    	_localizar_motorista: Método interno para buscar um motorista que atenda os requisitos do chamado.
    	registrar_corrida_passageiro: Método para registar corridas do Passageiro.
    	registrar_corrida_motorista: Método para registar corridas do Motorista.
    	consultar_corridas_motorista: Método para consultar dicionário de corridas para um determinado CPF de motorista com retorno de um resumo.
    	consultar_corridas_passageiros: Método para consultar dicionário de corridas para um determinado CPF e retornar a soma dos valores finais das corridas realizadas
    	_validar_dados_passageiros: Método de validação de atributos.

## 	FUNCIONALIDADES:

    1.	Solicitação de Viagem: Os usuários podem solicitar uma viagem indicando seu local atual e destino desejado.
    2.	Pagamento Eletrônico: Os usuários podem efetuar o pagamento da viagem diretamente pelo aplicativo, usando opções de pagamentos disponíveis.
    3.	Classificação e avaliação: Os usuários podem visualizar as notas dos motoristas, assim como os motoristas podem visualizar as notas dos usuários.
    4.	Histórico de viagem: Os usuários podem visualizar o histórico de suas viagens anteriores, incluindo detalhes, custos e informações do motorista.



===============================================================

# RIDE SHARING SYSTEM:
This is a simplified ride-sharing system written in Python. It allows the creation of vehicles (cars and motorcycles), drivers, and passengers, and the execution of rides.

## REQUIREMENTS
Python 3.10.10.

## MODULES
Vehicles: Contains the definition of the Car and Motorcycle classes.
People: Contains the definition of the Driver_Registration and Passenger classes.
Ride: Contains the definition of the Ride class.

## HOW TO RUN
Create a virtual environment in the folder where you want to run the project's modules, run the MAIN module with the command:

`

python main.py
`

## HOW TO USE:

Create instances of Car or Motorcycle (some objects are already created in the main.py module.)
Create instances of Driver_Registration (some objects are already created in the main.py module.)
Note*: You will not be able to create objects from the Car and Driver classes that already exist recorded in the .json file which is the database, when restarting the main.py script it is necessary to delete the file or create objects with attributes different from those already recorded in the file.
Create an instance of Passenger.
Call the function start_ride_passenger to start a ride.
Use the function passenger_report to get a passenger's ride report.
Use the function check_driver_rides to get a driver's ride report.
If you created a virtual environment remember to activate it.
If you are running from the terminal and want to terminate the execution send ctrl + c to terminate.

## CONTRIBUTIONS:
Contributions are welcome! Please, fork this repository and create a pull request if you have something to add.

## PROJECT STRUCTURE:
To facilitate the development and handling of the software, it is divided into 5 different MODULES, namely:

### MAIN MODULE: MODULE that contains the creation of objects, exception handling, and report calling. To execute the project, this MODULE must be executed.
### PEOPLE MODULE: MODULE that contains the abstract Person Class, concrete Passenger Class, concrete Driver_Registration Class, concrete Driver_Ride Class, as explained below:

a)	Person Class: Abstract class to define attributes and methods common to passengers and drivers.
i)	Passenger Class: Concrete class to store passenger attributes and have information methods and ride request, method that creates a report of rides and paid amounts, as follows:
1.	start_ride_passenger: Method for the passenger to request a ride. It creates a ride object, and a driver is found according to criteria, who is called to respond, the response returns in 'call'.
2.	passenger_ride_data: Method that returns a dictionary with passenger data.
3.	passenger_report: Method that returns the report of completed rides based on the provided CPF.
ii)	Driver_Registration Class: Concrete class to register and store driver data in a Json database.
iii)	Driver_Ride Class: Concrete class to accept or reject the ride by the Driver.
1.	accept_ride: Method to accept or reject the ride by the Driver.
2.	_driver_ride_data: Report with all general data to be used in the ride report.


### VEHICLE MODULE: MODULE that contains the abstract Vehicle Class, concrete Car Class, and concrete Motorcycle Class, as explained below:

a)	Vehicle Class: Abstract class that defines the construction of Car and Motorcycle Classes.
i)	Car Class: Concrete class to gather data about cars.
ii)	Motorcycle Class: Concrete class to gather data about motorcycles.


### PAYMENT MODULE: MODULE that contains the concrete Payment Class, as explained below:

a)	Payment Class: Concrete class to calculate the values of the rides according to the type of ride
