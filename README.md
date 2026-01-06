# RoboAutomaçãoSistemaDesktop

## Descrição

Este projeto é um robô de automação de processos (RPA) desenvolvido com UiPath. O robô foi projetado para interagir com um sistema de desktop, automatizando tarefas como a leitura de dados de uma planilha do Excel e a inserção desses dados no sistema.

## Funcionalidades

- **Leitura de Dados:** O robô lê os dados de uma planilha do Excel (`Transactions.xlsx`).
- **Login no Sistema:** Realiza o login no aplicativo de desktop `UIDemo.exe`.
- **Lançamento de Transações:** Para cada linha da planilha, o robô insere os dados da transação no sistema.
- **Obtenção do ID da Transação:** Após cada lançamento, o robô captura o número da transação gerado pelo sistema.
- **Atualização da Planilha:** O número da transação (ou uma mensagem de erro) é escrito de volta na planilha do Excel.
- **Tratamento de Erros:** O processo inclui um mecanismo de repetição (retry) e tratamento de exceções para lidar com possíveis falhas durante a automação.
- **Modularização:** O projeto é dividido em fluxos de trabalho menores e reutilizáveis para login, lançamento de dados e atualização da planilha.

## Pré-requisitos

- UiPath Studio instalado.
- As dependências do projeto listadas no arquivo `project.json` devem ser instaladas.

## Como executar

1. Abra o projeto no UiPath Studio.
2. Certifique-se de que o arquivo `UIDemo.exe` e a planilha `Transactions.xlsx` estejam no diretório `arquivos`.
3. Execute o arquivo `Main.xaml` a partir do UiPath Studio.

## Estrutura do Projeto

- **Main.xaml:** O fluxo de trabalho principal que orquestra a automação, lendo a planilha e invocando os outros fluxos.
- **ProcessBox/IniciarSistemaLogin.xaml:** Fluxo de trabalho responsável por abrir o aplicativo `UIDemo.exe` e realizar o login.
- **ProcessBox/RealizarLancamentos.xaml:** Fluxo de trabalho que insere os dados de uma transação no sistema, obtém o ID da transação e invoca o fluxo para escrita na planilha. Contém a lógica de retry e tratamento de exceção.
- **ProcessBox/EscreverCelula.xaml:** Fluxo de trabalho que escreve o resultado (ID da transação ou erro) na célula correspondente da planilha Excel.
- **project.json:** Arquivo de configuração do projeto, incluindo dependências.
- **arquivos/:** Contém os arquivos de dados e o executável do sistema a ser automatizado.
    - **Transactions.xlsx:** Planilha com os dados de transações a serem processados.
    - **UIDemo.exe:** O aplicativo de desktop alvo da automação.

*RPA criado como desafio do curso Automatize Process com Erimateia*
