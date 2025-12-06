# RoboAutomaçãoSistemaDesktop

## Descrição

Este projeto é um robô de automação de processos (RPA) desenvolvido com UiPath. O robô foi projetado para interagir com um sistema de desktop, automatizando tarefas como a leitura de dados de uma planilha do Excel e a inserção desses dados no sistema.

## Funcionalidades

- Leitura de dados de uma planilha do Excel (`Transactions.xlsx`).
- Lançamento e interação com o aplicativo de desktop (`UIDemo.exe`).
- Inserção de dados da planilha no sistema.
- Tratamento de exceções e erros durante a automação.

## Pré-requisitos

- UiPath Studio instalado.
- As dependências do projeto listadas no arquivo `project.json` devem ser instaladas.

## Como executar

1. Abra o projeto no UiPath Studio.
2. Certifique-se de que o arquivo `UIDemo.exe` e a planilha `Transactions.xlsx` estejam no diretório `arquivos`.
3. Execute o arquivo `Main.xaml` a partir do UiPath Studio.

## Estrutura do Projeto

- **Main.xaml:** O fluxo de trabalho principal que orquestra a automação.
- **project.json:** Arquivo de configuração do projeto, incluindo dependências.
- **arquivos/:** Contém os arquivos de dados e o executável do sistema a ser automatizado.
    - **Transactions.xlsx:** Planilha com os dados de transações a serem processados.
    - **UIDemo.exe:** O aplicativo de desktop alvo da automação.

"RPA criado como desafio do curso Automatize Process com Erimateia"
